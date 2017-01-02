# silverleague/silverstripe-console

## Status: In development

| Role | Assignee |
| ---- | --- |
| Maintainer | [robbieaverill](https://github.com/robbieaverill) |
| Co-maintainer | TBC |
| Advocate | TBC |

[Proposal tracker](https://github.com/silverleague/silverleague.github.io/issues/1).

## Introduction

The SilverLeague Console is a [Symfony console](http://symfony.com/doc/current/components/console.html) application which interfaces directly with a SilverStripe application for a better command line experience.

## Use case

The [SilverStripe framework](https://github.com/silverstripe/silverstripe-framework) ships with a built in CLI management tool - "framework/cli-script.php". It also has a bash wrapper called "sake". This tool essentially lets you run controllers from the command line in much the same way as you would from the browser, while providing added benefits such as not having to worry about web server timeouts, being able to run in a cron task, etc.

This tool is limited. The SilverLeague console aims to replace its use with a more powerful, flexible and featured tool for managing SilverStripe applications.

## Functionality

* Most importantly the console will automatically detect all `BuildTask` instances from the SilverStripe application and expose them as console commands
* Database build, manifest flushing
* Database management (import, dump, dev-stripping)
* Asset management (import, dump)
* Member management (create, change password, change groups, change roles)
* Cache management (clear, inspect, clear individual areas)
* Module creation - initialise a new module, choose classes to extend and choose new DataObjects to create
* Extensibility - ability to add custom commands to a user directory, or specific folder in a SilverStripe application to be run by the console

## License

To be released under the MIT license.

## Contributing

Please see the [Contributing section](../#contributing) for more information.
