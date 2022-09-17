# Integration standard

Integration is the wiring between applications, the standard keeps the entire landscape uniform and robust. 

```
Clone this repo and document your integration standard here:



```
> Content:
>
> - [Guidelines](#guidelines)
> - [Basics](#basics)
> - [Integration architecture](#integration-architecture)

The integration platform is a set of tools, patterns and guidelines that *must* be used to connect applications to each other.
A modern platform typically consists of (API-) gateways, proxies, load-balancers, routers, message queues and such. 
Legacy platforms typically are build around a large central ESB (Enterprise Service Bus).

The platform has a very focused function: decoupling of communication in space (location) and in time (asynchronization).
Use it exclusively for reliable, scalable and decoupled communication.
Datalakes, databases, datawarehouses and streaming platforms are typically **not** part of the integration platform.

There are different approaches to integration. The guidelines below provide maximal (team) autonomy and agility.


## Guidelines

- [ ] Backlog exceptions to these guidelines as technical debt


- [ ] Register your application's integrations in the central registry here: ...................


- [ ] Teams are responsible for their own integrations, the platform must give DevOps teams self-service and autonomy


- [ ] Decentralize the integration platform to the application as much as possible (e.g [sidecar pattern](https://www.oreilly.com/library/view/designing-distributed-systems/9781491983638/ch02.html))


- [ ] Place integrations as high up in the OSI-stack as possible 


- [ ] Assume the platform has no way of inspecting data content


- [ ] Smart endpoints, dumb pipes! Do not use the integration platform for:
  - Business logic
  - Validation, enrichment, transformation
  - Storage, replay
  - Security
  - Hosting
  - etc.


- [ ] Use open standards
  - AMQP 1.0 for high-speed messaging, IoT, M2M, A2A, B2B (synchronous and asynchronous, unicast en multicast)
  - HTTP/1.1 and HTTP/2 for IoT, A2A, B2B, C2A (synchronous, services and resources)
  - MQTT 3.x and 5.x for IoT on lightweight and edge devices as fallback for AMQP 


- [ ] Always use fully qualified names


- [ ] Use standard and well-documented [integration patterns](https://www.enterpriseintegrationpatterns.com/)


- [ ] Your application always connects to components of the integration platform, never directly to other applications


- [ ] Build your producers/servers consumer-agnostic


- [ ] Consumers/clients - not producers - do data transformation


- [ ] Avoid using a unified intermediate format or canonical data models as these reduce agility and autonomy


- [ ] Build your application for an untrusted environment (the open internet)


- [ ] Avoid platform as product lockins as much as possible


- [ ] Integrations may not disclose implementation details


- [ ] Make communication asynchronous as much as possible (using queues and topics)


- [ ] Make shared services and resources state-less as much as possible


- [ ] Share reusable data and logic **opportunistically** (but secure) on the platform, even if there are no consumers (yet)
  - Share passive data as REST resources ([request-response pattern](#basic-integration-patterns))
  - Share business logic as XML services ([request-response pattern](#basic-integration-patterns))
  - Share streaming data / telemetry on a MQ topic ([publish-subscribe pattern](#basic-integration-patterns))

## Basics

Integration allows modules to communicate with each other. Integration tooling needs to decouple communicating modules in location and time.

### Types of integration

- Services – (SOA/XML) reusable business logic (client-server)
- Resources – (REST) universal resource manipulation (client-server)
- Messaging – Sending and receiving messages (sender-receiver, producer-consumer)

### Types of communication

- Synchronous – senders wait / block for reply
- Asynchronous – senders do not wait for reply but can be interrupted later with the reply or poll for it
- Fire-and-forget – senders do not expect replies

### Basic integration patterns

- Send-Receive - unidirectional communication from sender to receiver
- Request-Response - bi-directional communication from requester to responder (and back)
- Publish-Subscribe - unidirectional many-to-many communication from publishers to subscribers

### Types of asynchronization buffers

- Queues - message buffers that allow for asynchronous n:1 messaging
- Topics – message buffers that allow for asynchronous n:m messaging often called PubSub from Publish-Subscribe


## Integration architecture

Integration patterns are 'architectural solution templates' across or between applications, often combined with the main architecture.

- Client-server pattern
- Master-slave pattern
- Pipe-filter pattern
- Broker pattern
- Peer-to-peer pattern
- [Event-bus pattern](https://www.oreilly.com/library/view/software-architecture-patterns/9781491971437/ch02.html)

