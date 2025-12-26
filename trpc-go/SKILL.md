---
name: trpc-go
description: tRPC-Go framework examples and tutorials - comprehensive guide for Go microservices with tRPC (user)
---

# tRPC-Go Framework Examples & Tutorials

Comprehensive guide for building high-performance microservices with tRPC-Go - a pluggable, testable RPC framework for Go.

## When to Use This Skill

Use this skill when the user asks about or needs help with:

- **Building tRPC-Go services**: Creating servers, clients, or microservices
- **tRPC-Go examples**: Looking for code examples or patterns
- **Service configuration**: Configuring tRPC-Go services with YAML files
- **Protocol implementation**: Working with tRPC, HTTP, or custom protocols
- **Admin interfaces**: Adding administrative features to services
- **Attachments**: Sending large data alongside RPC messages
- **Context cancellation**: Implementing timeout and cancellation patterns
- **Client-server communication**: Setting up RPC calls between services
- **Plugin integration**: Using or creating tRPC-Go plugins
- **trpc CLI tool**: Generating code from protobuf definitions
- **AI ecosystem integration**: Working with trpc-agent-go, trpc-a2a-go, or trpc-mcp-go

### Specific Trigger Examples

- "How do I create a tRPC-Go server?"
- "Show me a tRPC client example"
- "How to configure timeout in tRPC-Go?"
- "How to send attachments with tRPC?"
- "What's the basic structure of a tRPC-Go service?"
- "How to use the trpc CLI tool?"
- "How to implement HTTP protocol in tRPC-Go?"

## Key Concepts

### Core Architecture

- **Multi-service support**: One server process can start multiple services listening on multiple addresses
- **Pluggable design**: All components are pluggable with standard interfaces
- **Mockable interfaces**: All interfaces can be mocked using gomock/mockgen
- **Protocol flexibility**: Supports any third-party protocol, with built-in support for tRPC and HTTP
- **Universal development**: Same code can switch between tRPC and HTTP protocols

### AI Ecosystem

- **trpc-agent-go**: Framework for building LLM-powered agents with reasoning, tool calling, and state management
- **trpc-a2a-go**: Agent-to-Agent service integration for tRPC-Go ecosystem
- **trpc-mcp-go**: Model Context Protocol (MCP) service integration

### Project Structure

```
feature-name/
├── README.md          # Feature documentation
├── client/
│   ├── main.go       # Client implementation
│   └── trpc_go.yaml  # Client config
├── server/
│   ├── main.go       # Server implementation
│   └── trpc_go.yaml  # Server config
└── proto/            # Protocol buffer definitions
```

## Quick Reference

### 1. Basic Server Setup

```go
package main

import (
    "fmt"
    "git.code.oa.com/trpc-go/trpc-go"
    pb "git.code.oa.com/trpc-go/trpc-go/testdata"
)

func main() {
    // Initialize server
    s := trpc.NewServer()

    // Register service
    pb.RegisterGreeterService(s.Service("trpc.examples.greeter"), &GreeterImpl{})

    // Start server
    if err := s.Serve(); err != nil {
        fmt.Println(err)
    }
}
```

### 2. Basic Client Setup

```go
package main

import (
    "context"
    "git.code.oa.com/trpc-go/trpc-go/client"
    pb "git.code.oa.com/trpc-go/trpc-go/testdata"
    "git.code.oa.com/trpc-go/trpc-go/log"
)

func main() {
    // Create client proxy
    proxy := pb.NewGreeterClientProxy(client.WithTarget("ip://127.0.0.1:8000"))

    // Make RPC call
    req := &pb.HelloRequest{Msg: "trpc-go-client"}
    rsp, err := proxy.SayHello(context.Background(), req)
    if err != nil {
        log.Errorf("SayHello err: %v", err)
        return
    }
    log.Infof("Response: %s", rsp.String())
}
```

### 3. Context with Timeout

```go
// Create context with timeout
ctx, cancel := context.WithTimeout(context.Background(), time.Millisecond*2000)
defer cancel()

// Make RPC call with timeout
rsp, err := clientProxy.SayHello(ctx, req)
if err != nil {
    log.ErrorContextf(ctx, "SayHello err: %v", err)
    return
}
```

### 4. Sending Attachments

```go
import (
    "bytes"
    "git.code.oa.com/trpc-go/trpc-go/client"
)

// Create attachment
bts := []byte("client attachment data")
attachment := client.NewAttachment(bytes.NewReader(bts))

// Send with RPC call
rsp, err := c.UnaryEcho(
    trpc.BackgroundContext(),
    &pb.EchoRequest{Message: "message"},
    client.WithAttachment(attachment),
)

// Read response attachment
data := bufPool.Get()
defer bufPool.Put(data)
_, err = attachment.Response().Read(data)
```

### 5. Admin Interface Registration

```go
import (
    "net/http"
    "git.code.oa.com/trpc-go/trpc-go/admin"
)

func init() {
    // Register custom admin handler
    admin.HandleFunc("/testCmds", func(w http.ResponseWriter, r *http.Request) {
        w.Write([]byte("test cmds response"))
    })
}
```

### 6. Basic YAML Configuration

```yaml
global:
  namespace: Development
  env_name: test
  local_ip: 0.0.0.0
  read_buffer_size: 4096
  max_frame_size: 20000000

server:
  app: test
  server: hello
  service:
    - name: trpc.test.hello.Greeter
      ip: 127.0.0.1
      port: 8000
      protocol: trpc
```

### 7. trpc CLI Tool - Installation

```bash
# Install trpc tool
go get -u trpc.tech/trpc-go/trpc-go-cmdline/v2/trpc

# Setup dependencies (protoc, protoc-gen-go, mockgen)
trpc setup

# Check version
trpc version

# Check for updates
trpc upgrade -l
```

### 8. trpc CLI Tool - Create Service

```bash
# Create a complete service project from proto file
trpc create -p hello.proto -o ./output

# Create RPC stub only
trpc create -p hello.proto -o ./output --rpconly

# Create HTTP protocol service
trpc create -p hello.proto -o ./output --protocol http

# Force overwrite existing code
trpc create -p hello.proto -o ./output -f
```

### 9. HTTP Protocol Configuration

```yaml
server:
  service:
    - name: trpc.test.http.Greeter
      protocol: http  # Use HTTP instead of tRPC protocol
      ip: 127.0.0.1
      port: 8080
```

### 10. Context Cancellation Pattern

```go
import "context"

// Create cancellable context
ctx, cancel := context.WithCancel(context.Background())

// Normal request
rsp, err := clientProxy.SayHello(ctx, req)

// Cancel the context
cancel()

// Subsequent requests will fail with context cancelled error
rsp, err = clientProxy.SayHello(ctx, req) // Will return error
```

## Reference Files

This skill includes comprehensive documentation organized into several key areas:

### code_patterns.md
- **Common implementation patterns** for servers and clients
- **File organization guidelines** (proto/, client/, server/, shared/)
- **Go patterns** used throughout tRPC-Go:
  - Context-based operations
  - Error handling patterns
  - Service initialization
  - Resource management
  - Logging and monitoring

### configuration.md
- **YAML configuration** structure and examples
- **Go modules** dependency management
- **Common configuration patterns**:
  - Service discovery setup
  - Transport configuration (HTTP, gRPC, custom)
  - Filter configuration
  - Timeout settings
- **Real configuration examples** from the codebase

### features.md
- **40+ feature examples** categorized by functionality:
  - **Core features**: helloworld, config, timeout, compression
  - **Advanced features**: stream, http, admin, robust, discovery
  - **Transport options**: fasthttp, quic, http3
  - **Testing & monitoring**: filters, rpcz, health checks
- Each feature includes README, client/server examples, and configs

### getting_started.md
- **Quick start guide** with helloworld example
- **Step-by-step instructions** for running examples
- **Project structure** explanation
- **Navigation tips** for exploring the 40+ feature examples

## Working with This Skill

### For Beginners

1. **Start with helloworld**: The simplest client-server example
2. **Understand the structure**: Every example follows the same pattern (client/, server/, proto/)
3. **Try basic features**: timeout, config, compression
4. **Read the Quick Reference**: Copy-paste examples to get started quickly

### For Intermediate Users

1. **Explore advanced features**: stream, http gateway, admin interfaces
2. **Learn configuration patterns**: Study configuration.md for best practices
3. **Use the trpc CLI tool**: Generate code from your proto definitions
4. **Implement attachments**: For sending large data efficiently
5. **Add observability**: Integrate filters, rpcz for debugging

### For Advanced Users

1. **Create custom plugins**: Use the plugin interface for third-party components
2. **Implement custom protocols**: Beyond tRPC and HTTP
3. **Build robust services**: Explore fault tolerance patterns in the robust examples
4. **Integrate AI ecosystem**: Use trpc-agent-go for LLM-powered services
5. **Contribute**: Check TAPD for planned features and contribution guidelines

### Navigation Tips

- **Examples are in features/**: 40+ examples organized by functionality
- **Each example is self-contained**: Has its own README, client, server, and config
- **Start simple, go deep**: Begin with basic examples, then explore advanced features
- **Use the trpc tool**: Generate boilerplate code to start faster
- **Check testdata/**: Contains reference configuration files

## Additional Resources

- **Framework docs**: https://iwiki.woa.com/p/89292279
- **trpc CLI tool docs**: https://git.woa.com/trpc-go/trpc-go-cmdline
- **Plugin example**: https://git.woa.com/trpc-go/trpc-selector-cl5
- **Custom protocol example**: https://git.woa.com/trpc-go/trpc-codec
- **Issue tracker**: https://mk.woa.com/coterie/420
- **TAPD requirements**: https://tapd.woa.com/trpc_go/prong/stories/stories_list

## Languages & Technologies

Go, Protocol Buffers, YAML, JSON, HTTP, gRPC, Markdown

---

*Generated from tRPC-Go repository - High-performance, pluggable RPC framework for Go microservices*
