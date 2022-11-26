**< [devops-project-template](../README.md)**

# Planning method

The planning method determines the content and order of increments to be done on the project.

```
Clone this repo and document your planning method here:



```
> Content
> - [Tips and hints](#tips-and-hints)
> - [Waterfall](#waterfall)
> - [Scrum](#scrum)
> - [Kanban](#kanban)
> - [DSDM](#dsdm)

![optimisation](devops-planning-optimisation.png)
DevOps is compatible with many agile project planning (incremental) methods. Often a hybrid approach will work best,
cherry-picking elements from different methods, like ScrumBan. 

## Tips and hints

- [ ] [Plan](planning-method.md) minimal valuable increments and measure their success before progressing upon them


- [ ] Use [Kanban](#kanban) in the initial, experimental phase of the project


- [ ] [Scrum](#scrum) is a good default if:
  - the application has obvious natural increments (e.g. the screens of UI's or endpoints of API's) or a functional design is available (see [Project Plan](project-plan.md)) 
  - a product backlog of user-stories is available or an external process for requirements engineering is in place


- [ ] [DSDM](#dsdm) is a good default when requirements can / need to be engineered JIT or on-the-fly


- [ ] Progressively move to Scrumban en ultimately [Kanban](#kanban) (team-less crowdsourcing) as functionality stabilizes


- [ ] Open-source as many parts of the project as (security-wise) possible to allow for [scalable collaboration](../README.md#scalable-collaboration)


- [ ] Allocate 50% of project time to non-functionals, optimization and DevOps maintenance


- [ ] Plan minimal valuable increments (MVI) and measure their success


- [ ] Allocate dedicated periods to focus on one context only, avoid context-switching



## Waterfall

Waterfall projects have the classic planning phases:
- Requirements engineering
- Functional design and architecture
- Technical and solution design
- Implementation (coding)
- Testing
- Maintenance

The waterfall is still relevant but as a staged process in which (larger) project increments are waterfalls on their own, many in parallel.
Big advantage is that implementation can be planned using the design (the dependency graph) and will be very efficient. 
Big disadvantage is the lack of agility.

## Scrum

This method works with a product backlog of stories that are planned into sprints of typical 2 weeks during refinements.
The team consists of a product-owner, a process-owner (Scrum master) and developers. Often a solution-architect is a
valuable addition.

Requirements Engineering, Functional design ans architecture are done before or outside the actual Scrum process and result in a product backlog.
Without a functional design a much higher refactoring load can be expected as correct modularity needs to be discovered and corrected on the fly.

Typically uses [incremental implementation](project-plan.md#incremental-implementation) or [iterative architectur](project-plan.md#iterative-architecture) project flow.

See [The Scrum guide](https://scrumguides.org/index.html)

> General purpose method that is a good choice for:
> - Teams of up to 10 persons
> - Medium size, trivial / conventional applications that don't need extensive design
> - Applications that have natural increments / modularity like web applications and REST-API's
> - Scrum is not suited for maintenance-dominant projects or operations / incident-management, 
once the functionality stabilizes, Kanban is a better choice

## Kanban

This is the simplest but most scalable method. Especially suited for ad hoc, isolated tasks that need
to be open-sourced. Kanban has no specific roles or team composition.
Tasks are placed in the backlog and ordered by descending priority by the team. Collaborators clear the backlog top to bottom.

See [The Kanban guide](https://kanbanguides.org/english/)

> General purpose, scalable method that is a good choice for:
> - A-teams that can do without the limitations of Scrum
> - maintain and evolving existing applications
> - microtasking (like bug fixing)
> - open source collaboration of up to thousands of collaborators

## DSDM

This method is a best-effort, fixed time and price approach.
It uses time-boxes based on MOSCOW prioritization of features to be able to deliver as much functionality as possible.
Uses modeling, prototyping and workshops to define the product.

Typically uses [incremental requirements](project-plan.md#incremental-requirements) project flow

See: [The DSDM handbook](https://www.agilebusiness.org/page/TheDSDMAgileProjectFramework)

> Method that is a good choice for
>  - cost or time-limited projects with higher degree of uncertainty
>  - projects that can be developed in close collaboration with business and users

## LEAN startup

The Lean Startup provides a scientific approach to creating and managing startups and get a desired product to customers' hands faster. 
The Lean Startup method teaches you how to drive a startup-how to steer, when to turn, and when to persevere-and grow a business with maximum acceleration. 
It is a principled approach to new product development.

In general the development progresses from POC's to prototypes to a MVP.

See [Lean Startup Methodology](http://theleanstartup.com/principles)


