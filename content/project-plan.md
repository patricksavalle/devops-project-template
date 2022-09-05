# Project plan

```
Clone this repo and document your project plan here:



```
> Content
> - [Tips and hints](#tips-and-hints)
> - [Stakeholders](#stakeholders)
> - [Project Phases](#product-stages)
> - [Product Stages](#product-stages)
> - [Architectures](#architectures)
> - [Platform](#platform)

The project plan outlines the (intermediate) deliverables and project stages as well as the general development strategy.

## Tips and hints  

- [ ] Use [POC](#proof-of-concept)'s to test assumptions as they become visible


- [ ] Try to identify and validate the [RAT's](#rats) (riskiest assumptions) as early in the project as possible


- [ ] Use [prototypes](#prototype) to engineer requirements because not all stakeholders understand technical specifications


- [ ] Make a [functional design](#2-functional-design-and-architecture) when the requirements do not have clear, natural increments or when 'iceberg functionality' exists


- [ ] Make a [technical design](#3-technical-design) every time the required functionality or proposed solution of a new feature is new to the team


- [ ] Apply an [architecture](#architectures) before the [MVP](#minimum-viable-product) phase; the [microservices](#microservices) architecture is a good default to consider


- [ ] Release a MVP as soon as possible, to get [user feedback](optimization-method.md) and test-run your DevOps setup


- [ ] Regularly reverse engineer the implementation's [dependency graph](../README.md#modularity) and bring back to the desired state (often the functional design's [modularity](../README.md#modularity))


## Stakeholders

**Roughly: user, customer, developer, business, operation.**

Dev Includes all people involved in developing software products and services including but not exclusive to:
- Architects, business representatives, customers, product owners, project managers, quality assurance (QA), testers and analysts, suppliers …

Ops Includes all people involved in delivering and managing software products and services including but not exclusive to:
- Information security professionals, systems engineers, system administrators, IT operations engineers, release engineers, database administrators (DBAs), network engineers, support professionals, third party vendors and suppliers…

## Development Phases

All systems are built in phases. In agile projects these phases are done incrementally and only when needed.

![Development Phases](devops-development-phases.png)

### 1. Requirements engineering and RAT's

Requirements engineering is the process of defining, documenting, and maintaining requirements in the engineering design process.

Requirements describe, using human language, prototypes and sketches, the service a system must provide
concise enough to be used for system building and validation.
This stage is done in collaboration with all stake-holder.

With a strict [BDD/TDD](developer-testing-strategy.md) approach requirements are formulated as a set of tests which the implementation must satisfy. 

#### RAT's

RAT or Riskiest Assumptions Tests using POC's en prototypes are done to reduce uncertainty to an acceptable level before continuing.
The objective in this phase is to fail as cheap and soon as possible. If that fails, the project can continue.

### 2. Functional design and architecture

An important goal of functional design is to create the desired modularity of the system based on functional cohesion and coupling, and the appropriate architecture. 
It formally describes the functional structure using pseudo-coding, UML, BPML etc.
A functional design needs to be complete to be useful. This phase needs to be done by experienced architects.

#### Architecture

Architecture applies regularity to system design by mandating patterns. This creates simplicity, flexibility and maintainability. 
[Architecture](#architectures) has many aspects, such as:
- Security
- Integration
- Application
- ...

In modern application landscapes the [integration architecture](integration-standard.md) is often leading.

### 3. Technical design

Technical design translates the functional design into codeable constructions, using the appropriate technical
standards, architectures and patterns.
The design is formulated in UML.
Technical design is not meant to be complete, just complete enough to manage coding complexity.

### 4. Implementation (coding)

Coding creates an instantiable image of the software application. Code is stored in Git.

## Product Stages

### Proof-of-concept

A POC is an assumption (in)validator. Often multiple POC’s are needed. 
POC's don't need to be in the target technology or environment, they just need to be as cheap as possible.

### Prototype

A prototype is a functionality / UX demonstrator, without the full set of non-functionals and in one-off fashion.

### Minimum Viable Product

Minimum Viable Product is that version of the product that enables a full turn of the Build-Measure-Learn loop
with a minimum amount of effort and the least amount of development time.
It's also a test run for the entire DevOps setup.

### Beta release

The Beta is a production-release which can be tested in a larger, tolerant user group to iron out the last flaws.

## Architectures

See also: [Integration architectures](integration-standard.md#integration-architecture)

The architecture is a pattern that is applied to the highest levels of aggregation of the application structure.
Architectures can be recursively combined. Common architectures are: 

### Microservices

In the [micoservices architecture](https://www.oreilly.com/library/view/software-architecture-patterns/9781491971437/ch04.html) the application is divided into highly autonomous, single purpose, loosely coupled modules that have their own lifecycles and data stores.
Modules usually have REST-API's through which they interact but can also be implemented using an [event-based architecture](integration-standard.md#types-of-integration) if asynchronous communication is necessary or advantageous. 

See also: [The top 5 software architecture patterns: How to make the right choice](https://techbeacon.com/app-dev-testing/top-5-software-architecture-patterns-how-make-right-choice)

### Microkernel

The [microkernel architecture](https://www.oreilly.com/library/view/software-architecture-patterns/9781491971437/ch03.html) (sometimes referred to as the plug-in architecture pattern) is a natural pattern for implementing extensible, user configurable applications.

### Space based

The [space-based architecture](https://www.oreilly.com/library/view/software-architecture-patterns/9781491971437/ch05.html) pattern is specifically designed to address and solve scalability and concurrency issues. The space-based pattern (also sometimes referred to as the cloud architecture pattern) minimizes the factors that limit application scaling.


## Platform 

### Azure Cloud

### AWS Cloud

### Docker

### Kubernetes

