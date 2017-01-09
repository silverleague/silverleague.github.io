# silverleague/silverstripe-async

## Status: Development

| Role | Assignee |
| ---- | --- |
| Maintainer | [assertchris](https://github.com/assertchris) |
| Co-maintainer | TBC |
| Advocate | [robbieaverill](https://github.com/robbieaverill) |

* [Proposal tracker](https://github.com/silverleague/silverleague.github.io/issues/6)
* [Repository](https://github.com/silverleague/silverstripe-async)

## Why?

SilverStripe has a traditional, synchronous execution model. Except for [QueuedJobs](https://github.com/silverstripe-australia/silverstripe-queuedjobs), no other supported module offers anything nearly useful for implementing asynchronous execution in places where an application could use it.

A module – which offers an event loop, web sockets, and sane parallel execution – could allow for more interesting and useful extensions to the CMS. This would make things like multi-user editing, presence, parallel queue execution, and DataObject push hooks trivial to implement.

## Details

I propose we use [Amp](https://github.com/amphp). It requires `^7.0`, which would become the required version for this module. It provides a mature event loop, promise, and web socket implementations. It also offers a parallel execution model that depends on Pthreads or PCNTL.

I suggest we abstract the parallel execution code, and base the first version on `exec` instead (as this will already be used for the initial CronTask (event loop daemon).

> Aspects of this have already been worked into QueuedJobs, but are disabled by default. They are also present in the [Serve module](https://github.com/silverstripe/silverstripe-serve).

## Functionality

* Create a CronTask to "daemonize" the main event loop process
* Create interfaces for web socket listener classes
* Create a "global" web socket listener class, to broadcast DataObject events to subscribed web socket clients
* Create/embed sane parallel execution scheme
* Abstract FE web socket code, paving the way for additional modules
* Propose DataObject push hooks module
* Propose Presence module
* Propose "new" multi-user editing module
* Propose "new" (or changes to existing) queued jobs module, which uses parallel execution by default

## Framework support

^4.0

## License

To be released under the MIT license.

## Contributing

Please see the [Contributing section](../#contributing) for more information.
