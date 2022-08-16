# Versioning Strategy

```
Clone this repo and document your specific choice here:



```
> Content
> - [Best practices](#best-practices)
> - [Breaking changes and backward compatibility](#breaking-changes-and-backward-compatibility)
> - [SimVer](#simver)
> - [SemVer](#semver)
> - [CalVer](#calver)

The versioning strategy determines the version numbering of releases. In general:
- SimVer and SemVer are very suitable for API’s with many consumers
- SimVer and SemVer minor versions should be backward compatible and not introduce breaking changes
- CalVer is very suitable for end-user applications and apps (in the leafs of the dependency graph)

## Best practices

- [ ] Use SimVer for API's and libraries


- [ ] Use CalVer for applications and apps


- [ ] Backward compatibility for major version numbers is sacred


- [ ] Keep old versions running for a short but reasonable grace period before deprecation


## Breaking changes and backward compatibility

For API's it's vital to not introduce breaking changes that break backward compatibility.

When using SemVer or SimVer the consumers must be able to rely on the version numbers. 
Only changes in major version number may break backward compatibility and this must not occur often. 
Often een grace period is granted before deprecating the old version, 
indicating the need to maintain multiple production environments and a fitting [delivery strategy](delivery-strategy.md).

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
