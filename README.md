# Command

Simplify cobra testing

## Using

```go
package cmd

import (
	"github.com/iyo/command"
	"testing"
)

func TestServe(t *testing.T) {
	output, err := command.ExecuteCommand(rootCmd, "serve")
	if output != "" {
		t.Errorf("Unexpected output: %v", output)
	}
	if err != nil {
		t.Fatalf("Unexpected error: %v", err)
	}
}
```