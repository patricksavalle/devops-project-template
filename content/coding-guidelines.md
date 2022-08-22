# Coding guidelines

```
Clone this repo and document your specific choice here:



```
> Content
> - [Guidelines](#guidelines)
> - [Design Patterns](#design-patterns)
> - [Design-by-Contract](#design-by-contract)
> - [Const-correctness](#const-correctness)

Good code is:
- simple and elegant
- self-documenting
- tested
- peer-reviewed

## Guidelines

- [ ] Use industry standards and styles 


- [ ] Make code self-documenting but add inline documentation (only) when needed


- [ ] Prefer using a well-known [design pattern](#design-patterns) over writing an over-optimized one-off solution


- [ ] Open-source as much code as (security-wise) possible to allow [scaling](../README.md#best-practices) your collaboration 


- [ ] Use (automated) code linting


- [ ] Use (automated) code formatting 


- [ ] Apply [design-by-contract](#design-by-contract) principles


- [ ] Apply [const-correctness](#const-correctness) principles


- [ ] Build automated test according to the [developer testing strategy](developer-testing-strategy.md) 


- [ ] Code for testing-in-operation according to the [acceptance testing strategy](acceptance-testing-strategy.md)


- [ ] Code for observability according to the [optimization method](optimization-method.md)


## Design Patterns

Design Patterns are pieces of reusable design. 

See:
- [Design Patterns](https://sourcemaking.com/design_patterns)
- [14 Patterns to Ace Any Coding Interview Question](https://hackernoon.com/14-patterns-to-ace-any-coding-interview-question-c5bb3357f6ed)
- [Integration Patterns](https://www.enterpriseintegrationpatterns.com/)


## Design-by-Contract

Design-by-Contract is a concept that originated in the Eiffel language but can be used in any language.

See: 
- https://www.eiffel.com/values/design-by-contract/introduction/
- http://se.inf.ethz.ch/~meyer/publications/computer/contract.pdf
- https://en.wikipedia.org/wiki/Design_by_contract

## Const-correctness

This is a concept that originated in early-days C++ programming but it can be applied to some in degree in other languages too. It is just another form of type safety that is supported by some languages through the ```const```-keyword..

See: 
- https://isocpp.org/wiki/faq/const-correctness
- https://en.wikipedia.org/wiki/Const_(computer_programming)