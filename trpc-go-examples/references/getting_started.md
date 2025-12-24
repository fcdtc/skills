# Getting Started with tRPC-Go Examples

## Quick Start

### 1. Basic Hello World

The `helloworld` directory contains the simplest example:

```bash
# Start server
cd helloworld
go run server/main.go

# In another terminal, start client
go run client/main.go
```

### 2. Explore Features

The `features/` directory contains 40+ examples demonstrating specific capabilities:

- `admin/` - Administrative features
- `compression/` - Compression
- `http/` - HTTP integration
- `stream/` - Streaming
- `timeout/` - Timeout handling

## Project Structure

Each feature follows this pattern:
```
feature-name/
├── README.md          # Feature documentation
├── client/
│   ├── main.go       # Client implementation
│   └── trpc_go.yaml  # Client config
├── server/
│   ├── main.go       # Server implementation
│   └── trpc_go.yaml  # Server config
└── shared/           # Optional shared code
