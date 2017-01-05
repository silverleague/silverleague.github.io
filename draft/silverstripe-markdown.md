# silverleague/silverstripe-markdown

## Status: Draft

| Role | Assignee |
| ---- | --- |
| Maintainer | TBC |
| Co-maintainer | TBC |
| Advocate | TBC |

[Proposal tracker](https://github.com/silverleague/silverleague.github.io/issues/3).

## Introduction

Markdown is a common standard for editing rich text in modern websites.

This module would aim to provide a drop in replacement for a WYSIWYG editor for SilverStripe. It should contain some SilverStripe features such as internal linking and image selectors for inserting assets.

It should use an established markdown parser to generate the preview and render for the frontend. GitHub would be ideal, but requires an external HTTP request. Parsedown might be more suitable.

It should work with SilverStripe 4 and be React friendly.

## Why?

There are a few markdown modules around, but they all have limitations and/or have limited support involvement.

This proposal would establish a new standard for markdown editing in SilverStripe.

It would be a drop-in replacement for TinyMCE.

## Framework support

^4.0

## Functionality

* Textarea entry with buttons for quick formatting (e.g. bold, italic, heading)
* Preview tab/button to see rendered HTML output
* "Add link" button with popup and two options:
 * External: enter the link and text
 * Internal: select an internal SilverStripe Page, and enter the link text
* "Add image" button with popup to select or upload (?) an existing SilverStripe asset
* Ability to configure which text editor to use globally (later on, at a more granular level) and have the editor be switched automatically
* Return rendered HTML by default if calling from a template context

## License

To be released under the MIT license.

## Contributing

Please see the [Contributing section](../#contributing) for more information.
