# gogrpc
Checking out gRPC with GO

## Hello World
This example contains a simple greeting service. 

### Running Hello Greeting
1. Create gRPC Code:
```shell
  protoc --go_out=. --go_opt=paths=source_relative \
  --go-grpc_out=. --go-grpc_opt=paths=source_relative \
  internal/helloworld/hello_world.proto
```
2. Run the server
```shell
go run cmd/greeter_server/main.go
```
3. Run the client
```shell
go run cmd/greeter_client/main.go --name=Christoph
```

## Basic Tutorial RouteGuide
Creating the tutorial from [Basic Tutorial at gRPC.io](https://grpc.io/docs/languages/go/basics/) with the source code 
from [here](https://github.com/grpc/grpc-go/tree/master/examples/route_guide)
### Running RouteGuide
1. Create gRPC Code:
```shell
  protoc --go_out=. --go_opt=paths=source_relative \
  --go-grpc_out=. --go-grpc_opt=paths=source_relative \
  internal/routeguide/route_guide.proto
```
2. Run the server
```shell
go run cmd/route_guide_server/server.go
```
3. Run the client
```shell
go run cmd/route_guide_client/client.go
```