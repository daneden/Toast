# Toast Framework
The Toast framework is a grid. That's it. Soon, it might have type styles and whatnot, but it's power is in its highly customisable design.

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

`$grid-namespace` and `$grid-column-namespace` adjusts the class names for the grid. With default values, grid wrappers have a class of `.grid` and columns `.grid__col`.

`$col-groups(n)` adjusts column divisions. For example, `$col-groups(12)` will produce a 12-column grid. `$col-groups(3,6,8)` will produce a 3-, 6-, and 8-column grid.

`$gutter-width` is—you guessed it—the gutter
width. Accepts any unit.

That’s it. Have fun.
