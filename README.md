# proto
Shared protobuf contracts for relay's gRPC services, managed with buf

## Regenerating Go code

Install the plugins at the pinned versions:

```
go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.36.12
go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.6.2
```

Then, with `$(go env GOPATH)/bin` on `PATH`:

```
buf generate
cd go && go mod tidy && go build ./...
```
