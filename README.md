# RazorGrid
Ultralight weight, zero dependency CSS grid.

I created this grid system for my own use - my priority is to be able to hand code HTML/CSS without dealing with preprocessors and being able to use aribitary number of "columns" (in quotes because no actual column is used since this is based on Flexbox) without having to re-compile CSS.

At the same time, it lets me utilize different number of grid columns for different pages of a website, without having to redefine the grid template for each page (thus, utilizing Flexbox).

**v2 released, still being tweaked**

V2 have several improvements:

  1. Refactored media query to use common conventions, column width defined using `--span` with small `--s-span`, medium `--m-span` and large `--l-span` prefixes with each affecting all larger sizes.
  2. Also includes small only `--so-span`, medium only `--mo-span` and large only `--lo-span` (only needed if you need to add more page sizes such as extra large `--x-span`) prefixes.
  3. Ability to set horizontal and vertical column order using `--order` and `--v-order`
  4. Much easier to stack all columns just by setting `--prefix-span` to 1 on the row instead of setting flex-direction to column and manually removing gutters and offsets.
  5. Removed the ability to set fixed column size to simplify codebase, set the content width and shrink-wrap the column instead.

Features:

  - Set width and offset in fractions using `--prefix-span` and `--prefix-offset`: 1/2, 2/3, 4/7 etc.
  - Set auto-width (equal width) by setting the span to `0`.
  - Shrink-wrap column (content width) by setting the span to `-1`.
  - Collapse columns by setting the span to `1` on the row.
  - Prevent columns collpasing by adding `lock` attribute to the row.

Limitations:

  - There is no negative margin to worry about, however it does not support mutiline rows.
  - Due to lack of negative margin, styling doesn't work correctly if you moving first child back, can only move other children forward by setting `--order` or `--v-order` to `-1`.
  - There exists 2 variants with negative margin and flex-gap, both support multiline rows. They will be released when I have tweaked the codebase to my satisfaction.

In Development:

  - Add vertical grid similar to Foundation
  - Custom property name tweaks

For a demo, see my website at www.miragecraft.com
