#### Tonic_rs

 - https://github.com/hyperium/tonic

Hello World Example
- https://github.com/hyperium/tonic/blob/master/examples/helloworld-tutorial.md

To run the example

```
docker build -t tonic_helloworld_server -f Dockerfile.helloworld_server .
docker build -t tonic_helloworld_client -f Dockerfile.helloworld_client .

docker run -d --rm --network tonic --name tonic_helloworld_server tonic_helloworld_server
docker run -d --network tonic --name tonic_helloworld_client tonic_helloworld_client
```

Response should look something like the following

```
docker logs tonic_helloworld_client   

RESPONSE=Response { metadata: MetadataMap { headers: {"content-type": "application/grpc", "date": "Thu, 19 Mar 2020 21:09:38 GMT", "grpc-status": "0"} }, message: HelloReply { message: "Hello Tonic!" } }

```
