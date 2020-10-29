# RazorGrid
Ultralight weight, zero dependency CSS grid.

I created this grid system for my own use - my priority is to be able to hand code HTML/CSS without dealing with preprocessors and being able to use aribitary number of "columns" (in quotes because no actual column is used since this is based on Flexbox) without having to re-compile CSS.

At the same time, it lets me utilize different number of grid columns for different pages of a website, without having to redefine the grid template for each page (thus, utilizing Flexbox).

[Try Demo](http://www.miragecraft.com/projects/razorgrid.html)

**V3 Released**

_Gap Edition: requires Flexbox gap support, but removes negative margins._

Breaking Change:

  - `<i-row>` is changed to class of `.grid-x`, this lets you turn semantic elements such as `<main>`, `<nav>`, `<ul>`, `<dl>` etc. into grids. `<i-col>` is obsolete as style is assigned using child selector.
  - Changed media query prefix for small (and up) from `--s-property` to `--property`, to follow convention and make property assignment more intuitive when responsiveness is not required.
  - Removed large only `--lo-property` prefix as it's redundant.
  - `--gutter` and `--v-gutter` for grid gap is now changed to `--gap`, `--gap-x` and `--gap-y` to align name with native CSS property name. 

Features:

  - Multiline support for `.grid-x`.
  - Vertical grid via `.grid-y`.
  - Auto-collapsing `.grid-x` at small size, nested `.grid-x` at medium size
  - Set width and offset in fractions using `--prefix-span` and `--prefix-offset`: 1/2, 2/3, 4/7 etc. You can apply this at either the grid level or cell level.
  - Set auto-width (equal width) by setting the span to `0`.
  - Shrink-wrap column (content width) by setting the span to `-1`.
  - Collapse columns by setting the span to `1` on parent `.grid-x`.
  - Prevent columns from auto collapsing by adding `.lock` class to parent `.grid-x`.
  - Responsive CSS custom properties for:
      - `--span` (grid cell span)
      - `--offset` (grid cell offset)
      - `--display` (used for hiding content)
      - `--align` (text-align)
      - `--size` (font-size)
      - `--align-x` and `--align-y` (aligning grid cell to track)
      - `--align-grid` (aligning grid tracks to container)
  - Special custom properties for:
      - `--order` and `--v-order` (vertical order) let cells change order when collapsed
  - Container Query using `--breakpoint` (don't forget to disable auto-collapse using `.lock`)
      - `.backfold` tells Container Query to reverse order of children when collapsed
  - Automatic sticky footer by adding `.stretch` to `.grid-y` under `<body>`
  - 100% height for grid when not collapsed using `.elastic`
  - Overlay one cell over the parent grid (takes it out of the document flow) using `.overlay`
  

Limitations:

  - Grid container has negative top and left margin, Flexbox gap support is required to remove them but browser support is limited.
  - Vertical `.grid-y` doesn't support multiline, due to a Flexbox quirk that adds phantom whitespace. [Problem Demonstration](https://codepen.io/Miragecraft/pen/RwRgeqw)

In Development for version 4:

  - Sub-grid support that enables pre-set values for margin, padding and font sizes.
