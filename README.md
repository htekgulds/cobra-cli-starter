# Cobra CLI Starter

Opinionated CLI starter for Golang using [Viper](https://github.com/spf13/viper), [Cobra](https://github.com/spf13/cobra) and [Charmbracelet Fang](https://github.com/charmbracelet/fang)

If you do not want to use `fang` just change the following lines:

```go
func Execute() {
	if err := fang.Execute(context.Background(), rootCmd); err != nil {
		os.Exit(1)
	}
}
```

to this:

```go
func Execute() {
	if err := rootCmd.Execute(); err != nil {
		os.Exit(1)
	}
}
```

## Setup

Change package name in `main.go` and `cmdName` in `cmd/root.go` to whatever you want. Then run `go mod tidy` to update `go.mod` file.

## Build

```bash
go build .
```

## Dev

```bash
go run main.go
```


