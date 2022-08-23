# Developer Testing Strategy

```
Clone this repo and document your developer testing strategy here:



```
> Content
> - [Best practices](#best-practices)
> - [Isolation vs integration tests](#isolation-vs-integration-tests)
> - [Mocking](#mocking)
> - [Test driven development](#tdd-test-driven)
> - [Behavioral driven development](#bdd-behavioral-driven)

The trick of testing in general is to fail as fast as possible when bugs still have minimal impact.

Developer testing is used to check if the application code is ready to be deployed. 
As opposed to [acceptance testing](acceptance-testing-strategy.md) that used after it is deployed to check if a new deployment can be put into production.

## Best Practices

- [ ] Use Design-by-Contract to complement testing


- [ ] Write high level tests for the new feature as a whole **before** implementing the feature's functionality


- [ ] Write lower level tests for the feature's parts **after** the implementation passes the high-level tests and it's design is satisfactory. 
   - this prevent continuously having to refactor the tests while implementation's design still changes
   - these test now serve to prevent and help locate regression during refactors
   - write these test based on requirements, not based on knowledge of the implementation


- [ ] Use a framework to mock integrations, turning integration test into isolation tests (unit tests)


- [ ] Always only test interfaces so you can optimize implementation without breaking tests


- [ ] Automate as many tests as you can


- [ ] Remove tests that are not 100% reliable or representative


- [ ] Avoid tests that are so complex they need their own tests


See: https://techbeacon.com/app-dev-testing/6-best-practices-integration-testing-continuous-integration 

## Isolation vs integration tests

*Note I use a different but more intuitive definition compared to conventional wisdom*

Isolation tests test modules in isolation using mocks that represent their integrations.
Integrations tests test modules with their integrations.
Integration tests become unit tests when integrations are mocked.
**The difference is isolation**.

> **Isolation test** replaces **Unit test**. 

Traditionally isolation testing is called unit testing. But practically unit tests exist on different levels of aggregation, following application architecture.
A method or function can be a unit, a class an even entire microservice's can be units too.

Developer tests are run manually during development and automated during continuous integration and delivery.

## Mocking

Test mocks are fake functionality that represent external dependencies. They can be used to isolate the unit to be tested.

## DBC

DBC (Design-by-contract) is a strategy of decorating functions and methods with precondition, post-condition and invariant checks.
Often using assert-code that can be disabled in production.

DBC is a *fail-fast at runtime strategy* that can complement TDD, which is a *fail-fast at build time strategy*.
Contrary to TDD, DBC can test not just for preconditions and post-conditions but also for invariants. DBC can also be used in production code. DBC is always on, continuously checking the state of the appication.

see: https://en.wikipedia.org/wiki/Design_by_contract and https://www.eiffel.com/values/design-by-contract/introduction/

## TDD (test-driven)

In TDD the developer writes his/her own tests to verify correctness and detect regression during refactoring.
These are the unit and integration tests.

In agile software development, where refactoring is continuous, integration tests are written before the unit tests.
Unit tests are only put in place after the integrations tests pass and the initial code architecture feels good.

## BDD (behavioral-driven)
 
In BDD not the developer but other stakeholders (usually test-engineers) write the tests in natural language.
Using tooling this is than translated into automated test code.

BDD can easily be combined with TDD. In that case the BDD tests could replace the TDD integration tests. 


