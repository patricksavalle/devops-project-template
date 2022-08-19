# Acceptance Testing Strategy

```
Clone this repo and document your specific choice here:



```
> Content
> - [Best practices](#best-practices)
> - [Ring Deployment](#user-rings)
> - [Feature Flags](#feature-flags)
> - [Canary Deployments](#canary-deployment)
> - [Blue-Green Deployments](#blue-green-deployments)

**Acceptance testing** is used to check if a new feature can be made accessible for end-users. 
Acceptance testing can be done on a dedicated production-like environment, but also in production.
The Acceptance Testing Strategy and the [Delivery Strategy](delivery-strategy.md) are therefore closely linked.

Traditionally acceptance testing is done on a separate environment, but often a testing-in-production strategy is more effective because:
- often differences exist between the real production and the production-like environments
- testing in production can be setup to be more incremental, only testing new features when opportune
- using user rings and canary deployments to limit the blast radius of bugs
- deploying large microservices architectures to new environments often is difficult and expensive

An acceptance test is an integration test based on a use-case or scenario and run on a production(-like) environment.
Depending on the type of use-case there are different types of acceptance tests:
- Alpha Testing (done by in-house test engineers) 
- Beta Testing (done by client)
- Contract Acceptance Testing
- Regulation Acceptance Testing
- Operational Acceptance Testing
- Black Box Testing
- etc.

see: https://cache404.net/understanding-azure-devops-deployment-patterns/

## Best practices

-	Risk based testing: highest risk module get highest test coverage


- [ ] Share test results with appropriate partners

## User rings


## Feature flags


## Canary deployment


## Blue-green deployments