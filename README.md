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
  5. Able to set auto (equal) column width using `--span` value of `0`.
  6. Able to shrink-wrap the column using `--span` value of `-1`.
  7. Removed the ability fixed column size to simplify codebase, set the content width and shrink-wrap the column instead.

Limitations:

  1. It does not support multiline rows, this is a conscious decision to avoid using negative margin.
  2. There exists 2 variants with negative margin and flex-gap, both support multiline rows. They will be released when I have tweaked the codebase to my satisfaction.

In Development:

  1. Add vertical grid similar to Foundation
  2. Custom property name tweaks

For a demo, see my website at www.miragecraft.com
