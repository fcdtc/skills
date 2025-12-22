# Releases

Version history for this repository (95 releases).

## v0.8.0: Release v0.8.0
**Published:** 2025-12-18

## What's Changed
* .github: check go build in examples, interface{} usage and license headers in all go files by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/808
* llmagent: add refresh toolset on run option by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/793
* summary: fix concurrent map read and write by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/815
* agent: provide SubAgentSetter to set subagents by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/792
* feat(artifact): add S3-compatible artifact storage service by @grignolalouis in https://github.com/trpc-group/trpc-agent-go/pull/784
* {model/ollama, model/gemini}: standardize options initialization by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/806
* .github: enhance gofmt output info to avoid confusion by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/819
* examples: add graph MCP tool example by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/804
* docs: add graph tools QA by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/822
* session/summary: add option to skip recent events during summarization by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/810
* graph: per-run channels isolation by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/812
* session: enhance GetSessionSummaryText with filter key support by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/817
* docs: clarify summarization trigger conditions in session docs and comments by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/823
* docs: add graph concurrency note by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/829
* server/agui: emit text end event when finish_reason occurs by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/825
* docs: enhance callbacks and runner documentation for safe stopping by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/824
* agent/graphagent: move initial state preparation after callbacks by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/826
* feat(storage): implement milvus vector store by @chengjoey in https://github.com/trpc-group/trpc-agent-go/pull/744
* internal/state: preserve numeric literals in session state injection by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/811
* storage: impl mongodb storage by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/757
* model: optimize the initialization of TokenCounter and TailoringStrategy by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/807
* {llmagent, graphagent}: improve message filtering mode options by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/779
* agent/graphagent: collect agent error for after agent callback by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/827
* {knowledege, storage}: fix gofmt linter by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/833
* knowledge: fix metadata filter(break changes) and fix issue on pgvector hybrid filtering by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/754
* summary: add pre/post summary hooks for input/output modification by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/838
* session: support hook for GetSession and AppendEvent by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/809
* tool: add web fetch by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/722
* summary: fix session events not in user->assistant order after summary by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/759
* a2a: support code execution transfer and fix issue on non-streaming a2a transfer by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/813
* example: simplify examples of knowledge by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/846
* {processor/content, tool/agent}: enhance message filtering to ensure that invocation.Message is not lost by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/818
* examples/graph: reorder error handling in streaming response processing by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/820
* graph: fix subgraph event filterKey hierarchy by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/828
* examples: upgrade agui dependencies to prevent known vulnerabilities by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/830
* docs: add RemoveAllMessages guidance to manage message history by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/831
* examples/summary: add filterKey example with AppendEventHook for summary by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/848
* knowledge: fix issue on tcvector cond converter by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/835
* session/redis: refactor to solve cyclomatic complexity by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/841
* git-action: remove detailed output of unit test in github action by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/843
* docs: add positioning for session and memory by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/842
* {agent, docs}: support summary for graph agent by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/850
* tool:  include required fields based on JSON tags for pointer type by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/851
* summary: update summarization options to use custom skip function by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/840
* tool: add ToolResultMessages callback by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/856
* tools: treat the toolCalls of delta type choice as tool responses. by @chengjoey in https://github.com/trpc-group/trpc-agent-go/pull/821
* feat(model): implement Hunyuan-compatible model by @chengjoey in https://github.com/trpc-group/trpc-agent-go/pull/832
* a2agent: add invoke_agent span for telemetry by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/834
* invocation/notice: enhance handling of the "notify-before-wait" scenario in event persistence by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/847
* session: fix UpdateSessionState unmarshalling for postgres and mysql session services by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/849
* internal/tool: refactor JSON schema generation to solve linter by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/854
* server/agui: cache AG-UI session in tracker to cut session service calls by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/855
* .github: add goimports check in GitHub Actions workflow by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/859
* lsc: ensure father agent events persist before launching sub-agent by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/836
* telemetry/langfuse: add new observation types and transform function for agent spans by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/867
* lsc: use context logger at all places by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/816
* runner: avoid duplicate graph completion message by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/871
* model: support DeepSeek 3.2 thinking format in OpenAI variant by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/870
* docs: update memory documentation for clarity and usage examples by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/864
* session: add dsn option for pg session by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/860
* agent: add per-agent llm/tool limits by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/863
* session: add SetPrompt and SetModel methods to SessionSummarizer interface by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/858
* vectorstore/milvus: enhance the field conversion of filter and align the filter query conditions by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/837
* session: preserve context values in async summary jobs using WithoutCancel by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/865
* session: fix TestMemoryService_ProcessSummaryJob_RecoversFromPanic  by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/875
* session: impl summary interface for ctxCaptureSummarizer test by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/876
* graph: avoid additional json marshal for json bytes by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/877
* lsc: implement context cloning for goroutines by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/872
* session: remove duplicate SetPrompt and SetModel methods from ctxCaptureSummarizer by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/881
* docs: enhance OpenAI model doc with model name parameter details by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/882
* telemetry: enhance agent invocation tracing with error handling and event emission by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/874
* knowledge: add unified score normalized of milvus and fix issue on condition convert of milvus by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/844
* graph: add EventEmitter for node custom event emission by @965954485 in https://github.com/trpc-group/trpc-agent-go/pull/869
* knowledge: fix gomod of milvus vectorstore by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/884
* lsc: move debug server internal by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/887
* internal/flow: insert summary after the first system message by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/888
* telemetry:  accumulate token usage for invoke_agent by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/894
* readme: update architecture graph by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/883
* {agent, runner, docs}: supports dynamic agent switching on request level by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/845
* runner: enhance context handling in summary jobs by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/889
* session: enhance summary job processing with cascade fallback by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/895
* {server/agui, docs, examples}: support StartSpan for AG-UI by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/890
* internal/flow: format session summary content by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/891
* {agent, internal/flow}: support reasoning content discarding in agents by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/873
* session: start async summary worker only when summarizer is provided by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/904

## New Contributors
* @grignolalouis made their first contribution in https://github.com/trpc-group/trpc-agent-go/pull/784
* @965954485 made their first contribution in https://github.com/trpc-group/trpc-agent-go/pull/869

**Full Changelog**: https://github.com/trpc-group/trpc-agent-go/compare/v0.7.0...v0.8.0

[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/v0.8.0)

---

## v0.7.0: Release v0.7.0
**Published:** 2025-12-04

## What's Changed
* agui: add UpdateSessionState method for test server to fix test by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/743
* model/openai: sanitize empty tool_calls chunks by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/745
* graph: check nil choices from final response by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/747
* docs: update graph.md for consistency and clarity by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/748
* examples: fix format output of graph basic example by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/749
* lsc: use valid version instead of v0.0.0-00010101000000-000000000000 by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/753
* server/debug: add detached context for debug server by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/751
* a2a: support a2a compatible with adk by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/731
* knowledge: support ocr handling  by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/643
* {agent, graph}: implement generic getter for typed state retrieval by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/752
* server/openai: add OpenAI-compatible server by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/707
* knowledge/reranker: add query parameters to the rerank interface to provide sufficient contextual information for rerank processing by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/729
* {session/mysql, session/postgres}: fix event filtering to ensureat least one user message by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/750
* knowledge: fix knowledge reader not auto registered by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/760
* agent: add generic getter for typed runtime state retrieval by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/765
* server/agui: still return existing messages even on snapshot error by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/763
* agent: add runtime state retrieval from context by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/768
* docs: update the code snippet in the session by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/769
* model: append tool outputschema to tool description by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/756
* knowledge/vectorstore/pgvector: optimize document update operations to reduce unnecessary network calls by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/770
* docs: add track events table for postgres by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/773
* graph: return Done Response event but keep not emit it by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/776
* docs: add callback registration usage by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/771
* {docs, agent}: enhance AfterAgentArgs to include FullResponseEvent by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/775
* {agent,graph,internal/util}: add internal utility package by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/777
* invocation: add logging for notifications to help debug timeout issues by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/774
* {server/agui, graph}: support graph event for agui by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/762
* {session, memory}: simplify duplicate logic in the new service through refactoring by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/758
* graph/checkpoint/redis: support redis checkpoint service by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/720
* tool: add a new email tool and an example agent for sending email by @201430098137 in https://github.com/trpc-group/trpc-agent-go/pull/714
* checkpoint/redis: fix incorrect log package import by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/785
* internal/flow: use per-invocation include_contents flag by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/780
* {checkpoint/inmemory, checkpoint/sqlite}: align the semantics of namespaces with Redis by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/783
* tool/mcp: append StructuredContent to mcp results by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/789
* telemetry: add support for thinking_enabled attribute in GenAI tracing by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/791
* log: add context logger by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/794
* examples: update go.mods and add new one for graph module by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/798
* {server/agui, docs, examples}: add ctx params for Translate by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/799
* model: improve httpClient and standardize options initialization by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/790
* lsc: standardize options initialization by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/788
* {evaluation, docs, examples}: support tool criterion by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/742
* .github: add CI check for examples go.mod and go.sum files by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/800
* {server/agui, examples}: support activity message for history by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/766
* add:model gemini by @pherzheyu in https://github.com/trpc-group/trpc-agent-go/pull/732
* lsc: use real version instead of v0.0.0-00010101000000-000000000000 by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/801
* internal/flow: insert session summary after existing system messages by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/796
* document: correct session document by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/805
* feat(model): implement Ollama-compatible model by @chengjoey in https://github.com/trpc-group/trpc-agent-go/pull/781
* server/a2a:  support both pointer and value types part in A2A protocol  converter by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/802
* server/agui: support aggregator to aggregate AGUI events by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/797
* agent: allow dynamic toolsets by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/795
* lsc: update copyright and license and downgrade go version by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/803

## New Contributors
* @201430098137 made their first contribution in https://github.com/trpc-group/trpc-agent-go/pull/714

**Full Changelog**: https://github.com/trpc-group/trpc-agent-go/compare/v0.6.0...v0.7.0

[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/v0.7.0)

---

## session/mysql/v0.6.0: Release  session/mysql/v0.6.0
**Published:** 2025-12-01



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/session/mysql/v0.6.0)

---

## tool/arxivsearch/v0.6.1: Release tool/arxivsearch/v0.6.1
**Published:** 2025-11-26



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/tool/arxivsearch/v0.6.1)

---

## server/debug/v0.6.1: Release server/debug/v0.6.1
**Published:** 2025-11-26



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/server/debug/v0.6.1)

---

## server/agui/v0.6.1: Release server/agui/v0.6.1
**Published:** 2025-11-26



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/server/agui/v0.6.1)

---

## model/provider/v0.6.1: Release v0.6.1
**Published:** 2025-11-26



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/model/provider/v0.6.1)

---

## model/anthropic/v0.6.1: Release model/anthropic/v0.6.1
**Published:** 2025-11-26



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/model/anthropic/v0.6.1)

---

## memory/postgres/v0.6.1: Release memory/postgres/v0.6.1
**Published:** 2025-11-26



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/memory/postgres/v0.6.1)

---

## memory/mysql/v0.6.1: Release memory/mysql/v0.6.1
**Published:** 2025-11-26



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/memory/mysql/v0.6.1)

---

## evaluation/v0.6.1: Release evaluation/v0.6.1
**Published:** 2025-11-26



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/evaluation/v0.6.1)

---

## server/debug/v0.6.0: release server/debug/v0.6.0
**Published:** 2025-11-25



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/server/debug/v0.6.0)

---

## evaluation/v0.6.0: Release evaluation v0.6.0
**Published:** 2025-11-25



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/evaluation/v0.6.0)

---

## v0.6.0: Release v0.6.0
**Published:** 2025-11-24

## What's Changed
* feat(tool): implement arxiv search tool by @chengjoey in https://github.com/trpc-group/trpc-agent-go/pull/629
* difyagent: Add DifyAgent package to support Dify platform integration by @liujin0506 in https://github.com/trpc-group/trpc-agent-go/pull/651
* example: optimize comment on code by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/658
* graph: refactor the conditional edge processing logic in the graph by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/626
* fix(test): use fake arxiv server for example test by @chengjoey in https://github.com/trpc-group/trpc-agent-go/pull/660
* session: remove unnecessary check and fix tests by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/659
* {examples, docs}: best practices for AG-UI generates documentation by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/656
* graph: fix deep copy for time.Time pointers by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/657
* internal/flow: refactor mergeParallelToolCallResponseEvents by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/652
* examples: fix parallel execution issue in graph_debugserver by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/665
* session: impl mysql session by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/653
* docs: add strict mkdocs build workflow and update docs relative path by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/661
* session: optimize duplicate hash calculation in async task dispatching by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/662
* docs: restore model switching docs deleted accidentally by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/664
* .github: add patch coverage threshold by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/684
* examples/llmagent: integrate runner  by @wangxuw in https://github.com/trpc-group/trpc-agent-go/pull/685
* telemetry: fix token usage handle by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/667
* {difyagent,evaluation}: Fix the version of trpc-agent-go in go.mod by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/671
* session: enhance job enqueueing test with blocking summarizer by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/672
* docs: correct the default value of SkipSummarization to false by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/687
* {docs, examples, model}: implement token tailoring for provider by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/655
* knowledge: support minscore in knowledge tool by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/686
* session/mysql: aligning asynchronous persistence and session summary feature with the standard by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/673
* memory/redis: enhance Redis service connection handling by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/674
* memory/mysql: add MySQL memory service with initialization and configuration options by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/676
* memory/postgres: add schema support by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/678
* tool/funciton: add inputschema and outputschema option by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/682
* codeexector/local: add WithCodeBlockDelimiter option by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/677
* trpc-agent-go: break down each module test into jobs by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/689
* feat(tool): implement google toolSet(search) by @chengjoey in https://github.com/trpc-group/trpc-agent-go/pull/669
* model: add WithShowToolCallDelta option by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/688
* feat(openai): add accumulate chunk token usage functionality by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/666
* a2a: support tool calls and tool response event transfer on a2a by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/681
* session: fix event filtering to ensure at least one user message by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/679
* openai: refactor reasoning content to cout token usage when handling empty choices by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/694
* telemetry/lanfuse: transform user id and session id by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/695
* add embedder: text-embedding-interface, which is support by huggging face by @wjf222 in https://github.com/trpc-group/trpc-agent-go/pull/670
* graph: add DeepCopier interface for custom deep copy behavior in user-defined types by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/692
* examples: add react style graph agent example by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/697
* {llmagent,flow}: add WithToolFilter configuration to LLMAgent for tool filtering during execution by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/690
* tool/mcp: add unified tool filter interface and deprecate legacy filters by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/654
* session: move session/internal/session to internal/session by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/700
* docs/session: fix mysql session docs by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/702
* examples: use event.IsRunnerCompletion to prevent hang by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/704
* openai: don't skip chunk when having token usage by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/706
* go.mod: go mod tidy all the directories by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/710
* server/agui: correct id for assistant message and tool result event by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/703
* docs: enhance error handling and improve output formatting in session examples by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/718
* tool/mcp: add Init to surface MCP init errors by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/716
* graph: refactor and consolidate graph state copy logic to avoid unnecessary deep copies by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/696
* skill: demonstrate usage of file input by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/709
* examples: refactor memory service configuration by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/717
* go.mod: remove unused replace directive for postgres memory package by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/723
* example: simplify runner exampls and add session examples by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/724
* {model, docs}: support WithHeaders Option by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/721
* {evaluation, server/debug}: integrate evaluation for debug server by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/711
* model: support thinking time calculate by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/708
* agent: add with resume option for agent by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/680
* {server, session}: store agui events in session by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/698
* trpc-agent-go: fix coverage report in CI by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/712
* knowledge: fix document id generation in synchronous mode by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/730
* model: propagate finished reasons to the final response by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/728
* examples: add go.mod for debugserver example by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/727
* flow: unify transfer_to history to one user message by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/691
* doc: fix summary document by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/735
* lsc: introduce structured callback interfaces for better expandability by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/644
* examples: make dependencies of runner as simple as possible by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/736
* a2a: fix multi tools transfer on a2a by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/740
* {agent, event, log}: Output EmitEvent logs at the trace level by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/739
* session/redis: improve hash index calculation by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/738
* {session/inmemory,session/redis}: fix event filtering to ensure at least one user message by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/737
* session: support update session state by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/713

## New Contributors
* @liujin0506 made their first contribution in https://github.com/trpc-group/trpc-agent-go/pull/651
* @wangxuw made their first contribution in https://github.com/trpc-group/trpc-agent-go/pull/685

**Full Changelog**: https://github.com/trpc-group/trpc-agent-go/compare/v0.5.0...v0.6.0

[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/v0.6.0)

---

## storage/tcvector/v0.6.0: Release storage/tcvector/v0.6.0
**Published:** 2025-11-24



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/storage/tcvector/v0.6.0)

---

## storage/redis/v0.6.0: storage/redis/v0.6.0
**Published:** 2025-11-24



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/storage/redis/v0.6.0)

---

## storage/postgres/v0.6.0: relaase storage/postgres/v0.6.0
**Published:** 2025-11-24



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/storage/postgres/v0.6.0)

---

## storage/mysql/v0.6.0: storage/mysql/v0.6.0
**Published:** 2025-11-24



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/storage/mysql/v0.6.0)

---

## storage/elasticsearch/v0.6.0: storage/elasticsearch/v0.6.0
**Published:** 2025-11-24



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/storage/elasticsearch/v0.6.0)

---

## session/redis/v0.6.0: session/redis/v0.6.0
**Published:** 2025-11-24



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/session/redis/v0.6.0)

---

## session/postgres/v0.6.0: session/postgres/v0.6.0
**Published:** 2025-11-24



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/session/postgres/v0.6.0)

---

## server/agui/v0.6.0: server/agui/v0.6.0
**Published:** 2025-11-24



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/server/agui/v0.6.0)

---

## model/tiktoken/v0.6.0: model/tiktoken/v0.6.0
**Published:** 2025-11-24



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/model/tiktoken/v0.6.0)

---

## model/anthropic/v0.6.0: model/anthropic/v0.6.0
**Published:** 2025-11-24



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/model/anthropic/v0.6.0)

---

## memory/redis/v0.6.0: memory/redis/v0.6.0
**Published:** 2025-11-24



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/memory/redis/v0.6.0)

---

## memory/postgres/v0.6.0: memory/postgres/v0.6.0
**Published:** 2025-11-24



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/memory/postgres/v0.6.0)

---

## memory/mysql/v0.6.0: memory/mysql/v0.6.0
**Published:** 2025-11-24



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/memory/mysql/v0.6.0)

---

## knowledge/vectorstore/tcvector/v0.6.0: knowledge/vectorstore/tcvector/v0.6.0
**Published:** 2025-11-24



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/vectorstore/tcvector/v0.6.0)

---

## knowledge/vectorstore/pgvector/v0.6.0: knowledge/vectorstore/pgvector/v0.6.0
**Published:** 2025-11-24



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/vectorstore/pgvector/v0.6.0)

---

## knowledge/vectorstore/elasticsearch/v0.6.0: knowledge/vectorstore/elasticsearch/v0.6.0
**Published:** 2025-11-24



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/vectorstore/elasticsearch/v0.6.0)

---

## knowledge/embedder/gemini/v0.6.0: knowledge/embedder/gemini/v0.6.0
**Published:** 2025-11-24



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/embedder/gemini/v0.6.0)

---

## knowledge/document/reader/pdf/v0.6.0: knowledge/document/reader/pdf/v0.6.0
**Published:** 2025-11-24



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/document/reader/pdf/v0.6.0)

---

## codeexecutor/container/v0.6.0: codeexecutor/container/v0.6.0
**Published:** 2025-11-24



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/codeexecutor/container/v0.6.0)

---

## v0.5.0: Release v0.5.0
**Published:** 2025-11-13

## What's Changed
* examples: show pre-request model switching with runner by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/567
* docs: fix typo and remove dots by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/569
* server/agui: use IsRunnerCompletion instead of IsFinalResponse by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/570
* knowledge: add storage layer of pgvector by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/568
* {example, model}: update token tailoring formula and refactor example by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/572
* storage: make deafault client builder of pgsql private by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/576
* model/openai: do not ignore reasoning content while streaming by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/577
* examples: fix jsonschema comma separator by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/581
* graph: provide external tool example using interrupt/resume by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/584
* storage: make default client builders private and simplify registry lookups by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/579
* storage/mysql: implement storage for MySQL client by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/571
* {agent, examples, docs}: implement State for Invocation by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/565
* telemetry: add metrics by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/519
* graph: skip internal state key to avoid map panic by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/585
* {model, examples, docs}: support anthropic model by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/575
* examples: update example to execute normal tool after external tool by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/591
* model: add PromptTokensDetails to  observe Prompt/Context caching by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/582
* {storage, memory, examples}: mysql implementation for memory service by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/515
* {evaluation, examples, docs}: support evaluation by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/416
* telemetry/appid: add app/agent name registry for report by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/597
* feat: support jupyter code execution by @chengjoey in https://github.com/trpc-group/trpc-agent-go/pull/578
* feat(telemetry): allow overriding OTEL resource service fields and custom attrs via env or options by @minimAluminiumalism in https://github.com/trpc-group/trpc-agent-go/pull/594
* {server, examples, docs}: add messages snapshot event for agui by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/595
* tool: add  filtering mechanism by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/590
* server/agui: supports parallel tool calls for agui by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/604
* {server/agui, docs}: add agui base url usage document by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/601
* graph: provide multi-conditional edges by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/596
* {server/agui, examples, docs}: add userID for AG-UI MessagesSnapshotEvent by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/602
* agent: add per-run tool filtering support by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/580
* session: impl pgsql session by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/592
* {processor/content,graph_agent,llm_agent}: support  branchFilterMode option and timelineFilterMode option to filter event message by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/593
* model: Add a variant type: deepseek by @wjf222 in https://github.com/trpc-group/trpc-agent-go/pull/599
* tool/function: support skip summarization for function tools by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/607
* graph: add node callbacks as internal state key and check nil by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/609
* {server/agui, docs}: support RunOptionResolver for AG-UI by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/612
* flow: lower error log to warn by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/610
* tool: print warning log when name or description is empty by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/614
* {graph,state_schema}: allow disabling deep copy per key by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/613
* feat(telemetry): add dual time-to-first-token metrics and stream request attribute by @minimAluminiumalism in https://github.com/trpc-group/trpc-agent-go/pull/611
* {model, docs, examples}: support model provider by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/600
* knowledge: support coditioned filter and mult documents in search tool by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/586
* readme: add Star History chart by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/619
* {memory, examples}: postgres implementation for memory service  by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/598
* feat(embedder): implement ollama embedder by @chengjoey in https://github.com/trpc-group/trpc-agent-go/pull/603
* server/agui: add log for agui by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/615
* {examples, docs}: add provider example by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/618
* event: add JSON marshal/unmarshal to avoid field shadowing by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/588
* server/agui: unique user messages based on requestID in AGUI MessagesSnapshot by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/616
* memory/mysql: remove UTC conversion for timestamps by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/622
* session: Remove incorrect UTC conversion, alter app_state/user_state to text by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/623
* model:Add a variant type: qwen by @pherzheyu in https://github.com/trpc-group/trpc-agent-go/pull/625
* {session/postgres}: add timeout for async persistence by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/620
* session/summary: align PostgreSQL session summary logic with the standard by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/621
* runner: implement Close method for resource cleanup by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/628
* session: add WaitGroup to ensure async workers closing correctly by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/630
* knowledge: support custom index param in pgvector by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/627
* memory: fix Delete and Clear tools not having a default creator by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/633
* {doc, model}: support token tailoring for anthropic by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/606
* session: export local session operations to enable users to implement custom session service by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/632
* Docs: Add the introduction documentation of variant by @wjf222 in https://github.com/trpc-group/trpc-agent-go/pull/624
* doc(toolset): add documentation for custom toolset naming option in NewMCPToolSet by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/636
* model/openai: remove duplicate chatResponseCallback calls by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/635
* {docs, examples}: update runner cleanup instructions by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/639
* docs: keep docs up to date with code by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/640
* processor/content: fix user message loss issue in TimelineFilterCurrentInvocation mode by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/637
* {llmflow, graph}: fix error always nil in AfterModel and AfterAgent callbacks by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/641
* skill: implement preview of agent skills by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/573
* examples: add HTTP headers example using HTTPBeforeRequest by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/574
* knowledge: support remote embedding of tcvector by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/605
* add:model qwen enabel thinking by @pherzheyu in https://github.com/trpc-group/trpc-agent-go/pull/634
* knowledge: enhance markdown chunking by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/638
* processor/content: fix ObjectType mismatch by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/646
* {agent, server}: set response IDs and object types in a2a by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/650
* llmagent: set the wrapperChannel's capacity to match the original channel's capacity by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/649
* server/agui: filter event with empty content by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/647
* graph: prevent stale interrupt resume data from being reused by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/642
* server/debug: keep graph completion event in streaming mode by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/648

## New Contributors
* @chengjoey made their first contribution in https://github.com/trpc-group/trpc-agent-go/pull/578
* @minimAluminiumalism made their first contribution in https://github.com/trpc-group/trpc-agent-go/pull/594
* @wjf222 made their first contribution in https://github.com/trpc-group/trpc-agent-go/pull/599
* @pherzheyu made their first contribution in https://github.com/trpc-group/trpc-agent-go/pull/625

**Full Changelog**: https://github.com/trpc-group/trpc-agent-go/compare/v0.4.0...v0.5.0

[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/v0.5.0)

---

## storage/tcvector/v0.5.0: Release storage/tcvector/v0.5.0
**Published:** 2025-11-13



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/storage/tcvector/v0.5.0)

---

## storage/redis/v0.5.0: Release storage/redis/v0.5.0
**Published:** 2025-11-13



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/storage/redis/v0.5.0)

---

## storage/postgres/v0.5.0: storage/postgres/v0.5.0
**Published:** 2025-11-13



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/storage/postgres/v0.5.0)

---

## storage/mysql/v0.5.0: storage/mysql/v0.5.0
**Published:** 2025-11-13



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/storage/mysql/v0.5.0)

---

## storage/elasticsearch/v0.5.0: storage/elasticsearch/v0.5.0
**Published:** 2025-11-13



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/storage/elasticsearch/v0.5.0)

---

## session/redis/v0.5.0: session/redis/v0.5.0
**Published:** 2025-11-13



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/session/redis/v0.5.0)

---

## session/postgres/v0.5.0: session /postgres/v0.5.0
**Published:** 2025-11-13



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/session/postgres/v0.5.0)

---

## server/agui/v0.5.0: server/agui/v0.5.0
**Published:** 2025-11-13



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/server/agui/v0.5.0)

---

## model/tiktoken/v0.5.0: model/tiktoken/v0.5.0
**Published:** 2025-11-13



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/model/tiktoken/v0.5.0)

---

## model/anthropic/v0.5.0: model/anthropic/v0.5.0
**Published:** 2025-11-13



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/model/anthropic/v0.5.0)

---

## memory/redis/v0.5.0: memory/redis/v0.5.0
**Published:** 2025-11-13



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/memory/redis/v0.5.0)

---

## memory/postgres/v0.5.0: memory /postgres/v0.5.0
**Published:** 2025-11-13



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/memory/postgres/v0.5.0)

---

## memory/mysql/v0.5.0: memory/mysql/v0.5.0
**Published:** 2025-11-13



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/memory/mysql/v0.5.0)

---

## knowledge/vectorstore/tcvector/v0.5.0: knowledge/vectorstore/tcvector/v0.5.0
**Published:** 2025-11-13



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/vectorstore/tcvector/v0.5.0)

---

## knowledge/vectorstore/pgvector/v0.5.0: knowledge/vectorstore/pgvector/v0.5.0
**Published:** 2025-11-13



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/vectorstore/pgvector/v0.5.0)

---

## knowledge/vectorstore/elasticsearch/v0.5.0: knowledge/vectorstore/elasticsearch/v0.5.0
**Published:** 2025-11-13



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/vectorstore/elasticsearch/v0.5.0)

---

## knowledge/embedder/gemini/v0.5.0: knowledge/embedder/gemini/v0.5.0
**Published:** 2025-11-13



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/embedder/gemini/v0.5.0)

---

## knowledge/document/reader/pdf/v0.5.0: knowledge/document/reader/pdf/v0.5.0
**Published:** 2025-11-13



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/document/reader/pdf/v0.5.0)

---

## codeexecutor/container/v0.5.0: codeexecutor/container/v0.5.0
**Published:** 2025-11-13



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/codeexecutor/container/v0.5.0)

---

## v0.4.0: Release v0.4.0
**Published:** 2025-10-28

## What's Changed
* knowledge: enhance the retrieval and filtering capabilities of vector store by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/464
* tool: add Name interface and NamedToolSet struct to fix naming conflict by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/473
* model: implement custom JSON marshaling and unmarshaling for FunctionDefinitionParam by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/481
* typos: update typos.toml to ignore UE by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/475
* examples/knowledge: change module path and go mod tidy by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/476
* tool: enhance function tool documentation with LLM API naming requirements by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/477
* examples/transfer: add time calculation agent and update transfer system by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/479
* knowledge/vectorstore/elasticsearch: correct export field serialization/deserialization mismatch by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/486
* docs: enhance session.md with session summarization by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/488
* knowledge: support SearchMode parameter passthrough by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/490
* {graph, knowledge/embedder}: refactor to solve cyclomatic complexity and go mod tidy by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/489
* knowledge/vectorstore/pgvector: support user-defined document parsing and export field by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/480
* knowledge/vectorstore/tcvector: export collection fields with support for user-defined field names​ by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/484
* {server/agui, examples, docs}: support translate callback for agui by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/487
* knowledge/vectorstore/pgvector: add universal query filters for pgvector store by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/491
* {.github, knowledge}: run tests across all go modules in CI by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/493
* lsc: update telemetry to integrate galileo by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/478
* knowledge: support Like and Between filter condition by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/492
* knowledge: support desc and name options of knowledge tool by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/485
* knowledge/vectorstore/inmemory: add universal query filters for in-memory store by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/494
* docs: add docs for graph node-level retry by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/474
* docs: add docs on custom graph event generation by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/482
* knowledge/vecstor/inmemory: enhance panic handling in comparisonFunc by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/497
* {graph/executor,knowledge/vectorstore}: fix panic issues caused by reflect operation​ by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/498
* docs/runner: fix example code by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/496
* {graph, model, examples}: implement token tailoring functionality with strategies and counters by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/411
* graph: implement validation for stateSchema by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/500
* knowledge/vector: improve unit test cases for filterCondition boundary conditions by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/501
* internal: avoid always calling StreamableCall for NamedTool by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/502
* graph: support node cache by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/467
* knowledge: increase test coverage by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/508
* model/openai: refactor empty chunk check and improve tests by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/503
* flow/processor/functioncall: support callbacks to intervene when tool execution fails by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/509
* docs: fix misplaced braces by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/512
* agent: support transfer cutomed http header and specific user ID header of a2a agent  by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/505
* agenttool: add history scope option by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/483
* tool/file: capture per-iter var and fix test by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/499
* examples: add mapreduce example for graph by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/506
* graph: support visualization for graph by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/507
* graph: add retrieval placeholder example by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/514
* event: add is runner completion helper function by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/513
* flow: Add TansferTag to filter internal delegation messages for users by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/516
* {graph, runner, tool}: refactor to solve linter by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/520
* update codecov token configuration for protected branch by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/526
* session: increase test coverage for session package by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/529
* storage: increase test coverage for storage package by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/528
* flow/responseProcessor: skip processing of IsPartial events by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/523
* memory: increase test coverage for memory package by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/531
* {agent, model}: improve test coverage significantly by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/532
* graph: increase test coverage for graph package by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/524
* internal: increase test coverage for internal package by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/525
* telemetry: add unit test by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/535
* session/redis: clean up unused Summary field by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/534
* tool: improve test coverage by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/533
* {event, runner}: add more tests by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/530
* event: increase test coverage for event package by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/537
* server: increase test coverage for server package by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/538
* graph: implement per-node ends with branch validation by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/504
* {server/agui, docs}: add RunAgentInput Hook for AG-UI by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/536
* event: remove duplicate test by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/542
* agent: resolve agent card by a2a.Client by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/511
* state: support mustache form for placeholders by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/517
* flow: add option to set or ignore delegation message by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/510
* runner: support third party agent config in runner by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/518
* docs: add docs for batch API, retry and switching by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/544
* tool: add recursive structure support in JSON schema by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/447
* agent: support setting of instruction dynamically by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/540
* graph: support mapping last_response to user_input option by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/541
* {memory, session}: add more tests by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/546
* codeexecutor: increase test coverage for codeexecutor package  by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/547
* knowledge: improve unit test of knowledge by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/545
* knowledge/vector/elasticsearch: supports SearchModeFilter pattern search for ES by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/543
* knowledge: fix unit test of es by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/550
* {knowldege, agent} : improve unit test  by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/552
* docs: fix reference path in graph by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/551
* knowledge: fix deadlock of reader registry by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/549
* session/inmemory: optimize lock acquisition timing by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/554
* model: increase model coverage by @sandyskies in https://github.com/trpc-group/trpc-agent-go/pull/555
* Agent: Increase Agent coverage by @sandyskies in https://github.com/trpc-group/trpc-agent-go/pull/556
* {server/agui, examples/agui}: fix css in copilotkit and upgrade agui sdk by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/557
* Agent: Increase Agent unittest coverage by @sandyskies in https://github.com/trpc-group/trpc-agent-go/pull/559
* graph: support parallel execution for tool node by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/548
* telemetry:  add session id and user id for chat and tool span by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/561
* session/redis: skip malformed event for json unmarshal by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/562
* flow: add preserve same branch to keep correct roles by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/564
* docs: update model.md to include http header setting by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/566
* {doc, examples, agent}: support model switching by name by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/558


**Full Changelog**: https://github.com/trpc-group/trpc-agent-go/compare/v0.3.0...v0.4.0

[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/v0.4.0)

---

## storage/tcvector/v0.4.0: Release storage/tcvector/v0.4.0
**Published:** 2025-10-28

Release storage/tcvector/v0.4.0

[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/storage/tcvector/v0.4.0)

---

## storage/redis/v0.4.0: Release storage/redis/v0.4.0
**Published:** 2025-10-28



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/storage/redis/v0.4.0)

---

## storage/elasticsearch/v0.4.0: Release storage/elasticsearch/v0.4.0
**Published:** 2025-10-28



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/storage/elasticsearch/v0.4.0)

---

## session/redis/v0.4.0: Release session/redis/v0.4.0
**Published:** 2025-10-28



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/session/redis/v0.4.0)

---

## server/agui/v0.4.0: Release server/agui/v0.4.0
**Published:** 2025-10-28



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/server/agui/v0.4.0)

---

## memory/redis/v0.4.0: Release memory/redis/v0.4.0
**Published:** 2025-10-28



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/memory/redis/v0.4.0)

---

## knowledge/vectorstore/tcvector/v0.4.0: Release knowledge/vectorstore/tcvector/v0.4.0
**Published:** 2025-10-28



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/vectorstore/tcvector/v0.4.0)

---

## knowledge/vectorstore/pgvector/v0.4.0: Release knowledge/vectorstore/pgvector/v0.4.0
**Published:** 2025-10-28



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/vectorstore/pgvector/v0.4.0)

---

## knowledge/vectorstore/elasticsearch/v0.4.0: Release knowledge/vectorstore/elasticsearch/v0.4.0
**Published:** 2025-10-28



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/vectorstore/elasticsearch/v0.4.0)

---

## knowledge/embedder/gemini/v0.4.0: Release knowledge/embedder/gemini/v0.4.0
**Published:** 2025-10-28



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/embedder/gemini/v0.4.0)

---

## knowledge/document/reader/pdf/v0.4.0: Release knowledge/document/reader/pdf/v0.4.0
**Published:** 2025-10-28



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/document/reader/pdf/v0.4.0)

---

## codeexecutor/container/v0.4.0: Release codeexecutor/container/v0.4.0
**Published:** 2025-10-28



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/codeexecutor/container/v0.4.0)

---

## v0.3.0: Release v0.3.0
**Published:** 2025-10-14

## What's Changed
* tool/agent: fix test compatibility with tool input event synchronization by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/421
* examples: remove hardcoded API key from graph_debugserver by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/422
* {agent, telemetry}: add output for invoke_agent span by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/419
* {flow,agent_tool,processor/functioncall}: improve the notification wating time during multiple rounds of flow sessions to prevent message non persistence in multi-agent mode by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/424
* internal/flow: fix duplicate tool messages emitted after parallel tool execution by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/420
* graph: Fix event leakage between concurrent nodes by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/425
* docs: update graph docs on subagents by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/428
* knowledge: add url source alias option by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/427
* graph: support multiturn chat for graph by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/423
* {session/summary, examples}: introduce session summary and add summarization example by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/256
* {server/agui, examples, docs}: support agui by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/379
* {invocation,event,runner,session/redis}: improve channel buffer size for runner and add queue monitoring logs by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/426
* {processor/content,session,runner}: Fix read/write race condition in session events by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/429
* {invocation,processor/functioncall,transfer_tool}: Fix transfer message loading failure and Remove the unused endInvocation field by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/430
* docs: update on session service usage on debugserver by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/431
* examples: enhance math specialist tool with input schema and update README by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/432
* examples/llmagent: refactor llmagent example for clarity by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/433
* events: use the correct import of logger by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/434
* {docs, examples}: add agui dependency explanation by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/436
* lsc: refactor to solve linter by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/435
* runner: adjust runner's channel buffer size to match agent's by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/438
* processor/content: refactor get history event message by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/437
* lsc: replace interface{} with any and gofmt files by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/439
* lsc: rename files for clarity by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/442
* lsc: replace isToolEvent with IsFinalResponse method by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/443
* planner: update comment of planner by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/448
* processor/output: enhance JSON extraction in output processor logic by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/440
* knowledge: support user-defined document parsing by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/444
* {examples, model}: support streaming reasoning content and add thinking demo by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/445
* docs: format list for artifact by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/451
* docs: restructure navigation and enable Mermaid diagrams by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/454
* lsc: replace event.Choices with event.Response.Choices by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/452
* tool: default agent tool's skip summarization to false by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/450
* docs: update event stream handling section in agent docs by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/449
* docs: add doc about thinking enabled without planner by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/456
* internal/flow/processor: optimize the logic for extracting JSON objects by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/459
* knowledge/embedder: extract response func to eliminate code duplication by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/461
* {docs,examples}: add usage instructions for RequestID by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/458
* invocation: improve outlier handling for invocation notice by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/455
* telemetry: align with OpenTelemetry GenAI semantic conventions by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/460
* {server/agui, docs}: refactor AG-UI server to use service factories and export runner package by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/457
* {server/agui, examples}: use official agui go sdk dependency by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/463
* examples: update copyright by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/468
* tool: update ToolSet interface to return Tool type by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/469
* tool: update Tools method to return Tool type instead of CallableTool by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/471
* graph: pass pregel error to event.Error by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/470
* graph: add subgraph node and example by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/462
* tool/mcp: add session-level reconnection mechanism by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/378
* knowledge: fix maxResult parameter not working by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/472
* docs: improve graph docs by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/453
* {docs, examples}: add custom translator example for agui by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/466
* graph: support node-level retry for graph by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/465


**Full Changelog**: https://github.com/trpc-group/trpc-agent-go/compare/v0.2.2...v0.3.0

[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/v0.3.0)

---

## session/redis/v0.3.0: 
**Published:** 2025-10-14



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/session/redis/v0.3.0)

---

## server/agui/v0.3.0: Release server/agui/v0.3.0
**Published:** 2025-10-14



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/server/agui/v0.3.0)

---

## v0.2.2: Release v0.2.2
**Published:** 2025-09-25

## What's Changed
* graph: support tool set in graph nodes by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/381
* {processor/functioncall}: improve error handling for functioncall by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/359
* graph: include instruction + user_input in model execution events and fix test validation by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/392
* knowledge/vectorstore/elasticsearch: add support for extra builder-specific options by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/387
* graph: wrap context with sub-invocation for agent node run by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/393
* trpc-agent-go: fix img relative path by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/394
* docs: refactor agent with sub chapter by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/395
* a2a: avoid premature end of streaming for tool events by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/391
* {model, internal/flow}: fix transfer tool call by preventing EndInvocation propagation to target agents by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/396
* graph: add subagent state access example by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/397
* graph: document node I/O conventions and add examples with tools by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/399
* {graph,graphagent,functioncall,llmagent}: improve toolCallbacks retrieval and deprecate the ToolCallbacks field in Invocation and agents for clearer logic  by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/390
* {agent,invocation}: improve AgentCallback retrieval and deprecate the AgentCallbacks field in Invocation for clearer logic by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/388
* telemetry/langfuse: enhance langfuse trace level integration  by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/400
* knowledge/vectorstore/elasticsearch: fix search query builders to handle empty filters without post-filters by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/402
* runner: enhance event check in runner by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/403
* {model/openapi,llmagent,llmflow,graphagent}: improve ModelCallbacks retrieval and deprecate the ModelCallbacks field in Invocation and agents for clearer logic by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/389
* tool/callbacks: change BeforeToolCallback to accept pointer to jsonArgs by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/406
* doc: add a2a agent document by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/407
* graph/executor: skip intermediate nodes after routed by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/404
* graph: support adding generation config for llm model node by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/410
* docs: add Callbacks documentation and update mkdocs navigation by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/412
* planner: Fix content truncated in react by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/405
* graph/state_graph: complete invocation information of internal events in node by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/409
* tool/agent: fix AgentTool infinite loop and refactor event handling by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/401
* model/openai: add ChatStreamCompleteCallback for stream completion handling by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/415
* graph: support placeholder for llm model node by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/413
* tool/agent: ensure tool input is available throughout all AgentTool LM calls by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/417
* server/debug: add graph agent support for debug server by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/414
* graph: continue for nil result returned to avoid stop by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/418
* {graph/executor,invocation}: enhance organizational capabilities of events emitted by graph nodes by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/408
* {llmagent,processor/transfer}: support return to the parent execution process after transfer by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/398


**Full Changelog**: https://github.com/trpc-group/trpc-agent-go/compare/v0.2.1...v0.2.2

[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/v0.2.2)

---

## knowledge/vectorstore/elasticsearch/v0.2.2: Release knowledge/vectorstore/elasticsearch/v0.2.2
**Published:** 2025-09-25



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/vectorstore/elasticsearch/v0.2.2)

---

## v0.2.1: Release v0.2.1
**Published:** 2025-09-19

## What's Changed
* Gomod: downgrade go version to go 1.21 by @sandyskies in https://github.com/trpc-group/trpc-agent-go/pull/364
* Gomod: update gomod by @sandyskies in https://github.com/trpc-group/trpc-agent-go/pull/367
* examples: go mod tidy to fix gomod by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/368
* Gomod: fix elasticsearch go mod by @sandyskies in https://github.com/trpc-group/trpc-agent-go/pull/369
* lsc: downgrage go version and update docs by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/371
* {invocation,event,runner} enhance control over event organization​ for business-layer by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/358
* examples/graph/parallel: aggregate from node_responses and add -verbose by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/360
* internal/flow/processor: simplify tool call handling and improve event merging by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/362
* docs: fix edit_url and improve the robustness of multi-level lists by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/363
* {tool, examples}: support read_multiple_files tool for file tool set by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/361
* session/redis: fix linter and add tests by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/374
* graph: ​​improve event sending in the graph agent​​ by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/365
* knowledge: make syncMockVectorStore thread-safe in tests by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/377
* runner: auto-seed WithMessages into session, processor reads session only by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/370
* graph: pass pre-callback state to node; reorder AfterNode callbacks by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/380
* agent: add panic recovery for ParallelAgent to prevent service crashes by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/375
* agent: cleanup misleading and useless tool fields by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/372
* {session,processor/content}: improve event filtering to ensure only valid events are added to the session by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/357
* a2a: optimize message handling of a2a server by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/376
* {invocation,processor/functioncall,graph/state_graph,docs,example}: fix add notice channel panic by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/382
* graph: deep-copy state for task inputs and checkpoints to prevent concurrent map iteration panics by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/383
* graph/executor: deep-copy final state for completion event to prevent concurrent map iteration during JSON marshal by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/385
* graph: fix panic of state deep copy by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/386
* tool/agent: enhance event filtering in StreamableCall to support sub-agent context by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/384


**Full Changelog**: https://github.com/trpc-group/trpc-agent-go/compare/v0.2.0...v0.2.1

[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/v0.2.1)

---

## storage/tcvector/v0.2.0: Release storage/tcvector/v0.2.0
**Published:** 2025-09-18



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/storage/tcvector/v0.2.0)

---

## storage/elasticsearch/v0.2.1: Release storage/elasticsearch/v0.2.1
**Published:** 2025-09-18



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/storage/elasticsearch/v0.2.1)

---

## storage/elasticsearch/v0.2.0: Release storage/elasticsearch/v0.2.0
**Published:** 2025-09-17



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/storage/elasticsearch/v0.2.0)

---

## knowledge/vectorstore/elasticsearch/v0.2.1: Release knowledge/vectorstore/elasticsearch/v0.2.1
**Published:** 2025-09-17



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/vectorstore/elasticsearch/v0.2.1)

---

## knowledge/embedder/gemini/v0.0.1: Release knowledge/embedder/gemini/v0.0.1
**Published:** 2025-09-18



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/embedder/gemini/v0.0.1)

---

## knowledge/document/reader/pdf/v0.0.1: Release knowledge/document/reader/pdf/v0.0.1
**Published:** 2025-09-18



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/document/reader/pdf/v0.0.1)

---

## v0.2.0: Release v0.2.0
**Published:** 2025-09-16

## What's Changed
* {examples, graph}: add parallel fan-out execution by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/270
* tool/mcp: change connection logs from INFO to DEBUG level by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/292
* Docs： readme update by @sandyskies in https://github.com/trpc-group/trpc-agent-go/pull/299
* lsc: downgrade to go1.21 with pdf/embedder/container as separate modules by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/291
* docs: add artifact.md by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/298
* graph: implement checkpoint and interrupt utilities by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/269
* examples: Update README and configuration for knowledge and A2A subagent examples by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/301
* multiagent: fix the sub-agent's AgentCallbacks not working and reset the invocation within the sub-agent context by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/304
* {internal/flow, server}: avoid memory aliasing in event processing  by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/305
* knowledge: avoid deplicated query enhancer by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/300
* agent: add delta-aware State for CallbackContext by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/295
* knowledge: support data filter and agentic filter by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/236
* {artifact, examples}: fix typo inmemeory => inmemory by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/306
* tool/mcp: add OutputSchema support for MCP tools by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/297
* flow: fix transfer behavior on name and event by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/303
* examples: enhance human-in-the-loop functionality with model and streaming options by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/309
* graph: refactor executor to enhance checkpoint handling and state restoration by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/307
* knowledge/vectorstore: export field name options for elastic search by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/310
* example/debugserver: refactor to support command-line model selection by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/314
* graphagent: remove with tools by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/317
* knowledge/vectorstore: refactor any and improve error handling by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/316
* knowledge/vectorstore: fix default field values for Elasticsearch options by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/319
* graph: increase test coverage by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/320
* {session, docs} : fix session documents by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/318
* {examples/a2a, a2aagent, graph, flow}: improve graph a2asubagent example by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/324
* agenttool: support agent tool inner streaming by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/322
* trpc-agent-go: move requirements.txt and mkdocs.yaml to docs dir by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/321
* {flow, functioncall}: refactor flow and function call response processor ​​to better define its functional boundarie. by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/315
* tool/mcp: fix timeout not working for SSE and streamable_http by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/328
* {graph, examples/graph/basic}: fix messages merge via reducer and clean basic example by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/327
* a2a: add hook for a2a server, add state transfer for a2a agent by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/326
* session/redis: support asynchronous persistence session capability with… by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/325
* {runner, invocation,outputprocessor}: fix runner send notice might block forever when event production rate exceeds runner consumption rate by 5 seconds by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/329
* docs: add custom agent and example by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/336
* {graph, internal/flow}: refactor for cyclomatic and improve coverage by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/331
* {agent, internal/flow/processor}: improve context handling in tests and clean up unused test function by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/338
* {runner,invocation}: enhance notice channel cleanup to prevent resource leaks by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/339
* flow/processor: drain parallel results channel to avoid missing tool responses by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/343
* runner: support run with messages by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/340
* graph: add panic recover protect by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/342
* telemetry: add langfuse exporter to convert attributes by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/312
* docs: improve custom agent docs and example by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/337
* examples/runner: refactor for clarity by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/330
* a2a: optimize a2a error handling by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/334
* session/redis: enhance performance of asynchronous persistence in high-concurrency scenarios by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/344
* {agent, examples/memory, memory, runner}: refactor memory and move to runner by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/323
* a2a: add example test for a2a server by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/346
* examples/graph/diamond: correct results reducer, barrier routing and resume by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/347
* graph: correct empty metadata filter handling and improve example event reporting by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/345
* fix(langfuse): remove hardcoded WithInsecure() and clarify host format by @weeco in https://github.com/trpc-group/trpc-agent-go/pull/351
* {event,invocation,processor/content}: ​​refactor event struct for improved filtering and clearer Branch field guidelines​​  by @nomand-zc in https://github.com/trpc-group/trpc-agent-go/pull/341
* examples: support debug agent demo by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/349
* {codeexecutor,internal}: support relative path and fix codeexecutor event by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/348
* {flow/processor, flow}: propagate SkipSummarization, guard nil final event by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/350
* graph: fix fan-out task writers/triggers resolution and example by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/353
* model/openai: Implement max_completion_tokens option in OpenAI model by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/352
* Docs: remove changelog by @sandyskies in https://github.com/trpc-group/trpc-agent-go/pull/355
* knowledge: Add rag data management by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/296

## New Contributors
* @nomand-zc made their first contribution in https://github.com/trpc-group/trpc-agent-go/pull/304
* @weeco made their first contribution in https://github.com/trpc-group/trpc-agent-go/pull/351

**Full Changelog**: https://github.com/trpc-group/trpc-agent-go/compare/v0.1.2...v0.2.0

[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/v0.2.0)

---

## storage/redis/v0.2.0: Release  storage/redis/v0.2.0
**Published:** 2025-09-16



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/storage/redis/v0.2.0)

---

## session/redis/v0.2.1: Release session/redis/v0.2.1
**Published:** 2025-09-16



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/session/redis/v0.2.1)

---

## session/redis/v0.2.0: Release  session/redis/v0.2.0
**Published:** 2025-09-16



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/session/redis/v0.2.0)

---

## memory/redis/v0.2.0: Release memory/redis/v0.2.0
**Published:** 2025-09-16



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/memory/redis/v0.2.0)

---

## knowledge/vectorstore/tcvector/v0.2.0: Release knowledge/vectorstore/tcvector/v0.2.0
**Published:** 2025-09-16



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/vectorstore/tcvector/v0.2.0)

---

## knowledge/vectorstore/pgvector/v0.2.0: Release knowledge/vectorstore/pgvector/v0.2.0
**Published:** 2025-09-16



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/vectorstore/pgvector/v0.2.0)

---

## v0.1.2: v0.1.2
**Published:** 2025-09-04

## What's Changed
* trpc-agent-go: upgrade codecov version to v5 by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/230
* log: fix log.SetLevel not take effect by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/234
* agent: enhance LLMAgent configuration validation in New function by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/232
* {tool,examples}: support file tool set by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/229
* model/openai: Add OpenAI Batch API support by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/231
* examples/memory: refactor memory service for clarity by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/237
* storage: refactor storage and add tests for Redis and TcVector clients by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/235
* session: fix redis session events issues by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/238
* {memory, examples}: introduce custom instruction builder for memory services by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/241
* log: enhance error logging for tool call failures by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/242
* agent: support structured output by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/233
* examples: fix react example by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/243
* test: remove duplicated dummy tool implementations by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/250
* docs: building documentation with mkdocs by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/247
* a2aagent: use agent url as fallback url for agent card by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/251
* docs: gomod for assets and deploy pages only when docs changes by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/252
* trpc-agent-go: delete blank documents temporary by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/253
* trpc-agent-go: allows manual triggering of deployment and updating of trigger conditions by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/254
* {agent, internal}: refactor for cyclomatic complexity and replace 'interface{}' with 'any' by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/255
* {llmflow, transfer}: enhance transfer_to_agent tool compatibility by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/249
* docs: add full docs by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/257
* examples/transfer: move specialized agents to their own file by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/260
* docs: update README with new examples and usage instructions by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/259
* tool/mcp: support nested object properties in MCP schema conversion by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/262
* examples/callbacks: refactor callbacks examples and add invocation ctx usage by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/265
* examples: add retry mechanism examples and documentation for MCP tools by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/264
* trpc-agent-go: add documentation chapter in README and zh-CN README by @Flash-LHR in https://github.com/trpc-group/trpc-agent-go/pull/263
* docs: Add streaming output configuration in documentation by @1005281342 in https://github.com/trpc-group/trpc-agent-go/pull/261
* {storage, knowledge, examples}: Implement Elasticsearch vector store for knowledge by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/240
* a2a: support streaming protocol for a2a agent by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/248
* graph: properly align the user,tool,assistent messages by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/267
* {agent, runner}: wrap invocation context in runner by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/268
* docs: add Memory documentation by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/271
* session: add cleaning to the session service by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/244
* [WIP] graph: support subagent in graph agent node by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/246
* chore: bump trpc.group/trpc-go/trpc-mcp-go to v0.0.4 by @bytethm in https://github.com/trpc-group/trpc-agent-go/pull/274
* lsc: update license and gofmt files by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/273
* docs: update ecosystem path by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/275
* session: fix message truncated in session by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/276
* graph: add node responses keys by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/278
* graph: introduce new reducers to enhance graph messages processing by @WineChord in https://github.com/trpc-group/trpc-agent-go/pull/280
* Fix markdown chunking issue by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/281
* {examples, session}: fix version of go.mod by @hyprh in https://github.com/trpc-group/trpc-agent-go/pull/282
* storage/elasticsearch: reimplement vectorstore architecture by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/277
* artifact: add artifact interface, and two implement cos and inmemeory by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/272
* storage/elasticsearch: move Elasticsearch client interface into internal by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/285
* graph: enhance validation for node destinations and add related tests by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/287
* docs: add Elasticsearch vector store support and update configurations by @Rememorio in https://github.com/trpc-group/trpc-agent-go/pull/283
* Docs: update changelog for v0.1.0 by @sandyskies in https://github.com/trpc-group/trpc-agent-go/pull/284
* docs: streamline Langfuse integration instructions in observability.md by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/286
* artifact:  move storage/cos to artifact/cos by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/290
* Docs: changelog for v0.1.1 by @sandyskies in https://github.com/trpc-group/trpc-agent-go/pull/289
* artifact/cos: update NewService function to include service name para… by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/293
* Docs: update version in changelog to v0.1.2 by @liuzengh in https://github.com/trpc-group/trpc-agent-go/pull/294

## New Contributors
* @1005281342 made their first contribution in https://github.com/trpc-group/trpc-agent-go/pull/261

**Full Changelog**: https://github.com/trpc-group/trpc-agent-go/compare/v0.0.4...v0.1.2

[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/v0.1.2)

---

## storage/tcvector/v0.0.4: Release storage/tcvector/v0.0.4
**Published:** 2025-09-04



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/storage/tcvector/v0.0.4)

---

## storage/redis/v0.0.4: Release storage/redis/v0.0.4
**Published:** 2025-09-04



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/storage/redis/v0.0.4)

---

## storage/elasticsearch/v0.0.1: Release storage/elasticsearch/v0.0.1
**Published:** 2025-09-04



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/storage/elasticsearch/v0.0.1)

---

## session/redis/v0.0.5: Release session/redis/v0.0.5
**Published:** 2025-09-04



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/session/redis/v0.0.5)

---

## knowledge/vectorstore/tcvector/v0.0.4: Release knowledge/vectorstore/tcvector/v0.0.4
**Published:** 2025-09-04



[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/knowledge/vectorstore/tcvector/v0.0.4)

---

## v0.0.4: Release v0.0.4
**Published:** 2025-08-18

## [0.0.4] - 2025-08-18

### Features
- **agent**: Add A2A agent support for agent-to-agent communication. (#222)
- **agent**: Support input schema for agent configuration. (#212)
- **agent**: Implement multi-model switching functionality with dynamic model selection. (#224)
- **llmagent**: Add content prefix option for enhanced prompt customization. (#219)
- **model**: Add reasoning content to non-streaming and final response. (#226)
- **graph**: Switch to Pregel engine with rich event output for better workflow orchestration. (#220)
- **graphagent**: Support setting of initial state at each run for improved state management. (#210)
- **tool**: Enhance JSON schema support with descriptions, enum and required fields for input/output structs. (#216)

### Bug Fixes
- **session**: Fix Redis session event order issue to ensure proper event sequencing. (#223)

### Examples
- **examples**: Add comprehensive model retry example with detailed usage documentation. (#218)
- **examples**: Enhance model example with detailed README and improved output messages. (#221)
- **examples**: Provide token tracker example for monitoring token usage. (#214)
- **examples**: Demonstrate the usage of placeholders for dynamic content. (#213)
- **examples**: Enhance knowledge chat example with multiple embedder support and improved configuration. (#211)
- **examples/telemetry**: Refactor to use environment variables for LangFuse configuration. (#215)
- **examples**: Reorganize model retry example structure for better clarity. (#225)
- **examples**: Update placeholder example. (#228)

### Documentation
- **docs**: Update license files across the project. (#217)

### Dependencies
- **deps**: Bump A2A and MCP requirement versions. （#227）


[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/v0.0.4)

---

## v0.0.3: Release v0.0.3
**Published:** 2025-08-14

## [0.0.3] - 2025-08-13

### Features
- **telemetry**: Support HTTP protocol to integrate Langfuse. (#203)
- **storage**: Add extra options for Redis storage. (#202)
- **memory**: Add Redis memory service support. (#172)
- **knowledge**: Add metadata handling and consistency tests. (#201)
- **planner**: Add `actionPreamble` for ReAct prompt. (#169)
- **processor**: Add time-aware processor. (#168)
- **model**: Add support for `reasoning_content` field. (#167)
- **agent**: Support output key and output schema. (#153)
- **agent**: Export `Options` struct for easier reuse. (#163)
- **model**: Suppress events during tool-call chunks. (#165)
- **model**: Suppress empty chat chunks and add default object for completion. (#164)
- **chunking**: Ensure safe UTF-8 chunking. (#170)

### Bug Fixes
- **model**: Fix issue on internal platform. (#204)
- **mcp**: Fix default values and enum support. (#166)
- **redis**: Remove over-strict validation of Redis URL to avoid false errors. (#205)

### Chore
- **gomod**: Update go.mod in submodules. (#162)

### Examples
- **examples**: Update Cycle example. (#171)


[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/v0.0.3)

---

## v0.0.2: Release v0.0.2
**Published:** 2025-08-07

## [0.0.2] - 2025-08-07

### Features
- **tool/stream**: Add context and error for streaming tool call. (#160)

### Bug Fixes
- **model**: Fix issue of tool call on different platform. (#159)

[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/v0.0.2)

---

## v0.0.1: Release v0.0.1
**Published:** 2025-08-07



### Features

#### Core Framework
- **Agent Interface**: Core `agent.Agent` interface with support for sub-agents, tools, and execution lifecycle.
- **Runner System**: Session-based agent execution with event streaming and lifecycle management.
- **Event System**: Comprehensive event-driven architecture for tracking agent execution progress.
- **Model Integration**: Support for multiple LLM providers including OpenAI and Google GenAI.

#### Built-in Agents
- **LLMAgent**: Wrapper for chat-completion models with configurable system instructions and parameters.
- **ChainAgent**: Sequential execution of multiple sub-agents in a pipeline.
- **ParallelAgent**: Concurrent execution of sub-agents with result merging.
- **CycleAgent**: Iterative execution with termination conditions.
- **GraphAgent**: Complex workflow orchestration with conditional routing and state management.

#### Tool System
- **Tool Interface**: Unified tool specification with JSON schema validation.
- **Function Tools**: JSON-schema based function tools with automatic argument validation.
- **Streamable Tools**: Support for streaming tool responses and progressive data delivery.
- **Tool Merging**: Intelligent merging of tool results and responses.
- **Built-in Tools**: DuckDuckGo search, file operations, and document processing tools.
- **MCP Integration**: Model Context Protocol (MCP) support for dynamic tool execution.

#### Planning & Reasoning
- **Planner Interface**: Extensible planning system for agent reasoning.
- **Built-in Planner**: Simple planning with system instruction injection.
- **ReAct Planner**: Reasoning and Acting (ReAct) pattern implementation for step-by-step problem solving.

#### Memory System
- **Memory Interface**: Abstract memory service with CRUD operations.
- **In-Memory Storage**: Session-based memory with topic tagging and search capabilities.
- **Memory Tools**: Built-in tools for memory operations (add, update, delete, search, load).
- **Memory Instructions**: Automatic instruction generation for memory-enabled agents.

#### Knowledge Management
- **Knowledge Interface**: Document processing and retrieval system.
- **Vector Store Support**: Integration with vector databases for semantic search.
- **Document Processing**: Support for PDF, DOCX, and text document ingestion.
- **Chunking & Embedding**: Document chunking strategies and embedding generation.
- **Retrieval System**: RAG (Retrieval-Augmented Generation) capabilities with reranking.

#### Code Execution
- **CodeExecutor Interface**: Safe code execution in controlled environments.
- **Local Execution**: Local code execution with sandboxing.
- **Container Execution**: Docker-based code execution for isolation.

#### Session Management
- **Session Interface**: User session management with state persistence.
- **In-Memory Sessions**: Fast in-memory session storage.
- **Redis Sessions**: Distributed session storage with Redis backend.
- **State Management**: Session state tracking and persistence.

#### Telemetry & Observability
- **OpenTelemetry Integration**: Comprehensive tracing across all framework layers.
- **Metrics Collection**: Performance metrics and monitoring capabilities.
- **Event Streaming**: Real-time event streaming for debugging and monitoring.
- **Debug Server**: HTTP server for real-time agent interaction and debugging.

#### Examples & Documentation
- **Tool Usage Examples**: Complete examples demonstrating tool creation and usage.
- **Multi-Agent Examples**: Chain, parallel, and cycle agent compositions.
- **Graph Workflow Examples**: Complex workflow orchestration demonstrations.
- **Telemetry Examples**: OpenTelemetry setup and usage examples.
- **MCP Tool Examples**: Model Context Protocol integration examples.
- **Debug Web Demo**: Interactive web interface for agent testing and debugging.
- **Memory Examples**: Memory system usage and integration examples.
- **Code Execution Examples**: Safe code execution demonstrations.

#### Developer Experience
- **Comprehensive Testing**: Extensive test coverage across all packages.
- **Go Modules**: Modern Go module system with dependency management.
- **Linting & Code Quality**: golangci-lint configuration and code quality tools.
- **Documentation**: Detailed README, contributing guidelines, and code documentation.
- **Error Handling**: Structured error types and comprehensive error handling.
- **Context Support**: Full context.Context support for cancellation and timeouts.

### Technical Features
- **Streaming Support**: Both input and output streaming for real-time interactions.
- **JSON Schema Validation**: Automatic validation of tool arguments and responses.
- **Concurrent Execution**: Thread-safe agent execution with proper synchronization.
- **Resource Management**: Proper cleanup and resource management across all components.
- **Extensible Architecture**: Plugin-based architecture for easy extension and customization.
- **Cross-Platform Support**: Works on Linux, macOS, and Windows.
- **Go 1.24.1+ Support**: Modern Go features and optimizations.

### Dependencies
- **OpenAI Go SDK**: OpenAI API integration.
- **Google GenAI**: Google's Generative AI integration.
- **OpenTelemetry**: Observability and tracing.
- **Docker SDK**: Container-based code execution.
- **Redis**: Distributed session storage.
- **PDF Processing**: Document processing libraries.
- **DOCX Processing**: Microsoft Word document support.
- **Vector Store Libraries**: Vector database integrations.

---

This is the initial release of tRPC-Agent-Go, providing a comprehensive framework for building intelligent agent systems with large language models, hierarchical planning, memory management, and a rich tool ecosystem. 


[View on GitHub](https://github.com/trpc-group/trpc-agent-go/releases/tag/v0.0.1)

---

