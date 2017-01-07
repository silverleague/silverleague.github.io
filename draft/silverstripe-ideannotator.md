# silverleague/silverstripe-ideannotator

## Status: Draft

| Role | Assignee |
| ---- | --- |
| Maintainer | [axyr](https://github.com/axyr) |
| Co-maintainer | [Firesphere](https://github.com/Firesphere) |
| Advocate | TBC |

[Proposal tracker](https://github.com/silverleague/silverleague.github.io/issues/7).

## Why?

The SilverStripe ORM definition with static arrays are unreadable for PHPStorm and NetBeans (and other IDE's), to support auto-completion on properties and methods.

## Details

This module generates @property, @method and @mixin tags for DataObjects, Page_Controllers and (Data)Extensions, so IDE's like PHPStorm recognize the database and relations that are set in the $db, $has_one, $belongs_to, $has_many and $many_many arrays including PropertyID for $has_one relations.

The docblocks can be generated/updated with each dev/build and with a DataObjectAnnotatorTask per module or classname.

## Functionality

- [x] Generate `@property` annotations to models and pages
- [x] Generate `@method` annotations to models and pages
- [x] Generate `@mixn` annotations to models and pages
- [x] Only scan assigned modules

## To do

- [] SilverStripe 4 support
- [] Namespaces

## Framework support

^3.2
^4.0

## License

BSD-3-Clause

## Contributing

Please see the [Contributing section](../#contributing) for more information.
