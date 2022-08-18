# Integration standard

```
Clone this repo and document your specific choice here:



```
> Content:
>
> - [Guidelines](#guidelines)
> - [Basics](#basics)

The integration platform is a set of tools, patterns and guidelines that *must* be used to connect applications to each other.
A modern platform typically consists of (API-) gateways, proxies, load-balancers, routers, message queues and caches. 

The platform has a very dedicated function: decoupling of communication from location and in time (asynchronization).

## Guidelines

There are different approaches to integration. These guidelines provide maximal team autonomy and agility, matchting DevOps. 
They avoid lock-in on specific technology, at the expense of having to include some extra non-functionality in the applications.


- [ ] Backlog exceptions to these guidelines as technical debt


- [ ] Teams are responsible for their own integrations


- [ ] Register your integrations in the central registry here: ...................


- [ ] Use the integration platform for reliable, scalable and decoupled communication


- [ ] Assume the platform has no way of inspection data content
  
  Ideally all data it handles is already encrypted at the endpoints


- [ ] Do not use the integration platform for:
  - Business logic
  - Transformation
  - Storage
  - Replay
  - Security

  -> this is the responsibility of the application layer


- [ ] Use open standards
  - AMQP 1.0 for high-speed messaging, IoT, M2M, A2A, B2B (synchronous and asynchronous, unicast en multicast)
  - HTTP/1.1 and HTTP/2 for IoT, A2A, B2B, C2A (synchronous, services and resources)
  - MQTT 3.x and 5.x for IoT on lightweight and edge devices as fallback for AMQP 


- [ ] Always use fully qualified domain names


- [ ] Use standard and well-supported [integration patterns](https://www.enterpriseintegrationpatterns.com/)


- [ ] Build producers/servers consumer-agnostic


- [ ] Consumers/clients, not producers, do data transformation 


- [ ] Avoid using a unified intermediate format or canonical data model 

  -> this would be incompatible with DevOps autonomy 


- [ ] Smart endpoints, dumb pipes! Decentralize integration.


- [ ] Build your application assuming an untrusted environment (the open internet)


- [ ] Applications always connect to the integration platform never directly to other applications


- [ ] Integrations may not disclose implementation details


- [ ] Make communication asynchronous if possible


- [ ] Make shared services and resources state-less if possible


- [ ] Share reusable data and logic opportunistically (but secure) on the platform, even if there are no consumers yet
  - Share passive data as REST resources (request-response pattern)
  - Share business logic as XML services (request-response pattern)
  - Share streaming data on a MQ topic (publish-subscribe pattern)

## Basics

Integration allows modules to communicate with each other. Integration tooling needs to decouple communicating modules in location and time.

### Types of integration

- Services – (SOA) reusable business logic (client-server)
- Resources – (REST) universal resource manipulation (client-server)
- Messaging – Sending and receiving messages (sender-receiver, producer-consumer)

### Types of communication

- Synchronous – senders wait for reply
- Asynchronous – senders do not wait for reply but can be interrupted later with the reply
- Fire-and-forget – senders do not expect replies

### Basic integration patterns

- Send-Receive - unidirectional communication from sender to receiver
- Request-Response - bi-directional communication from requester to responder (and back)
- Publish-Subscribe - unidirectional many-to-many communication from publishers to subscribers

### Types of asynchronization buffers

- Queues - message buffers that allow for asynchronous n:1 messaging
- Topics – message buffers that allow for asynchronous n:m messaging often called PubSub from Publish-Subscribe
