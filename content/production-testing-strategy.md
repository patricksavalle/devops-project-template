# Production Testing Strategy

Production testing is black box testing on production in order to find defects and bugs before they become problems.

```
Clone this repo and document your production testing strategy here:



```
> Content
> - [Tips and hints](#tips-and-hints)
> - [Chaos engineering](#chaos-engineering)
> - [SRE](#sre)

**Production testing** is used to:
- identify defects before they become problems
- verify resilience under stress
- create temporary workarounds for defects that are not yet fixed

Production testing is **not** Testing-in-Production (TiP) which is part of the [acceptance testing](acceptance-testing-strategy.md).

Production testing is also not monitoring, it is actively provoking the production system into a response.

## Tips and hints

- [ ] Setup [monitoring](monitoring-strategy.md) first


- [ ] Have a [disaster recovery procedure](disaster-recovery-procedure.md) in place


- [ ] Have a [rollback or backup strategy](rollback-strategy.md) in place


- [ ] Beware not to expose vulnerabilities to the public


- [ ] Avoid degrading user experience


- [ ] Experiment with [chaos engineering](#chaos-engineering)


- [ ] Test experiments before running them in production

## Chaos engineering

Chaos Engineering is the discipline of experimenting on a system in order to build confidence in the system’s capability to withstand turbulent conditions in production.
- Focus on the measurable output of a system
- Vary Real-world Events
- Prioritize events either by potential impact or estimated frequency
- Run Experiments in Production
- Automate Experiments to Run Continuously
- Minimize Blast Radius

Steps:
1. Hypothesize
2. Plan
3. Execute
4. Interpret
5. Improve

See: 
- [A curated list of awesome Chaos Engineering resources](https://github.com/dastergon/awesome-chaos-engineering)
- [Principle of Chaos Engineering](https://principlesofchaos.org)
- [Continuous Chaos](https://medium.com/capital-one-tech/continuous-chaos-introducing-chaos-engineering-into-devops-practices-75757e1cca6d)

## SRE 

See: [Testing for Reliability](https://sre.google/sre-book/testing-reliability/)