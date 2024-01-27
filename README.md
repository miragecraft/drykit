# DryKit
Hyper-opinionated, no-build vanilla CSS framework.

Key Features:

  - No dependency and no build steps
  - Superpowered Flexbox and Grid
  - Easy column collapse based on parent or child width (simplified container query)
  - Typography tools with `@scope` emulation as well as spacing and indentation automation
  - Linear spacing scale and modular type scale
  - Per-property responsiveness based on the space toggle technique
  - Utilizes the latest CSS features available in mainline browsers - Firefox, Chrome/Edge and Safari
 
**Documentation**

Code is self-documentating, I do plan to create more detailed documentation and examples to showcase its power once the codebase has stablized.

Here's a simple explanation of each file:

 - **_import.css** - single file to import, you can also compile all the CSS files together and minify it however since this is meant for personal sites I'd rather keep the files separated and formatted for easy editing/development.
 - **dryflight.css** - an adaptation of Tailwind's preflight.css for normalization, can swap to other resets/normalize.
 - **dryflight-extra.css** - my own normalization/baseline styles with scales for spacing and text, kept separate to make upgrading/swapping out **dryflight.css** trivial.
 - **layout.css** - smart Flexbox and Grid with pseudo container query
 - **prose.css** - typography helps and logic, with `@scope` emulation
 - **prose-simple.css** - optional feature to automatically remove `.prose` style from children with id or class
 - **media.css** - Space toggle based media query

**Philosophy**

This is an extremely personal and opinionated framework, it deviates from accepted best practice and values ergonomics over performance, such as using CSS `@import`.

It harkens back to the era of CSS Zen Garden, and imagines what would a framework look like if developers back then had all the latest CSS features available to them.
