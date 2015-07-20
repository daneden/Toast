# Toast Framework
The Toast framework is a grid. That's it. Soon, it might have type styles and whatnot, but its power is in its highly customisable design.

Set any number of columns, any gutter size you want, and whatever classes you need. Just edit the `_grid.scss` file’s variables to your needs.

You should also know that you’d be insane to use Toast’s grid.

To learn more, go to http://daneden.github.io/Toast

## Quick-start guide

Using Toast is easy. First, link to grid.css in your HTML document's head:

```<link rel="stylesheet" href="css/toast/grid.css">```

Then, to use the grid, you'll need a wrap (provided in your own CSS) and a `.grid` container.

```html
<div class="container">
  <div class="grid">
        <div class="grid__col grid__col--1-of-4">

        </div>
        <div class="grid__col grid__col--3-of-4">

        </div>
        <div class="grid__col grid__col--6-of-12">

        </div>
  </div>
</div>
```

## Customising

`$toast-grid-namespace` and `$toast-grid-column-namespace` adjusts the class names for the grid. With default values, grid wrappers have a class of `.grid` and columns `.grid__col`.

`$toast-col-groups(n)` adjusts column divisions. For example, `$toast-col-groups(12)` will produce a 12-column grid. `$toast-col-groups(3,6,8)` will produce a 3-, 6-, and 8-column grid.

`$toast-gutter-width` is—you guessed it—the gutter
width. Accepts any unit.

`$toast-breakpoint-medium` and `$toast-breakpoint-small` are breakpoint placeholders. Columns have hooks to change their behaviour under these breakpoints. See the “Modifiers” section below.

## Modifiers

Toast has some modifiers to make different kinds of layouts easier. There are breakpoint hooks to have columns behave differently than their default behaviour under breakpoints:

```html
<div class="grid">
  <div class="grid__col--1-of-3 grid__col--m-1-of-2 grid__col--s-1-of-2 grid__col">
    This column will behave like a 1-of-2 column under the medium breakpoint and the small breakpoint.
  </div>

  <div class="grid__col--1-of-3 grid__col--ab grid__col">
    This column aligns to the bottom of its row.
  </div>

  <div class="grid__col--1-of-3 grid__col--am grid__col">
    This column aligns to the middle of its row.
  </div>

  <div class="grid__col--3-of-5 grid__col--centered grid__col">
    This column is centered and alone in its row.
  </div>

  <div class="grid__col--1-of-2 grid__col--d-last grid__col">
    This column comes first in the DOM, but appears last in its row.
  </div>

  <div class="grid__col--1-of-2 grid__col--d-first grid__col">
    This column appears last in the DOM, but appears first in its row.
  </div>
</div>
```

That’s it. Have fun.
