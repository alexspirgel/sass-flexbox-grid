# SASS Flexbox Grid

Create a grid of items using a SASS mixin.

## Options

Option | Type | Default | Description
------ | ---- | ------- | -----------
`item-selector` | string | `'#{&}__item'` | The input string becomes interpolated as the SASS selector for grid items.
`item-align` | string | `'left'` | Alignment for partially filled rows. Choices are: `left`, `right`, or `center`.
`columns` | number | `2` | Number of columns for the grid.
`gutter-horizontal` | number | `0px` | Horizontal distance between grid items.
`gutter-vertical` | number | `0px` | Vertical distance between grid items.

## Notes

* Use SASS interpolation when passing `&` as part of the `item-selector` option. Refer to the default value for an example.
* By design, gutters will only add spacing between grid items. If space between grid items and the grid wrapper is needed, add padding directly to the grid wrapper.

## Changelog

#### Version 1.0.1
* Fixed a bug where passing certain item selector values would result in incorrect child selectors.

#### Version 1.0.0
* Initial creation.