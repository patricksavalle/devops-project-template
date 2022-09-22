# Incident management procedure

an incident is a single unplanned event that causes a service disruption.

```
Clone this repo and document your incident management procedure here:



```
> Content
> - [Tips and hints](#tips-and-hints)
> - [Stages](#stages)
> - [Roles](#roles)
> - [Root cause](#proximate-and-root-causes)
> - [SRE](#sre)
> - [ITIL](#itil)

Incident management is the process of resolving an incident.
An incident is resolved when the affected service resumes functioning in its intended state. 
This includes only those tasks required to mitigate impact and restore functionality. 

Incident Management needs a [monitoring and observability strategy](monitoring-strategy.md).

Problem management is not incident management. Problems can cause incidents unless they are solved.

See [Atlassian](https://www.atlassian.com/incident-management) for a practical incident management guide.

## Tips and hints

- [ ] Enable autonomous decision-making by people and teams


- [ ] Establish a culture of open, blameless communication 


- [ ] Use [chatops](https://www.atlassian.com/incident-management/devops/chatops)


- [ ] Utilize on-call scheduling to position developers and sysadmins as SREs


- [ ] Ensure members of your teams can communicate across the organization with chat tools


- [ ] Use an easy-to-remember URL that redirects to the internal Service Desk portal


## Stages

The IM process has 5 stages :

1. Detect
1. Respond
1. Recover
1. Learn / Postmortem
1. Improve

## Roles

Typical roles are:

- Incident manager
- Tech lead
- Communications manager


## Proximate and root causes

When you’re writing or reading a postmortem, it’s necessary to
distinguish between the proximate and root causes.
- Proximate causes are reasons that directly led to this incident.
- Root causes are reasons at the optimal place in the chain of events where making a change will prevent this entire class of incident.

- A postmortem seeks to discover root causes and decide how to best
mitigate them. 

Root causes can fall into different categories:

- Bug
- Change
- Scale
- Architecture
- Dependency
- Unknown

## SRE


## ITIL
