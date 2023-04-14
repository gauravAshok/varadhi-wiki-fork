## Initial Release - MVP
RestBus message delivery with P2P and Publish/Subscribe communication pattern having at least once delivery guarantee (w/o ordered delivery). Should handle soft failures via retries and hard failures via DLT (dead letter topic) during message consumption. 

## Coming Next
### Ordered delivery 
Support ordered delivery of messages. Web interface for administrative actions.

### Improved failure handling and troubleshooting.
Provide Support for faster MTTR with selective consumption and failure troubleshooting capabilities. Improved retry mechanism/policies.

### High availability & Disaster recovery 
Enable disaster recovery support i.e.cross zonal availability of message produce and consumption flows.

### Additional feature
* Server side filtering so that applications consume only messages they are interested in, instead of all messages by default.
* Message consumption callback to message producers for P2P communication pattern.
* Message batching in produce path.
* Message batching in consumption path.

## Alternate Tech Stack implementation
To deliver required functionality Varadhi uses a set of underlying technologies e.g. messaging stack, persistence storage etc. Core functionality is provided using interfaces abstracting out specific choices, however it does provide default implementation for each of them. We envision to provide implementations of these abstractions over different tech stacks to enable Varadhi uses in different environments. Some possible alternatives are -
 * Messaging stack - Apache Pulsar (default), Apache Kafka. 

## Convenience features
Below are some of the thoughts for additional features that can be build on top of core Varadhi functionality. 

  * Alternate protocol support e.g grpc
  * Encryption at rest 
  * Data protection (masking/blocking/audit)
  * Exactly once delivery
  * Message deduplication.
  * Scheduled/delayed delivery
  * Replay of messages.
  * Schema validation
