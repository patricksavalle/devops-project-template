# Branching strategy

Branching strategy defines how different new features are developed in parallel and integrated into a new release.


```
Clone this repo and document your branching strategy here:



```
> Content
> - [Tips and hints](#tips-and-hints)
> - [GitFlow](#gitflow)
> - [GitLabFlow](#gitlabflow)
> - [GitHubFlow](#githubflow)
> - [Trunk-based](#trunk-based)

De industry standard for collaborative coding and revision control is GIT. 
Integration with GIT is done using merge requests into branches. 
GIT branching strategy should match life-cycle-, test- and deployment strategy.

In general:
- Production code is stored in a permanent branch  
- New features or fixes are developed in temporary feature branches
- Feature branches are merged back into the production branch when ready 
- Merging is done using merge-requests which incorporate code review by another developer

See: 

- [Git branching strategies](https://www.flagship.io/git-branching-strategies/) 
- [Git to know this before you do Trunk Based Development (TBD)](https://medium.com/contino-engineering/git-to-know-this-before-you-do-trunk-based-development-tbd-476bc8a7c22f)
- [DevOps tech: Trunk-based development](https://cloud.google.com/architecture/devops/devops-tech-trunk-based-development)

## Tips and hints

- [ ] Keep features and merge request small, avoid merge hell


- [ ] Start with [trunk-based development](branching-strategy.md#trunk-based) and switch to a [GitFlow](branching-strategy.md) when the product can be built in feature increments or when the project is crowdsourced


## GitFlow

Complex, only needed when multiple concurrent releases must be supported.

## GitLabFlow

Flexible, can be as simple as Github-flow or as complex as Git-flow. 

## GitHubFlow

Simple, release always tight to the permanent master-branch.

## Trunk-based

Trunk-based development (TBD) is a branching strategy that in fact requires no branches but instead, 
developers integrate their changes into a shared trunk at least once a day. This shared trunk 
should be ready for release anytime. This can be done with a feature flag or user ring based [delivery strategy](delivery-strategy.md)
to keep the new trunks isolated in production.

Good choice for the initial stages of the project when changes in functionality and volatility of solutions make GitFlow's unpractical.