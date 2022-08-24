# Production Testing Strategy

```
Clone this repo and document your production testing strategy here:



```
> Content
> - [Best practices](#best-practices)
> - [Chaos engineering](#chaos-engineering)
> - [SRE](#sre)

**Production testing** is used to identify potential production problems before they happen and verify resilience under stress.
Production testing is **not** Testing-in-Production (TiP) which is part of the [acceptance testing](acceptance-testing-strategy.md).

Production testing is also not monitoring, it is actively provoking the production system into a response.

See:

## Best practices

- [ ] Only test what is being monitored

- [ ] Set up for chaos engineering in selected rings (latency, error-responses, time-outs, etc.)

## Chaos engineering

Chaos Engineering is the discipline of experimenting on a system in order to build confidence in the system’s capability to withstand turbulent conditions in production.
- Focus on the measurable output of a system
- Vary Real-world Events
- Prioritize events either by potential impact or estimated frequency
- Run Experiments in Production
- Automate Experiments to Run Continuously
- Minimize Blast Radius

See: [Principle of Chaos](https://principlesofchaos.org)

## SRE 

See: [Testing for Reliability](https://sre.google/sre-book/testing-reliability/)