# DevOps maturity check

*[CC-NC-SA-BY 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode) By Patrick Savalle*

> ## Part of the [DevOps project template](../README.md)

> A total score of zero indicates workable, non-optimized DevOps

## Agility

- How soon can new features be planned?
  - [ ] ```-20```Months / Next program increment (e.g. SAFe)
  - [ ] ```-0 ```Weeks / next sprint (e.g. Scrum)
  - [ ] ```+20```Days / next task (e.g. Kanban)


- Are merge requests deployed instantly and automatically?
  - [ ] ```-20```No
  - [ ] ``` 0 ```Yes, to test or acceptance
  - [ ] ```+20```Yes, to production (user ring, canary deployment, feature toggle)  
  - [ ] ```+30```Yes, to production (automated acceptance tests)


- Does the application have an independent lifecycle?

  - [ ] ```-20```No
  - [ ] ``` 0 ```Yes


- Can the application be deployed independently?

  - [ ] ```-20```No
  - [ ] ``` 0 ```Yes


## Optimality

- Is an optimization strategy implemented?
  - [ ] ```-20```No
  - [ ] ``` 0 ```Yes


- Is optimality explicitly defined (e.g. quantified in KPI's)?
  - [ ] ```-20```No
  - [ ] ```+0 ```Yes, basic (e.g. application health)
  - [ ] ```+20```Yes, full spectrum (UX, application health, DevOps performance)


- Is sub-optimality continuously identified and backlogged?
  - [ ] ```-20```No
  - [ ] ``` 0 ```Yes, periodic ceremonies
  - [ ] ```=20```Yes, partly automated 


- Is 50% of development time allocatable **by developers** to non-functionals, optimizations and DevOps infrastructure maintenance?
  - [ ] ``` 0 ```No
  - [ ] ```+10```Yes

  
## Learning

- Is the team pair programming?
  - [ ] ``` 0 ```No
  - [ ] ```+10```Yes


- Is code reviewed with merge requests?
  - [ ] ```-20 ```No
  - [ ] ``` 0 ```Yes


- Is the team regularly doing retrospectives?
  - [ ] ```-20```No
  - [ ] ``` 0 ```Yes




## Collaboration

- Are relevant stakeholders participating in all phases of the project?
  - [ ] ```-20 ```No
  - [ ] ``` 0  ```Yes


- Who **are** reporting issues and feature requests?
  - [ ] ```-20 ```Team
  - [ ] ```-10 ```Company (inner-sourced)
  - [ ] ``` 0 ``` Public (open-sourced)


- Who **are** collaborating on (parts of) the code?
  - [ ] ```-10```Team
  - [ ] ``` 0 ```Company(inner-sourced)
  - [ ] ```+10```Public (open-sourced)


- Who can collaborate on the user support platform?
  - [ ] ```-10```Team
  - [ ] ``` 0 ```Company (inner-sourced)
  - [ ] ```+10```Public (open-sourced)


## Culture

- Purpose mastery autonomy



- Is everything open for discussion?

- Who takes the important decisions in the team?
  - [ ] ```-10```The project owner
  - [ ] ```-10```The Scrum master
  - [ ] ``` 0 ```The team as a whole


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
