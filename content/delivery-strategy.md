**< [devops-project-template](../README.md)**

# Delivery Strategy

The delivery strategy determines how changes of all kinds are staged into production.

```
Clone this repo and document your delivery strategy here:



```
> Content
> - [Tips and hints](#tips-and-hints)
> - [DTAP](#dtap)
> - [Staged](#staged)
> - [No-TA](#no-ta)

Continuous Delivery is the ability to get changes of all types—including new features, configuration changes, bug fixes and experiments—into production, or into the hands of users, safely and quickly in a sustainable way.

The goal is to make deployments—whether of a large-scale distributed system, a complex production environment, an embedded system, or an app—predictable, routine affairs that can be performed on demand.

See: 
- [Four Principles of Low-Risk Software Releases](https://www.informit.com/articles/article.aspx?p=1833567)
- [Implementing Continuous Delivery](https://continuousdelivery.com/implementing/)

## Tips and hints

- [ ] Align the Delivery strategy with [application architecture](project-plan.md#architectures) and [rollback](rollback-strategy)- and [testing-strategy](acceptance-testing-strategy.md)


- [ ] Progressively expose new features to a wider audience to reduce blast radius of [problems](/README.md#bugs-defects-and-problems)


- [ ] Decouple deployment from release (user rings, feature flags)


- [ ] Focus on reducing batch (new features) size


- [ ] Optimize for resilience


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
- Dark launches
- [Blue Green](https://martinfowler.com/bliki/BlueGreenDeployment.html)  






