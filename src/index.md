---
title: Sass workflow for UIkit
description: A Sass workflow for UIkit with Eleventy and LiquidJS
layout: base
---
Use Eleventy 2.0.1, UIkit 3.16.26 and Sass 1.64.2 to automatically build CSS files from the SCSS framework. Then, serve Eleventy and refresh the browser to see the modifications.

[Live example](https://getuikit.com/assets/uikit/tests/index.html)

## How to build

- UIkit makes use of the SCSS syntax.
- import three SCSS files from UIkit in the correct order into in your own SCSS code.

Example:
```
// 1. Your custom variables and variable overwrites.
$global-link-color: #DA7D02;

// 2. Import default variables and available mixins.
@import "variables-theme.scss";
@import "mixins-theme.scss";

// 3. Your custom mixin overwrites.
@mixin hook-card() { color: #000; }

// 4. Import UIkit.
@import "uikit-theme.scss";
```
### Note

- The example uses the styling of the included default theme.
- Alternatively, you can import variables.scss, mixins.scss and uikit.scss to only include the core styling.

## Create a UIkit theme