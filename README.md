# DevOps/Agile Project Template

*[CC-NC-SA-BY 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode) By Patrick Savalle*

> ## Clone this repo and use it to setup, review or document your own project configuration 
> - [x] Review and check all the items

> Contents:
>
> - [Checklist](#checklist)
> - [Best practices](#best-practices)
> - [Fundamentals](#fundamentals)

DevOps is an [iterative and incremental](#iterations-and-increments) approach to software development with emphasis on *autonomy*, *automation*, *continuous
improvement* and *collaboration* (loose definition).

![DevOps overview](content/devops-overview.png)

There are four main processes in DevOps:

- **Continuous Integration (CI)** - Merging new code into the production code.
- **Continuous Delivery (CD)** - Putting application changes in production.
- **Continuous Feedback (CF)** - Detecting suboptimalities in processes and deliverables.
- **Continuous Operation (CO)** - Keeping the application up and running.

## Checklist

### General

- [ ] [Project plan](content/project-plan.md)

### CI

- [ ] [Planning method](content/planning-method.md) 

- [ ] [Branching strategy](content/branching-strategy.md)

- [ ] [Design guidelines](content/design-guidelines.md)

- [ ] [Coding guidelines](content/coding-guidelines.md)

- [ ] [Versioning strategy](content/versioning-strategy.md)
 
- [ ] [Developer Testing strategy](content/developer-testing-strategy.md)


### CD

- [ ] [Pipeline setup](content/pipeline-setup.md)

- [ ] [Delivery strategy](content/delivery-strategy.md)

- [ ] [Provisioning and configuration](content/provisioning-configuration.md)

- [ ] [Acceptance Testing strategy](content/acceptance-testing-strategy.md)


### CF

- [ ] [Optimization method](content/optimization-method.md)

- [ ] [Production Testing strategy](content/production-testing-strategy.md)

- [ ] [Feature request and issue tracking](content/feature-request-issue-tracking.md)


### CO

- [ ] [Ops Strategy](content/operations-setup.md)

- [ ] [Monitoring Strategy](content/monitoring-strategy.md)

- [ ] [Incident management procedure](content/incident-management-procedure.md)

- [ ] [Rollback procedure](content/rollback-strategy.md)

- [ ] [Disaster recovery procedure](content/disaster-recovery-procedure.md)

 
## Standards & Guidelines

- [ ] [API standard](content/api-standard.md)

- [ ] [Integration guidelines](content/integration-standard.md)

- [ ] [Security guidelines](content/security-guidelines.md)

## Tools

- [ ] [Tools](content/tools.md)


## Best Practices


- [ ] Never go dark, never assume, communicate with appropriate stakeholders in all phases of the project


- [ ] Enable projects to function autonomously


- [ ] Create in ever shorter increments and optimize in ever shorter iterations until everything is continuous


- [ ] Move progressively to [Kanban](content/planning-method.md#kanban) and [innersourding](https://about.gitlab.com/topics/version-control/what-is-innersource/) as functionality stabilizes


- [ ] Include end-users in the learning loop as soon as possible


- [ ] Make 50% of time allocatable to non-functionals, optimizations and DevOps infrastructure maintenance


- [ ] Open-source as much as (security-wise etc.) possible to allow scaling of collaboration


- [ ] Start with [trunk-based development](content/branching-strategy.md#trunk-based) and switch to a [GitFlow](content/branching-strategy.md) when the product reaches [MVP stage](content/project-plan.md#minimum-viable-product)


- [ ] Everything is code, all code is in Git


- [ ] Everything is automated


- [ ] Everything is peer reviewed or tested


- [ ] Explicitly define optimality 


- [ ] Continuously [remove sub-optimality](content/optimization-method.md) 


## Fundamentals

### Parts, aspects and modularity

Systems are made up of interconnected subsystems (partitions or parts), this is called **modularity**.
Parts have natural low coupling externally and high cohesion internally.
A selection of the system based on functionality present across multiple subsystems is called an aspectsystem or (aspect).

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
dependencies. Modules translate to increments in the [planning](content/planning-method.md). 

### Iterations and increments

Workflows are made up of increments that sequentially add new parts or aspects and iterations that repetitively improve
existing parts or aspects. Increments generally make systems more complete based on feed-forward (design), iterations generally make it more perfect based on
feed-back (bug reports, performance issues, enz.).

### Complexity

Complexity is roughly the result of quantity, diversity and coupling. Software complexity can be managed with:

- Divide-and-conquer
- White-box / blackbox strategy
- Encapsulation
- Patterns or symmetry
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

### Scalable collaboration

To make collaboration scalable it must be based on [stigmergic principles](https://medium.com/@patricksavalle/designing-distributed-scalable-collaboration-9c6aabd5777e). 
Both coding using Git and tasking using a Kanban board fullfills 

![DevOps scalable collaboration](content/devops-collaboration.png)
