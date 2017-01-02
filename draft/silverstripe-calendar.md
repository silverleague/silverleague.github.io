# silverleague/silverstripe-calendar

## Status: Draft - porting proposed

| Role | Assignee |
| ---- | --- |
| Maintainer | TBC |
| Co-maintainer | [anselmdk](https://github.com/anselmdk) |
| Advocate | TBC |

[Proposal tracker](https://github.com/silverleague/silverleague.github.io/issues/2).

## Introduction

This is a porting proposal for [titledk/silverstripe-calendar](https://github.com/titledk/silverstripe-calendar).

The calendar for SilverStripe 3.x is a solid base for all your calendaring needs, it's built to be flexible and configurable so that it fits to most scenarios - both for web sites with public events, and web apps with private events - or a combination hereof.

## Framework support

^3.1

## Use case

TBC.

## Functionality

* Extensible. Customize it any way you want, while the basic concepts are taken care of.
* Solid, opinionated models.
* Event/Calendar/Category relations allowing complex filtering.
* Public/Private events.
* All features are configurable, so if you only need the basics, you can turn the rest off.
* Comprehensive calendar/event administration.
* JavaScript enhanced edit event form, usable both on frontend and backend, with date picker, time picker and dropdown, and duration dropdown, still allowing manual inputs
* Listing of events on the frontend through the CalendarPage
* Frontend calendar view, using the fullcalendar jQuery plugin
* Event Registrations (this might be moved to an external module)
* Calendar colors with configurable color options, and JS color palette field (works on both frontend and backend) - shading calendars allow for holiday calendars etc. to appear in the background
* No default frontend styling.
* Composer based workflow. You’ll be able to add and update the module using Composer.

## Wish list

* More comprehensive unit tests
* Recurring events
* Everything should be translatable

## License

To be re-released under the MIT license.

## Contributing

Please see the [Contributing section](../README.md#contributing) for more information.
