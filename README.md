# DevOps Cheat Sheet

*CC-SA-BY 4.0 Patrick Savalle*

Use this to setup or optimize your Devops Project.


> Contents:
>
> - [Checklist](#checklist)
> - [Overview](#overview)
> - [Fundamentals](#fundamentals)
> - [Best Practices](#best-practices)

## Checklist

*(The checked options are optimal for larger REST-based microservices-architectures)*

### Strategies & methods

- [Planning method](content/planning-method.md) (determines the content and order of *increments* of the project)
  - [ ] ................


- [Optimization method](content/optimization-method.md) (determines the content and order of *iterations* of the project)
    - [ ] ................


- Versioning scheme
    - [ ] SimVer (```major.minor```)
    - [ ] SemVer (```major.minor.patch```)
    - [ ] CalVer (```year.release.build-status```)
    - [ ] GitTags
    - [ ] ................


- Test strategy
    - [ ] TDD (test-driven)
    - [ ] BDD (behavioral-driven)
    - [ ] Classic ATDD (acceptance test-driven)
    - [ ] ................


- GIT Branching strategy
    - [ ] Git-flow
    - [ ] Github-flow
    - [ ] GitLab-flow
    - [ ] ................


- Delivery Strategy
    - [ ] Classic DTAP (permanent environments)
    - [ ] Staged (temporary environments)
    - [ ] NoTA (testing in production)
    - [ ] ................

### Standards

- Coding standard
    - [ ] ................
  

- API standard
    - [ ] ................


- Integration standard
    - [ ] ................

### Procedures

- Incident management
    - [ ] ................


- Rollback procedure
    - [ ] ................

### Tools

- Code collaboration and version control (GIT)
    - [ ] GitLab
    - [ ] GitHub
    - [ ] BitBucket
    - [ ] Azure DevOps
    - [ ] ................


- Agile board
    - [ ] JIRA
    - [ ] Gitlab
    - [ ] Azure DevOps
    - [ ] ................


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

### Development Phases

Alle new systems are built in phases. In agile project these phases are done incrementally. Only trivial systems or experienced teams don't need a functional or technical design.

#### 1. Requirements analysis

Requirements describe, using human language, prototypes and sketches, the functionality and non-functionality of a
system concise enough to be used for system validation and acceptance testing.
This stages is done in collaboration with all stake-holder.

#### 2. Functional design

Functional design creates the desired modularity of the system based on functional dependencies and architecture. It
formally describes the behaviour of it using pseudocoding, UML, BPML etc.
A functional design needs to be complete to be useful.

#### 3. Technical design

Technical design translates the functional design into codeable constructions, using the appropriate technical
standards, architectures and patterns.
The design is formulated in UML.
Technical design is not meant to be complete, just complete enough to manage coding complexity.

#### 4. Implementation (code)

Coding creates an instantiable image of the software application.
De code defines the state space (type) of the application. The user-interactions define its actual state (instance).

### Product Stages

#### Proof-of-concept

A POC is an assumption (in)validator. Often multiple POC’s are needed.

#### Prototype

A prototype is a functionality / UX demonstrator, without the full set of non-functionals and in one-off fashion.

#### Minimum Viable Product 

Minimum Viable Product is that version of the product that enables a full turn of the Build-Measure-Learn loop 
with a minimum amount of effort and the least amount of development time. 
It's also a test run for the entire DevOps setup.

#### Beta release

The Beta is a production-release which can be tested in a larger, tolerant user group to iron out the last flaws.

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

- Validate assumptions before you start building, riskiest assumptions first
- Create in short increments and optimize in short iterations
- Optimize only what can be measured
- Collaborate using the agile board
- Communicate
- Peer review
- Automate
- Monitor

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

