## tRPC-Go Hello World

**The demo was forked from [trpc examples](https://github.com/trpc-group/trpc-go/tree/main/examples/helloworld) which is used to test [go auto instr](https://github.com/alibaba/opentelemetry-go-auto-instrumentation)**

This is a very simple example to run Hello World in tRPC-Go.

Run hello world server:
```bash
$ cd helloworld/server && go run main.go
```

Start a new terminal to run hello world client:
```bash
$ cd helloworld/client && go run main.go
```
You will see `Hello world!` displayed as a log.

Congratulations! You’ve just run a client-server application with tRPC-Go.

Check [docs](https://trpc.group/docs/languages/go/) to get deeper into tRPC-Go.


## Auto instrumetation

**This is just my own method of intrumentation, and there may be errors.**

**I only tested the trpc client instrumentation.**

**You should start the server first with `cd helloworld/server && go run main.go`**

```
./otel set -debug
./otel go build -o client helloworld/client/main.go
```