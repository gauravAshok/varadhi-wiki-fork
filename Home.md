## Varadhi

Varadhi is a message bus implementation with a REST interface, supporting both P2P (point-to-point) and Publish-Subscribe messaging models.

The idea behind Varadhi, or RESTBus, is to take your HTTP API stack and automatically transform it into service bus-driven, queued, message-oriented endpoints. This means that the communication protocol with Varadhi will utilize HTTP 1.1/2 or even gRPC. Senders are required to include additional headers specifying the target URL and the Method to be used. Varadhi will use these headers to deliver messages to the receiver.