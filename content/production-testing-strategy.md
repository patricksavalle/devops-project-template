# Production Testing Strategy

```
Clone this repo and document your production testing strategy here:



```
> Content
> - [Best practices](#best-practices)
> - [Chaos engineering](#chaos-engineering)
> - [SRE](#sre)

**Production testing** is used to identify potential production problems before they happen and verify resilience under stress.


## Best practices

- [ ] Set up for chaos engineering for selected rings (latency, error-responses, time-outs, etc.)

## Chaos engineering

Chaos Engineering is the discipline of experimenting on a system in order to build confidence in the system’s capability to withstand turbulent conditions in production.
- Focus on the measurable output of a system
- Vary Real-world Events
- Prioritize events either by potential impact or estimated frequency
- Run Experiments in Production
- Automate Experiments to Run Continuously
- Minimize Blast Radius

From: https://principlesofchaos.org/

## SRE 