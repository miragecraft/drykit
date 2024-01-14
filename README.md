# DryKit
Ultra lightweight CSS framework.

No pre/post-processors, no dependences. Plug and play just like the old days.

**Previously name RazorGrid, completely rebuilt and expanded.**

Key Features:

  - No dependency and no build steps.
  - Pure CSS based solution.
  - Ultra lightweight (after minification)
  - Smart Flexbox - pseudo-grid with arbitrary column width (3/7, 4/11, 5/13...) in any combination
  - Smart CSS Grid - shortcuts for common layouts and patterns
  - Pseudo container query - trivially easy column collapse based on parent or child width
  - Typography - `@scope` emulation via `.prose` and `.not-prose`
  - Scales - linear for spacing, modular for text 
  - Per-property responsiveness based on the space toggle technique. 

I started this framework for my own use - my priority is to be able to hand code HTML/CSS without dealing with any build tools while taking full advantage of modern CSS features.

Browser Support: latest browsers with CSS Nesting and `:has()` selector support.

**Alpha software**

Currently DryKit is alpha software, I consider it mostly feature complete and is currently using it to redesign my own website and working out the wrinkles.

Breaking change from RazorGrid: pretty much everything, as the previous framework is just a grid system which has now been rebuilt from scratch.
 
**Documentation**

Code is self-documentating, I do plan to create more detailed documentation and examples to showcase its power once the codebase has stablized.

Here's a simple explanation of each file:

 - **_import.css** - single file to import, you can also compile all the CSS files together and minify it however since this is meant for personal sites I'd rather keep the files separated and formatted for easy editing/development.
 - **dryflight.css** - an adaptation of Tailwind's preflight.css for normalization, can swap to other resets/normalize.
 - **dryflight-extra.css** - my own normalization/baseline styles with custom scales for spacing and text, kept separate to make upgrading/swapping out **dryflight.css** trivial.
 - **layout.css** - smart Flexbox and Grid with pseudo container query
 - **prose.css** - typography helps and logic, with `@scope` emulation
 - **prose-simple.css** - optional feature to automatically remove `.prose` style from children with id or class
 - **media.css** - Space toggle based media query

**Philosophy**

This is an extremely personal and opinionated framework, I make use of techniques/methods not considered good practice such as CSS `@import` and other "ugly hacks".

This is in keeping with the entire contrarian/oldschool mentality of the framework, as having no build step is almost considered archiac at this point, but permits development via the browser dev console and lowers the bar of entry for amature webmasters.

You have been warned.
