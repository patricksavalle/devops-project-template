# Planning methods

```
Clone this repo and document your specific choice here:



```
> Content
> - [Waterfall](#waterfall)
> - [Scrum](#scrum)
> - [Kanban](#kanban)
> - [DSDM](#dsdm)

The planning method determines the content and order of increments. DevOps is compatible with many agile project planning (incremental) methods. Often a hybrid approach will work best,
cherry-picking elements from different methods, like ScrumBan. 

## Best Practices

- [ ] Building large or functionally complex applications without a good functional design is not a good plan 


- [ ] Scrum is a good default if the application has clear natural increments (e.g. the screens of UI's or endpoints of API's) (see [Project Plan](project-plan.md)) 


- [ ] Progressively move to Scrumban en ultimately Kanban (team-less crowdsourcing) as functionality stabilizes


- [ ] Include an architect in the team, certainly if he can also be the DevOps coach


- [ ] Experienced teams don't need a Scrum-master they are the Scrum-master


- [ ] Allocate 50% of the board to the non-functionals in the DevOps process, not for the PO to control

## Waterfall

Waterfall projects have the classic planning increments:

- Requirements engineering
- Functional design and architecture
- Technical and solution design
- Implementation (coding)
- Testing
- Maintenance

## Scrum

This method works with a product backlog of stories that are planned into sprints of typical 2 weeks during refinements.  
The team consists of a product-owner, a process-owner (Scrum master) and developers. Often a solution-architect is a
valuable addition.

Requirements Engineering, Functional design ans architecture are done before the actual Scrum process and results in a product backlog.
Without a functional design a much higher refactoring load can be expected as correct modularity needs to be discovered and corrected on the fly.

> General purpose method that is a good choice for:
> - Teams of up to 10 persons
> - Medium size, trivial / conventional applications that don't need extensive design
> - Applications that have natural increments / modularity like web applications and REST-API's
> - Scrum is not suited for maintenance-dominant projects or operations / incident-management, 
once the functionality stabilizes, Kanban is a better choice

## Kanban

This is the simplest but most scalable method. Especially suited for ad hoc, isolated tasks that need
to be crowd-sourced. Kanban has no specific roles or team composition.

> General purpose, scalable method that is a good choice for:
> - bug fixing
> - maintain and evolving existing applications
> - microtasking
> - open source collaboration of up to thousands of collaborators

## DSDM

This method is a best-effort, fixed time and price approach. It uses time-boxes based on MOSCOW prioritization of
features to be able to deliver as much functionality as possible.
Uses modeling, prototyping and workshops to define the product.

> Method that is a good choice for
>  - cost or time-limited projects with higher degree of uncertainty
>  - projects that can be developed in close collaboration with business and users

## LEAN Start-Up

This method is especially well suited for developing applications that are based on new, unproven functionality, technology and/or concepts.
Key in LEAN startup is validating the riskiest assumptions as soon and cheap as possible. Every decision is based on representative proof.

In general the development progresses from POC's to prototypes to a MVP.


