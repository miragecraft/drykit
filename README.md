# RazorGrid
Ultra lightweight CSS framework.

No pre/post-processor, no dependences. Plug and play just like the old days.

Key Features:

  - Minimal markup and configuration
  - Flexbox grid with arbitrary column width (3/7, 4/11, 5/13...) in any combination
  - Column auto-collapse
  - Semantic CSS custom properties with smart responsive prefixes
  - Real margin-based gutters (instead of padding gutters)
  - Container query
  - Zero code and toolchain dependencies

I started this framework for my own use - my priority is to be able to hand code HTML/CSS without dealing with pre- and post-processors and being able to use aribitary number of columns with easy to define responsive behaviors.

[Try Demo](http://www.miragecraft.com/projects/razorgrid.html)

**V3 Released**

_Gap Edition: requires Flexbox gap support, but removes negative margins._

Breaking Change:

  - `<i-row>` is changed to class of `.grid-x`, this lets you turn semantic elements such as `<main>`, `<nav>`, `<ul>`, `<dl>` etc. into grids. `<i-col>` is obsolete as style is assigned using child selector.
  - Changed media query prefix for small (and up) from `--s-property` to `--property`, to follow convention and make property assignment more intuitive when responsiveness is not required.
  - Removed large only `--lo-property` prefix as it's redundant.
  - `--gutter` and `--v-gutter` for grid gap is now changed to `--gap`, `--gap-x` and `--gap-y` to align name with native CSS property name. 

Detailed Functionalities:

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
  - Responsive pre-fixes includes:
      - Small (no prefix), Small Only `--so-property`, Medium `--m-propety`, Medium Only `--mo-property` and Large `--l-property`.
      - Default breakpoints are set at Medium (640px and up) and Large (1024px and up)
  - Special custom properties for:
      - `--order` and `--v-order` (vertical order) let cells change order when collapsed
  - Set grid gap (gutters) using `--gap`, `--gap-x` and `--gap-y`
  - Container Query using `--breakpoint` (don't forget to disable auto-collapse using `.lock`)
      - `.backfold` tells Container Query to reverse order of children when collapsed
  - Automatic sticky footer by adding `.stretch` to `.grid-y` under `<body>`
  - 100% height for grid when not collapsed using `.elastic`
  - Overlay one cell over the parent grid (takes it out of the document flow) using `.overlay`
  - Better default font sizes for headings.

Limitations:

  - Grid container has negative top and left margin, Flexbox gap support is required to remove them but browser support is limited.
  - Vertical `.grid-y` doesn't support multiline, due to a Flexbox quirk that adds phantom whitespace. [Problem Demonstration](https://codepen.io/Miragecraft/pen/RwRgeqw)

In Development for version 4:

  - Sub-grid support that enables pre-set values for margin, padding and font sizes.
