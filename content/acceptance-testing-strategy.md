# Acceptance Testing Strategy

User Acceptance Testing (UAT) is used to check if a new feature can be made accessible for all end-users.

```
Clone this repo and document your acceptance testing strategy here:



```
> Content
> - [Tips and hints](#tips-and-hints)
> - [Acceptance testing](#acceptance-testing)
> - [Testing in production](#testing-in-production)


## Tips and hints

- [ ] Highest risk modules get highest test coverage (risk based testing)


- [ ] Share test results with appropriate partners


- [ ] Create representative (business value) scenario's with clear acceptance criteria


- [ ] Have your [incident reporting procedures](incident-management-procedure.md) in place before UAT-ing


- [ ] Do UAT in [production](delivery-strategy.md#no-ta) (user ring, feature flags, etc.)


- [ ] Testing-in-production requires good [monitoring](monitoring-strategy.md) and working [continuous feedback](optimization-method.md)


- [ ] Use temporary environments only when necessary (initial security tests, load test, etc.)


See: [User Acceptance Testing (UAT) – Checklist, Tips and hints, Approach, Example](http://tryqa.com/user-acceptance-testing-uat-checklist-tips-and-hints-approach-example-templates/)

## Acceptance testing 

An acceptance test is an [integration test](developer-testing-strategy.md#isolation-vs-integration-tests) based on a use-case or scenario and run on a production(-like) environment.
Depending on the type of use-case there are different types of acceptance tests:
- User Acceptance Testing
- Alpha Testing (done by in-house test engineers)
- Beta Testing (done by client)
- Contract Acceptance Testing
- Regulation Acceptance Testing
- Operational Acceptance Testing
- Black Box Testing
- etc.

see:
- [Azure DevOps deployment patterns](https://cache404.net/understanding-azure-devops-deployment-patterns/)
- [Testing in Production, the safe way](https://copyconstruct.medium.com/testing-in-production-the-safe-way-18ca102d0ef1)


## testing in production

Acceptance testing can be done on a dedicated production-like environment, but also in production.
The Acceptance Testing Strategy and the [Delivery Strategy](delivery-strategy.md) are therefore closely linked.

Traditionally acceptance testing is done on a separate environment, but often a testing-in-production strategy is more effective because:
- often differences exist between the real production and the production-like environments
- testing in production can be setup to be more incremental, only testing new features when opportune using user rings and canary deployments to limit the blast radius of bugs
- deploying large microservices architectures to new environments often is difficult and expensive


### User rings


### Feature flags


### Canary deployment


### Blue-green deployments