# silverleague/silverstripe-logviewer

## Status: Active Support

| Role | Assignee |
| ---- | --- |
| Maintainer | [robbieaverill](https://github.com/robbieaverill) |
| Co-maintainer | TBC |
| Advocate | TBC |

* [Proposal tracker](https://github.com/silverleague/silverleague.github.io/issues/5)
* [Repository](https://github.com/silverleague/silverstripe-logviewer)

## Introduction

As a developer you may not be as aware of SilverStripe logging as you may want to be.

This module intends to *add* a Monolog logger which will log to a database table that can be rendered to an area of the CMS admin for easy viewing.

## Why?

Because logs often go unnoticed, and since the 4.x framework has Monolog bundled with it, we can easily add a new `LoggerInterface` to push logs to the database. From here, they can easily be displayed in the admin as a GridField or similar.

## Details

A new CMS section which displays a GridFields listing all log entries stored.

Columns could be: log content, date/time, log level.

Provide the filter to certain log levels, and allow the GridField to be filterable so I could search for "Deprecated" for example, or to filter by a date range.

We would implement a `BuildTask` and/or a `CronTask` which would clear the logs that are older than *x* days (7? 14? 30?). A button in the CMS admin interface would also allow you to clear old logs.

Export to CSV functionality would be useful as well.

## Framework support

^4.0

## Functionality

* Add new CMSMain interface to the admin area
* Create `DataObject` representing a log entry
* Add and configure new monolog `LoggerInterface` to push the log into a new `LogEntry` (for example)
* Implement filterable/searchable/orderable GridField in the CMS admin
* Add `BuildTask`/`CronTask`/both to remove old log entries automatically
* Add button to CMS main to remove old log entries manually

## License

To be released under the MIT license.

## Contributing

Please see the [Contributing section](../#contributing) for more information.
