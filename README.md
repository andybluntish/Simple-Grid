# Simple Grids

A simple, responsive, fluid grid implementation.

Browser Support is limited to IE9+, and modern browsers, since it relies on `box-sizing: border-box` ([http://paulirish.com/2012/box-sizing-border-box-ftw/](http://paulirish.com/2012/box-sizing-border-box-ftw/)) and `nth-of-type`.

## Grid types

Simple Grids comes in two forms, Column and Block. By default, both grid types are based on a 12-column layout, but this can be changed by overriding the `$simple-grids-columns` variable.

### Column Grids

#### Markup

Column grids are made up of rows and columns. Each column has one or more classes to specify the number of "grid units" the column will take up at the specified break point. For each row, these should add up to the total number of columns (default is 12).

For example, a two-column layout that is applied on medium sized screens:

    <div class="col-grid-row">
      <div class="col-grid-md-6">50%</div>
      <div class="col-grid-md-6">50%</div>
    </div>


### Block Grids

#### Markup

Block grids are based on simple HTML lists (`ul` and `ol`). Each grid has one or more classes to specify the number of columns to display at the specified break point (**note:** this is the _inverse_ of how sizes are specified for the Column Grid).

For example, a two-column layout that is applied on medium sized screens:

    <ul class="block-grid-md-2">
      <li>50%</li>
      <li>50%</li>
    </ul>

Block grids are ideal for creating a grid from items that are already marked up in a list.


### Compact Grids

By default, both Column and Block grids contain padding in each cell. This value can be updated by globally overriding the SASS variables. Alternatively, you can add the `.compact` class to the `.col-grid-row` or `.block-grid-*` elements to remove all padding in child cells.


## Media Queries

Grid classes exist for the following break points. Breakpoint values can be overridden using SASS variables.

  * `xs` is applied on screens > 0em (`.col-grid-xs-1`, `.block-grid-xs-2`)
  * `sm` is applied on screens > 30em (`.col-grid-sm-1`, `.block-grid-sm-2`)
  * `md` is applied on screens > 40em (`.col-grid-md-1`, `.block-grid-md-2`)
  * `lg` is applied on screens > 48em (`.col-grid-lg-1`, `.block-grid-lg-2`)


## Example

Check out an example on [CodePen](http://codepen.io/andybluntish/pen/RNzyZM/right/?editors=010).
