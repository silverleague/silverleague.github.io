# silverleague/silverstripe-ideannotator

## Status: Complete

| Role | Assignee |
| ---- | --- |
| Maintainer | [axyr](https://github.com/axyr) |
| Co-maintainer | [Firesphere](https://github.com/Firesphere) |
| Advocate | [robbieaverill](https://github.com/robbieaverill)] |

* [Proposal tracker](https://github.com/silverleague/silverleague.github.io/issues/7)
* [Repository](https://github.com/silverleague/silverstripe-ideannotator)

## Why?

The SilverStripe ORM definition with static arrays are unreadable for PHPStorm and NetBeans (and other IDE's), to support auto-completion on properties and methods.

## Details

This module generates `@property`, `@method` and `@mixin` tags for DataObjects, Page_Controllers and (Data)Extensions, so IDE's like PHPStorm recognize the database and relations that are set in the `$db`, `$has_one`, `$belongs_to`, `$has_many` and `$many_many` arrays including `PropertyID` for `$has_one` relations.

The docblocks can be generated/updated with each `dev/build` and with a `DataObjectAnnotatorTask` per module or classname.

## Functionality

- [x] Generate `@property` annotations to models and pages
- [x] Generate `@method` annotations to models and pages
- [x] Generate `@mixn` annotations to models and pages
- [x] Only scan assigned modules

## To do

- [x] SilverStripe 4 support
- [ ] Namespaces

## Framework support

* SS ^3.2 via IA 2.x release line
* SS ^4.0 via IA 3.x release line

## License

BSD-3-Clause

## Contributing

Please see the [Contributing section](../#contributing) for more information.
