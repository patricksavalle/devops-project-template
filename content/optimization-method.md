# Optimization Method

```
Clone this repo and document your specific choice here:



```
> Content
> - [Best Practices](#best-practices)
> - [Chaos engineering](#chaos-engineering)
> - [LEAN](#lean)
> - [Kaizen](#kaizen)
> - [6Sigma](#six-sigma-dmaic)


Een optimization method determines the  *iterations* of the project. DevOps is compatible with many optimization methods. Often hybrid methods will work best, cherry-picking
elements from multiple methods. Optimization is an iterative process based on feedback or learning loops.
Establish the learning loop as early in the project as practical but no later than the MVP phase.

Incident management is not optimization. Optimizations are fed back to the planning process whereas incidents are handled immediately.  

Optimizations include:
- Refactorings to improve modularity or to better match functional modularity
- Improving performance
- Reduce resource usage
- Improving UX
- Removing slack, engineering debt or TODO's
- Redesign weak functionality

## Best Practices

- [ ] Build for observability (logging, tracing, monitoring) and testing in production (fault injection, user rings)


- [ ] Explicitly define optimality, make deviations objective


- [ ] optimize only what can be measured or monitored


- [ ] continuously monitor and backlog sub-optimality 


- [ ] never sacrifice simplicity and elegance (if an optimization doesn't feel right, redesign the entire solution)

## Chaos engineering

Chaos Engineering is the discipline of experimenting on a system in order to build confidence in the system’s capability to withstand turbulent conditions in production.
- Focus on the measurable output of a system
- Vary Real-world Events
- Prioritize events either by potential impact or estimated frequency
- Run Experiments in Production
- Automate Experiments to Run Continuously
- Minimize Blast Radius

From: https://principlesofchaos.org/ 

## LEAN

Lean software development is a translation of lean manufacturing principles and practices to the software development domain.

1. Eliminate waste
2. Building Quality In
3. Amplify Knowledge
4. Decide as late as possible
5. Deliver as fast as possible
6. Empower the team
7. Optimize the whole

Waste include:

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

