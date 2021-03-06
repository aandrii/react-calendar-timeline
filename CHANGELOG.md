# Change Log
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/)
and this project adheres (more or less) to [Semantic Versioning](http://semver.org/).

## Unreleased
When you submit a PR, add your changes here!

## [0.14.0]
### Added
- Use `headerLabelFormats` and `subHeaderLabelFormats` to customise the header labels. @Slowyn #68
- Optional pluggable `resizeDetector` to detect when the element's container is resized. @Ziller321 #94

### Fixed
- Fix renders with empty `groups` array. @signalwerk #106

## [0.13.0]
### Added
- An option to add another sidebar to the right of the Timeline. @goooseman #80
- `itemRenderer` prop to allow specifying a custom component to render the items @nicocrm #103
- `groupRenderer` prop to allow specifying a custom component to render the groups @nicocrm #103
- `showCursorLine` prop to show a vertical line at the snap position @meikoudras
- You can now select multiple items if you take control of the `selected` prop and the `onItemSelect` handler. @meengit #71
- Canvas context menu handler `onCanvasContextMenu` @meikoudras

### Fixed
- Calculate width when we receive sidebar width property @jmerriweather #75
- Avoid updating updateDimensions right after updateScrollCanvas @nicocrm #87
- Fix typo collision detection in stack() @nicocrm #96
- Remove dead code @signalwerk #101
- Disable cursor style by interactjs @bkniffler #89
- Fixed header width and Header label weekday support @meikoudras #66

### Changed
- [Deprecated] To have content above the left sidebar, pass it in a `sidebarContent={<div />}` prop, not as children to the component.

## [0.11.1]
### Fixed
- Without canResize prop in items it gave a Uncaught TypeError. @tgosp

## [0.11.0]
### Added
- An option to fully update the calendar at every scroll event. With this change, labels of items are always fully visible, even if looking at a multi day event with a zoom level set at 30min. @mariusandra

## [0.10.1]
### Changed
- The left resize edge mouse cursor is now a left arrow @mariusandra

## [0.10.0]
### Added
- You can also resize items from the left now @mariusandra

## [0.9.0]
### Added
- Allow disabling selection clicks on items #58 by @sjchmiela
- Allow passing additional props to `Item`'s `<div/>` #58 by @sjchmiela
- Add `clickTolerance` so dragging more than 3 pixels is no longer a click @mariusandra

### Changed
- [BREAKING] Same arguments order (groupId, time, e) for onCanvasDoubleClick and onCanvasClick #52 by @signalwerk
- [Deprecated] `onTimeChange` now gets `updateScrollCanvas` as the third argument. Doing `this.updateScrollCanvas` is no longer needed and will be removed soon.
- Moved React & Moment from dependencies to peerDependencies #53 by @meikoudras
- Fix resizing when inside DIV #47 by @semargal
- Fix demo for IE11 #44 by @lucidlemon
- Package a .css file, not a .scss file as previously done. @mariusandra

[0.9.0]: https://github.com/namespace-ee/react-calendar-timeline/compare/v0.8.6...v0.9.0
[0.10.0]: https://github.com/namespace-ee/react-calendar-timeline/compare/v0.9.0...v0.10.0
[0.10.1]: https://github.com/namespace-ee/react-calendar-timeline/compare/v0.10.0...v0.10.1
[0.11.0]: https://github.com/namespace-ee/react-calendar-timeline/compare/v0.10.1...v0.11.0
[0.11.1]: https://github.com/namespace-ee/react-calendar-timeline/compare/v0.11.0...v0.11.1
[0.13.0]: https://github.com/namespace-ee/react-calendar-timeline/compare/v0.11.1...v0.13.0
[0.14.0]: https://github.com/namespace-ee/react-calendar-timeline/compare/v0.13.0...v0.14.0
