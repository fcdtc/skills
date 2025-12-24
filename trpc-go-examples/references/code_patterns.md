# Code Patterns & Best Practices

## Common Patterns

### 1. Server Implementation

```go
package main

import (
    "context"
    "git.code.oa.com/trpc-go/trpc-go/trpc"
)

func main() {
    // Initialize service
    s := trpc.NewServer()

    // Register service
    // ... service registration

    // Start server
    s.Serve()
}
```

### 2. Client Implementation

```go
package main

import (
    "context"
    "git.code.oa.com/trpc-go/trpc-go/trpc"
)

func main() {
    // Create client connection
    client := trpc.NewClient()

    // Call service
    // ... service calls
}
```

## File Organization

- `proto/` - Protocol buffer definitions
- `client/` - Client implementations
- `server/` - Server implementations
- `shared/` - Shared utilities

## Key Go Patterns Observed

1. **Context-based operations**
2. **Error handling patterns**
3. **Service initialization**
4. **Resource management**
5. **Logging and monitoring**
