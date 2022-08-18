# Project plan

```
Clone this repo and document your specific choice here:



```
> Content
> - Best Practices
> - Project Phases
> - Product Stages
> - Architectures

The project plan outlines the project phasing, product evolution en general development strategy. 


## Best Practices 

- [ ] Validate the riskiest assumptions first with the least amount of effort 


- [ ] Create in short increments and optimize in short iterations


- [ ] Include all stakeholders in the project


- [ ] Allocate 50% of the board to non-functionals, optimizations and DevOps process maintenance


- [ ] Move progressively to Kanban and [innersourding](https://about.gitlab.com/topics/version-control/what-is-innersource/) as functionality stabilizes


- [ ] Peer review everything


- [ ] Automate as much as possible


- [ ] Optimize only what can be measured


- [ ] Include the end-users in the learning loop as soon as possible


- [ ] Prefer self-documentation and inline-documentation over external documentation


- [ ] Everything is code


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

Architecture applies regularity to system design by mandating patterns. This in turn creates flexibility and maintainabiity. 
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

### 
