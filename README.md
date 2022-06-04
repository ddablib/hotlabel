# Hot Label Component

## Description

_TPJHotLabel_ is a simple Delphi component that descends from _TLabel_. It provides a clickable label that can start the default browser or email client to access a specific URL. Key features of the component are:

* All properties of _TLabel_ are supported, although the usage and default values of some of the inherited properties have been changed.
* The _URL_ property is used for storing the URL to be accessed when the label is clicked and the _Caption_ property can either store descriptive text or can reflect the URL, depending on the value of the _CaptionIsURL_ property. The ability to link the caption and URL makes it easy to display the URL without having to keep two properties synchronised.
* The URL can be validated to check for supported protocols. This validation is switched on and off using the _ValidateURL_ property. Supported protocols are:
  * `http://`
  * `https://`
  * `mailto:`
  * `file:`
  * `ftp://`
* The label's _Font_ property defaults to navy blue to indicate a link.
* The label can be highlighted when the mouse passes over it. Highlighting is used if the _HighlightURL_ property is True, and the font used for highlighting is set using the _HighlightFont_ property.
* The label can also display in a different style when its "link" has been clicked successfully. The font to be used is specified via the _VistedFont_ property. The user can switch the visited state on and off via the _Visited_ property or the component can be enabled to track visits automatically using the _TrackVisits_ property.
* The label displays the "hand point" cursor by default.
* The component's pop-up hints can be customised as follows, using the _HintStyle_ property:
  * the hint text can come from the _Hint_ property as normal, _or_
  * the hint text can come from the URL property with the _Hint_ property being ignored, _or_
  * the hint text can be modified just before the hint is shown by handling the _OnCustomHint_ event, which is useful for displaying dynamic information in the hint.

## Compatibility

Release v2.2.0 was tested with all native 32 bit Windows Delphi compilers from Delphi 7 through to XE4, excluding Delphi 2005. It was also tested with the 64 bit compiler of Delphi XE2 through to XE4.

Release v2.2.1, which was just a simple bug fix, was tested only with Delphi 10 Seattle's Win32 personality, but should still work with Delphi 7 and later, along with 64 bit Windows targets.

It is possible that the component will also compile with Delphi 4, 5 and 6, but this has not been tested for a long time.

This is a VCL component and so is not compatible with the FireMonkey framework.

## Installation

The _Hot Label Component_ unit and accompanying files are supplied in a zip file. Before installing you need to extract the files, preserving the directory structure. The following files will be extracted:

* **`PJHotLabel.pas`** – Component source code.
* **`PJHotLabel.dcr`** – Component palette glyph.
* `README.md` – This read-me file.
* `CHANGELOG.md` – The project change log.
* `MPL-2.txt` – The Mozilla Public License v2.0.
* `Documentation.url` – Short-cut to the component's online documentation.

In addition to the above files you will find the source code of the [demo project](#demo-program) in the `Demo` sub-directory.

You can now install the components into the Delphi IDE. To do this, the files `PJHotLabel.pas` and `PJHotLabel.dcr` should be added to a design time package. If you need help doing this [see here](https://delphidabbler.com/url/install-comp).

## Documentation

The component is fully documented [online](https://delphidabbler.com/url/hotlabel-docs).

## Demo Program

Source code for a program that demonstrates the component is included in the download. Most of the demo's functionality depends on the properties of the various hot label components it uses – there is very little code.

The demo requires Delphi 7 or later.

## Update History

A complete change log is provided in [`CHANGELOG.md`](https://github.com/ddablib/hotlabel/blob/main/CHANGELOG.md) that is included in the download.

## License

The _Hot Label Component_ is released under the terms of the [Mozilla Public License v2.0](https://www.mozilla.org/MPL/2.0/).

All relevant trademarks are acknowledged.

## Bugs and Feature Requests

Bugs can be reported or new features requested via the project's [Issue Tracker](https://github.com/ddablib/hotlabel/issues). A GitHub account is required.

Please check if an issue has already been created for a similar report or request. If so then please add a comment containing as much information as you can to the existing issue, or if you've nothing to add, just add a :+1: (`:+1:`) comment. If there is no suitable existing issue then please add a new issue and give as much information as possible.

## About the Author

I'm Peter Johnson – a hobbyist programmer living in Ceredigion in West Wales, UK, writing mainly in Delphi. My programs and other library code are available from: [https://delphidabbler.com/](https://delphidabbler.com/).

This document is copyright © 2007-2022, [P D Johnson](https://gravatar.com/delphidabbler).
