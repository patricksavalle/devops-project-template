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
cherry-picking elements from different methods.




## Waterfall

Waterfall projects have the classic planning increments:

- Requirements engineering
- Functional design and architecture
- Technical and solution design
- Implementation (coding)

## Scrum

This method works with a product backlog of stories that are planned into sprints of typical 2 weeks during refinements.  
The team consists of a product-owner, a process-owner (Scrum master) and developers. Often a solution-architect is a
valuable addition.

Requirements Engineering, Functional design ans architecture are done before the actual Scrum process and results in a product backlog.
Without a functional design a much higher refactoring load can be expected as correct modularity needs to be discovered and corrected on the fly.

> General purpose method that is a good choice for:
> - Teams of up to 10-12 persons
> - Medium size, trivial / conventional applications that don't need extensive design
> - Applications that have natural increments / modularity like web applications and REST-API's

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


