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

### sync_docs_to_iwiki.json
```
[
  {
    "iwikiPageID": "279550562",
    "iwikiPageTitle": "tRPC-Go 框架概述",
    "gitFilePath": "docs/overview.zh_CN.md"
  },
  {
    "iwikiPageID": "118272478",
    "iwikiPageTitle": "tRPC-Go 快速上手",
 ...
```

### .resources/examples/robust/trpc-robust-dashboard.json
```
{
  "__inputs": [
    {
      "name": "DS_PROMETHEUS",
      "label": "Prometheus",
      "description": "",
      "type": "datasource",
      "pluginId": "prometheus",
      "pluginName": "Prometheus...
```

### testdata/trpc_go.yaml
```
global:  # global config.
  namespace: Development  # environment type, two types: production and development.
  env_name: test  # environment name, names of multiple environments in informal settings...
```

### testdata/trpc_go_error.yaml
```
global:                             # global config.
  namespace: Development            # environment type, two types: production and development.
  env_name: test                    # environment na...
```

### testdata/trpc_go_restful_cors.yaml
```
global:                             # global config.
  namespace: Development            # environment type, two types: production and development.
  env_name: test                    # environment na...
```

