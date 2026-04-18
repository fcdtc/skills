---
name: note
description: Summarize conversation into a knowledge note in basic-memory vault
---

# Note Skill — 沉淀为知识笔记

将当前 Claude Code 会话对话内容总结为一篇知识笔记，通过 basic-memory MCP 写入 vault。

## Usage

```
/note [--dir 目录名]
```

| 命令 | 效果 |
|------|------|
| `/note` | 保存到 `learning/` 目录 |
| `/note --dir aiinfra` | 保存到 `project/aiinfra/` 目录 |

## Important: MCP 项目指定

**所有 basic-memory MCP 工具调用必须指定 `main` 项目。** 在调用任何 MCP 函数前，确认当前项目为 main，或在调用参数中显式指定项目为 main。

## Behavior

1. **解析参数** — 检查 `--dir` 参数。无参数时目标目录为 `learning/`，有 `--dir xxx` 时目标目录为 `project/xxx/`。`xxx` 必须原样使用，不做任何转换。

2. **分析对话** — 回顾从会话开始到当前的全部对话内容，识别核心知识点、关键概念、技术细节和结论。

3. **生成标题** — 从对话内容中提取最核心的主题，生成简洁、描述性的标题。中文优先（匹配 vault 现有风格），英文专有名词保留原文（如 `HNSW`、`PostgreSQL`）。

4. **生成标签** — 从内容中提取 3-7 个标签。优先使用小写英文标签（如 `distributed-systems`、`vector-search`），对没有英文等价词的领域概念使用中文标签（如 `分布式事务`）。至少生成一个标签。

5. **生成 permalink**：
   - 默认（无 `--dir`）：`main/learning/{slug}`
   - 有 `--dir xxx`：`main/project/{xxx}/{slug}`
   - Slug 规则：保留专有名词和缩写的大小写（如 `HNSW`、`PostgreSQL`、`Claude Code`），空格转为连字符，保留中文字符。示例：`main/learning/HNSW`、`main/learning/Claude Code 生态工具集调研报告`
   - 不插入子分类路径。Vault 中存在不一致的子分类模式（约 33 篇有子分类，20 篇无子分类），新笔记统一使用扁平格式，避免 LLM 错误猜测子分类。

6. **搜索相关笔记** — 使用 basic-memory MCP 的 `search_notes` 工具（`search_type: "hybrid"`，项目=main）搜索与当前内容相关的已有笔记：
   - 用标题关键词和标签作为搜索查询
   - 从搜索结果中提取 `title` 字段（不是 permalink）作为 wikilink 目标
   - **关键**：Wikilink 必须使用笔记标题格式 `[[HNSW]]`、`[[Agent 召回技术]]`，而不是 permalink 格式 `[[main/learning/hnsw]]`。这匹配 vault 现有约定和 Obsidian 解析行为
   - 选择最多 5 篇最相关的笔记
   - 如果 `search_notes` MCP 不可用，跳过此步骤并在完成后告知用户
   - 如果没有找到相关笔记，`## 相关笔记` 区域留空，不添加 `- [[]]` 占位行

7. **碰撞检测** — 使用 basic-memory MCP 的 `search_notes`（项目=main）按标题搜索是否已存在同名笔记。如果存在，告知用户该笔记将被覆盖，然后继续。

8. **写入文件** — 使用 basic-memory MCP 的 `write_note` 工具（项目=main）写入笔记：

   调用参数：
   - `title`: 生成的标题
   - `content`: 笔记正文内容（含相关笔记区域），格式如下：
     ```markdown
     {根据对话内容自然组织的知识总结，自由结构}

     ## 相关笔记

     - [[已有笔记标题]] — 关联说明
     - [[另一篇笔记标题]] — 关联说明
     ```
   - `directory`: 目标目录（`learning` 或 `project/{xxx}`）
   - `tags`: 生成的标签列表
   - `note_type`: `note`
   - `overwrite`: true

   - 笔记正文为自由结构，根据对话内容的自然逻辑组织章节
   - `## 相关笔记` 是唯一定位的固定区域
   - frontmatter 由 write_note 自动生成（title, type, tags, permalink 等字段）
   - 如果没有找到相关笔记，content 中 `## 相关笔记` 后不留任何占位行

9. **确认完成** — 告知用户笔记已创建，显示标题、目录路径和关联笔记数量。提醒用户如需立即搜索此笔记，可运行 `basic-memory sync`。

## Tag 示例

参考 vault 中现有标签风格：

| 英文标签 | 中文标签 |
|---------|---------|
| `distributed-systems` | `分布式事务` |
| `vector-search` | `幂等性` |
| `mcp` | `限流` |
| `agent` | `对账` |
| `claude-code` | |
| `postgresql` | |

## Permalink 示例

| 标题 | Permalink | 目录 |
|------|-----------|------|
| HNSW | `main/learning/HNSW` | `learning` |
| Claude Code 生态工具集调研报告 | `main/learning/Claude Code 生态工具集调研报告` | `learning` |
| Agent 召回技术 | `main/learning/Agent 召回技术` | `learning` |
| 云端知识图谱 | `main/project/aiinfra/云端知识图谱` | `project/aiinfra` |
