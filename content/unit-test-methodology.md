# Unit Test Methodology

```
Clone this repo and document your specific choice here:



```
> Content
> - [Unit vs integration tests](#unit-vs-integration-tests)
> - [Best practices](#best-practices)
> - [Test driven development](#tdd-test-driven)
> - [Behavioral driven development](#bdd-behavioral-driven)
> - [Acceptance test driven development](#atdd-classic-acceptance-test-driven)

The trick of testing in general is to fail as fast as possible when bugs still have minimal impact.

Unit (and integration) testing is used to validate the application code before it is even deployed.

## Unit vs integration tests

*Note I use a different but more intuitive definition compared to conventional wisdom*

Unit tests test modules in isolation using mocks that represent their integrations.
Integrations tests test modules with their integrations.
Integration tests become unit tests when integrations are mocked.
**The difference is isolation**. A better name for unit test would be **isolation test**.

Unit and integration tests exist on different levels of aggregation, following application architecture.
A method or function can be a unit, a class or an entire microservice can be units too.

Unit and integration tests are run manually during development and automated during continuous integration and delivery.

## Best Practices

- [ ] Use Design-by-Contract to complement testing
- [ ] Write high level (integration) tests for feature as a black box before implementing the feature's functionality
- [ ] Write (unit) tests for the internal parts **after** the implementation passes the high-level tests and initial modularity is satisfactory
- [ ] Be flexible with this when needed
- [ ] Test functionality so you can optimize implementation without breaking tests
- [ ] Automate as many tests as you can
- [ ] Remove tests that are not 100% reliable and representative
- [ ] Leave it up to the planning and optimisation methods to add more features and tests, and to optimize existing ones

See: https://techbeacon.com/app-dev-testing/6-best-practices-integration-testing-continuous-integration 

## DBC

DBC (Design-by-contract) is a strategy of decorating functions and methods with precondition, post-condition and invariant checks.
Often using assert-code that can be disabled at runtime.

DBC is a *fail-fast at runtime strategy* that can complement TDD, which is a *fail-fast at build time strategy*.
Contrary to TDD, DBC can test not just for preconditions and post-conditions but also for invariants. DBC can also be used in production code.

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


