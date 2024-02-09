connect-go-example
==================

This is a simple example that uses [buf.build](https://buf.build) to generate a simple Go API using [connect-rpc](https://connectrpc.com/).

## Prerequisites

- [buf](https://buf.build/docs/installation)
- [protoc-gen-connect-openapi](https://github.com/sudorandom/protoc-gen-connect-openapi)

## Usage

```bash
❯ buf generate
```

View the generated code in `gen`

You can also view the openapi spec in `gen/openapi.json`

A generated version of the documentation is also hosted on [bump.sh](https://bump.sh/aranw/doc/connect-go-example)

## Testing 

```bash
❯ curl \
    --header "Content-Type: application/json" \
    --data '{"name": "Aran"}' \
    http://localhost:8080/greet.v1.GreetService/Greet
```
