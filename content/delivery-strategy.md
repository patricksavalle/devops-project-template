# Delivery Strategy

```
Clone this repo and document your delivery strategy here:



```
> Content
> - [Best practices](#best-practices)
> - [DTAP](#dtap)
> - [Staged](#staged)
> - [No-TA](#no-ta)

The delivery strategy determines how new deployments are tested before they're put into production. 
The Delivery strategy should be aligned with application architecture and [rollback](rollback-strategy)- and [testing-strategy](acceptance-testing-strategy.md)

## Best practices

- [ ] Choose a strategy that matches your architecture and project
  - Larger microservices architectures probably work best with No-TA
  -  Simple web project can work very well with DTAP


- [ ] Use deployment rings to progressively expose new features to a wider audience


## DTAP

Classic model. Phases new releases through permanent test, acceptance and production environments (development is always the developer’s local environment)

## Staged

Creates on-demand temporary environment for different stages, production is the only permanent environment

## No-TA

Only has Development and Production environments. Uses coded and configured mechanisms (feature flags, user rings, canary deployments) that allow for testing-in-production

Large modular systems (s.a. microservices architectures) are difficult to continuously deliver using ‘classic DTAP’ and testing-strategies. 
Non-production environments are often not representative for tests either. The solution is Testing-in-Operation. Techniques includes:
- Feature flags
- Ring deployments
- Blue Green  



