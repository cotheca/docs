# Versioning

**Cotheca** uses Semantic Versioning for all software releases. This means that we will keep track of versions using a `<major>.<minor>.<patch>` format, so that we can communicate changes and compatibility with everyone involved.


## Versioning Scheme

### Major Version
The major version will increase when we make changes that will break existing functionality or if there are new features that may affect existing functionality. This may also include changes to the API.


### Minor Version
The minor version will increase when we add new functionality or features in a way that won't break existing code. This may include new APIs, features, or improvements.


### Patch Version
The patch version will increase for bug fixes, performance improvements, or other small changes that don't affect functionality or break compatibility.


## Versioning Rules
* Version numbers will look like `major.minor.patch`.
* We will increase version numbers in the following order: major, minor, patch.
* If we're releasing a test version, we can add a hyphen and a series of dot-separated identifiers (e.g. `1.0.0-beta.1`).
* If we're building a version, we can add a plus sign and a series of dot-separated identifiers (e.g. `1.0.0+build.1`).


## References
Versioning system based on [Semantic Versioning 2.0.0](https://semver.org/spec/v2.0.0.html).


## Release Process
Please check out the [Release Cycle document](./release-cycle.md) for more details.