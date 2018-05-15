# SASS Flexbox Grid

Create a grid of items using flexbox via SASS mixin.

## Usage

**HTML:**
```html
<div class="grid">
  <div class="grid__item">
    <div class="grid__item__inner">1</div>
  </div>
  <div class="grid__item">
    <div class="grid__item__inner">2</div>
  </div>
  <div class="grid__item">
    <div class="grid__item__inner">3</div>
  </div>
  <div class="grid__item">
    <div class="grid__item__inner">4</div>
  </div>
</div>
```

**SASS:**
```sass
.grid {

  @include flexbox-grid((
    item-selector: '#{&}__item',
    columns: 1,
    gutter-vertical: 10px
  ));

  @media (min-width: 500px) {
    @include flexbox-grid((
      item-align: 'center',
      columns: 2,
      gutter-horizontal: 15px,
      gutter-vertical: 15px
    ));
  }

  @media (min-width: 1000px) {
    @include flexbox-grid((
      item-selector: '.grid__item',
      item-align: 'left',
      columns: 4,
      gutter-horizontal: 25px,
      gutter-vertical: 25px
    ));
  }

}
```

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

#### Version 1.0.0
* Initial creation.