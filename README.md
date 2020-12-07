CSS-Coding-Standards
====================

Cascading Style Sheets (CSS) is a stylesheet language used to describe the presentation of a document written in HTML or XML (including XML dialects such as SVG, MathML or XHTML). CSS describes how elements should be rendered on screen, on paper, in speech, or on other media.

CSS is among the core languages of the open web and is standardized across Web browsers according to W3C specifications. Previously, development of various parts of CSS specification was done synchronously, which allowed versioning of the latest recommendations. You might have heard about CSS1, CSS2.1, CSS3. However, CSS4 has never become an official version.

From CSS3, the scope of the specification increased significantly and the progress on different CSS modules started to differ so much, that it became more effective to develop and release recommendations separately per module. Instead of versioning the CSS specification, W3C now periodically takes a snapshot of the latest stable state of the CSS specification.


Personal coding standards for crafting CSS

This is a living document. My goal is to update this as my knowledge evolves and promote more consistency in my own code.


## Guidelines
* Prefer one global stylesheet. ex. `style.css`
* Avoid using IDs for styling. IDs are great for anchor links and JS hooks, but avoid using them as styling hooks. [Source](http://oli.jp/2011/ids/)
* Include a link at the top of the stylesheet back to these coding standards.
* If you are minifing your CSS, include a link at the top to view the unminified CSS. `style.max.css` [Source](http://daneden.me/2012/07/max-css-in-depth/)
* Prefix all javascript-based selectors, (IDs, Classes) with `js-`. [Source](https://github.com/styleguide/javascript)
* Never reference `js-` prefixed class names from CSS files. `js-` base classes are to be used exclusively in JS files. [Source](https://github.com/styleguide/css)
* Use the `is-` prefix for state rules that are shared between CSS and JS.
* Avoid qualifying class names with type selectors. `Prefer .nav {...} instead of ul.nav {...}`


## Formatting CSS

* Prefer soft-tabs with 2 space indent.
* Add a single space before the opening bracket `{` in rule sets.
* Separate selectors and declarations by new lines. (multi-lined)
* Order your CSS rules alphabetically.
* Put prefixed rules before the unprefixed rules.
* Line up prefixed declarations so values are in line vertically.
* Add a space between properties and values after the colon. `display: block`
* Include a semi-colon after every declaration, including the last declaration.
* Use quotes when needed in selctors or values, prefer double quotes. `input[type="checkbox"]`
* Prefer shorthand hex values for colors. `background-color: #fff;`
* Use lowercase format for property and value names.
* When using zero based values, leave the value unitless. `margin: 0;`
* Omit leading “0”s in values. `font-size: .8em;`
* Place closing bracket of declaration block on its own line.
* Add one blank line bewteen rule sets.
