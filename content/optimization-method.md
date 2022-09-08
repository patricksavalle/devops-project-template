# Optimization Method

An optimization method determines the iterations of the project.

```
Clone this repo and document your optimization method here:



```
> Content
> - [Tips and hints](#tips-and-hints)
> - [LEAN](#lsd-lean)
> - [Kaizen](#kaizen)
> - [6Sigma](#six-sigma-dmaic)

![optimisation](devops-planning-optimisation.png)

Optimization is an iterative process based on feedback or learning loops.
DevOps is compatible with many optimization methods. 
Often hybrid methods will work best, cherry-picking elements from multiple methods. 

Optimizations include:
- Refactorings to improve modularity or remove weak design
- Improving performance and resource usage
- Improving UX and functionality
- Removing slack, engineering debt or TODO's

Optimization starts with detecting sub-optimality or waste.

[Incident management](incident-management-procedure.md) is not optimization: optimizations are fed back to the planning process whereas incidents are handled immediately.

## Tips and hints

- [ ] Implement [LSD](#lsd-lean) (LEAN) as optimization method before the [MVP](project-plan.md#minimum-viable-product) is released 


- [ ] Explicitly define [optimality](#optimality), make sub-optimality measurable


- [ ] Only what is measured ([monitored](monitoring-strategy.md)), can be optimized


- [ ] Continuously identify **and** backlog sub-optimality in periodic optimization ceremonies


- [ ] Involve and facilitate all stake-holders in identifying waste (sub-optimality)


- [ ] Identify both waste / sub-optimality in the DevOps process itself and in the user's processes as facilitated by the product


- [ ] Do [production-testing](production-testing-strategy.md) (fault injection, chaos engineering)


## Optimality

To be able to optimize, optimality must be defined (quantified) and continuously measured. Use metrics for this.

[TODO] 

## LSD (LEAN)

Lean software development is a translation of lean manufacturing principles and practices to the software development domain.
Part of Lean is to continuously eliminate waste.
The original Lean (TPS) recognized 3 types of waste

- **Muda** : waste, uselessness, non-value added or idleness
- **Muri** : overburden, impossible, beyond one’s power excessiveness.
- **Mura** : unevenness, irregularity or lack of uniformity.

### Types of waste

Waste elimination is defined as the removal of anything that fails to add value to your development process and/or the final product. Here are the seven types of waste identified by LSD:

- **Defects or bugs.** Prevent bugs from being introduced in the first place.


- **Hand-offs.** Passing the work from one specialist, team, or department to another causes pauses and delays. 


- **Waiting/Delays.** When a development team member isn't able to move forward on the highest priority task.


- **Task switching.** This waste occurs when developers need to jump from one context to another. 


- **Repetitive processing of the same information, or re-learning.** This happens when a team doesn’t have an effective knowledge-sharing approach and poorly documents its decisions.


- **Extra or unnecessary features.** These are features that don’t solve a customer issue, or generally have low priority. 


- **Incomplete or partially completed work.** There are many examples of this type of waste: unfinished/partially developed but never released features; hours spent in meetings without any actionable steps defined; bugs that are defined and discussed, but never fixed; a completed design for a full-featured module that is only partially implemented.


See: [Key principles of Lean Software Development methodology](https://railsware.com/blog/lean-software-development-guide/)

## Kaizen

Kaizen is a concept referring to business activities that continuously improve all functions and involve all employees from the CEO to the assembly line workers.

1. Good processes bring good results
2. Go see for yourself to grasp the current situation
3. Speak with data, manage by facts
4. Take action to contain and correct root causes of problems
5. Work as a team
6. Kaizen is everybody’s business
7. Make small changes over time

The approach first originated in Japan in which everyone must continually evaluate his or her work at each step helping them with a chance to look back and understand where they could have done better. The Kaizen approach proves to be more collaborative giving every individual a way to become smarter employees.

## Six Sigma (DMAIC)

Six Sigma and DevOps are similar in approach as they both use metrics based feedback.

1. Define
2. Measure
3. Analyse
4. Improve
5. Control or verify

The Characteristics of Six Sigma are as follows:

- **Statistical Quality Control.** Six Sigma is derived from the Greek Letter ? which denote Standard Deviation in statistics. Standard Deviation is used for measuring the quality of output.


- **Methodical Approach.** The Six Sigma is a systematic approach of application in DMAIC and DMADV which can be used to improve the quality of production. DMAIC means for Design-Measure- Analyze-Improve-Control. While DMADV stands for Design-Measure-Analyze-Design-Verify.


- **Fact and Data-Based Approach.** The statistical and methodical method shows the scientific basis of the technique.


- **Project and Objective-Based Focus.** The Six Sigma process is implemented to focus on the requirements and conditions.


- **Customer Focus.** The customer focus is fundamental to the Six Sigma approach. The quality improvement and control standards are based on specific customer requirements.


- **Teamwork Approach to Quality Management.** The Six Sigma process requires organizations to get organized for improving quality.




