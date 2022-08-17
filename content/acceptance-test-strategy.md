# Acceptance Test Strategy

```
Clone this repo and document your specific choice here:



```
> Content
> - [Best practices](#best-practices)
> - [Ring Deployment](#user-rings)
> - [Feature Flags](#feature-flags)
> - [Canary Deployments](#canary-deployment)
> - [Blue-Green Deployments](#blue-green-deployment)

**Acceptance testing** is used to check if a new deployment can be put into production.

Acceptance testing uses the same principles as [Unit Testing](unit-test-methodology.md) but implemented in different technology and always on a production (-like) deployment.
An acceptance test is an integration test based on a use-case or scenario instead of a feature.
Depending on the type of use-case there are different types of acceptance tests:
- Alpha Testing (done by in-house test engineers) 
- Beta Testing (done by client)
- Contract Acceptance Testing
- Regulation Acceptance Testing
- Operational Acceptance Testing
- Black Box Testing
- etc.

The acceptance test strategy and the delivery strategy are closely linked.
Traditionally acceptance testing is done on a separated environment which after acceptance is then promotod to production.
For more complex microservices architectures a testing-in-production strategy is more effective.
Using user rings and canary deployments to limit the blast radius of bugs.

see: https://cache404.net/understanding-azure-devops-deployment-patterns/

## Best practices

- [ ] Test in production


-	Risk based testing: highest risk module get highest test coverage


- [ ] Use a [No-TA delivery strategy](delivery-strategy.md#no-ta)


- [ ] Use user rings to allow for acceptance testing in production while limiting impact


- [ ] Set up for chaos engineering for selected rings (latency, error-responses, time-outs, etc.)


- [ ] Share test results with appropriate partners