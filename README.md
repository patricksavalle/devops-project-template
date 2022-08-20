# DevOps Project Template

*[CC-NC-SA-BY 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode) By Patrick Savalle*

> ## Clone this repo and use it to setup and document your own project configuration 
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

- **Continuous Integration (CI)** - Merging code changes into the application code.
- **Continuous Delivery (CD)** - Putting application changes in production.
- **Continuous Feedback (CF)** - Detecting sub-optimalities in production.
- **Continuous Operation (CO)** - Keeping the application up and running.

## Checklist

### Strategies & methods

- [ ] [Project plan](content/project-plan.md)

- [ ] [Planning method](content/planning-method.md) 
  
- [ ] [Optimization method](content/optimization-method.md) 

- [ ] [Delivery strategy](content/delivery-strategy.md)

- [ ] [Developer Testing strategy](content/developer-testing-strategy.md)

- [ ] [Acceptance Testing strategy](content/acceptance-testing-strategy.md)

- [ ] [Production Testing strategy](content/production-testing-strategy.md)

- [ ] [Versioning strategy](content/versioning-strategy.md)

- [ ] [Branching strategy](content/branching-strategy.md)

- [ ] [Configuration management](content/configuration-management.md)

- [ ] [Provisioning and Deployment](content/provisioning-deployment.md)

- [ ] [Ops Strategy](content/operations-setup.md)

- [ ] [Monitoring Strategy](content/monitoring-strategy.md)

 
### Standards & Guidelines

- [ ] [Coding standard](content/coding-standard.md)

- [ ] [API standard](content/api-standard.md)

- [ ] [Integration guidelines](content/integration-standard.md)

- [ ] [Security guidelines](content/security-guidelines.md)

### Procedures and tooling

- [ ] [Incident management procedure](content/incident-management-procedure.md)

- [ ] [Rollback procedure](content/rollback-strategy.md)

- [ ] [Tools](content/tools.md)


## Best Practices

- [ ] Enable projects to function autonomously


- [ ] Add in ever shorter increments and optimize in ever shorter iterations until everything is continuous


- [ ] Include end-users in the learning loop as soon as possible


- [ ] Make 50% of time allocatable to non-functionals, optimizations and DevOps infrastructure maintenance


- [ ] Move progressively to [Kanban](content/planning-method.md#kanban) and [innersourding](https://about.gitlab.com/topics/version-control/what-is-innersource/) as functionality stabilizes


- [ ] Start with [trunk-based development](content/branching-strategy.md#trunk-based) and to switch to a [GitFlow](content/branching-strategy.md) when the product reaches [MVP stage](content/project-plan.md#minimum-viable-product)


- [ ] Everything is code


- [ ] Everything is automated


- [ ] Everything is peer reviewed or tested


- [ ] Define optimality 


- [ ] Continuously remove sub-optimality 


- [ ] Self-documenting over inline-documentation over external documentation


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

