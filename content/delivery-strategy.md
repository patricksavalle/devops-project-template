# Planning methods

```
Clone this repo and document your specific choice here:



```
> Content
> - [Best practices](#best-practices)
> - [DTAP](#dtap)
> - [Staged](#staged)
> - [No-TA](#no-ta)

Delivery strategy determines how new deployments are tested before put into production. 

In general:
- Delivery strategy should be aligned with application architecture and rollback- and testing-strategy
- DevOps combines well with microservices-architectures which are very difficult to continuously deliver with classic DTAP

## Best practices

- [ ] Choose a strategy that matches your architecture and project


- [ ] Larger microservices architectures probably work best with No-TA


- [ ] Simple web project can work very well with DTAP


## DTAP

Classic model. Phases new releases through permanent test, acceptance and production environments (development is always the developer’s local environment)

## Staged

Creates on-demand temporary environment for different stages, production is the only permanent environment

## No-TA

Only has Development and Production environments. Uses coded and configured mechanisms (feature flags, user rings, canary deployments) that allow for testing-in-production


