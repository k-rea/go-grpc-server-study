# go-grpc-server-study

## Version
```shell
protoc --version
# libprotoc 27.0
```

## プロトコルバッファの生成
```shell
protoc --go_out=. --go-grpc_out=. proto/greeter.proto
```

## サーバーの起動
```shell
go run server/main.go
```

## クライアントを起動しての確認
```shell
go run client/main.go 名前
```

## grpcurlでの確認
```shell
brew install grpcurl
```

```shell
grpcurl -plaintext localhost:50051 list
```

```shell
grpcurl -plaintext localhost:50051 list greeter.Greeter
```
 
```shell
grpcurl -plaintext localhost:50051 greeter.Greeter.SayHello
```