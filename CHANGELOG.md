# 1.0.0-beta.6

Weekly beta preview release.

### Features

- Pickers can now be used and is styled in Bubble theme

### Bug Fixes

- Fix editing within formula [#702](https://github.com/quilljs/quill/issues/702)
- Fix adding new line when deleting across lists [#741](https://github.com/quilljs/quill/issues/741)
- Fix placeholder when default block tag is changed [#743](https://github.com/quilljs/quill/issues/743)
- Keep Bubble tooltip open on format [#744](https://github.com/quilljs/quill/issues/744)
- Fix format loss when copying from Quill [#748](https://github.com/quilljs/quill/issues/748) [#750](https://github.com/quilljs/quill/issues/750)
- Break long lines in Firefox [#751](https://github.com/quilljs/quill/issues/751)
- Fix cursor position being off after formatting and typing quickly [#752](https://github.com/quilljs/quill/issues/752)
- Remove image resizing handles on Firefox [#753](https://github.com/quilljs/quill/issues/753)
- Fix removing blockquote on initialization [#754](https://github.com/quilljs/quill/issues/754)
- Fix adding blank lines on initialization [#756](https://github.com/quilljs/quill/issues/756)

Thank you [abejdaniels](https://github.com/abejdaniels), [benbro](https://github.com/benbro), [davelozier](https://github.com/davelozier), [fernandogmar](https://github.com/fernandogmar), [KameSama](https://github.com/KameSama), and [WriterStat](https://github.com/WriterStat) for contributions to this release.


# 1.0.0-beta.5

Weekly beta preview release.

### Features

- Add blur() [#726](https://github.com/quilljs/quill/pull/726)

### Bug Fixes

- Fix null error [#728](https://github.com/quilljs/quill/issues/728)
- Fix building with Node v6 [#732](https://github.com/quilljs/quill/issues/732)
- Ensure button type for supplied buttons [#733](https://github.com/quilljs/quill/issues/733)
- Fix line break pasting on Firefox [#735](https://github.com/quilljs/quill/issues/735)
- Fix 'user' source on API calls [#739](https://github.com/quilljs/quill/issues/739)

Thanks to [benbro](https://github.com/benbro), [lukechapman](https://github.com/lukechapman), [sachinrekhi](https://github.com/sachinrekhi), and [saw](https://github.com/saw) for their contributions to this release.


# 1.0.0-beta.4

Weekly beta preview release.

### Breaking Changes

- Headers no longer generates id attribute [#700](https://github.com/quilljs/quill/issues/700)
- Add Control+Y hotkey on Windows [#705](https://github.com/quilljs/quill/issues/705)
- BlockEmbed Blots are now length 1 and represented in a Delta the same as an inline embed
  - value() used to return object and newline, newline is now removed
  - formats used to be attributed on the newline character, it is now attributed on the object

### Features

- Enter on empty and indented list removes indent [#707](https://github.com/quilljs/quill/issues/707)
- Allow base64 images to be inserted via APIs [#721](https://github.com/quilljs/quill/issues/721)

### Bug Fixes

- Fix typing after clearing inline format [#703](https://github.com/quilljs/quill/issues/703)
- Correctly position Bubble tooltip when selecting multiple lines [#706](https://github.com/quilljs/quill/issues/706)
- Fix typing after link format [#708](https://github.com/quilljs/quill/issues/708)
- Fix loss of selection on using link tooltip [#709](https://github.com/quilljs/quill/issues/709)
- Fix `setSelection(null)` [#722](https://github.com/quilljs/quill/issues/722)

Thank you [@benbro](https://github.com/benbro), [@brynjagr](https://github.com/brynjagr), and [@sachinrekhi](https://github.com/sachinrekhi) for contributions to this release.


# 1.0.0-beta.3

Weekly beta preview release.

### Breaking Changes

- Keyboard was incorrectly using `metaKey` to refer to the control key on Windows. It now correctly refers to the Window key and `shortKey` has been added to refer the common platform specific modifier for hotkeys (metaKey for Mac, ctrlKey for Windows/Linux)
- Formula is now a module, since it uses KaTeX

### Features

- Picker now uses text from original `<option>` if available
- Tabbing inside code blocks inserts tab to each line

### Bug Fixes

- Enter preserves inline formats [#666](https://github.com/quilljs/quill/issues/666)
- Fix resetting format button with no selection [#667](https://github.com/quilljs/quill/issues/667)
- Fix paste interpretation from Word [#668](https://github.com/quilljs/quill/issues/668)
- Focus scrolls to correct cursor position [#669](https://github.com/quilljs/quill/issues/669)
- Fix deleting image on otherwise empty document [#670](https://github.com/quilljs/quill/issues/670)
- Fix bubble toolbar formatting [#679](https://github.com/quilljs/quill/issues/679)
- Fix pasting ql-indent lines [#681](https://github.com/quilljs/quill/issues/681)
- Fix getting into state with double underline tag [#695](https://github.com/quilljs/quill/issues/695)
- Fix source type on delete [#697](https://github.com/quilljs/quill/issues/697)
- Fix indent becoming NaN [#698](https://github.com/quilljs/quill/issues/698)

Thanks to [@benbro](https://github.com/benbro), [@Cinamonas](https://github.com/Cinamonas), [@emanuelbsilva](https://github.com/emanuelbsilva), [@jasonmng](https://github.com/jasonmng), [@jonnolen](https://github.com/jonnolen), [@LucVanPelt](https://github.com/LucVanPelt), [@sachinrekhi](https://github.com/sachinrekhi), [@sagacitysite](https://github.com/sagacitysite), [@WriterStat](https://github.com/WriterStat) for their contributions to this release.


# 1.0.0-beta.2

Weekly beta preview release. Major emphasis on keyboard API and customization.

### Breaking Changes

- Rename code highlighter module to syntax
- Clipboard matchers specified in configuration appends to instead of replaces default matchers
- Change video embed to use `<iframe>` instead of `<video>` enabling Youtube/Vimeo links

### Features

- Add contextual keyboard listeners
- Allow indent format to take +1/-1 in addition to target indent level
- Shortcuts for creating ordered or bulleted lists
- Autofill mailto for email links [#278](https://github.com/quilljs/quill/issues/278)
- Enter does not continue header format [#540](https://github.com/quilljs/quill/issues/540)

### Bug Fixes

- Allow native handling of backspace [#473](https://github.com/quilljs/quill/issues/473) [#548](https://github.com/quilljs/quill/issues/548) [#565](https://github.com/quilljs/quill/issues/565)
- removeFormat() removes last line block formats [#649](https://github.com/quilljs/quill/issues/649)
- Fix text direction icon directon [#654](https://github.com/quilljs/quill/issues/654)
- Fix text insertion into root scroll [#655](https://github.com/quilljs/quill/issues/655)
- Fix focusing on placeholder text in FF [#656](https://github.com/quilljs/quill/issues/656)
- Hide placeholder on formatted line [#657](https://github.com/quilljs/quill/issues/657)
- Fix selection handling on focus and blur [#664](https://github.com/quilljs/quill/issues/664)

Thanks to [@anovi](https://github.com/anovi), [@benbro](https://github.com/benbro), [@jbrowning](https://github.com/jbrowning), [@kei-ito](https://github.com/kei-ito), [@quentez](https://github.com/quentez), [@u9520107](https://github.com/u9520107) for their contributions to this release!


# 1.0.0-beta.1

Weekly beta preview release.

### Breaking Changes

- Toolbar only attaches to `<button>` and `<select>` elements
- Toolbar uses button `value` attribute, instead of `data-value`
- Toolbar handlers overwrite default handlers instead of possibly cascading
- Deprecate keyboard `removeBinding` and `removeAllBindings`

### Features

- Expose default keyboard bindings in configuration
- Add context listener to keyboard bindings

### Bug Fixes

- Error when cursor places next to video embed [#644](https://github.com/quilljs/quill/issues/644)
- Selection removed when clicking on a menu button in the toolbar [#645](https://github.com/quilljs/quill/issues/645)
- Editor looses focus in FF after typing two bold characters [#646](https://github.com/quilljs/quill/issues/646)
- Get rid of resize boxes in code in IE11 [0ad636](https://github.com/quilljs/quill/commit/0ad6363c9fcd70c52ca667d39a393760eeb646b5)
- Text direction icon should flip the arrow when pressed [#651](https://github.com/quilljs/quill/issues/651)
- Not possible to combine direction:rtl with text-align:left [#652](https://github.com/quilljs/quill/issues/652)

Thanks to [@benbro](https://github.com/benbro) for the bug reports for this release!


# 1.0.0-beta.0

Please see the [Upgrading to 1.0](http://beta.quilljs.com/guides/upgrading-to-1-0/) guide.


# 0.20.1

Patch release for everything prior to Parchment's integration into Quill.

### Features

- API for hotkey removal [#110](https://github.com/quilljs/quill/issues/110), [#453](https://github.com/quilljs/quill/pull/453)

### Bug Fixes

- Editor jumps to top when clicking formatting buttons [#288](https://github.com/quilljs/quill/issues/288)
- Editor does not preserve bold text when pasted from itself [#306](https://github.com/quilljs/quill/issues/306)
- Focus issues when scrolled down in IE10+ [#415](https://github.com/quilljs/quill/issues/415)
- Error if keyboard shortcut used for unavailable format [#432](https://github.com/quilljs/quill/issues/432)
- Scrolls to cursor if not visible after enter/deletion/paste [#433](https://github.com/quilljs/quill/issues/433)

Thanks to [@devtimi](https://github.com/devtimi), [@emannes](https://github.com/emannes), [@ivan-i](https://github.com/ivan-i), [@magus](https://github.com/magus), [@Nick-The-Uncharted](https://github.com/Nick-The-Uncharted), [@rlivsey](https://github.com/rlivsey), [@thomsbg](https://github.com/thomsbg), [@wallylawless](https://github.com/wallylawless) for their bug reports and pull requests!


# 0.20.0

### Breaking Changes
- `getBounds` now returns `null` instead of throwing an error [#412](https://github.com/quilljs/quill/pull/412)

### Features
- Allow `Document` module to be `Quill.require`'d [#400](https://github.com/quilljs/quill/pull/400)
- Paste manager can optionally accept a custom conversion function [#401](https://github.com/quilljs/quill/pull/401)
- Undo manager can optionally only affect user initiated changes [#413](https://github.com/quilljs/quill/pull/413)

### Bug Fixes
- Retain formats between lines [#403](https://github.com/quilljs/quill/pull/403)
- Fix bug that allows nested format tags [#406](https://github.com/quilljs/quill/pull/406)
- Flatten nested list instead of truncating on paste [#421](https://github.com/quilljs/quill/issues/421)
- Fix handling Chrome's usage of font-weight instead of tags [#423](https://github.com/quilljs/quill/issues/423)
- Fix bug that allows nested parent tags [#426](https://github.com/quilljs/quill/pull/426)

Thank you [@thomsbg](https://github.com/thomsbg), [@yyjhao](https://github.com/yyjhao), [@willrowe](https://github.com/willrowe), [@hryanjones](https://github.com/hryanjones), [@nickretallack](https://github.com/nickretallack) for your contributions to this release!
