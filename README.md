# DevOps Cheat Sheet

*CC-SA-BY 4.0 Patrick Savalle*

Use this to setup or optimize your Devops Project.


> Contents:
>
> - [Overview](#overview)
> - [Checklist](#checklist)
> - [Fundamentals](#fundamentals)
> - [Best Practices](#best-practices)

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

## Checklist

*(The checked options are optimal for larger REST-based microservices-architectures)*

### Strategies & methods

- Planning method (determines the content and order of *increments* of the project)
    - [ ] Design Driven
    - [ ] Scrum
    - [ ] Kanban
    - [ ] DSDM
    - [ ] XP
    - [ ] ................


- Optimization method (determines the content and order of *iterations* of the project)
    - [ ] LEAN
    - [ ] Kaizen
    - [ ] 6SIGMA
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

## Fundamentals

### Parts, aspects and modularity

Systems are made up of interconnected subsystems (partitions or parts), this is called modularity.
Parts have low coupling externally and high cohesion internally.
A selection of the system based on functionality present in all subsystems is called an aspectsystem or (aspect).

> Examples:
> - the rooms of a house are subsystems, the electrical wiring and the plumbing are aspectsystems
> - the pixels of a display are subsystems or parts, all red parts of the pixels together form an aspectsystem

### Iterations and increments

Workflows are made up of increments that sequentially add new parts or aspects and iterations that repetitively improve
existing parts or aspects.
Increments make systems more complete based on feed-forward (design), iterations make it more perfect based on
feed-back.

### Modularity and Natural Order

Parts of modular systems have a natural mutual order visualized by the a directed graph.
This dependency graph visualizes how parts depend on other parts, how changes propagate and what is the most efficient
order in which to build the system.

The Modularity Principle states that programs should be built from cohesive, loosely coupled modules in order of their
dependencies.

> To determine natural order
> 1. Modules with no dependencies have order 0
> 1. ther parts have the number of dependencies in the longest path o the furthest order 0 module as their order
> 1. Modules that have mutual cyclic dependencies are one single module

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

Changing a system’s modularity without changing its functionality is called refactoring.

> Reasons to refactor a system include:
> - accomodate large changes in requirements
> - making parts of it reusable in other systems and improving changeability
> - restoring drift from ideal functional modularity caused by agile (design-less) project planning

### Encapsulation and Interfaces

To hide (implementation) complexity it needs to be hidden, encapsulated by an interface. Users only need to see the (
simple) interface, not the (complex) implementation.

A good interface is:

- Minimal
- Complete
- Opaque (it hides implementation details)
- Self-explanatory
- Consistent
- Documented

### Development Phases

#### 1. Requirements analysis

Requirements describe, using human language, prototypes and sketches, the functionality and non-functionality of a
system concise enough to be used for system validation.
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

A MVP is a production-grade first version of a product, good enough to start including end-users in your DevOps
process.

### Integration Technology Basics

Integration allows modules to interact with each other. It defines the connections between modules. Integration
tooling needs to decouple communicating modules in location and time.

Types of integration:

- Services – (SOA) reusable business logic (client-server)
- Resources – (REST) universal resource manipulation (client-server)
- Messaging – Sending and receiving messages (sender-receiver, producer-consumer)

Types of communication

- Synchronous – senders wait for reply
- Asynchronous – senders do not wait for reply but can be interrupted later with the reply
- Fire-and-forget – senders do not expect replies

Types of buffers

- Queues - message buffers that allow for asynchronous n:1 messaging
- Topics – message buffers that allow for asynchronous n:m messaging

### Planning Methods

DevOps is compatible with many agile project planning (incremental) methods. Often hybrid methods will work best,
cherry-picking elements from multiple methods.

#### Scrum

This method works with a backlog of stories that are planned into sprints of typical 2 weeks during refinements.  
The team consists of a product-owner, a process-owner (Scrum master) and developers. Often a solution-architect is a
valuable addition.

#### Kanban

This is the simplest and most scalable method. Especially suited for ad hoc, isolated tasks like bug fixing that need
to be crowd-sourced.
Kanban has no specific roles or team composition.

#### XP

This method places emphasis on small and regular release with the expectation of change and refactoring.
Build the simplest thing that could possibly work.
Peer programming, collective code ownership, unit testing.

#### DSDM

This method is a best-effort, fixed time and price approach. It uses time-boxes based on MOSCOW prioritization of
features to be able to deliver as much functionality as possible.
Uses modeling, prototyping and workshops to define the product.

### Optimization Methods

DevOps is compatible with many optimization (iterative) methods. Often hybrid methods will work best, cherry-picking
elements from multiple methods.

#### LEAN

1. Eliminate waste
2. Building Quality In
3. Amplify Knowledge
4. Decide as late as possible
5. Deliver as fast as possible
6. Empower the team
7. Optimize the whole

#### Kaizen

1. Good processes bring good results
2. Go see for yourself to grasp the current situation
3. Speak with data, manage by facts
4. Take action to contain and correct root causes of problems
5. Work as a team
6. Kaizen is everybody’s business
7. Make small changes over time

#### Six Sigma

1. Define
2. Measure
3. Analyse
4. Improve
5. Control

## Best Practices

### Feature Design & Coding

- Use the corporate standards
- Use industry standard design patterns and solutions
- Use a branching strategy
- Use (automated) code linting
- Use (automated) code formatting
- Use Design-By-Contract
- Apply const-correctness principles
- Build automated integration-tests that test for functional properties
- Build automated unit-tests only for strategic units
- Code for testability and observability

### Optimization

- Premature optimization is the root of all evil
- Optimize only things that can be tested and measured

### Integration

- Use integration for reliable and decoupled communication
- Do not use integration for:
    - Transformation
    - Storage
    - Security
- The consuming (client) modules do data transformation, never the producing (server)
- Decentralize integration -> application side
- Do not rely on infrastructure, applications should be independent of platform
