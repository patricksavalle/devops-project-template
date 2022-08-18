# Branching strategy

```
Clone this repo and document your specific choice here:



```
> Content
> - [Best practices](#best-practices)
> - [GitFlow](#gitflow)
> - [GitLabFlow](#gitlabflow)
> - [GitHubFlow](#githubflow)

Branching strategy defines how different new features are developed in parallel and integrated into a new release. 

De industry standard for collaborative coding and revision control is GIT. 
Integration with GIT is done using merge requests into branches. 
GIT branching strategy should match life-cycle-, test- and deployment strategy.

In general:
- Production code is stored in a permanent branch  
- New features or fixes are developed in temporary feature branches
- Feature branches are merged back into the production branch when ready 
- Merging is done using merge-requests which incorporate code review by another developer

See: https://www.flagship.io/git-branching-strategies/ 

## Best practices

- [ ] Keep features and merge request small, avoid merge hell


- [ ] Let the team decide, it's their dog food


- [ ] Consider trunk-based strategy for maximum agility


## GitFlow

Complex, only needed when multiple concurrent releases must be supported.

## GitLabFlow

Flexible, can be as simple as Github-flow or as complex as Git-flow. 

## GitHubFlow

Simple, release always tight to the permanent master-branch.

## Trunk-based

Trunk-based development is a branching strategy that in fact requires no branches but instead, 
developers integrate their changes into a shared trunk at least once a day. This shared trunk 
should be ready for release anytime. This can be done with a feature flag or user ring based [delivery strategy](delivery-strategy.md)
to keep the new trunks isolated in production.
