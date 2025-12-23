---
name: trpc-agent-go
description: Go语言编程框架，用于使用大型语言模型（llm）和工具构建Agent系统
---

# trpc-agent-go

tRPC agent for Go 

## Description

trpc-agent-go is a powerful Go framework for building intelligent agent systems using large language models (LLMs) and tools.

**Repository:** [trpc-group/trpc-agent-go](https://github.com/trpc-group/trpc-agent-go)
**Language:** Go
**Stars:** 770
**License:** Other

## When to Use This Skill

Use this skill when you need to:

### Specific Trigger Conditions:
- **Building AI agents in Go**: When you want to create intelligent autonomous agents that can reason, remember, and act
- **Multi-agent orchestration**: When you need to chain agents, run them in parallel, or create complex workflows
- **Tool integration**: When you need to integrate external APIs, databases, or custom functions with LLMs
- **Memory and state management**: When agents need to maintain context across sessions
- **RAG (Retrieval-Augmented Generation)**: When you need to build knowledge-aware agents that can search and understand documents
- **Evaluation and testing**: When you need to measure agent performance with eval sets and metrics
- **Production deployment**: When you need enterprise-grade monitoring, tracing, and reliability

### Concrete Use Cases:
- Customer support bots with context awareness
- Data analysis assistants that query databases and generate reports
- DevOps automation for deployment and monitoring
- Business process automation with human-in-the-loop
- Research and knowledge management systems
- Code generation and execution environments

## Quick Reference

### 1. Basic Agent with Calculator Tool
```go
// Create a simple agent with a calculator tool
modelInstance := openai.New("deepseek-chat")
calculatorTool := function.NewFunctionTool(
    calculator,
    function.WithName("calculator"),
    function.WithDescription("Execute addition, subtraction, multiplication, and division"),
)

agent := llmagent.New("assistant",
    llmagent.WithModel(modelInstance),
    llmagent.WithTools([]tool.Tool{calculatorTool}),
)
```

### 2. Chain Multiple Agents
```go
// Create a pipeline of agents
pipeline := chainagent.New("pipeline",
    chainagent.WithSubAgents([]agent.Agent{
        analyzer, processor, reporter,
    }))
```

### 3. Parallel Agent Execution
```go
// Run multiple agents concurrently
parallel := parallelagent.New("concurrent",
    parallelagent.WithSubAgents(tasks))
```

### 4. Memory Integration
```go
// Add persistent memory to agent
memory := memorysvc.NewInMemoryService()
agent := llmagent.New("assistant",
    llmagent.WithTools(memory.Tools()),
    llmagent.WithModel(model))

runner := runner.NewRunner("app", agent,
    runner.WithMemoryService(memory))
```

### 5. Graph-Based Workflow
```go
// Create conditional routing in graphs
sg := graph.NewStateGraph(schema)
sg.AddNode("router", func(ctx context.Context, s graph.State) (any, error) {
    return nil, nil
})
sg.AddMultiConditionalEdges(
    "router",
    func(ctx context.Context, s graph.State) ([]string, error) {
        return []string{"goA", "goB"}, nil
    },
    map[string]string{"goA": "A", "goB": "B"},
)
```

### 6. Streaming Configuration
```go
// Enable streaming output
genConfig := model.GenerationConfig{
    Stream: true,
}

agent := llmagent.New("assistant",
    llmagent.WithModel(modelInstance),
    llmagent.WithGenerationConfig(genConfig),
)
```

### 7. Agent Skills Integration
```go
// Skills are folders with SKILL.md specs
repo, _ := skill.NewFSRepository("./skills")
tools := []tool.Tool{
    skilltool.NewLoadTool(repo),
    skilltool.NewRunTool(repo, localexec.New()),
}
```

### 8. Evaluation Setup
```go
// Evaluate agent performance
evaluator, _ := evaluation.New("app", runner,
    evaluation.WithNumRuns(3))
result, _ := evaluator.Evaluate(ctx, "math-basic")
```

### 9. Telemetry Configuration
```go
// OpenTelemetry integration
runner := runner.NewRunner("app", agent,
    runner.WithTelemetry(telemetry.Config{
        TracingEnabled: true,
        MetricsEnabled: true,
    }))
```

### 10. Process Streaming Events
```go
// Handle streaming responses
for event := range events {
    if event.Object == "chat.completion.chunk" {
        fmt.Print(event.Response.Choices[0].Delta.Content)
    }
}
```

## Detailed Reference Files

### Available References:
- `references/README.md` - **Complete documentation** covering all features, architecture, and examples
- `references/CHANGELOG.md` - **Version history** and detailed changes between releases
- `references/issues.md` - **Recent GitHub issues** including both open and closed problems
- `references/releases.md` - **Release notes** with detailed changelogs for each version
- `references/file_structure.md` - **Repository structure** showing all directories and files

### Navigation Tips:
1. Start with `README.md` for understanding capabilities
2. Check `CHANGELOG.md` for recent changes and deprecations
3. Look at `issues.md` for common problems and solutions
4. Use `file_structure.md` to locate specific components

## Working with This Skill

### For Beginners:
1. **Start simple**: Begin with basic agent creation using `examples/runner`
2. **Understand the flow**: Runner → Agent → Tools → Memory
3. **Explore examples**: Check out `examples/llmagent` and `examples/multitools`
4. **Learn the basics**: Focus on tool integration before moving to complex patterns

### For Intermediate Users:
1. **Multi-agent patterns**: Explore chain, parallel, and graph agents
2. **Memory management**: Implement persistent memory with Redis
3. **Knowledge integration**: Add RAG capabilities with vector stores
4. **Evaluation**: Set up eval sets to measure agent performance

### For Advanced Users:
1. **Custom agents**: Implement your own agent interfaces
2. **Production deployment**: Configure telemetry, tracing, and monitoring
3. **A2A interoperability**: Connect with other agent systems
4. **Advanced workflows**: Build complex graph-based orchestrations

### Best Practices:
- **Start with examples**: The framework has 50+ examples covering every feature
- **Use streaming**: Enable streaming for better user experience
- **Add telemetry**: Always configure monitoring for production
- **Test thoroughly**: Use the evaluation framework to measure quality

## Key Concepts

### Core Components:
- **Runner**: Orchestrates execution with session management
- **Agent**: Processes requests using specialized components
- **Tools**: Execute specific tasks (API calls, calculations, searches)
- **Memory**: Maintains context and learns from interactions
- **Knowledge**: Provides RAG capabilities for document understanding

### Agent Types:
- **LLMAgent**: Basic chat-completion model wrapper
- **ChainAgent**: Linear pipeline of sub-agents
- **ParallelAgent**: Concurrent agent execution
- **GraphAgent**: Conditional workflows with state management
- **CycleAgent**: Iterative execution until termination

### Storage Options:
- **Session Services**: In-memory, Redis, PostgreSQL, MySQL
- **Vector Stores**: TCVector, PostgreSQL with pgvector, Milvus, Elasticsearch
- **Artifact Storage**: In-memory, S3, COS for file versioning

### Protocols:
- **AG-UI**: Agent-User Interaction protocol
- **A2A**: Agent-to-Agent interoperability
- **MCP**: Model Context Protocol for tool integration

---

Repository Info:
- **Homepage:** https://trpc-group.github.io/trpc-agent-go/
- **Topics:** a2a, agent, ai, llm, mcp
- **Open Issues:** 29
- **Last Updated:** 2025-12-22

Recent Releases:
- **v0.8.0** (2025-12-18): Enhanced graph capabilities, S3 storage, telemetry improvements
- **v0.7.0** (2025-12-04): OpenAI-compatible server, OCR support, reranker integration

---

**Generated by Skill Seeker** | GitHub Repository Scraper
