# RazorGrid
Ultralight weight, zero dependency CSS grid.

I created this grid system for my own use - my priority is to be able to hand code HTML/CSS without dealing with preprocessors and being able to use aribitary number of "columns" (in quotes because no actual column is used since this is based on Flexbox) without having to re-compile CSS.

At the same time, it lets me utilize different number of grid columns for different pages of a website, without having to redefine the grid template for each page (thus, utilizing Flexbox).

For responsiveness, it is NOT mobile first, but rather mobile last and utilizes 2 breakpoints.

  1. Fold - nested columns collapse into rows
  2. Stack - all columns collapse into rows

That's it.

Currently includes 3 files:

- razorgrid.css
  - *most compatible version*
- razorgrid - gap and order.css
  - *utilizing "gap" support for Flexbox, enables reordering, not yet fully supported by latest browsers*
- razorgrid - base.css
  - *shows underlying logic, makes it easier to understand how the grid works*

For a demo, see my website at www.miragecraft.com
