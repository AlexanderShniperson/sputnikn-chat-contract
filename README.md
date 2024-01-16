# sputnikn-chat-contract
SputnikN chat network contract


Must install
go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@latest

GO-gRPC
https://github.com/grpc/grpc-go/blob/master/examples/gotutorial.md

Protobuf Golang
https://protobuf.dev/getting-started/gotutorial/

Protobuf Dart
https://protobuf.dev/getting-started/darttutorial/

protoc -I=$(pwd) --go_out=$(pwd) $(pwd)/contract.proto

protoc --go_out=./contract/v1/ --go_opt=paths=source_relative \
    --go-grpc_out=./contract/v1/ --go-grpc_opt=paths=source_relative \
    ./contract.proto


===
go get -u google.golang.org/protobuf/cmd/protoc-gen-go
go install google.golang.org/protobuf/cmd/protoc-gen-go

go get -u google.golang.org/grpc/cmd/protoc-gen-go-grpc
go install google.golang.org/grpc/cmd/protoc-gen-go-grpc

# generate the messages
 protoc --go_out="$GO_GEN_PATH" -I "$dependecies" "$proto"

# generate the services
 protoc --go-grpc_out="$GO_GEN_PATH" -I "$dependecies" "$proto"