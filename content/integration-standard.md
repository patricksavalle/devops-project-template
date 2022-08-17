# Integration standard

```
Clone this repo and document your specific choice here:



```
> Content:
>
> - [Guidelines](#guidelines)
>

The integration platform is a set of tooling that must be used to connect applications to each other.
It typically consists of gateways, load-balancers, queues, topics and caches.

A good integration platform has a very dedicated function: decoupling of communication from location and in time (asynchronization).

## Guidelines

There are different approaches to integration. These guidelines provide maximal flexibility and agility. 
It avoid lock-in on specific technology at the expense of some overhead in the applications.


- [ ] Mark exceptions to these guidelines as technical debt on your project board


- [ ] Teams are responsible for their own integrations


- [ ] Register your integrations in the central registry here: ...................


- [ ] Use the integration platform for reliable, scalable and decoupled communication


- [ ] Do not use the integration platform for:
  - Business logic
  - Transformation
  - Storage
  - Replay
  - Security


- [ ] Use open standards
  - AMQP 1.0 for high-speed messaging, IoT, M2M, A2A, B2B (synchronous and asynchronous, unicast en multicast)
  - HTTP/1.1 and HTTP/2 for IoT, A2A, B2B, C2A (synchronous, services and resources)
  - MQTT 3.x and 5.x for IoT on lightweight devices as fallback for AMQP 


- [ ] Always use fully qualified domain names


- [ ] Use standard and well-known integration patterns


- [ ] Consuming modules do their own data transformation
  - producing modules never do transformations
  - avoid using a unified intermediate format or canonical datamodel


- [ ] Decentralize integration to application side as much as possible. Smart endpoints, dumb pipes!
  - Avoid:
    - central hubs
  - Prefer:
    - application side queueing
    -  


- [ ] Applications should be independent of platform, put integration in layer 7 of the OSI-stack


- [ ] Applications always connect to the integration platform never directly to other applications


- 
  Bouw voor een onvertrouwde omgeving (CoSI  ), de applicatie moet overal kunnen draaien
  Interfaces mogen geen implementatiedetails ontsluiten
  Asynchroon, niet synchroon, indien toepasselijk (IRA 4.4.3)
  Maak gedeelde services en resources toestandsloos (IRA 4.4.4)
  Verstuur notificaties en doe dit naar een trigger-topic op het platform (event-driven architecture)

