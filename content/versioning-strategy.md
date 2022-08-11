# Versioning Strategy

```
Clone this repo and document your specific choice here:



```
> Content
> - [SimVer](#simver)
> - [SemVer](#semver)
> - [CalVer](#calver)

The versioning strategy determines the version numbering of releases. In general:
- SimVer and SemVer are very suitable for API’s with many consumers
- SimVer and SemVer minor versions should be backward compatible and not introduce breaking changes
- CalVer is very suitable for end-user applications and apps (in the leafs of the dependency graph)

## SimVer

```major.minor```

Simple semantic versioning. Well suited for API's. Minor versions are always backward compatible.
Breaking changes require a new major version.

## SemVer

```major.minor.patch```

Semantic versioning. Well suited for API's. Minor versions and patches are always backward compatible.
Breaking changes require a new major version.

## CalVer

```year.release.build-status```

Calendar versioning. Well suited for applications. 
