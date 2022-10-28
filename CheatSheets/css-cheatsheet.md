---
title: CSS CheatSheet
description: The most commonly used css properties and attributes are given here.
created: 2022-10-20
---

## Table of Contents

- [CSS CheatSheet for Developers](#css-cheatsheet-for-developers)
  - [CSS Properties](#css-properties)
  - [CSS Selectors](#css-selectors)
  - [CSS Pseudo Classes](#css-pseudo-classes)
  - [CSS Attribute Selectors](#css-attribute-selectors)

# CSS CheatSheet for Developers

## CSS Properties

*Syntax*: **`property-name : value;`**

**Some common values to all properties**: `inherit / initial / revert / revert-layer / unset`

| Property Name | Description | Values (Separated by /) |
| ------------- | ----------- | ----------------------- |
| `align-content` | Aligns a flex container's lines within the flex container when there is extra space in the cross-axis | `flex-start / flex-end / center / space-between / space-around / space-evenly / stretch / start / end / baseline / first baseline / last baseline / safe center / unsafe center` |
| `align-items` | Aligns flex items of the current line the same way as justify-content | `flex-start / flex-end / center / baseline / stretch` |
| `align-self` | Aligns flex items of the current line the same way as justify-content | `auto / flex-start / flex-end / center / baseline / stretch` |
| `all` | Sets all the properties | `initial / inherit / unset` |
| `animation` | A shorthand property for all the animation-* properties | Syntax: `animation-name animation-duration animation-timing-function animation-delay animation-iteration-count animation-direction animation-fill-mode animation-play-state` |
| `animation-delay` | Defines when the animation will start | `time / %` |
| `animation-direction` | Defines whether the animation should play in reverse on alternate cycles | `normal / reverse / alternate / alternate-reverse` |
| `animation-duration` | Defines how long an animation should take to complete one cycle | `time / %` |
| `animation-fill-mode` | Defines a style for the target element when the animation is not playing (when it is finished, or when it has a delay) | `none / forwards / backwards / both` |
| `animation-iteration-count` | Defines the number of times an animation should be played | `number / infinite` |
| `animation-name` | Specifies a name for the @keyframes animation | `none / keyframes-name` |
| `animation-play-state` | Defines whether the animation is running or paused | `running / paused` |
| `animation-timing-function` | Defines the speed curve of the animation | `ease / linear / ease-in / ease-out / ease-in-out / cubic-bezier(n,n,n,n)` |
| `backface-visibility` | Defines whether or not the back face of an element should be visible when facing the user | `visible / hidden` |
| `background` | A shorthand property for all the background-* properties | Syntax `background-color background-image background-position background-size background-repeat background-origin background-clip background-attachment background-blend-mode` |
| `background-attachment` | Sets whether a background image scrolls with the rest of the page, or is fixed | `scroll / fixed / local` |
| `background-blend-mode` | Specifies the blending mode of each background layer (color/image) | `normal / multiply / screen / overlay / darken / lighten / color-dodge / saturation / color / luminosity` |
| `background-clip` | Specifies how far the background (color or image) should extend within an element | `border-box / padding-box / content-box` |
| `background-color` | Sets the background color of an element | `color` |
| `background-image` | Sets one or more background images for an element | `url(image-path) / none` |
| `background-origin` | Specifies the origin position of a background image | `padding-box / border-box / content-box` |
| `background-position` | Sets the starting position of a background image | `top left / top center / top right / center left / center center / center right / bottom left / bottom center / bottom right / x-axis y-axis / x-axis / y-axis` |
| `background-repeat` | The way the background image is repeated | `repeat / repeat-x / repeaty / no-repeat ` |
| `background-size` | Background image size | `length / percentage / auto / cover / contain` |
| `border` | Sets all border properties in one line | Syntax: `top right bottom left` / `top-bottom left-right` / `all-at-once` |
| `border-bottom`| Bottom border properties in one line | Syntax: `width style color` |
| `border-bottom-color`| Color of the bottom | `color (RGB, HEX, name) / transparent` |
| `border-bottom-left-radius` | Border bottom left radius | `length / percentage` |
| `border-bottom-right-radius` | Border bottom right radius | `length / percentage` |
| `border-bottom-style` | Border bottom style | `none / hidden / dotted / dashed / solid / double / groove / ridge / inset / outset` |
| `border-bottom-width` | Border bottom width | `length / percentage` |
| `border-collapse` | Collapses the borders between table cells | `collapse / separate` |
| `border-color` | Sets all border color properties in one line | Syntax: `top right bottom left` / `top-bottom left-right` / `all-at-once` |
| `border-image` | Shorthand property for border-image-* | Syntax: `source slice width outset repeat` |
| `border-image-outset` | Outset of the border image | `length / number` |
| `border-image-repeat` | How the border image is repeated | `stretch / repeat / round` |
| `border-image-slice` | Slices the border image | `number / percentage` |
| `border-image-source` | Source of the border image | `url (path to image) / none` |
| `border-image-width` | Width of the border image | `length / percentage / number` |
| `border-left` | Left border properties in one line | Syntax: `width style color` |
| `border-left-color` | Color of the left border | `color (RGB, HEX, name) / transparent` |
| `border-left-style` | Style of the left border | `none / hidden / dotted / dashed / solid / double / groove / ridge / inset / outset` |
| `border-left-width` | Width of the left border | `length / percentage` |
| `border-radius` | Sets all border radius properties in one line | Syntax: `top-left top-right bottom-right bottom-left` / `top-bottom left-right` / `all-at-once` |
| `border-right` | Right border properties in one line | Syntax: `width style color` |
| `border-right-color` | Color of the right border | `color (RGB, HEX, name) / transparent` |
| `border-right-style` | Style of the right border | `none / hidden / dotted / dashed / solid / double / groove / ridge / inset / outset` |
| `border-right-width` | Width of the right border | `length / percentage` |
| `border-spacing` | Spacing between the cells | `length / percentage` |
| `border-style` | Sets all border style properties in one line | Syntax: `top right bottom left` / `top-bottom left-right` / `all-at-once` |
| `border-top` | Top border properties in one line | Syntax: `width style color` |
| `border-top-color` | Color of the top border | `color (RGB, HEX, name) / transparent` |
| `border-top-left-radius` | Border top left radius | `length / percentage` |
| `border-top-right-radius` | Border top right radius | `length / percentage` |
| `border-top-style` | Style of the top border | `none / hidden / dotted / dashed / solid / double / groove / ridge / inset / outset` |
| `border-top-width` | Width of the top border | `length / percentage` |
| `border-width` | Sets all border width properties in one line | Syntax: `top right bottom left` / `top-bottom left-right` / `all-at-once` |
| `bottom` | Distance from the bottom of the element | `length / percentage / auto` |
| `box-shadow` | Adds shadow to the box | Syntax: `h-offset v-offset blur spread color inset` |
| `box-sizing` | Defines how the width and height of the element are calculated | `content-box / border-box` |
| `caption-side` | Position of the table caption | `top / bottom` |
| `caret-color` | Color of the caret | `color (RGB, HEX, name) / auto` |
| `clear` | Specifies on which sides of an element floating elements are not allowed | `none / left / right / both` |
| `clip` | Clipping region | `rect (top right bottom left) / auto` |
| `color` | Text color | `color (RGB, HEX, name) / transparent` |
| `column-count` | Number of columns | `number / auto` |
| `column-fill` | How to fill columns | `balance / auto` |
| `column-gap` | Gap between the columns | `length / percentage` |
| `column-rule` | Sets all column rule properties in one line | Syntax: `width style color` |
| `column-rule-color` | Color of the column rule | `color (RGB, HEX, name) / transparent` |
| `column-rule-style` | Style of the column rule | `none / hidden / dotted / dashed / solid / double / groove / ridge / inset / outset` |
| `column-rule-width` | Width of the column rule | `length / percentage` |
| `column-span` | How many columns an element should span across | `none / all` |
| `column-width` | Width of the columns | `length / percentage` |
| `columns` | Sets all column properties in one line | Syntax: `column-width column-count` |
| `content` | Used with the ::before and ::after pseudo-elements, to insert generated content | `string / url (path to image) / none` |
| `counter-increment` | Increases or decreases the value of one or more CSS counters | `counter-name value` |
| `counter-reset` | Resets one or more CSS counters | `counter-name value` |
| `cursor` | Specifies the mouse cursor to be displayed when pointing over an element | `auto / default / none / context-menu / help / pointer / progress / wait / cell / crosshair / text / vertical-text / alias / copy / move / no-drop / not-allowed / e-resize / n-resize / ne-resize / nw-resize / s-resize / se-resize / sw-resize / w-resize / ew-resize / ns-resize / nesw-resize / nwse-resize / col-resize / row-resize / all-scroll / zoom-in / zoom-out / grab / grabbing` |
| `direction` | Specifies the text direction/writing direction | `ltr / rtl` |
| `display` | Specifies how a certain HTML element should be displayed | `none / inline / block / inline-block / list-item / run-in / compact / marker / table / inline-table / table-row-group / table-header-group / table-footer-group / table-row / table-column-group / table-column / table-cell / table-caption / ruby / ruby-base / ruby-text / ruby-base-container / ruby-text-container / contents / flow / flow-root / table / flex / inline-flex / grid / inline-grid / ruby-base-group / ruby-text-group` |
| `empty-cells` | Specifies whether or not to display borders and background on empty cells in a table | `show / hide` |
| `filter` | Defines effects (e.g. blurring or color shifting) on an element before the element is displayed | `none / url (path to SVG filter) / blur (length) / brightness (percentage) / contrast (percentage) / drop-shadow (h-offset v-offset blur spread color) / grayscale (percentage) / hue-rotate (angle) / invert (percentage) / opacity (percentage) / saturate (percentage) / sepia (percentage)` |
| `flex` | Sets all flex properties in one line | Syntax: `flex-grow flex-shrink flex-basis` |
| `flex-basis` | Specifies the initial length of a flexible item | `length / auto` |
| `flex-direction` | Specifies the direction of the flexible items | `row / row-reverse / column / column-reverse` |
| `flex-flow` | Sets all flex flow properties in one line | Syntax: `flex-direction flex-wrap` |
| `flex-grow` | Specifies how much the item will grow relative to the rest | `number` |
| `flex-shrink` | Specifies how the item will shrink relative to the rest | `number` |
| `flex-wrap` | Specifies whether the flexible items should wrap or not | `nowrap / wrap / wrap-reverse` |
| `float` | Specifies whether or not a box should float | `left / right / none` |
| `font` | Sets all font properties in one line | Syntax: `font-style font-variant font-weight font-size/line-height font-family` |
| `font-family` | Specifies the font family for text | `font-name / generic-family` |
| `font-feature-settings` | Controls advanced typographic features in OpenType fonts | `normal / string` |
| `font-kerning` | Controls the usage of the kerning information | `auto / normal / none` |
| `font-language-override` | Controls the usage of language-specific glyphs in a typeface | `normal / string` |
| `font-size` | Specifies the font size of text | `length / percentage / xx-small / x-small / small / medium / large / x-large / xx-large / smaller / larger` |
| `font-size-adjust` | Preserves the readability of text when font fallback occurs | `none / number` |
| `font-stretch` | Selects a normal, condensed, or expanded face from a font family | `normal / ultra-condensed / extra-condensed / condensed / semi-condensed / semi-expanded / expanded / extra-expanded / ultra-expanded` |
| `font-style` | Specifies the font style for text | `normal / italic / oblique` |
| `font-synthesis` | Controls which missing typefaces (bold or italic) may be synthesized by the browser | `none / weight / style / weight style` |
| `font-variant` | Specifies whether or not a text should be displayed in a small-caps font | `normal / small-caps / all-small-caps / petite-caps / all-petite-caps / unicase / titling-caps` |
| `font-variant-alternates` | Controls the usage of alternate glyphs associated to alternative names defined in @font-feature-values | `normal / string` |
| `font-variant-caps` | Controls the usage of alternate glyphs for capital letters | `normal / small-caps / all-small-caps / petite-caps / all-petite-caps / unicase / titling-caps` |
| `font-variant-east-asian` | Controls the usage of alternate glyphs for East Asian scripts | `normal / string` |
| `font-variant-ligatures` | Controls which ligatures and contextual forms are used in textual content of the elements it applies to | `normal / none / string` |
| `font-variant-numeric` | Controls the usage of alternate glyphs for numbers, fractions, and ordinal markers | `normal / ordinal / slashed-zero / lining-nums / oldstyle-nums / proportional-nums / tabular-nums / diagonal-fractions / stacked-fractions` |
| `font-variant-position` | Controls the usage of alternate glyphs of smaller size positioned as superscript or subscript regarding the baseline of the font | `normal / sub / super` |
| `font-weight` | Specifies the weight of a font | `normal / bold / bolder / lighter / 100 / 200 / 300 / 400 / 500 / 600 / 700 / 800 / 900` |
| `grid` | Sets all grid properties in one line | Syntax: `grid-template-rows grid-template-columns grid-template-areas grid-auto-rows grid-auto-columns grid-auto-flow grid-column-gap grid-row-gap` |
| `grid-area` | Specifies a name for the grid item | `grid-row-start / grid-column-start / grid-row-end / grid-column-end` |
| `grid-auto-columns` | Specifies the size of an implicitly-created column track | `length / percentage / auto` |
| `grid-auto-flow` | Specifies how auto-placed items are inserted in the grid | `row / column / row dense / column dense` |
| `grid-auto-rows` | Specifies the size of an implicitly-created row track | `length / percentage / auto` |
| `grid-column` | Specifies a grid item's size and location within the grid column by referring to specific grid lines | `grid-column-start / grid-column-end` |
| `grid-column-end` | Specifies where to end the grid item | `grid-column-line` |
| `grid-column-gap` | Specifies the size of the gap between columns | `length / percentage` |
| `grid-column-start` | Specifies where to start the grid item | `grid-column-line` |
| `grid-gap` | Sets the gap between the rows and columns | Syntax: `grid-row-gap grid-column-gap` |
| `grid-row` | Specifies a grid item's size and location within the grid row by referring to specific grid lines | `grid-row-start / grid-row-end` |
| `grid-row-end` | Specifies where to end the grid item | `grid-row-line` |
| `grid-row-gap` | Specifies the size of the gap between rows | `length / percentage` |
| `grid-row-start` | Specifies where to start the grid item | `grid-row-line` |
| `grid-template` | Sets all grid template properties in one line | Syntax: `grid-template-rows grid-template-columns grid-template-areas` |
| `grid-template-areas` | Specifies how to display columns and rows, using named grid items | `none / string` |
| `grid-template-columns` | Specifies the size of the columns, and how many columns in a grid layout | `none / track-list` |
| `grid-template-rows` | Specifies the size of the rows in a grid layout | `none / track-list` |
| `height` | Sets the height of an element | `length / percentage / auto` |
| `hyphens` | Specifies how to split words to improve the layout of paragraphs | `none / manual / auto` |
| `image-orientation` | Specifies the orientation of an image | `angle / from-image` |
| `image-rendering` | Gives a hint to the browser about what aspects of an image are most important to preserve when the image is scaled | `auto / optimizeSpeed / optimizeQuality` |
| `image-resolution` | Specifies the intended resolution for a raster image | `from-image / resolution` |
| `ime-mode` | Specifies the state of the Input Method Editor for text fields | `auto / normal / active / inactive / disabled` |
| `initial-letter` | Specifies the styling of dropped, raised, and sunken initial letters | `normal / number / length / percentage` |
| `initial-letter-align` | Specifies the alignment of an initial letter | `auto / alphabetic / hanging / ideographic / mathematical` |
| `initial-letter-wrap` | Specifies whether the initial letter may be wrapped to the next line | `normal / first / all` |
| `inline-size` | Sets the width or height of an inline box, depending on the value of the writing-mode property | `length / percentage / auto` |
| `justify-content` | Specifies the alignment between the items inside a flexible container when the items do not use all available space | `flex-start / flex-end / center / space-between / space-around / space-evenly / start / end / left / right` |
| `justify-items` | Specifies the alignment for items inside a flexible container | `auto / normal / stretch / start / end / center / self-start / self-end / left / right / baseline / first baseline / last baseline / safe center / unsafe center` |
| `justify-self` | Specifies the alignment for selected items inside a flexible container | `auto / normal / stretch / start / end / center / self-start / self-end / left / right / baseline / first baseline / last baseline / safe center / unsafe center` |
| `left` | Specifies the left position of a positioned element | `length / percentage / auto` |
| `letter-spacing` | Increases or decreases the space between characters in a text | `normal / length` |
| `line-break` | Specifies how/if to break lines | `auto / loose / normal / strict / anywhere` |
| `line-height` | Specifies the line height | `normal / number / length / percentage` |
| `list-style` | Sets all the properties for a list in one declaration | Syntax: `list-style-type list-style-position list-style-image` |
| `list-style-image` | Specifies an image as the list-item marker | `none / url` |
| `list-style-position` | Specifies the position of the list-item markers (bullet points) | `inside / outside` |
| `list-style-type` | Specifies the type of list-item marker | `none / disc / circle / square / decimal / decimal-leading-zero / lower-roman / upper-roman / lower-greek / lower-latin / upper-latin / armenian / georgian / lower-alpha / upper-alpha / hebrew / cjk-ideographic / hiragana / hiragana-iroha / katakana / katakana-iroha` |
| `margin` | Sets all the margin properties in one declaration | Syntax: `margin-top margin-right margin-bottom margin-left` |
| `margin-block-end` | Sets the margin at the bottom of an element | `length / percentage / auto` |
| `margin-block-start` | Sets the margin at the top of an element | `length / percentage / auto` |
| `margin-bottom` | Sets the bottom margin of an element | `length / percentage / auto` |
| `margin-inline-end` | Sets the margin on the right side of an element | `length / percentage / auto` |
| `margin-inline-start` | Sets the margin on the left side of an element | `length / percentage / auto` |
| `margin-left` | Sets the left margin of an element | `length / percentage / auto` |
| `margin-right` | Sets the right margin of an element | `length / percentage / auto` |
| `margin-top` | Sets the top margin of an element | `length / percentage / auto` |
| `max-height` | Sets the maximum height of an element | `length / percentage / none` |
| `max-inline-size` | Sets the maximum width or height of an inline box, depending on the value of the writing-mode property | `length / percentage / none` |
| `max-width` | Sets the maximum width of an element | `length / percentage / none` |
| `min-block-size` | Sets the minimum height or width of an element, depending on the value of the writing-mode property | `length / percentage` |
| `min-height` | Sets the minimum height of an element | `length / percentage` |
| `min-inline-size` | Sets the minimum width or height of an element, depending on the value of the writing-mode property | `length / percentage` |
| `min-width` | Sets the minimum width of an element | `length / percentage` |
| `mix-blend-mode` | Specifies how an element's content should blend with its direct parent background | `normal / multiply / screen / overlay / darken / lighten / color-dodge / saturation / color / luminosity` |
| `object-fit` | Specifies how the contents of a replaced element should be fitted to the box established by its used height and width | `fill / contain / cover / none / scale-down` |
| `object-position` | Specifies the alignment of the replaced element inside its box | `x-axis y-axis / x-axis / y-axis / center` |
| `offset` | Sets all the offset properties in one declaration | Syntax: `offset-path offset-distance offset-rotate offset-anchor` |
| `offset-anchor` | Specifies the position of the origin of an element's offset | `auto / x-axis y-axis / x-axis / y-axis / center` |
| `offset-distance` | Specifies the distance between the origin of an element's offset and its offset path | `length / percentage / auto` |
| `offset-path` | Specifies the path the element should follow | `none / path() / <basic-shape> / <geometry-box>` |
| `offset-position` | Sets all the offset-position properties in one declaration | Syntax: `offset-path offset-distance offset-rotate` |
| `offset-rotate` | Specifies how an element should be rotated along the offset path | `auto / angle / reverse` |
| `opacity` | Sets the opacity level for an element | `number` |
| `order` | Specifies the order of the flexible item, relative to the rest | `integer` |
| `orphans` | Specifies the minimum number of lines that must be left at the bottom of a page when a page break occurs inside an element | `integer` |
| `outline` | Sets all the outline properties in one declaration | Syntax: `outline-width outline-style outline-color` |
| `outline-color` | Sets the color of an outline | `color` |
| `outline-offset` | Offsets an outline, and draws it beyond the border edge | `length` |
| `outline-style` | Sets the style of an outline | `none / hidden / dotted / dashed / solid / double / groove / ridge / inset / outset` |
| `outline-width` | Sets the width of an outline | `thin / medium / thick / length` |
| `overflow` | Specifies what happens if content overflows an element's box | `visible / hidden / scroll / auto / overlay / clip` |
| `overflow-wrap` | Specifies whether or not the browser may break lines within words in order to prevent overflow (when a string is too long to fit its containing box) | `normal / break-word / anywhere` |
| `overflow-x` | Specifies whether or not to clip the left/right edges of the content, if it overflows the element's content area | `visible / hidden / scroll / auto / overlay / clip` |
| `overflow-y` | Specifies whether or not to clip the top/bottom edges of the content, if it overflows the element's content area | `visible / hidden / scroll / auto / overlay / clip` |
| `padding` | Sets all the padding properties in one declaration | Syntax: `padding-top padding-right padding-bottom padding-left` |
| `padding-block-end` | Sets the padding at the bottom of an element | `length / percentage` |
| `padding-block-start` | Sets the padding at the top of an element | `length / percentage` |
| `padding-bottom` | Sets the bottom padding of an element | `length / percentage` |
| `padding-inline-end` | Sets the padding on the right side of an element | `length / percentage` |
| `padding-inline-start` | Sets the padding on the left side of an element | `length / percentage` |
| `padding-left` | Sets the left padding of an element | `length / percentage` |
| `padding-right` | Sets the right padding of an element | `length / percentage` |
| `padding-top` | Sets the top padding of an element | `length / percentage` |
| `page-break-after` | Specifies the page-breaking behavior after an element | `auto / always / avoid / left / right` |
| `page-break-before` | Specifies the page-breaking behavior before an element | `auto / always / avoid / left / right` |
| `page-break-inside` | Specifies the page-breaking behavior inside an element | `auto / avoid` |
| `perspective` | Gives a 3D-positioned element some perspective | `none / length` |
| `perspective-origin` | Defines at which position the user is looking at the 3D-positioned element | `x-axis y-axis / x-axis / y-axis / center` |
| `place-content` | Sets the align-content and justify-content properties in one declaration | Syntax: `align-content justify-content` |
| `place-items` | Sets the align-items and justify-items properties in one declaration | Syntax: `align-items justify-items` |
| `place-self` | Sets the align-self and justify-self properties in one declaration | Syntax: `align-self justify-self` |
| `pointer-events` | Defines whether or not an element reacts to pointer events | `auto / none / visiblePainted / visibleFill / visibleStroke / visible / painted / fill / stroke / all` |
| `position` | Specifies the type of positioning method used for an element (static, relative, absolute or fixed) | `static / relative / absolute / fixed / sticky` |
| `quotes` | Specifies how quotation marks should look | `none / string string string string` |
| `resize` | Specifies whether or not an element is resizable by the user | `none / both / horizontal / vertical / block / inline` |
| `right` | Specifies the right position of a positioned element | `length / percentage / auto` |
| `row-gap` | Sets the size of the gap between an element's grid rows | `length / percentage` |
| `scroll-behavior` | Specifies whether to smoothly animate the scroll position in a scrollable box, instead of a straight jump | `auto / smooth` |
| `tab-size` | Specifies the width of a tab character | `number / length` |
| `table-layout` | Specifies the algorithm used to lay out table cells, rows, and columns | `auto / fixed` |
| `text-align` | Specifies the horizontal alignment of text | `left / right / center / justify / justify-all / start / end / match-parent` |
| `text-align-last` | Specifies the alignment of the last line of a block element | `auto / left / right / center / justify / start / end` |
| `text-combine-upright` | Specifies how to combine multiple characters into the space of a single character | `none / all / digits` |
| `text-decoration` | Sets all the text-decoration properties in one declaration | Syntax: `text-decoration-line text-decoration-color text-decoration-style text-decoration-thickness` |
| `text-decoration-color` | Specifies the color of the text-decoration | `color` |
| `text-decoration-line` | Specifies the type of line in a text-decoration | `none / underline / overline / line-through / blink` |
| `text-decoration-skip` | Specifies what parts of an element's content are skipped over when applying any text decoration | `none / objects / spaces / ink` |
| `text-decoration-style` | Specifies the style of the line in a text decoration | `solid / double / dotted / dashed / wavy` |
| `text-decoration-thickness` | Specifies the thickness of the line in a text decoration | `auto / from-font / length` |
| `text-indent` | Specifies the indentation of the first line in a text-block | `length / percentage` |
| `text-orientation` | Specifies the orientation of the text in a line | `mixed / upright / sideways / sideways-right / sideways-left / use-glyph-orientation` |
| `text-overflow` | Specifies what should happen when text overflows the containing element | `clip / ellipsis` |
| `text-rendering` | Gives a fine-grained control over the algorithm used to render text | `auto / optimizeSpeed / optimizeLegibility / geometricPrecision` | 
| `text-shadow` | Adds shadow to text | `none / h-shadow v-shadow blur color` |
| `text-transform` | Controls the capitalization of text | `none / capitalize / uppercase / lowercase / full-width / full-size-kana` |
| `text-underline-offset` | Specifies the position of the underline which is set using the text-decoration property | `auto / length` |
| `text-underline-position` | Specifies the position of the underline which is set using the text-decoration property | `auto / under / left / right` |
| `top` | Specifies the top position of a positioned element | `length / percentage / auto` |
| `touch-action` | Specifies whether and how a particular region can be manipulated by a user | `auto / none / pan-x / pan-left / pan-right / pan-y / pan-up / pan-down / pinch-zoom` |
| `transform` | Applies a 2D or 3D transformation to an element | `none / matrix() / matrix3d() / perspective() / rotate() / rotate3d() / rotateX() / rotateY() / rotateZ() / scale() / scale3d() / scaleX() / scaleY() / scaleZ() / skew() / skewX() / skewY() / translate() / translate3d() / translateX() / translateY() / translateZ()` |
| `transform-box` | Defines the box to which the transform-origin property applies | `border-box / fill-box / view-box` |
| `transform-origin` | Allows you to change the position on transformed elements | `x-axis y-axis z-axis / x-axis y-axis / x-axis / y-axis / z-axis / left / center / right / top / bottom` |
| `transform-style` | Specifies how nested elements are rendered in 3D space | `flat / preserve-3d` |
| `transition` | A shorthand property for all the transition-* properties | Syntax: `transition-property transition-duration transition-timing-function transition-delay` |
| `transition-delay` | Specifies when the transition effect will start | `time` |
| `transition-duration` | Specifies how many seconds or milliseconds a transition effect takes to complete | `time` |
| `transition-property` | Specifies the name of the CSS property the transition effect is for | `none / all / property` |
| `transition-timing-function` | Specifies the speed curve of the transition effect | `ease / ease-in / ease-out / ease-in-out / linear / step-start / step-end / steps() / cubic-bezier()` |
| `unicode-bidi` | Used together with the direction property to set or return whether the text should be overridden to support multiple languages in the same document | `normal / embed / bidi-override` |
| `user-select` | Specifies whether the text of an element can be selected | `auto / none / text / all / contain` |
| `vertical-align` | Sets the vertical alignment of an element | `baseline / sub / super / top / text-top / middle / bottom / text-bottom / length / percentage` |
| `visibility` | Specifies whether or not an element is visible | `visible / hidden / collapse` |
| `white-space` | Specifies how white-space inside an element is handled | `normal / pre / nowrap / pre-wrap / pre-line / break-spaces` |
| `width` | Sets the width of an element | `length / percentage / auto` |
| `will-change` | Indicates what will change before the element is actually changed | `auto / contents / scroll-position / transform` |
| `word-break` | Specifies how words should break when reaching the end of a line | `normal / break-all / keep-all / break-word` |
| `word-spacing` | Increases or decreases the space between words in a text | `normal / length` |
| `word-wrap` | Specifies whether or not the browser may break lines within words in order to prevent overflow (when a string is too long to fit its containing box) | `normal / break-word` |
| `writing-mode` | Specifies whether lines of text are laid out horizontally or vertically and the direction which lines of text and blocks progress | `horizontal-tb / vertical-rl / vertical-lr / sideways-rl / sideways-lr` |
| `z-index` | Specifies the stack order of an element | `auto / number` |

**[🔼Back to Top](#table-of-contents)**

## CSS Selectors

| Command          | Description                         |
| ---------------- | ----------------------------------- |
| `*`              | all elements                        |
| `div`            | all 'div' tags                      |
| `div.p`          | all 'div' and 'p' paragraphs        |
| `div p`          | paragraphs inside divs              |
| `div > p`        | all 'p' tag one level deep in 'div' |
| `div + p`        | p tags immediately after div        |
| `div ~ p`        | p tags preceded by div              |
| `.class-name`    | all elements with class             |
| `#id-name`       | element with 'id'                   |
| `div.class-name` | divs with certain classname         |
| `div#id-name`    | div with certain 'id'               |
| `#id-name`       | all elements iside that #id-name    |

**[🔼Back to Top](#table-of-contents)**

## CSS Pseudo Classes

| Command                   | Description                  |
| ------------------------- | ---------------------------- |
| `a:link`                  | link in normal state         |
| `a:active`                | link in clicked state        |
| `a:hover`                 | link with mouse over it      |
| `a:visited`               | visited link                 |
| `p::after{content:"yo"/}` | add content after p          |
| `p::before`               | add content before p         |
| `input:checked`           | checked inputs               |
| `input:disabled`          | disabled inputs              |
| `input:enabled`           | enabled inputs               |
| `input:focus`             | input has focus              |
| `input:in-range`          | value in range               |
| `input:out-of-range`      | input value out of range     |
| `input:valid`             | input with valid value       |
| `input:invalid`           | input with invalid value     |
| `input:optional`          | no required attribute        |
| `input:required`          | input with requred attribute |
| `input:read-only`         | with readonly attribute      |
| `input:read-write`        | no readonly attrib.          |
| `div:empty`               | element with no children     |
| `p::first-letter`         | first letter in p            |
| `p::first-line`           | first line in p              |
| `p:first-of-type`         | first of some type           |
| `p:last-of-type`          | last of some type            |
| `p:lang(en)`              | p with en language attribute |
| `:not(span)`              | element that's not a span    |
| `p:first-child`           | first child of its parent    |
| `p:last-child`            | last child of its parent     |
| `p:nth-child(2)`          | second child of its parent   |
| `p:nth-child(3n+1)`       | nth-child (an + b) formula   |
| `p:nth-last-child(2)`     | second child from behind     |
| `p:nth-of-type(2)`        | second p of its parent       |
| `p:nth-last-of-type(2)`   | ...from behind               |
| `p:only-of-type`          | unique of its parent         |
| `p:only-child`            | only child of its parent     |
| `:root`                   | documents root element       |
| `::selection`             | portion selected by user     |
| `:target`                 | highlight active anchor      |

**[🔼Back to Top](#table-of-contents)**

## CSS Attribute Selectors

| Command                | Description                      |
| ---------------------- | -------------------------------- |
| `a[target]`            | links with a target attribute    |
| `a[target="_blank"]`   | links which open in new tab      |
| `[title~="chair"]`     | title element containing a word  |
| `[class^="chair"]`     | class starts with chair          |
| `[class="chair"]`      | class starts with the chair word |
| `[class*="chair"]`     | class contains chair             |
| `[class$="chair"]`     | class ends with chair            |
| `input[type="button"]` | specified input type             |

**[🔼Back to Top](#table-of-contents)**
