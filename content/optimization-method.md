# Optimization Method

```
Clone this repo and document your optimization method here:



```
> Content
> - [Best Practices](#best-practices)
> - [LEAN](#lean)
> - [Kaizen](#kaizen)
> - [6Sigma](#six-sigma-dmaic)

Optimization is an iterative process based on feedback or learning loops.
An optimization method determines the  *iterations* of the project. 
DevOps is compatible with many optimization methods. 
Often hybrid methods will work best, cherry-picking elements from multiple methods. 

Optimizations include:
- Refactorings to improve modularity or remove weak design
- Improving performance and resource usage
- Improving UX and functionality
- Removing slack, engineering debt or TODO's

Optimization starts with detecting sub-optimality or waste.

## Best Practices

- [ ] [Incident management](incident-management-procedure.md) is not optimization: optimizations are fed back to the planning process whereas incidents are handled immediately


- [ ] Explicitly define optimality, make deviations objective


- [ ] optimize only what can be measured (monitored)


- [ ] Continuously identify **and** backlog sub-optimality 


- [ ] Build for observability (logging, tracing, monitoring)


- [ ] Build for testing in production (fault injection, user rings)


## Optimality

To be able to optimize, optimality must be defined (quantified) and continuously measured. Use metrics for this.

[TODO] 

## LEAN

Lean software development is a translation of lean manufacturing principles and practices to the software development domain.

1. Eliminate waste
2. Building Quality In
3. Amplify Knowledge
4. Decide as late as possible
5. Deliver as fast as possible
6. Empower the team
7. Optimize the whole

Waste includes:

- Partially done work
- Extra features
- Relearning
- Task switching
- Waiting
- Handoffs
- Defects
- Management activities

Wee: https://en.wikipedia.org/wiki/Lean_software_development 

## Kaizen

Kaizen is a concept referring to business activities that continuously improve all functions and involve all employees from the CEO to the assembly line workers.

1. Good processes bring good results
2. Go see for yourself to grasp the current situation
3. Speak with data, manage by facts
4. Take action to contain and correct root causes of problems
5. Work as a team
6. Kaizen is everybody’s business
7. Make small changes over time

## Six Sigma (DMAIC)

1. Define
2. Measure
3. Analyse
4. Improve
5. Control

