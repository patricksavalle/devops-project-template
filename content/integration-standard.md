# Integration standard

```
Clone this repo and document your specific choice here:



```
> Content:
>
> - [Guidelines](#guidelines)
>

The integration platform is a set of tooling that must be used to connect applications to each other.
It typically consists of gateways, load-balancers, routers, queues, topics and caches.

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


- [ ] Use standard and well-supported [integration patterns](https://www.enterpriseintegrationpatterns.com/)


- [ ] Consumers, never producers, do data transformation (as a producer may never do assumptions on consumers' needs)


- { ] Avoid using a unified intermediate format or canonical data model (as this is incompatible with the autonomy in the DevOps model) 


- [ ] Decentralize integration to application side as much as possible. Smart endpoints, dumb pipes!


- [ ] Build for an untrusted environment 


- [ ] Applications always connect to the integration platform never directly to other applications


- [ ] Integrations may not disclose implementation details


- [ ] Asynchronous, not synchronous when possible


- [ ] Make shared services and resources state-less when possible


- [ ] Share reusable data, resources and services opportunistically (but secure) on the platform
