**< [devops-project-template](../README.md)**

# Coding guidelines

Coding guidelines ensure robust, maintainable code.

```
Clone this repo and document your coding guidelines here:



```
> Content
> - [Guidelines](#guidelines)
> - [Design Patterns](#design-patterns)
> - [Design-by-Contract](#design-by-contract)
> - [Const-correctness](#const-correctness)

## Guidelines

- [ ] Use industry standards and styles 


- [ ] Do pair programming


- [ ] Make code self-documenting but add inline documentation (only) when needed


- [ ] Prefer using a well-known [design pattern](#design-patterns) over writing an (over-optimized) one-off solution


- [ ] If a solution doesn't feel right, re-code (never sacrifice simplicity and elegance, never accept mediocre quality) or backlog as technical debt


- [ ] Ensure all code, the entire project, is always in a deployable state


- [ ] Apply [design-by-contract](#design-by-contract) principles


- [ ] Apply [const-correctness](#const-correctness) principles


- [ ] Use (automated) code linting


- [ ] Use (automated) code formatting


- [ ] Build automated test according to the [developer testing strategy](developer-testing-strategy.md) 


- [ ] Code for testing-in-operation according to the [acceptance testing strategy](acceptance-testing-strategy.md)


- [ ] Code for observability according to the [optimization method](optimization-method.md) and [incident management procedures](incident-management-procedure.md)


## Design Patterns

Design Patterns are reusable pieces of tested and documented design. Like templates.

See:
- [Design Patterns](https://sourcemaking.com/design_patterns)
- [14 Patterns to Ace Any Coding Interview Question](https://hackernoon.com/14-patterns-to-ace-any-coding-interview-question-c5bb3357f6ed)
- [Integration Patterns](https://www.enterpriseintegrationpatterns.com/)


## Design-by-Contract

Design-by-Contract is a concept that originated in the Eiffel language but can be used in any language.
It uses ```assert``` syntax to check pre-conditions, post-conditions and invariants of a method's or function's contract. Example:

```
@Invariant({"title != null && title.length() > 0", "price > 0"})
public class Book {
    private final String title;
    private int price;
 
    @Requires({"title != null && title.length() > 0", "price > 0"})
    public Book(String title, int price) {
        this.title = title;
        this.price = price;
    }
 
    @Requires("price > 0")
    public void setPrice(int price) {
        this.price = price;
    } 
}
```

DBC is not a substitute for [developer testing](developer-testing-strategy.md).

See: 
- [Eiffel - introduction DbC](https://www.eiffel.com/values/design-by-contract/introduction/)
- [Meyer - Applying DbC](http://se.inf.ethz.ch/~meyer/publications/computer/contract.pdf)
- [Wikipedia - Design by Contract](https://en.wikipedia.org/wiki/Design_by_contract)

## Const-correctness

This is a concept that originated in early-days C++ programming but it can be applied to some degree in other languages too. It is just another form of type safety that is supported by some languages through the ```const```-keyword..

See: 
- [C++ const-correctness](https://isocpp.org/wiki/faq/const-correctness)
- [Wikipedia - const](https://en.wikipedia.org/wiki/Const_(computer_programming))