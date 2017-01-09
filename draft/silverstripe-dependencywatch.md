# silverleague/silverstripe-dependencywatch

## Status: Draft

| Role | Assignee |
| ---- | --- |
| Maintainer | [zanderwar](https://github.com/zanderwar) |
| Co-maintainer | [robbieaverill](https://github.com/robbieaverill) |
| Advocate | TBC |

[Proposal tracker](https://github.com/silverleague/silverleague.github.io/issues/4).

## Introduction

As a developer you can use `composer outdated` to check for updates to your dependencies.

This module aims to provide the same interface inside the CMS for both developers and content authors.

## Why?

Content authors and/or site users may not be the same as developers in terms of maintenance scope. A user might have paid a developer to create a SilverStripe application, then be left to their own devices.

This way anyone with permission could check the status of their application's dependencies and potentially view changelogs of new versions to decide whether they want to upgrade.

Upgrading would not be part of this module as we would encourage it to be done outside of a production environment.

This may also provide visibility for developers who either do not know about the command or don't use it regularly enough to get its benefit.

## Details

A new CMS section which displays two GridFields:

* SilverStripe modules
* Other dependencies

Each GridField would list the current version, the latest "safe" semver compatible version and the latest "unsafe" (major change) semver compatible version. Colour code the cells for visibility.

This module would assume that all dependencies conform to [semantic versioning](http://semver.org/).

There is limited benefit to listing dependencies of dependencies, so perhaps we only list project dependencies. We could show sub dependencies in a help-tip under each dependency, e.g.:

>`monolog/monolog` is locked at version 0.1.2 because `silverstripe/framework` is locked at version 1.2.3"

## Framework support

^4.0

## Functionality

- [ ] Add new CMSMain interface to the admin area
- [ ] Load project's Composer dependencies using the `composer/composer` library
- [ ] Distinguish between project dependencies and sub-dependencies
- [ ] Distinguish between SilverStripe modules and other dependencies
- [ ] Display SilverStripe modules and other dependencies in separate GridFields
- [ ] Display module name, description, current installed version, next "semver safe" version available (if applicable, otherwise the same), next "semver unsafe" (major version bumped) version available
- [ ] If there are "safe" framework updates, display an info message suggesting that it should be upgraded for security reasons

## License

To be released under the MIT license.

## Contributing

Please see the [Contributing section](../#contributing) for more information.
