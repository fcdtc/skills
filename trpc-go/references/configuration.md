# Configuration Guide

## Configuration Files

The project uses various configuration approaches:

### YAML Configuration

Most services use `trpc_go.yaml` for configuration:

```yaml
server:  # Server settings
client:  # Client settings
# Additional service-specific settings
```

### Go Modules

Dependencies are managed through `go.mod`:

```go
module git.code.oa.com/trpc-go/trpc-go/examples

go 1.21

require (
    git.code.oa.com/trpc-go/trpc-go v0.18.5
    # ... other dependencies
)
```

## Common Configuration Patterns

Based on the analyzed configuration files:

1. **Service Discovery**: Use naming services for service registration
2. **Transport**: Choose between HTTP, gRPC, or custom transport
3. **Filters**: Apply filters for logging, metrics, etc.
4. **Timeout**: Configure appropriate timeouts for services


## Example Configuration Files

### features/https/client_with_provider.yaml
```
client:
  service:
    - name: trpc.app.server.stdhttps
      target: ip://127.0.0.1:9443
      protocol: http_no_protocol
      network: tcp
      timeout: 1000
      tls_cert: testdata/client.crt
  ...
```

### features/config/custom.yaml
```
custom :
  test : test
  test_obj :
    key1 : value1
    key2 : false
    key3 : 1234...
```

### features/cfgtag/trpc_go.yaml
```
global:                   # 全局配置
  namespace: Development  # 环境类型，分正式 Production 和非正式 Development 两种类型
  env_name: test          # 环境名称，非正式环境下多环境的名称

server:                                     # 服务端配...
```

### features/reflection/server/trpc_go.yaml
```
global:
  namespace: Development
  env_name: test

server:
  app: examples
  server: echo
  reflection_service: &reflection_service trpc.reflection.v1.ServerReflection
  service:
    - name: trpc.test...
```

### features/reflection/server-do-not-modify-config-file/trpc_go.yaml
```
global:
  namespace: Development
  env_name: test

server:
  app: examples
  server: echo
  service:
    - name: trpc.test.helloworld.GreeterXXX
      ip: 127.0.0.1
      nic: eth0
      port: 8003
  ...
```

