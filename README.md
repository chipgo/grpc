# grpc
Self-research about gRPC APIs

## Tools
- [Evans](https://github.com/ktr0731/evans)  CLI virtual a gRPC Client.
- [Protocal Buffers](https://developers.google.com/protocol-buffers/docs/overview) are Google's language-neutral, platform-neutral, extensible mechanism for serializing structured data. This is used to define the:
    - Message (data, request and response)
    - Service (service name and RPC endpoints)
- [gRPC](https://www.grpc.io/docs/)

## Knowledge

4 types of API in gRPC:
1. Unary RPC
2. Server streaming RPC
3. Client streaming RPC
4. Bidirectional streaming RPC

## Q&A
PB : Protocol Buffers
- What is gRPC ?
    - where the answer??
- Why PB and why not JSON like we have in all the API is like REST API? Why PB is used to communicate?
    - The reason is because of <strong>the payload size</strong>, with PB we can make the size fewer than JSON. So we can save a lot of bandwidth.
    - We save in network bandwidth.
    - Parsing JSON is actually CPU intensive (because the format is human readable)
    - Parsing PB (binary format) is less CPU intensive because it's closer to how a machine represents data.
    - By using gRPC, the use of PB means faster and more efficient communication, friendly with mobile divices that have a slower CPU.
    - Easy to write message definition
    - The definition of the API is independent from the implementation
    - A huge amount of code can be generated, in any language, from a simple .proto file
    - The payload is binary, therefore very efficient to send/receive on a network and serialize/de-serializer on a CPU
    - PB defines rules to make an API evolve without breaking existing clients, which is helpful for micro-services

- Why gRPC can be used by any language?
    - Because the code can be generated for any language, it makes it super simple to create micro-serivces in any language that interact with each other
