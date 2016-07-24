# Bagel Grid
It's designed to be a incredibly easy to use fully customizable mobile-first grid.

Change anything you want to, the number of columns, the gutter size or unit, or even change the names of the classes themselves. Edit the variables in `_bagel.scss` to make it happen.

## Quick-start guide

It's intended to be mobile first. A column without a prefix will be treated the same no matter how big or small.
```
<div class="col col--1-of-4">
  A half column on a small screen size
</div>
```

If you want the column to be treated differently at different screen widths just include different classes to represent them.
```
<div class="col col--1-of-2 col--m-1-of-4 col--m-2-of-12">
  A half column in a small screen size,
  a quarter column in a medium screen size,
  and two twelfths in a large screen size
</div>
```

## Customizing

`$bagel-grid-namespace`, `$bagel-grid-column-namespace`, and `$bagel-wrapper-namespace` adjusts the class names for the grid. With default values, grid wrappers have a class of `.grid`, columns `.col`, and the wrapper `.bagel_wrapper`.

The `.bagel_wrapper` is my solution to maintaining a consistent page width for different devices. Changing the breakpoint changes not only which column classes take affect but also which wrapper size is used. You can choose to change everything about the wrapper or if the wrapper is included at all!

`$bagel-small-custom-grid`,  `$bagel-medium-custom-grid`, and `$bagel-large-custom-grid` allow you to choose whether or not you want the only the default grid sizes or if you also want custom grids for those sizes as well.
###### note: By default, the sizes included are 1, 2, 3, and 4
`$bagel-col-groups(n)` adjusts column divisions. For example, `$bagel-col-groups(12)` will produce a 12-column grid. `$toast-col-groups(3,6,8)` will produce a 3-, 6-, and 8-column grid for all the grid sizes you've enabled on the previous lines.
###### note: As of now you can only choose whether or not custom grids are enabled at different screen sizes. You cannot have different custom grids for different sizes.

`$bagel-gutter-width` is just that. It'll accept any unit.
###### note: if you choose to use percentage and intend to use the push and pulls make sure to have `$bagel-gutter-using-percent` true.

`$bagel-breakpoint-medium` and `$toast-breakpoint-small` are breakpoint placeholders. Columns and the bagel wrapper have hooks to change their behavior under these breakpoints.

## Extras

Bagel has some extra modifiers to make different kinds of layouts easier. Most of them are borrowed completely from the Toast Framework and aren't fully functional yet.
###### note: the push and pull for % gutter units seems fully functional at this time.

That just about does it. Enjoy!
