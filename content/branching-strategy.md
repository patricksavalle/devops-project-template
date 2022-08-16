# Branching strategy

```
Clone this repo and document your specific choice here:



```
> Content
> - [Best practices](#best-practices)
> - [GitFlow](#gitflow)
> - [GitLabFlow](#gitlabflow)
> - [GitHubFlow](#githubflow)

Collaborative coding and revision control  is done using GIT. Integration with GIT is done using merge requests into branches. 
GIT branching strategy should match life-cycle-, test- and deployment strategy.

In general:
- There is one permanent master branch representing ‘latest releasable’  
- Developers work on temporary features or fixes in isolated feature branches
- Feature branches are merged back into the selected shared release branch 
- Merging is done using merge-requests which incorporate code review by another team member
- Gitlab-flow is a practical default on most projects

See: https://www.flagship.io/git-branching-strategies/ 

## Best practices

- [ ] Keep features and merge request small, avoid merge hell


- [ ] It's personal, let the team decide

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




