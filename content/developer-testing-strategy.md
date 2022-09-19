# Developer Testing Strategy

Developer testing (a.k.a unit-testing) is automated testing used to check if the application code is ready to be deployed.


```
Clone this repo and document your developer testing strategy here:



```
> Content
> - [Tips and hints](#tips-and-hints)
> - [Isolation vs integration tests](#isolation-vs-integration-tests)
> - [Mocking](#mocking)
> - [Test driven development](#tdd-test-driven)
> - [Behavioral driven development](#bdd-behavioral-driven)

Developer testing is used to check if the application code is ready to be deployed. 
As opposed to [acceptance testing](acceptance-testing-strategy.md) that is done after the application is deployed to check if a new deployment can be put into production.

## Tips and hints

- [ ] Use [Design-by-Contract](coding-guidelines.md#design-by-contract) to complement developer testing


- [ ] Write high level tests for new features as a whole **before** implementing the feature


- [ ] Write lower level tests for new feature's parts **after** the implementation passes the high-level tests **and** it's design is satisfactory 

   > This prevents continuously having to refactor the tests while implementation's design still changes.
   > These test now serve to prevent and help locate regression during refactors


- [ ] Use a framework to mock integrations, turning integration test into isolation tests (unit tests)


- [ ] Always test interfaces so you can optimize implementations without breaking tests


- [ ] Only use automatable testing in this phase


- [ ] Remove tests that are not 100% reliable or representative


- [ ] Avoid tests that are so complex that they need their own tests


## Isolation vs integration tests

*Note I use a different but more intuitive definition compared to conventional wisdom*

Theoretically developers do unit testing. 
Units are the smallest modules in the application.
In practice however every level of aggregation has it's own units.
A method or function can be a unit, a class and even entire microservices can be units too.
The isolation test is a better concept for this reality than traditional unit testing. 
Developers need only write integration tests and use mocks to run the same test as isolation test (unit tests).

Isolation tests test modules in isolation using mocks that represent their integrations.
Integrations tests test modules with their integrations.
Integration tests become unit tests when integrations are mocked.
**The only difference is isolation**.

Developer tests are run manually during development and automated during continuous integration and delivery.

## Mocking

Mocking is the general term for the different techniques that can be used to isolate modules (units) from their integrations:
- Dummy objects are passed around but never actually used. Usually they are just used to fill parameter lists.
- Fake objects actually have working implementations, but usually take some shortcut which makes them not suitable for production (an in-memory database is a good example).
- Stubs provide canned answers to calls made during the test, usually not responding at all to anything outside what’s programmed in for the test.
- Mocks are objects pre-programmed with expectations [that] form a specification of the calls they are expected to receive.

See:
- [Sorens: A TDD Journey: 3- Mocks vs. Stubs; Test Frameworks; Assertions; ReSharper Accelerators](https://www.red-gate.com/simple-talk/development/dotnet-development/a-tdd-journey-3-mocks-vs-stubs-test-frameworks-assertions-resharper-accelerators/)
- [Fowler: Mocks aren't stubs](https://martinfowler.com/articles/mocksArentStubs.html#TheDifferenceBetweenMocksAndStubs)

## DBC

DBC (Design-by-contract) is a strategy of decorating functions and methods with precondition, post-condition and invariant checks.
Often using assert-code that can be disabled in production.

DBC is a *fail-fast at runtime strategy* that can complement TDD, which is a *fail-fast at build time strategy*.
Contrary to TDD, DBC can test not just for preconditions and post-conditions but also for invariants. DBC can also be used in production code. DBC is always on, continuously checking the state of the appication.

See: [Coding guidelines](coding-guidelines.md#design-by-contract)

## TDD (test-driven)

In TDD the developer writes his/her own tests to verify correctness and detect regression during refactoring.
These are the unit and integration tests.

In agile software development, where refactoring is continuous, integration tests are written before the unit tests.
Unit tests are only put in place after the integrations tests pass and the initial code architecture feels good.

See: https://www.red-gate.com/simple-talk/development/dotnet-development/a-tdd-journey-1-trials-and-tribulations/

## BDD (behavioral-driven)
 
In BDD not the developer but other stakeholders (usually test-engineers) write the tests in natural language.
Using tooling this is than translated into automated test code.

BDD can easily be combined with TDD. In that case the BDD tests could replace the TDD integration tests. 


