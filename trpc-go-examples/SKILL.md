---
name: trpc-go-examples
description: tRPC-Go framework examples and tutorials - comprehensive guide for Go microservices with tRPC
---

# trpc-go-examples Skill

This skill provides comprehensive knowledge of the trpc-go-examples project, including code examples, configurations, and usage patterns for building Go microservices with the tRPC framework.

## When to Use This Skill

Use this skill when you need to:

**Development Tasks:**
- Implement tRPC-Go services (client/server architecture)
- Configure tRPC services with YAML configuration files
- Work with protocol buffers and auto-generated code
- Set up service discovery and naming services
- Implement advanced features like streaming, compression, or timeouts

**Learning & Reference:**
- Understand tRPC-Go patterns and best practices
- Reference working examples of specific features
- Learn about tRPC configuration options
- Explore microservice architecture patterns

**Troubleshooting:**
- Debug tRPC service connectivity issues
- Resolve configuration problems
- Understand error patterns in tRPC applications

**Specific Triggers:**
- User mentions "tRPC", "trpc-go", or "microservices"
- User needs examples of Go service implementation
- User asks about YAML configuration for Go services
- User needs protocol buffer integration examples

## Quick Reference

### Basic Server Implementation
```go
package main

import (
    "git.code.oa.com/trpc-go/trpc-go"
    "git.code.oa.com/trpc-go/trpc-go/admin"
)

func main() {
    s := trpc.NewServer()
    // Register service handlers
    s.Serve()
}
```
*Simple tRPC server setup with admin interface*

### Client with Attachment Support
```go
func main() {
    c := pb.NewEchoClientProxy(client.WithTarget("ip://127.0.0.1:8000"))
    a := client.NewAttachment(bytes.NewReader([]byte("client attachment")))
    rsp, err := c.UnaryEcho(trpc.BackgroundContext(), &pb.EchoRequest{},
        client.WithAttachment(a))
}
```
*Client sending attachments along with RPC messages*

### Context Cancellation Example
```go
func main() {
    ctx, cancel := context.WithTimeout(context.TODO(), time.Millisecond*2000)
    defer cancel()

    clientProxy := pb.NewGreeterClientProxy(client.WithTarget(addr))
    rsp, err := clientProxy.SayHello(ctx, req)
}
```
*Handling request timeouts and cancellation*

### HTTPS Client Configuration
```yaml
client:
  service:
    - name: trpc.app.server.stdhttps
      target: ip://127.0.0.1:9443
      protocol: http_no_protocol
      network: tcp
      timeout: 1000
      tls_cert: testdata/client.crt
      tls_key: testdata/client.key
```
*Secure HTTPS client configuration with TLS certificates*

### Custom Configuration
```yaml
custom:
  test: test
  test_obj:
    key1: value1
    key2: false
    key3: 1234
```
*Custom configuration section for application-specific settings*

### Service Configuration Template
```yaml
server:
  app: test
  server: helloworld
  service:
    - name: trpc.test.helloworld.Greeter1
      ip: 127.0.0.1
      port: 8000
      network: tcp
      protocol: trpc
```
*Standard service configuration for tRPC server setup*

### Admin Interface Setup
```go
func testCmds(w http.ResponseWriter, r *http.Request) {
    w.Write([]byte("test cmds"))
}

func init() {
    admin.HandleFunc("/testCmds", testCmds)
}
```
*Custom admin command registration for service management*

## Detailed Reference Files

### code_patterns.md
Contains common Go patterns and best practices for tRPC development:
- Server implementation patterns
- Client connection management
- Error handling strategies
- Service initialization workflows
- File organization conventions

### configuration.md
Comprehensive configuration guide with:
- YAML configuration file structures
- Service discovery setup
- Transport protocol options
- Filter configurations
- Timeout and retry settings

### features.md
Overview of available features including:
- Core features (helloworld, config, timeout)
- Advanced features (streaming, HTTP integration)
- Transport options (fasthttp, QUIC, HTTP/3)
- Testing and monitoring tools

### getting_started.md
Quick start guide with:
- Basic hello world example setup
- Feature exploration roadmap
- Project structure explanation
- Step-by-step implementation guides

## Working with This Skill

### For Beginners
1. Start with the `helloworld` example to understand basic client-server communication
2. Explore the `features/` directory for specific functionality examples
3. Refer to individual feature READMEs for detailed setup instructions
4. Use the quick reference examples above as starting templates

### For Intermediate Users
1. Study the configuration patterns in `configuration.md`
2. Explore advanced features like streaming and compression
3. Implement custom filters and middleware
4. Reference the code patterns for best practices

### For Advanced Users
1. Dive into transport protocol implementations
2. Explore service discovery mechanisms
3. Implement custom protocol handlers
4. Study performance optimization techniques

### Navigation Tips
- Use glob patterns like `features/**/main.go` to find implementation examples
- Search for specific feature names using grep patterns
- Reference the file structure overview to understand project organization
- Check individual feature directories for specialized documentation

## Key Concepts

### tRPC Framework
A high-performance RPC framework for building microservices in Go, featuring:
- Protocol buffer-based service definitions
- Multiple transport protocol support
- Built-in service discovery
- Comprehensive monitoring and tracing

### Service Architecture
Typical tRPC service organization:
- **proto/**: Protocol buffer definitions
- **client/**: Client implementations
- **server/**: Server implementations
- **shared/**: Shared utilities and common code

### Configuration Patterns
- **YAML-based**: Primary configuration format
- **Environment-specific**: Namespace-based environment configuration
- **Service discovery**: Integrated naming service support
- **Transport configuration**: Protocol and network settings

### Common Patterns
1. **Context-based operations**: Request context propagation
2. **Error handling**: Structured error responses
3. **Resource management**: Connection pooling and cleanup
4. **Logging and monitoring**: Built-in observability features

---

*Generated from comprehensive repository analysis - Use this skill for all tRPC-Go development and learning needs*