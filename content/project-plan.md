# Project plan

```
Clone this repo and document your specific choice here:



```
> Content
> - [Best Practices](#best-practices)
> - [Stakeholders](#stakeholders)
> - [Project Phases](#product-stages)
> - [Product Stages](#product-stages)
> - [Architecture](#architecture)
> - [Platform](#platform)

The project plan outlines:
- project phases
- product stages
- architecture 
- platform
- general approach

## Best Practices 

- [ ] Never go dark, never assume, include appropriate stakeholders in all phases of the project 


- [ ] Make communication and collaboration available to all stakeholders


- [ ] Use [POC](#proof-of-concept)'s to test the riskiest assumptions ([RAT](#rats)) first with the least amount of effort possible


- [ ] Use [prototypes](#prototype) to engineer requirements as not all stakeholders understand technical specifications


- [ ] Make a functional design when the requirements do not have clear, natural increments or when 'iceberg functionality' exists


- [ ] Make a technical design when the functionality is new to the team


- [ ] Release a MVP as soon as possible, to validate functionality and test-run your DevOps setup


- [ ] Regularly reverse engineer the physical dependency graph and bring back to the desired state (often the functional design)


## Stakeholders

Dev Includes all people involved in developing software products and services including but not exclusive to:
- Architects, business representatives, customers, product owners, project managers, quality assurance (QA), testers and analysts, suppliers …

Ops Includes all people involved in delivering and managing software products and services including but not exclusive to:
- Information security professionals, systems engineers, system administrators, IT operations engineers, release engineers, database administrators (DBAs), network engineers, support professionals, third party vendors and suppliers…

## Development Phases

Alle new systems are built in phases. In agile project these phases are done incrementally. Only trivial systems or experienced teams don't need a functional or technical design.

### 1. Requirements engineering and RAT's

Requirements engineering is the process of defining, documenting, and maintaining requirements in the engineering design process.

Requirements describe, using human language, prototypes and sketches, the service a system must provide
concise enough to be used for system building and validation.
This stage is done in collaboration with all stake-holder.

#### RAT's

RAT or Riskiest Assumptions Tests using POC's en prototypes are done to reduce uncertainty to an acceptable level.
The objective in this phase is to fail as cheap and soon as possible. If that fails, the project can continue.

### 2. Functional design and architecture

Functional design creates the desired modularity of the system based on functional dependencies and architecture. 
It formally describes the functional structure using pseudocoding, UML, BPML etc.
A functional design needs to be complete to be useful. This phase needs to be done by experienced architects.

#### Architecture

Architecture applies regularity to system design by mandating patterns. This creates flexibility and maintainability. 
Architecture has many aspects, such as:
- Security
- Integration
- Application

In modern application landscapes the [integration architecture](integration-standard.md) is often leading.

### 3. Technical design

Technical design translates the functional design into codeable constructions, using the appropriate technical
standards, architectures and patterns.
The design is formulated in UML.
Technical design is not meant to be complete, just complete enough to manage coding complexity.

### 4. Implementation (coding)

Coding creates an instantiable image of the software application.
De code defines the state space (type) of the application. 
User-interactions define its actual state (instance).

## Product Stages

### Proof-of-concept

A POC is an assumption (in)validator. Often multiple POC’s are needed.

### Prototype

A prototype is a functionality / UX demonstrator, without the full set of non-functionals and in one-off fashion.

### Minimum Viable Product

Minimum Viable Product is that version of the product that enables a full turn of the Build-Measure-Learn loop
with a minimum amount of effort and the least amount of development time.
It's also a test run for the entire DevOps setup.

### Beta release

The Beta is a production-release which can be tested in a larger, tolerant user group to iron out the last flaws.

## Architectures

Architecture is a pattern that is usually applied to the highest levels of aggregation in the enterprise landscape.
Architectures can be recursively combined. 

### Microservices


See: https://www.oreilly.com/library/view/software-architecture-patterns/9781491971437/ch04.html

### Layered

See: https://www.oreilly.com/library/view/software-architecture-patterns/9781491971437/ch01.html 

### Event driven

See: https://www.oreilly.com/library/view/software-architecture-patterns/9781491971437/ch02.html


### Microkernel


See: https://www.oreilly.com/library/view/software-architecture-patterns/9781491971437/ch03.html

### Space based


See: https://www.oreilly.com/library/view/software-architecture-patterns/9781491971437/ch05.html 


## Platform 

### Azure Cloud

### AWS Cloud

### Docker

### Kubernetes

