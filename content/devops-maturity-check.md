# DevOps maturity check

*[CC-NC-SA-BY 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode) By Patrick Savalle*

> ## Part of the [DevOps project template](../README.md)

> A total score of zero indicates workable, non-optimized DevOps

## Agility

- How soon can new features be planned?
  - [ ] ```-20```Next program increment (e.g. SAFe)
  - [ ] ```-0 ```Next sprint (e.g. Scrum)
  - [ ] ```+20```Instantly (e.g. Kanban)


- Are merge requests deployed instantly and automatically?
  - [ ] ```-20```No
  - [ ] ``` 0 ```Yes, to test or acceptance
  - [ ] ```+20```Yes, to production (user ring, canary deployment, feature toggle)  
  - [ ] ```+30```Yes, to production (automated acceptance tests)


- Does the application have an independent lifecycle?

  - [ ] ```-20```No
  - [ ] ```+0 ```Yes


- Can the application be deployed independently?

  - [ ] ```-20```No
  - [ ] ```+0 ```Yes


## Optimality

- Is an optimization strategy implemented?
  - [ ] ```  0```No
  - [ ] ```+20```Yes


- Is optimality explicitly defined (quantified in KPI's)?
  - [ ] ```-20```No
  - [ ] ```+0 ```Yes, basic application health
  - [ ] ```+20```Yes, full spectrum (UX, application health, DevOps performance)


- Is sub-optimality continuously identified and backlogged?
  - [ ] ```-20```No
  - [ ] ```0  ```Yes


- Is 50% of development time allocatable **by developers** to non-functionals, optimizations and DevOps infrastructure maintenance?
  - [ ] ``` 0 ```No
  - [ ] ```+10```Yes

  
## Learning

## Collaboration

- Who are reporting issues and feature requests?
  - [ ] ```-20 ```Team
  - [ ] ```-10 ```Company (inner-sourced)
  - [ ] ``` 0 ``` Internetters (crowd-sourced)


- Who are collaborating on (parts of) the code?
  - [ ] ```-10```Team
  - [ ] ``` 0 ```Company (inner-sourced)
  - [ ] ```+10```Internetters (crowd-sourced)


- Who can collaborate on (parts of) the user support platform?
  - [ ] ```-10```team-sourced
  - [ ] ``` 0 ```inner-sourced
  - [ ] ```+10```crowd-sourced


## Culture

- Purpose mastery autonomy

- Is everything open for discussion?


### Product quality

- Is end-user feedback being collected?
  - [ ] ```-30```No
  - [ ] ``` 0 ```Yes, regularly
  - [ ] ``` 10```Yes, continuously
  - [ ] ``` 20```Yes, directly (AB-testing etc.)


- Are backward compatibility and versioning of products well maintained?
  - [ ] ```-20```No
  - [ ] ``` 0 ```Not applicable
  - [ ] ``` 0 ```Yes


### Service quality

- How fast are operational disturbances noticed?
  - [ ] ```-20```Depends
  - [ ] ``` 0 ```Instantly (reactive)
  - [ ] ```+10```Instantly (predictive)


- Is application health monitored?
  - [ ] ```-20```No
  - [ ] ``` 0 ```Yes, application uptime
  - [ ] ```+10```Yes, Golden Four
  - [ ] ```+20```Yes, Predictive 


- Is the 
