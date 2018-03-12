# SASS Flexbox Grid
Create a grid of items using a SASS mixin.

## Options
Option | Type | Default | Description
------ | ---- | ------- | -----------
`item-selector` | string | `'&__item'` | The input string becomes interpolated as the SASS selector for grid items.
`item-align` | string | `'left'` | Alignment for partially filled rows. Choices are: `left`, `right`, or `center`.
`columns` | number | `2` | Number of columns for the grid.
`gutter-horizontal` | number | `0px` | Horizontal distance between grid items.
`gutter-vertical` | number | `0px` | Vertical distance between grid items.

## Notes
* Gutters will only add spacing between items by design. If space between grid items and the grid wrapper is needed, it can be achieved by adding padding directly to the grid wrapper.

## Known Issues
* None

## Changelog
### Version 1.0.0
* Mixin creation.