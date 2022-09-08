# Provisioning and configuration Management

Provisioning is setting up the infrastructure.
Configuration management is a establishing and maintaining the system in a desired, consistent state.

```
Clone this repo and document your configuration management here:



```
> Content
> - [Tips and hints](#tips-and-hints)
> - [IaC](#iac)
> - [GitOps](#gitops)


## Tips and hints

TODO

## IaC

Infrastructure-as-Code (IaC)

## GitOps

GitOps is a way to automate application delivery.
GitOps works by using Git as a single source of truth for declarative infrastructure and applications.
It applies CI/CD (Continuous Integration/ Continuous Delivery) principles to configuration management.

- The entire system described declaratively
- The canonical desired system state versioned in Git
- Approved changes that can be automatically applied to the system
- Configuration agents ensure correctness and alert on divergence

### CI/CD controller pattern

In the CI/CD Controller pattern, an independent application or service is aware of the state of one or many source code repositories. 
It executes a CI/CD deployment automatically when code changes within a particular repository.

see: https://www.redhat.com/architect/gitops-implementation-patterns

### SCM controller pattern

In the SCM Controller pattern, source code that controls CI/CD deployment activity is colocated in the same Git repository as the application source code. 
Under the SCM Controller, the SCM service can internally execute actions such as builds, tests, and the eventual release to a staging or production target.

See: https://www.redhat.com/architect/gitops-implementation-patterns 



## Tips and hints


## LAMP


## Docker


## Kubernetes


## Cloud-native

