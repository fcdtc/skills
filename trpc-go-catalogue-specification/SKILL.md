---
name: trpc-go-catalogue-specification
description: 生成trpc-go项目代码需要遵守的规范目录规范
---

# trpc-go Catalogue Specification

## 触发条件

当用户请求以下操作时激活此技能：
- 创建新的 tRPC-Go 微服务项目
- 重构现有 tRPC-Go 项目结构
- 生成符合规范的 Go 代码文件

## 目录结构规范

```
project-root/
├── README.md                 # 必须：服务功能介绍文档
├── main.go                   # 必须：程序入口，保持简洁
├── main_test.go              # 可选：main 文件单测
├── trpc_go.yaml              # 必须：框架配置文件
├── xx_service.go             # 必须：服务入口，每个 service 一个文件
├── xx_service_test.go        # 必须：service 单测文件
├── entity/                   # 必须：共享实体结构层
│   ├── report/
│   │   └── metrics_counter.go
│   └── xxxutil/
│       └── xxx_util.go
├── logic/                    # 业务逻辑层
│   └── xxxx/                 # 按功能命名子目录
│       ├── api.go            # 对外接口定义
│       ├── api_mock.go       # mockgen 生成的桩代码
│       ├── api_impl.go       # 接口实现
│       └── api_impl_test.go  # 实现单测
└── repo/                     # 可选：外部依赖层
    ├── remotecfg/
    │   ├── api.go
    │   ├── api_mock.go
    │   ├── rainbow.go
    │   └── rainbow_test.go
    └── xxxx/
        ├── api.go
        ├── api_mock.go
        ├── mysql.go
        ├── mysql_test.go
        ├── rpc.go
        └── rpc_test.go
```

## 三层架构职责

|层级|职责|要求|
|---|---|---|
|Service|协议入口层，对外暴露RPC接口|RPC方法≤40行，尽量轻量|
|Logic|纯业务逻辑层，处理复杂业务|按功能拆分子目录，非按RPC方法|
|Repository|外部依赖层（RPC/DB/远程配置）|屏蔽实现细节，API参数用本服务结构体|
|Entity|共享实体层，贯穿所有层|定义常量、工具函数、数据结构|

## 依赖规则

**单向依赖链**：Service → Logic → Repository

- 各层通过 interface 联通，遵循依赖倒置原则
- 严禁反向依赖或跨层依赖
- Entity 层供所有层调用
- Server 之间不能相互 import

## 文件命名规范

|文件类型|命名格式|说明|
|---|---|---|
|服务入口|xx_service.go|每个service一个文件|
|服务单测|xx_service_test.go|gotests table driven格式|
|对外接口|api.go|定义interface|
|接口Mock|api_mock.go|mockgen生成|
|接口实现|api_impl.go|具体业务实现|
|实现单测|api_impl_test.go|gotests生成|
|外部依赖|mysql.go/rpc.go/rainbow.go|按依赖类型命名|

## 可测试性要求

1. **定义接口**：各层先定义 interface，不与实现绑定
2. **实现逻辑**：下层依赖声明在 impl struct 中，New 函数创建返回
3. **生成Mock**：`mockgen` 生成 gomock 桩代码
4. **生成单测**：`gotests` 生成 table driven 格式单测框架
5. **编写用例**：使用 `gomock.NewController(t)` 初始化，每个 case 添加 setup 函数


## 执行检查清单

生成或重构代码时必须确认：

- [ ] 每个 server 独立目录，高内聚低耦合
- [ ] 依赖关系单向：Service → Logic → Repository
- [ ] 各层通过 interface 联通
- [ ] 每层都有对应的 _test.go 单测文件
- [ ] mock 代码通过 mockgen 自动生成