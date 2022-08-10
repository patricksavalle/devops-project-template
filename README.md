# DevOps Cheat Sheet

*CC-SA-BY 4.0 Patrick Savalle*

>>**Clone this repo and use it to setup and document your project.**

> Contents:
>
> - [Checklist](#checklist)
> - [Overview](#overview)
> - [Fundamentals](#fundamentals)
> - [Best Practices](#best-practices)

## Checklist

### Strategies & methods

- [ ] [Project plan](content/project-plan.md)

- [ ] [Planning method](content/planning-method.md) 

- [ ] [Optimization method](content/optimization-method.md) 

- [ ] [Delivery Strategy](content/delivery-strategy.md)

- [ ] [Test strategy](content/test-strategy.md)

- [ ][Versioning strategy](content/versioning-strategy.md)

- [ ] [GIT Branching strategy](content/branching-strategy.md)


- Ops setup
  -  [ ] Team 
  -  [ ] SRE  
 
### Standards

- [ ] Coding standard

- [ ] API standard

- [ ] Integration guidelines

### Procedures

- [ ] Incident management

- [ ] Rollback procedure

### Tools

- [ ] Code collaboration and version control (GIT)


- [ ] Agile board


- Build tool
    - [ ] Maven
    - [ ] ................


- Configuration and provisioning (GitOps)
    - [ ] Ansible
    - [ ] Puppet
    - [ ] Chef
    - [ ] Azure DevOps
    - [ ] ................


- Communication & conferencing
    - [ ] Slack
    - [ ] Matrix + Jitsi
    - [ ] Teams
    - [ ] ................


- Pipeline
    - [ ] Jenkins
    - [ ] ................


- Issue tracker
    - [x] JIRA
    - [ ] Gitlab
    - [ ] Azure DevOps
    - [ ] ................


- Unit testing framework
    - [ ] ................


- Code linter
    - [ ] ................


- Delivery Pipeline
    - [x] Jenkins
    - [ ] Azure DevOps
    - [ ] Gitlab
    - [ ] ................


- Artefact Repository
    - [ ] Gitlab
    - [ ] Azure DevOps
    - [ ] Nexus
    - [ ] ................


- Deployment & orchestration platform
    - [ ] AWS
    - [ ] Azure
    - [ ] Docker Swarm
    - [ ] Kubernetes
    - [ ] ................


- Observability stack
    - [ ] ................

## Overview

What is DevOps? (loose definition)

> DevOps is an *iterative* and *incremental* approach to software development with emphasis on *automation*, *continuous
improvement* and *collaboration*.

There are four main processes in DevOps:

- **Continuous Integration (CI)** - Integration is merging code changes into the production code.

  - Planning
  - Design and coding
  - Reviewing and merging
  - Building and unit testing


- **Continuous Delivery (CD)** - Delivery is putting application changes in production.
  - Provisioning
  - Configuration
  - Deploy
  - Integration Testing


- **Continuous Feedback (CF)** - Feedback is collecting optimisations and improvements from production.
  - Monitoring
  - Issue tracking
  - Optimization


- **Continuous Operation (CO)** - Operation is keeping the application healthy and responsive.
  - Orchestration
  - Incident management
  - Rollback

## Fundamentals

### Parts, aspects and modularity

Systems are made up of interconnected subsystems (partitions or parts), this is called modularity.
Parts have low coupling externally and high cohesion internally.
A selection of the system based on functionality present in all subsystems is called an aspectsystem or (aspect).

> Examples:
> - the rooms of a house are subsystems, the electrical wiring and the plumbing are aspectsystems
> - the pixels of a display are subsystems or parts, all red parts of the pixels together form an aspectsystem

Parts of modular systems have a natural mutual order visualized by the a directed graph.
This dependency graph visualizes how parts changes propagate and what is the most efficient
order in which to build the system. To determine this order it's layering must be determined:
1. Modules with no outgoing dependencies have layer 0
1. A module's layer number is the longest path to layer 0
1. Modules that have mutual / cyclic dependencies are on the same layer
1. The system must be build in ascending order of layers

The Modularity Principle states that programs should be built from cohesive, loosely coupled modules in order of their
dependencies.

### Iterations and increments

Workflows are made up of increments that sequentially add new parts or aspects and iterations that repetitively improve
existing parts or aspects. Increments make systems more complete based on feed-forward (design), iterations make it more perfect based on
feed-back.

### Complexity

Software complexity can be managed with:

- Divide-and-conquer
- Encapsulation
- Patterns
- Abstraction

### Functionals vs. Non-functionals

Functionals are the system properties that the end-user needs to perform the desired tasks.

Non-functionals are the properties that give a system reliability, security, scalability, robustness, maintainability
and changeability.

### Refactoring

Changing a system’s **modularity** without changing its **functionality** is called refactoring.

Reasons to refactor a system include:

- accommodate large changes in requirements
- making parts of it reusable in other systems and improving changeability
- restoring drift from ideal functional modularity caused by agile (design-less) project planning

### Encapsulation and Interfaces

To make (implementation) complexity manageable it needs to be hidden, encapsulated by an interface. Users only need to see the (
simple) interface, not the (complex) implementation.

A good interface is:

- Minimal
- Complete
- Opaque (it hides implementation details)
- Self-explanatory
- Consistent
- Documented

### Integration Basics

Integration allows modules to communicate with each other. Integration tooling needs to decouple communicating modules in location and time.

Types of integration:

- Services – (SOA) reusable business logic (client-server)
- Resources – (REST) universal resource manipulation (client-server)
- Messaging – Sending and receiving messages (sender-receiver, producer-consumer)

Types of communication:

- Synchronous – senders wait for reply
- Asynchronous – senders do not wait for reply but can be interrupted later with the reply
- Fire-and-forget – senders do not expect replies

Types of buffers:

- Queues - message buffers that allow for asynchronous n:1 messaging
- Topics – message buffers that allow for asynchronous n:m messaging often called PubSub from Publish-Subscribe

## Best Practices

### Agile Development


### Feature Design & Coding

- Use (corporate) standards
- Use well-known design patterns
- Use (automated) code linting
- Use (automated) code formatting
- Apply design-by-contract principles
- Apply const-correctness principles
- Build automated integration-tests that test for functional properties
- Build automated unit-tests only for strategic units
- Code for testability and observability

### Integration

- Use integration for reliable and decoupled communication
- Do not use integration for:
    - Transformation
    - Storage
    - Security
- The consuming (client) modules do data transformation, never the producing (server)
- Decentralize integration -> application side
- Do not rely on infrastructure, applications should be independent of platform

- Communicate eer via het platform met andere applicaties
Bouw voor een onvertrouwde omgeving (CoSI  ), de applicatie moet overal kunnen draaien
Interfaces mogen geen implementatiedetails ontsluiten
Asynchroon, niet synchroon, indien toepasselijk (IRA 4.4.3)
Maak gedeelde services en resources toestandsloos (IRA 4.4.4)
Verstuur notificaties en doe dit naar een trigger-topic op het platform (event-driven architecture)

