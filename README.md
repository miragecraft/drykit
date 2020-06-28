# RazorGrid
Ultralight weight, zero dependency CSS grid.

I created this grid system for my own use - my priority is to be able to hand code HTML/CSS without dealing with preprocessors and being able to use aribitary number of "columns" (in quotes because no actual column is used since this is based on Flexbox) without having to re-compile CSS.

At the same time, it lets me utilize different number of grid columns for different pages of a website, without having to redefine the grid template for each page (thus, utilizing Flexbox).

Currently includes 3 files:
- razorgrid.css - full featured
- razorgrid - gap and order.css - utilizing "gap" support for Flexbox, add support for reordering columns, waiting for full support
- razorgrid - base.css - shows underlying logic without extra custom properties for media query, helps to understand how the grid works

For a demo, see my website at www.miragecraft.com


