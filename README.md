# webview_go

> [!NOTE]
> This is a fork of [webview/webview_go](https://github.com/webview/webview_go)
which seems to be long discontinued even tho the repo dosent explicitly say so.
This repo is just a version bump of webkit2gtk from version 4.0 to 4.1

[![GoDoc](https://godoc.org/github.com/webview/webview_go?status.svg)](https://godoc.org/github.com/webview/webview_go)
[![Go Report Card](https://goreportcard.com/badge/github.com/webview/webview_go)](https://goreportcard.com/report/github.com/webview/webview_go)

Go language binding for the [webview library][webview].

> [!NOTE]
> Versions <= 0.1.1 are available in the [old repository][webview].

### Getting Started

See [Go package documentation][go-docs] for the Go API documentation, or simply read the source code.

Start with creating a new directory structure for your project.

```sh
mkdir my-project && cd my-project
```

Create a new Go module.

```sh
go mod init example.com/app
```

Save one of the example programs into your project directory.

```sh
curl -sSLo main.go "https://raw.githubusercontent.com/webview/webview_go/master/examples/basic/main.go"
```

Install dependencies.

```sh
go get github.com/webview/webview_go
```

Build the example. On Windows, add `-ldflags="-H windowsgui"` to the command line.

```sh
go build
```

### Notes

Calling `Eval()` or `Dispatch()` before `Run()` does not work because the webview instance has only been configured and not yet started.

[go-docs]: https://pkg.go.dev/github.com/webview/webview_go
[webview]: https://github.com/webview/webview
