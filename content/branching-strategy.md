# Branching strategy

```
Clone this repo and document your specific choice here:



```
> Content
> - [GitFlow](#gitflow)
> - [GitLabFlow](#gitlabflow)
> - [GitHubFlow](#githubflow)

Collaborative coding and revision control  is done using GIT. Integration with GIT is done using merge requests into branches. 
GIT branching strategy should match life-cycle-, test- and deployment strategy.

In general:
- There is one permanent master branch representing ‘latest releasable’  
- Developers work on features or fixes in isolated feature branches
- Feature branches are merged back into the selected shared release branch 
- Merging is done using merge-requests which incorporate code review by another team member
- Gitlab-flow is a practical default on most projects

## GitFlow

Complex, only needed when multiple concurrent releases must be supported.

## GitLabFlow

Flexible, can be as simple as Github-flow or as complex as Git-flow. 

## GitHubFlow

Simple, release always tight to the permanent master-branch.

