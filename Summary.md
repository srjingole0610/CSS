# CSS Summary for Revision

## Introduction

Welcome to the **CSS Summary for Revision**!
This document is a concise, revision-friendly reference to the essential CSS concepts, best practices, and code examples you need while building web projects or preparing for interviews.

Whether you're a beginner or an experienced developer, use this summary to quickly review key CSS topics, syntax, and real-world tips.

---

## Table of Contents

- [What is CSS?](#1-what-is-css)
- [Types of Stylesheets](#2-types-of-stylesheets)
- [CSS Selectors](#3-css-selectors)
- [Comments in CSS](#4-comments-in-css)
- [Colors in CSS](#5-colors-in-css)
- [Backgrounds in CSS](#6-backgrounds-in-css)
- [Units in CSS](#7-units-in-css)
- [Fonts in CSS](#8-fonts-in-css)
- [Text Properties in CSS](#9-text-properties-in-css)
- [Box Model in CSS](#10-box-model-in-css)
- [Gradients in CSS](#11-gradients-in-css)
- [Box Shadow in CSS](#12-box-shadow-in-css)
- [drop-shadow Filter in CSS](#13-drop-shadow-filter-in-css)
- [CSS Filters](#14-css-filters)
- [CSS Lists](#15-css-lists)
- [CSS Display Property](#16-css-display-property)
- [CSS Anchor States (Links)](#17-css-anchor-states-links)
- [CSS Position Property](#18-css-position-property)
- [z-index in CSS](#19-z-index-in-css)
- [Overflow in CSS](#20-overflow-in-css)
- [Pseudo-Elements in CSS](#21-pseudo-elements-in-css)
- [CSS Pseudo-Classes](#22-css-pseudo-classes)
- [CSS Multi-Column Layout](#23-css-multi-column-layout)
- [CSS Flexbox](#24-css-flexbox)
- [CSS Grid](#25-css-grid)
- [CSS Transitions](#26-css-transitions)
- [CSS Transform](#27-css-transform)
- [CSS Animations](#28-css-animations)
- [CSS Variables](#29-css-variables)
- [CSS Specificity](#30-css-specificity)
- [CSS Float](#31-css-float)
- [CSS Media Queries](#32-css-media-queries)
- [CSS Container Queries](#33-css-container-queries)

---

## 1. What is CSS?

**CSS (Cascading Style Sheets)** is a style sheet language used to define the presentation and layout of HTML documents. It separates content (HTML) from design, enabling consistent styling across multiple web pages.

### 🔑 Key Concepts:
-
 **Separation of Concerns:** Structure (HTML) vs. Style (CSS)
- **Cascading Nature:** Multiple rules can apply to an element; the most specific one takes effect.
- **Inheritance:** Certain properties (e.g., `color`, `font-family`) pass from parent to child elements.


### ✅ Example:
```html
<!-- index.html -->
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="style.css">
<
/head>
<body>
  <h1>Hello, CSS!</h1>
</body>
</html>
```

```css

/* style.css */
h1 {
  color: teal;
 
 font-family: Arial, sans-serif;
}
```

---

## 2. Types of Stylesheets


CSS can be applied in three primary ways:

|
 Type        | Description | Use Case |
|-------------|-------------|----------|
| **Inline**   | Defined inside an element's `style` attribute | For quick testing or overriding |
| **Internal** | Placed within `<style>` in the HTML `<head>` | For single-page documents |
| **External** | Linked via `<link>` to a `.css` file | Recommended for maintainability and reuse |

#
## ✅ Example:
```html
<!-- Inline -->
<
p style="color: red;">This is inline styled</p>

<!-- Internal -->
<head>
  <style>
 
   p { color: blue; }
  </style>
</head>

<!-- External -->
<
head>
  <link rel="stylesheet" href="styles.css">
</head>
```

---

## 3. CSS Selectors

*
*Selectors** determine which HTML elements to style.

### 🎯 Common Selectors:
- `element` – Targets all specific elements (e.g., `p {}`)
-
 `.class` – Targets elements with a specific class
- `#id` – Targets a unique element by its ID
- `[attribute]` – Targets elements by attribute
- `:pseudo-class` – Styles elements in a specific state
-
 `::pseudo-element` – Styles a part of an element (e.g., `::first-line`)

### 🔢 Specificity (Priority Order):
`Inline Styles > #ID > .Class / [Attr] / :Pseudo-class > Element / ::Pseudo-element`


### ✅ Example:
```css
p { color: navy; }
.highlight { background: yellow; }
#main { border: 1px solid #333; }
i
nput[type="text"] { border-radius: 4px; }
a:hover { color: orange; }
```

---


## 4. Comments in CSS

C
omments help document your styles. They're ignored by browsers.

```css
/* This is a single-line comment */


/* Layout Styles */
.container {
  max-width: 1200px;
  margin: 0 auto;
}
`
``

---

## 5. Colors in CSS


CSS provides several ways to define color:

| Format     | Example                |
|------------|------------------------|
|
 Named      | `red`, `blue`          |
| Hex        | `#ff0000`, `#333`      |
| RGB        | `rgb(255, 0, 0)`       |
| RGBA       | `rgba(255, 0, 0, 0.5)` |
| HSL/HSLA   | `hsl(0, 100%, 50%)`    |


### 👀 Accessibility Tip:
Ensure **sufficient contrast** between foreground and background colors for better readability.

#
## ✅ Example:
```css
body {
  background-color: #f0f0f0;
  color: #222;
}

.button {
  background: linear-gradient(90deg, #3498db, #8e44ad);
  color: white;
}
```


---

}

.float-column {
    float: left;
    width: 30%;
    margin-right: 5%;
    padding: 15px;
    box-sizing: border-box;
    background-color: #f8f9fa;
    border-radius: var(--border-radius);
    min-height: 150px;
}

.float-column:last-child {
    margin-right: 0;
}

/* Interactive Playground */
.interactive-playground {
    background-color: white;
    border-radius: var(--border-radius);
    box-shadow: var(--box-shadow);
    padding: 25px;
    margin-bottom: 30px;
}

.controls {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-bottom: 20px;
}

.control-btn {
    background-color: var(--primary-color);
    color: white;
    border: none;
    padding: 8px 15px;
    border-radius: var(--border-radius);
    cursor: pointer;
    transition: var(--transition);
}

.control-btn:hover {
    background-color: var(--primary-color-hover);
}

.playground-container {
    background-color: #f8f9fa;
    border-radius: var(--border-radius);
    padding: 20px;
    margin-top: 20px;
}

.playground-box {
    overflow: hidden;
    margin-bottom: 20px;
    min-height: 200px;
}

.playground-item {
    width: 150px;
    height: 100px;
    background-color: var(--primary-color);
    color: white;
    text-align: center;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: var(--border-radius);
    transition: var(--transition);
}

.playground-text {
    margin-top: 10px;
}

.current-styles {
    margin-top: 20px;
}

/* Responsive Adjustments */
@media (max-width: 768px) {
    .float-column {
        float: none;
        width: 100%;
        margin-right: 0;
        margin-bottom: 20px;
    }
    
    .controls {
        flex-direction: column;
    }
    
    .back-button {
        position: static;
        display: inline-block;
        margin-bottom: 15px;
        transform: none;
    }
    
    .page-header {
        padding-top: 15px;
    }
}

## 6. Backgrounds in CSS

Control how an element's background appears using these properties:

### 📌 Properties:
- `background-color`
- `background-image`
- `background-repeat`
- `background-position`
- `background-size`
- `background-attachment`

### 💡 Shorthand:
```css
background: url('hero.jpg') no-repeat center/cover;
```

### ✅ Example:
```css
.hero {
  background: url('images/hero.jpg') no-repeat center/cover;
  color: white;
  padding: 60px 20px;
}

.card {
  background-color: #fff;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}
```

---

## 7. Units in CSS

CSS uses units to define sizes, spacing, and other length-related properties.

### 📏 Absolute Units:
- `px` – pixels
- `pt`, `cm`, `mm`, `in` – rarely used in screen design

### 📐 Relative Units:
- `%` – relative to parent
- `em` – relative to the font-size of the element
- `rem` – relative to the root (`html`) font-size
- `vw` – 1% of viewport width
- `vh` – 1% of viewport height

### 🔧 Best Practices:
- Prefer **relative units** (`rem`, `%`, `vw/vh`) for responsive design.
- Use `rem` for fonts to maintain scalability.

### ✅ Example:
```css
.container {
  width: 80vw;
  padding: 2rem;
}

.text-large {
  font-size: 2em;
}
```

---

## 8. Fonts in CSS

CSS provides powerful tools to control typography, which is essential for readability, branding, and user experience.

### Font Properties:
- **font-family:** Specifies the typeface. Always provide fallback fonts and end with a generic family (e.g., serif, sans-serif).
- **font-size:** Sets the size of the text. Use relative units (em, rem, %) for accessibility and responsiveness.
- **font-weight:** Controls the thickness of the text. Values: normal, bold, or numeric (100–900).
- **font-style:** Used for italic or oblique text.
- **font-variant:** Enables typographic features like small-caps.
- **@font-face:** Allows you to use custom fonts by specifying a font file.

### Fallback Fonts:
Always list multiple fonts in font-family to ensure text remains readable if a preferred font fails to load.

### Example:
```css
body {
  font-family: 'Segoe UI', Arial, sans-serif;
}
h1 {
  font-size: 2.5rem;
  font-weight: bold;
}
.italic {
  font-style: italic;
}
.small-caps {
  font-variant: small-caps;
}
@font-face {
  font-family: 'MyFont';
  src: url('MyFont.woff2') format('woff2');
}
.custom-font {
  font-family: 'MyFont', sans-serif;
}
```

### Best Practices:
- Use web-safe fonts or host custom fonts with @font-face.
- Prefer relative units for font-size.
- Always provide fallbacks in font-family.
- Use font-weight and font-style for emphasis and hierarchy.

---

## 9. Text Properties in CSS

CSS text properties allow you to control the appearance, alignment, spacing, and effects of text content. Mastery of these properties is essential for creating visually appealing and readable web pages.

### Text Alignment (`text-align`)
Controls horizontal alignment of text within its container. Values: `left`, `right`, `center`, `justify`.

```css
.text-center { text-align: center; }
.text-justify { text-align: justify; }
```

### Text Decoration (`text-decoration`)
Adds lines to text: `underline`, `overline`, `line-through`, or `none`. Can combine multiple values.

```css
.underline { text-decoration: underline; }
.line-through { text-decoration: line-through; }
```

### Text Transform (`text-transform`)
Controls capitalization: `uppercase`, `lowercase`, `capitalize`, or `none`.

```css
.uppercase { text-transform: uppercase; }
.capitalize { text-transform: capitalize; }
```

### Letter Spacing (`letter-spacing`)
Adjusts space between characters. Useful for headings or stylistic effects.

```css
.letter-spacing-wide { letter-spacing: 0.2em; }
```

### Word Spacing (`word-spacing`)
Adjusts space between words. Can improve readability or create stylistic effects.

```css
.word-spacing-wide { word-spacing: 1.5em; }
```

### Line Height (`line-height`)
Controls vertical space between lines of text. Use unitless values for best scalability.

```css
.line-height-loose { line-height: 2; }
```

### Text Shadow (`text-shadow`)
Adds shadow to text for emphasis or stylistic effect. Syntax: `text-shadow: offset-x offset-y blur color;`

```css
.text-shadow-basic { text-shadow: 2px 2px 4px #888; }
.text-shadow-color { text-shadow: 1px 1px 6px #3498db; }
```

### Best Practices
- Use text properties to improve readability and visual hierarchy.
- Combine properties for creative effects (e.g., uppercase + letter-spacing for headings).
- Avoid excessive decoration or shadow for body text.

---

## 10. Box Model in CSS

The CSS Box Model is fundamental to understanding layout and spacing in web design. Every element is a rectangular box made up of content, padding, border, and margin.

### Box Model Structure
- **Content:** The actual text, image, or media inside the box.
- **Padding:** Space between the content and the border.
- **Border:** The line surrounding the padding and content.
- **Margin:** Space outside the border, separating the element from others.

### Borders
Borders can be customized with `border-width`, `border-style`, `border-color`, and `border-radius`. The `border` shorthand sets all at once.

```css
.box-demo {
  border: 4px solid #3498db;
  border-radius: 8px;
}
```

### Padding
Padding is the space between the content and the border. Set each side individually or use the `padding` shorthand.

```css
.padding-demo {
  padding-top: 30px;
  padding-right: 10px;
  padding-bottom: 5px;
  padding-left: 40px;
}
.padding-shorthand {
  padding: 10px 30px;
}
```

### Margin
Margin is the space outside the border. You can set each side, use `auto` for centering, negative values, and the `margin` shorthand. Vertical margins between block elements may collapse.

```css
.margin-auto {
  margin: 0 auto;
}
.negative-margin {
  margin-top: -20px;
}
```

### Content Area & Sizing
The content area is sized with `width` and `height`. The `box-sizing` property determines if padding and border are included in the element's total width and height.
- `content-box` (default): width/height apply to content only.
- `border-box`: width/height include padding and border.

```css
.content-box-demo {
  box-sizing: content-box;
}
.border-box-demo {
  box-sizing: border-box;
}
```

### Best Practices
- Use `box-sizing: border-box` for easier layout control.
- Use shorthand properties for cleaner code.
- Visualize the box model using browser DevTools.

---

## 11. Gradients in CSS

CSS gradients allow you to create smooth transitions between two or more colors, without using images. Gradients are resolution-independent, highly customizable, and can be used for backgrounds, buttons, borders, overlays, and more.

### Types of Gradients
- **Linear Gradient:** Colors transition along a straight line. You can set the angle or direction and as many color stops as you want.
- **Radial Gradient:** Colors radiate outward from a center point in a circle or ellipse.
- **Conic Gradient:** Colors sweep around a center point, like a pie chart.
- **Repeating Gradients:** Any gradient type can be repeated to create patterns.
- **Multiple Gradients:** You can layer gradients for complex effects.
- **Angle & Color Stops:** Control the direction and exact position of each color.

### Example:
```css
.linear-gradient-demo {
  background: linear-gradient(90deg, #3498db, #8e44ad);
}
.radial-gradient-demo {
  background: radial-gradient(circle at 60% 40%, #f7971e, #ffd200 70%, #f7971e 100%);
}
.conic-gradient-demo {
  background: conic-gradient(from 45deg, #f7971e, #ffd200, #f7971e, #8e44ad);
}
.repeating-gradient-demo {
  background: repeating-linear-gradient(45deg, #3498db, #3498db 10px, #fff 10px, #fff 20px);
}
.multiple-gradient-demo {
  background:
    linear-gradient(135deg, #8e44ad 40%, transparent 60%),
    radial-gradient(circle at 80% 20%, #ffd200 20%, transparent 60%),
    linear-gradient(90deg, #3498db, #8e44ad);
}
.angle-gradient-demo {
  background: linear-gradient(120deg, #3498db 10%, #fff 50%, #8e44ad 90%);
}
```

### Browser Compatibility
CSS gradients are supported in all modern browsers (Chrome, Firefox, Edge, Safari, Opera). However, very old browsers (such as Internet Explorer 9 and below) may require vendor prefixes (e.g., `-webkit-`, `-moz-`) or may not support certain gradient types like conic gradients. For best results, test your gradients and consider using prefixes if you need to support legacy browsers.

### Best Practices
- Use gradients to add depth, highlight, or visual interest.
- Combine gradients with transparency for overlays.
- Use multiple gradients for creative backgrounds.
- Test gradients on different devices for color consistency.

---

## 12. Box Shadow in CSS

The <strong>box-shadow</strong> property in CSS adds shadow effects around an element's frame, creating depth and visual emphasis. It is highly customizable, allowing for multiple shadows, different colors, blur, spread, and even inner (inset) shadows.

### Syntax
```css
box-shadow: h-offset v-offset blur spread color [inset];
```
- <strong>h-offset</strong>: Horizontal shadow position (required)
- <strong>v-offset</strong>: Vertical shadow position (required)
- <strong>blur</strong>: Blur radius (optional)
- <strong>spread</strong>: Size of the shadow (optional)
- <strong>color</strong>: Shadow color (optional)
- <strong>inset</strong>: Makes the shadow appear inside the element (optional)

You can add <strong>multiple shadows</strong> by separating them with commas. Shadows are rendered front-to-back (first is on top).

### Examples
```css
.basic-shadow {
  box-shadow: 4px 4px 12px #888;
}
.colored-shadow {
  box-shadow: 0 8px 24px 0 rgba(52, 152, 219, 0.4);
}
.inset-shadow {
  box-shadow: inset 0 2px 8px 0 #8e44ad;
}
.multiple-shadow {
  box-shadow: 2px 2px 8px #3498db, 0 0 0 4px #fff, 0 8px 24px 0 rgba(52,152,219,0.2);
}
.interactive-shadow:hover {
  box-shadow: 0 8px 32px 0 #f7971e, 0 0 0 4px #ffd200;
}
```

### Best Practices
- Use <strong>box-shadow</strong> to add depth, focus, or highlight important UI elements.
- Avoid excessive or harsh shadows for a clean, modern look.
- Use <strong>rgba()</strong> for subtle, semi-transparent shadows.
- Combine with <strong>border-radius</strong> for soft, card-like effects.
- Test shadows on different backgrounds for contrast.

### Browser Compatibility
- <strong>box-shadow</strong> is supported in all modern browsers (Chrome, Firefox, Edge, Safari, Opera).
- For very old browsers (IE9 and below), vendor prefixes (<code>-webkit-</code>, <code>-moz-</code>) may be needed, but are rarely required today.

---

## 13. drop-shadow Filter in CSS

The **drop-shadow()** filter in CSS applies a shadow effect to the rendered shape of an element, including its transparency (alpha channel). Unlike `box-shadow`, which is applied to the element's rectangular box, `drop-shadow()` follows the visible shape, making it ideal for images with transparency, SVGs, and icons.

### Syntax

```
filter: drop-shadow(h-offset v-offset blur color);
```
- **h-offset**: Horizontal shadow position (required)
- **v-offset**: Vertical shadow position (required)
- **blur**: Blur radius (optional, default: 0)
- **color**: Shadow color (optional, default: black)

### Key Differences from box-shadow
- `drop-shadow()` works on the rendered shape (including transparency), not just the box.
- Used via the `filter` property, not as a standalone property.
- Multiple `drop-shadow()` filters can be chained for layered effects.
- Great for PNGs, SVGs, icons, and non-rectangular images.

### Examples
```css
.basic-drop-shadow {
  filter: drop-shadow(4px 4px 8px #888);
}
.colored-drop-shadow {
  filter: drop-shadow(0 8px 16px #8e44ad);
}
.multiple-drop-shadow {
  filter: drop-shadow(2px 2px 4px #3498db) drop-shadow(-2px -2px 4px #ffd200);
}
.interactive-drop-shadow:hover {
  filter: drop-shadow(0 8px 24px #f7971e) drop-shadow(0 0 8px #ffd200);
}
.transparent-drop-shadow {
  filter: drop-shadow(0 8px 16px #3498db);
}
```

### Best Practices
- Use `drop-shadow()` for images, SVGs, and icons with transparency.
- For UI elements like cards or buttons, prefer `box-shadow`.
- Chain multiple drop-shadows for creative effects.
- Test on different backgrounds for best results.

### Browser Compatibility
- Supported in all modern browsers (Chrome, Firefox, Edge, Safari, Opera).
- Not supported in Internet Explorer.

---

## 14. CSS Filters

CSS **filters** are functions that visually modify the rendering of an element, such as images, backgrounds, or even text. Filters can be used to blur, adjust brightness, change colors, and more—directly in the browser, without editing the source image.

### Common Filter Functions
- **grayscale()**: Converts the image to grayscale.
- **blur()**: Applies a Gaussian blur.
- **brightness()**: Adjusts the brightness.
- **contrast()**: Adjusts the contrast.
- **saturate()**: Increases or decreases color intensity.
- **hue-rotate()**: Rotates the color hue.
- **invert()**: Inverts the colors.
- **opacity()**: Adjusts the transparency.
- **sepia()**: Applies a warm, brownish tone.

### Syntax
```css
filter: grayscale(100%) blur(4px) brightness(1.2) contrast(120%) saturate(150%) hue-rotate(90deg) invert(1) opacity(0.5) sepia(100%);
```
- Multiple filters can be chained together.

### Examples
```css
.grayscale-demo { filter: grayscale(100%); }
.blur-demo { filter: blur(4px); }
.brightness-demo { filter: brightness(1.5); }
.contrast-demo { filter: contrast(200%); }
.saturate-demo { filter: saturate(300%); }
.hue-rotate-demo { filter: hue-rotate(120deg); }
.invert-demo { filter: invert(1); }
.opacity-demo { filter: opacity(0.5); }
.sepia-demo { filter: sepia(100%); }
.combined-demo { filter: grayscale(60%) blur(2px) brightness(1.2) contrast(120%) hue-rotate(60deg); }
```

### Best Practices
- Use filters for creative effects, image manipulation, and UI polish.
- Combine filters for advanced effects.
- Use transitions for smooth filter changes on hover/focus.
- Test filters on different backgrounds and devices.

### Browser Compatibility
- Supported in all modern browsers (Chrome, Firefox, Edge, Safari, Opera).
- Not supported in Internet Explorer.

---

## 15. CSS Lists

CSS provides several properties to control the appearance of HTML lists, including the marker type, position, and even custom images. These properties help you create visually appealing navigation menus, checklists, and more.

### List Properties
- **list-style-type**: Sets the marker type (e.g., disc, circle, square, decimal, lower-alpha, upper-roman, etc.).
- **list-style-position**: Sets whether the marker is inside or outside the list item's content box.
- **list-style-image**: Uses a custom image as the marker.
- **list-style**: Shorthand for all three properties.

### Syntax
```css
ul {
  list-style-type: disc;
  list-style-position: outside;
  list-style-image: none;
}

ol {
  list-style-type: decimal;
}

ul.custom {
  list-style: square inside url('star.png');
}
```

### Examples
```css
ul.disc-list { list-style-type: disc; }
ul.square-list { list-style-type: square; }
ul.circle-list { list-style-type: circle; }
ol.lower-alpha-list { list-style-type: lower-alpha; }
ul.inside-list { list-style-position: inside; }
ul.outside-list { list-style-position: outside; }
ul.image-list { list-style-image: url('https://img.icons8.com/color/32/super-mario.png'); }
ul.shorthand-list { list-style: square inside url('https://img.icons8.com/color/32/super-mario.png'); }
```

### Best Practices
- Use `list-style-type` for simple marker changes.
- Use `list-style-image` for branding or custom icons, but provide a fallback.
- Use `list-style-position: inside` for checklists or when you want the marker to be part of the content flow.
- Use the `list-style` shorthand for concise code.
- Test list styles for accessibility and readability.

### Browser Compatibility
- All list properties are supported in all modern browsers (Chrome, Firefox, Edge, Safari, Opera).
- Custom images may not display if the URL is incorrect or the image is missing.

---

## 16. CSS Display Property

The `display` property in CSS is fundamental for controlling how elements are rendered and participate in the document layout. It determines whether an element behaves as a block, inline, inline-block, or is removed from the flow entirely.

### Common Display Values

- **block**: The element starts on a new line and stretches to fill the container's width. Examples: `<div>`, `<h1>`, `<p>`.
- **inline**: The element flows within the current line, only taking up as much width as its content. Examples: `<span>`, `<a>`, `<strong>`.
- **inline-block**: Like `inline`, but allows width and height to be set. Elements sit inline but behave like blocks.
- **none**: The element is not rendered at all (removed from layout and accessibility tree).

Other values include `flex`, `grid`, `table`, etc., but the above are the most common for basic layout control.

### Example:
```css
.block-demo .demo-box {
  display: block;
}
.inline-demo .demo-box {
  display: inline;
}
.inline-block-demo .demo-box {
  display: inline-block;
}
.none-demo .demo-box {
  display: none;
}
```

### Usage & Best Practices

- Use `display` to control layout and stacking of elements.
- Prefer semantic HTML elements (e.g., use `<nav>`, `<main>`, `<section>` for structure).
- Hiding elements with `display: none` removes them from both the visual flow and assistive technology.
- `inline-block` is useful for horizontal alignment with block-like control.
- Inspect the [display.html](./HTML/display.html) page for live, interactive demos and code.

### Reference
See the updated [display.html](./HTML/display.html) page for a live example of the CSS display property, theory, and interactive demos.

---

## 17. CSS Anchor States (Links)

CSS anchors (links) are styled using pseudo-classes to reflect their different states: normal, visited, hover, active, and focus. Understanding and styling these states is essential for usability, accessibility, and visual feedback.

### Anchor States

- `a:link` — Unvisited link (default state)
- `a:visited` — Link the user has already visited
- `a:hover` — Link when the mouse is over it
- `a:active` — Link when being clicked
- `a:focus` — Link when focused (e.g., via keyboard navigation)

### Example

```css
a:link {
  color: #3498db;
}
a:visited {
  color: #8e44ad;
}
a:hover, a:focus {
  color: #fff;
  background: #3498db;
  text-decoration: underline;
}
a:active {
  color: #ffd200;
}
```

### Usage & Best Practices

- Always provide a visible focus style for accessibility.
- Use `:hover` and `:focus` together for consistent mouse and keyboard experience.
- Style `:visited` to help users distinguish visited links.
- Avoid removing underline unless you provide another clear indicator.
- Anchor states can be combined with classes for custom buttons (see the back button on the [Anchor States Example Page](./HTML/anchor-state.html)).

### Reference
See the updated [anchor-state.html](./HTML/anchor-state.html) page for a live example of anchor styling and interactive navigation.

---

## 18. CSS Position Property

The <strong>position</strong> property in CSS controls how elements are placed in the document flow. It enables you to move, layer, and fix elements in place, making it essential for layouts, overlays, tooltips, sticky headers, and more.

### Position Values

- <strong>static</strong>: Default. Elements are positioned according to the normal document flow. <em>Offsets (top, right, bottom, left, z-index) have no effect.</em>
- <strong>relative</strong>: The element is positioned relative to its normal position. Offsets move it visually, but its original space is preserved.
- <strong>absolute</strong>: The element is removed from the normal flow and positioned relative to the nearest ancestor with a position other than static. If none, it uses the viewport.
- <strong>fixed</strong>: The element is removed from the flow and positioned relative to the viewport. It stays fixed when scrolling.
- <strong>sticky</strong>: The element toggles between relative and fixed, depending on the scroll position. It "sticks" to a given offset as you scroll.

### Example

```css
.static-demo .demo-box {
  position: static;
}
.relative-demo .demo-box {
  position: relative;
  left: 24px;
  top: 10px;
}
.absolute-demo {
  position: relative;
}
.absolute-demo .demo-box {
  position: absolute;
  top: 24px;
  left: 24px;
}
.fixed-demo .demo-box {
  position: fixed;
  top: 32px;
  right: 32px;
}
.sticky-demo .demo-box {
  position: sticky;
  top: 8px;
}
```

### Usage & Best Practices

- Use <code>position: relative</code> for fine-tuning layout without removing elements from the flow.
- Use <code>absolute</code> and <code>fixed</code> for overlays, tooltips, or UI elements that must float.
- <code>sticky</code> is great for headers, menus, or call-to-action boxes that should remain visible while scrolling.
- Always test on different screen sizes and with keyboard navigation.
- Avoid overusing <code>absolute</code> and <code>fixed</code> as they can break responsive layouts.

### Reference
See the updated [positions.html](./HTML/positions.html) page for a live example of the CSS position property, theory, and interactive demos.

---

## 19. z-index in CSS

The <strong>z-index</strong> property controls the vertical stacking order of positioned elements (those with <code>position: relative</code>, <code>absolute</code>, <code>fixed</code>, or <code>sticky</code>). Elements with a higher <code>z-index</code> value appear in front of those with a lower value. <code>z-index</code> only works on elements that create a stacking context.

### How z-index Works
- <strong>Default stacking:</strong> Elements are stacked in the order they appear in the HTML (later elements on top).
- <strong>z-index:</strong> Assigns a stacking level. Higher values are closer to the viewer.
- <strong>Stacking context:</strong> Created by elements with <code>position</code> (not static) and a <code>z-index</code> value, <code>opacity &lt; 1</code>, <code>transform</code>, <code>filter</code>, <code>will-change</code>, <code>mix-blend-mode</code>, etc.
- <strong>Nested stacking:</strong> Each stacking context is independent; child z-index values are relative to their parent context.

### Usage & Best Practices
- Use <code>z-index</code> to control overlays, modals, tooltips, dropdowns, and layered UI effects.
- Use the smallest values needed to avoid confusion.
- Minimize stacking contexts for easier debugging.
- Document z-index values in your codebase for maintainability.

### Example:
```css
/* Basic z-index */
.box1 { z-index: 1; }
.box2 { z-index: 2; }

/* Stacking context */
.parent {
  position: relative;
  z-index: 10;
}
.child {
  position: absolute;
  z-index: 2;
}
```

### Interactive Example
See <strong>z-index.html</strong> for interactive demos:
- Default stacking (no z-index): later elements appear on top.
- z-index stacking: higher z-index appears on top, regardless of HTML order.
- Stacking context: child z-index is relative to its parent context, not the page.

[View the interactive z-index demo page &rarr;](HTML/z-index.html)

### Browser Compatibility
- <strong>z-index</strong> is supported in all modern browsers (Chrome, Firefox, Edge, Safari, Opera).
- For best results, always use <code>position</code> (not static) with <code>z-index</code>.

---

## 20. Overflow in CSS

The **overflow** property in CSS controls what happens when content exceeds the bounds of its container. It is essential for managing scrollbars, hiding excess content, and creating scrollable areas.

### Overflow Values
- **visible** (default): Content is not clipped and may overflow outside the box.
- **hidden**: Content is clipped and the rest is invisible (no scrollbars).
- **scroll**: Content is clipped, but scrollbars are always shown (even if not needed).
- **auto**: Content is clipped, and scrollbars appear only when needed.

You can also control horizontal and vertical overflow separately with `overflow-x` and `overflow-y`.

### Usage & Best Practices
- Use `overflow: auto` for scrollbars only when needed.
- Use `overflow: hidden` to crop content, but ensure important info isn't lost.
- Combine with `max-width` or `max-height` for responsive layouts.
- Test on different devices and browsers for consistent scrollbar behavior.

### Example:
```css
.overflow-visible { overflow: visible; }
.overflow-hidden { overflow: hidden; }
.overflow-scroll { overflow: scroll; }
.overflow-auto { overflow: auto; }
.overflow-x-scroll { overflow-x: scroll; }
.overflow-y-auto { overflow-y: auto; }
```

### Interactive Example
See **overflow.html** for interactive demos:
- `overflow: visible` — content spills out of the box.
- `overflow: hidden` — overflowing content is not visible.
- `overflow: scroll` — scrollbars are always shown.
- `overflow: auto` — scrollbars appear only if content overflows.

[View the interactive overflow demo page &rarr;](HTML/overflow.html)

### Browser Compatibility
- **overflow** is supported in all modern browsers (Chrome, Firefox, Edge, Safari, Opera).
- Scrollbar appearance may vary by OS and browser.

---

## ✅ Summary Tips
- Use an **external CSS** file for scalability.
- Organize your CSS with **clear comments** and **consistent naming conventions**.
- Always test styles across devices for **responsiveness**.
- Learn and apply **Flexbox** and **Grid** for advanced layouts.
- Use tools like **DevTools** to debug and experiment.

---

## 21. Pseudo-elements in CSS

**Pseudo-elements** allow you to style specific parts of an element or insert content before or after it, without extra HTML. They are written with a double colon (`::`) (e.g., `::before`), though single colon syntax is still supported for backward compatibility.

### Common Pseudo-elements
- `::before` / `::after`: Insert content before/after the element's content.
- `::first-letter`: Style the first letter of a block element.
- `::first-line`: Style the first line of a block element.
- `::selection`: Style the portion of text selected by the user.
- `::placeholder`: Style placeholder text in form fields.
- `::marker`: Style the marker box of list items.
- `::backdrop`: Style the background of modal elements.
- `::file-selector-button`: Style the button of file input fields.
- `::cue`: Style WebVTT cues in media elements.
- `::part()`: Style shadow DOM parts (advanced).

### Structural Pseudo-classes (for reference)
- `:first-child`, `:last-child`, `:nth-child()`, `:nth-of-type()`, `:only-child`, `:empty` — Select elements based on their position or content in the DOM.

### Usage & Best Practices
- Use pseudo-elements to add icons, highlights, or effects without extra markup.
- Use `::selection` for custom highlight colors.
- Use `::placeholder` to style form hints.
- Combine with transitions for interactive effects.

### Example
```css
.button::before { content: '🚀 '; }
.button::after { content: ' →'; }
.intro::first-letter { font-size: 2rem; color: #8e44ad; }
.intro::first-line { font-weight: bold; }
p::selection { background: #ffd200; color: #222; }
input::placeholder { color: #888; font-style: italic; }
li:first-child { color: #3498db; }
li:last-child { color: #e67e22; }
li:nth-child(2) { font-weight: bold; }
li:only-child { color: #27ae60; }
li:empty { background: #f7e9ff; }
```

### Interactive Example
See **psuedo-elements.html** for interactive demos:
- `::before`/`::after` — add icons to a button.
- `::first-letter`/`::first-line` — style the first letter/line of a paragraph.
- `::selection` — custom highlight color.
- `::placeholder` — style form placeholder text.
- Structural pseudo-classes — style list items based on position/content.

[View the interactive pseudo-elements demo page &rarr;](HTML/pseudo-elements.html)

### Browser Compatibility
- Most pseudo-elements are supported in all modern browsers (Chrome, Firefox, Edge, Safari, Opera).
- Some advanced pseudo-elements (e.g., `::backdrop`, `::part()`) may have limited support.

---

## 22. CSS Pseudo-Classes

CSS **pseudo-classes** are special selectors that target elements in a specific state, such as when a user hovers over a link, when an input is focused, or when an element is the first child of its parent. Pseudo-classes enable dynamic, interactive, and context-aware styling without extra classes or JavaScript.

### Common Pseudo-Classes
- `:hover` – Styles elements when hovered by a pointer.
- `:focus` – Styles elements when focused (e.g., via keyboard/tab).
- `:active` – Styles elements when activated (e.g., clicked).
- `:first-child` – Targets the first child of a parent.
- `:last-child` – Targets the last child of a parent.
- `:nth-child(n)` – Targets the nth child (e.g., `:nth-child(2n)` for even items).
- `:only-child` – Targets an element that is the only child of its parent.
- `:empty` – Targets elements with no children (including text).
- `:not(selector)` – Excludes elements matching a selector.
- `:checked`, `:disabled`, `:required`, `:valid`, `:invalid` – Target form states.

### Example Usage
```css
/* Highlight a button on hover and focus */
.button:hover, .button:focus {
  background: #8e44ad;
  color: #fff;
}
/* Style the first and last list items */
ul li:first-child { color: #8e44ad; }
ul li:last-child { color: #3498db; }
/* Alternate row colors */
table tr:nth-child(even) { background: #f0e6fa; }
/* Only child styling */
.card:only-child { border: 2px solid #ffd200; }
/* Exclude certain items */
.menu li:not(.active) { opacity: 0.7; }
```

### Best Practices
- Always provide <code>:focus</code> styles for accessibility.
- Combine pseudo-classes for advanced effects (e.g., <code>a:hover:active</code>).
- Use <code>:not()</code> to simplify complex selectors.
- Test pseudo-class behavior across browsers and devices.

### Reference Example
See [pseudo-class.html](HTML/pseudo-class.html) for a comprehensive, interactive demo and code examples of all major CSS pseudo-classes in action.

---

---

## 23. CSS Multi-Column Layout

The **CSS multi-column layout** module allows you to flow content into multiple columns, similar to newspapers or magazines. It is useful for improving readability, making better use of horizontal space, and creating visually engaging layouts.

### Key Properties
- <code>column-count</code>: Number of columns
- <code>column-gap</code>: Space between columns
- <code>column-rule</code>: Line between columns (shorthand for style, width, color)
- <code>column-width</code>: Ideal width of each column
- <code>column-span</code>: Make an element span across all columns
- <code>columns</code>: Shorthand for <code>column-width</code> and <code>column-count</code>

### Example Usage
```css
.columns-count {
  column-count: 3;
}
.columns-gap {
  column-count: 3;
  column-gap: 2.5em;
}
.columns-rule {
  column-count: 3;
  column-rule: 3px dashed #8e44ad;
}
.columns-width {
  column-width: 180px;
}
.columns-span {
  column-count: 3;
}
.span-all {
  column-span: all;
}
.columns-shorthand {
  columns: 180px 3;
}
```

### Usage & Best Practices
- Use multi-column layout for text-heavy content to improve readability.
- Test column layouts on different screen sizes for responsiveness.
- Use <code>column-span</code> for headings or elements that should stretch across all columns.
- Be cautious with interactive elements (forms, buttons) inside columns—they may break across columns.
- Combine with other layout techniques (Flexbox, Grid) for advanced designs.

### Reference Example
See [column-layout.html](HTML/column-layout.html) for a comprehensive, interactive demo and code examples of all major CSS multi-column layout properties in action.

---

## 24. CSS Flexbox

CSS **Flexbox (Flexible Box Layout)** is a powerful layout model that makes it easy to design flexible, responsive layouts. Flexbox allows you to align, distribute, and order space among items in a container—even when their size is unknown or dynamic.

### Key Concepts
- <code>flex-container</code>: The parent element with <code>display: flex</code> or <code>display: inline-flex</code>.
- <code>flex-item</code>: The direct children of a flex container.
- <code>main axis</code>: The primary axis (horizontal by default).
- <code>cross axis</code>: The perpendicular axis (vertical by default).

### Main Properties
- <code>display: flex</code> / <code>inline-flex</code>: Defines a flex container.
- <code>flex-direction</code>: Sets the direction of the main axis (row, row-reverse, column, column-reverse).
- <code>justify-content</code>: Aligns items along the main axis.
- <code>align-items</code>: Aligns items along the cross axis.
- <code>flex-wrap</code>: Allows items to wrap onto multiple lines.
- <code>gap</code>: Sets spacing between items.
- <code>flex-grow</code>, <code>flex-shrink</code>, <code>flex-basis</code>, <code>flex</code>: Control item sizing and flexibility.
- <code>align-content</code>: Aligns lines of items in a multi-line flex container.
- <code>align-self</code>: Allows individual items to override <code>align-items</code>.
- <code>order</code>: Controls the order of items.
- <code>flex-flow</code>: Shorthand for <code>flex-direction</code> and <code>flex-wrap</code>.

### Example Usage
```css
.flex-row {
  display: flex;
  flex-direction: row;
}
.flex-column {
  display: flex;
  flex-direction: column;
}
.flex-justify {
  display: flex;
  justify-content: space-between;
}
.flex-align {
  display: flex;
  align-items: flex-end;
}
.flex-wrap-demo {
  display: flex;
  flex-wrap: wrap;
}
.flex-gap {
  display: flex;
  gap: 24px;
}
.flex-grow-demo .grow1 { flex: 1; }
.flex-grow-demo .grow2 { flex: 2; }
.flex-grow-demo .grow3 { flex: 3; }
.flex-align-self .flex-item[style] { /* Inline align-self for demo only */ }
.flex-order .order1 { order: 3; }
.flex-order .order2 { order: 1; }
.flex-order .order3 { order: 2; }
.flex-align-content {
  display: flex;
  flex-wrap: wrap;
  align-content: space-between;
  height: 180px;
}
.flex-flow-demo {
  display: flex;
  flex-flow: row wrap;
  gap: 12px;
}
```

### Usage & Best Practices
- Use Flexbox for one-dimensional layouts (row or column).
- Combine with media queries for responsive design.
- Use <code>gap</code> for spacing instead of margins.
- Test layouts on different screen sizes and browsers.
- Use semantic HTML for better accessibility and maintainability.

### Reference Example
See <a href="HTML/flexbox.html">flexbox.html</a> for a comprehensive, interactive demo and code examples of all major CSS Flexbox properties in action.

---

## 25. CSS Grid

CSS **Grid Layout** is a powerful two-dimensional layout system that enables you to create complex, responsive web layouts with rows and columns. Unlike Flexbox (which is one-dimensional), Grid lets you control both axes simultaneously, making it ideal for page layouts, dashboards, galleries, and more.

### Key Concepts
- **Grid Container:** The parent element with `display: grid` or `display: inline-grid`.
- **Grid Items:** The direct children of the grid container.
- **Tracks:** Rows and columns in the grid.
- **Grid Lines:** The dividing lines between tracks, referenced by number or name.
- **Grid Areas:** Rectangular areas covering one or more cells, can be named for semantic placement.
- **Explicit Grid:** Defined by `grid-template-rows` and `grid-template-columns`.
- **Implicit Grid:** Created automatically when items are placed outside the explicit grid.

### Main Properties
- `display: grid | inline-grid` — Enables grid layout on the container.
- `grid-template-columns`, `grid-template-rows` — Define the number and size of columns and rows.
- `gap` (or `grid-gap`) — Sets spacing between rows and columns.
- `grid-column`, `grid-row` — Control where an item starts/ends and how many tracks it spans.
- `grid-area`, `grid-template-areas` — Name areas for semantic, maintainable layouts.
- `justify-items`, `align-items`, `justify-content`, `align-content` — Align items and tracks within the grid.
- `min-content`, `max-content`, `minmax()`, `fr`, `repeat()`, `auto-fill`, `auto-fit` — Advanced sizing and responsive features.

### Example Usage
```css
.container {
  display: grid;
  grid-template-columns: 120px 1fr 2fr;
  grid-template-rows: 60px 60px;
  gap: 16px;
}
.item1 {
  grid-column: 1 / span 2;
}
.item2 {
  grid-row: 2 / span 2;
}
.area-layout {
  display: grid;
  grid-template-areas:
    "header header"
    "sidebar main"
    "footer footer";
  grid-template-columns: 120px 1fr;
  grid-template-rows: 50px 120px 40px;
}
.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.main { grid-area: main; }
.footer { grid-area: footer; }
```

### Responsive Grid Example
```css
.responsive-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
  gap: 12px;
}
```

### Best Practices
- Use `fr` units for flexible, proportional columns.
- Combine `auto-fit` or `auto-fill` with `minmax()` for responsive grids.
- Use `grid-template-areas` for readable, maintainable layouts.
- Test your grid layouts on different screen sizes for responsiveness.
- Use browser DevTools to visualize and debug grid lines and areas.

### Reference Example
See the new [grid.html](./HTML/grid.html) page for a comprehensive, interactive guide to CSS Grid, including theory, property explanations, and live code demos.

---

## 26. CSS Transitions

**CSS transitions** allow you to animate changes to CSS property values smoothly, enhancing user experience with visual feedback and interactivity—without JavaScript. Transitions are triggered by state changes (like <code>:hover</code>, <code>:focus</code>, or class changes) and are ideal for simple, one-step animations.

### Transition Properties
- <strong>transition-property</strong>: The CSS property to animate (e.g., <code>background-color</code>, <code>width</code>).
- <strong>transition-duration</strong>: How long the transition takes (e.g., <code>0.5s</code>).
- <strong>transition-timing-function</strong>: The speed curve of the transition (e.g., <code>ease</code>, <code>linear</code>, <code>ease-in</code>, <code>cubic-bezier</code>).
- <strong>transition-delay</strong>: How long to wait before starting the transition (e.g., <code>0.2s</code>).
- <strong>transition</strong>: Shorthand for all the above.

### Syntax
```css
transition: property duration timing-function delay;
```
Example:
```css
transition: background-color 0.5s ease 0.2s;
```

### How Transitions Work
When a property specified in <code>transition-property</code> changes (such as on <code>:hover</code>), the browser animates the change over the specified duration and timing function. Only animatable properties can be transitioned (e.g., <code>color</code>, <code>background</code>, <code>transform</code>, <code>opacity</code>).

### Common Timing Functions
- <strong>ease</strong>: Starts slow, speeds up, then slows down (default)
- <strong>linear</strong>: Constant speed
- <strong>ease-in</strong>: Starts slow, then speeds up
- <strong>ease-out</strong>: Starts fast, then slows down
- <strong>ease-in-out</strong>: Starts and ends slow
- <strong>cubic-bezier</strong>: Custom curve

### Example
```css
.box {
  transition: background-color 0.5s, width 0.5s;
}
.box:hover {
  background-color: #8e44ad;
  width: 220px;
}
```

### Best Practices
- Use transitions for simple, state-based animations.
- Keep transitions short and subtle for best user experience.
- For complex, multi-step animations, use <code>@keyframes</code> and <code>animation</code>.

### See Also
- <a href="HTML/transitions.html">Interactive CSS Transitions Example</a>

---

## 27. CSS Transform

**CSS transform** is a versatile property that allows you to visually manipulate elements in 2D or 3D space. You can move, scale, rotate, skew, and combine these effects for engaging, interactive interfaces—all with hardware acceleration and no JavaScript required.

### Transform Functions
- **translate(x, y):** Moves an element along the X and/or Y axis.
- **scale(x, y):** Resizes an element (width and/or height).
- **rotate(angle):** Rotates an element clockwise or counterclockwise.
- **skew(x-angle, y-angle):** Skews (shears) an element along the X and/or Y axis.
- **matrix():** Combines all 2D transforms in one function.
- **perspective(), rotate3d(), scale3d(), translate3d():** 3D transforms for advanced effects.

### Syntax & Usage
```css
.box {
  transform: scale(1.2) rotate(8deg) translateY(-18px);
}
```
- Multiple transforms can be combined in a single property and are applied from left to right.
- Combine with `transition` for smooth, animated effects.

### Example
```css
.scale-demo {
  transition: transform 0.4s;
}
.scale-demo:hover {
  transform: scale(1.3);
}
```

### Best Practices
- Use `transform` for performant, hardware-accelerated animations.
- Transforms do not affect document flow—use with care for layout.
- Test transforms on different devices and browsers for consistency.
- Use `will-change: transform` for performance optimization on heavy transforms.

### See Also
- <a href="HTML/transform.html">Interactive CSS Transform Example</a>

---

## 28. CSS Animations

**CSS animations** allow you to animate CSS property values over time using `@keyframes`. Unlike transitions, animations can define multiple steps, loop, alternate, and run automatically.

### Animation Properties
- **animation-name:** The name of the `@keyframes` to use.
- **animation-duration:** How long one cycle of the animation takes (e.g., `2s`).
- **animation-timing-function:** The speed curve of the animation (e.g., `ease`, `linear`, `steps`, `cubic-bezier`).
- **animation-delay:** How long to wait before starting the animation.
- **animation-iteration-count:** How many times the animation repeats (`1`, `infinite`, or a number).
- **animation-direction:** Whether the animation runs normal, reverse, alternate, or alternate-reverse.
- **animation-fill-mode:** How styles are applied before/after animation (`none`, `forwards`, `backwards`, `both`).
- **animation-play-state:** Whether the animation is running or paused.
- **animation:** Shorthand for all the above.

### Syntax & Usage
```css
@keyframes bounce {
  0%   { transform: translateY(0); }
  50%  { transform: translateY(-40px); }
  100% { transform: translateY(0); }
}
.box {
  animation: bounce 1s ease-in-out infinite;
}
```

### Best Practices
- Use `animation` for multi-step, automatic, or looping effects.
- Keep animations short and meaningful for best user experience.
- Combine with `transition` and `transform` for advanced UI effects.
- Test animations on different devices and browsers for consistency.
- Use `will-change` for performance optimization on heavy animations.
- Respect user preferences for reduced motion (see [`@media (prefers-reduced-motion)`](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion)).

### See Also
- <a href="HTML/animations.html">Interactive CSS Animations Example</a>

---

## 29. CSS Variables

**CSS Variables**, also known as **Custom Properties**, allow you to store reusable values in your stylesheet. They make your code more maintainable, readable, and dynamic, especially for theming and managing complex designs.

### Syntax
- **Declaration:** Define a variable using two dashes, e.g., `--main-color: #3498db;`.
- **Usage:** Access the variable using the `var()` function, e.g., `color: var(--main-color);`.

### Scope
- **Global Scope:** Variables defined in the `:root` pseudo-class are available globally.
- **Local Scope:** Variables defined within a selector (e.g., a class) are only available to that element and its descendants.

### Key Features
- **Fallback Values:** Provide a default if a variable isn't set: `var(--custom-color, black)`.
- **Dynamic:** Can be updated with JavaScript or by changing classes, making them ideal for theming.
- **Inheritance:** Variables are inherited by child elements.

### ✅ Example:
```css
/* Global variables */
:root {
  --primary-color: #3498db;
  --base-font-size: 16px;
}

body {
  font-size: var(--base-font-size);
}

.button {
  background-color: var(--primary-color);
  color: white;
}

/* Local override */
.button-danger {
  --primary-color: #e74c3c; /* This overrides the global variable */
}
```

For a detailed, interactive guide, see the [CSS Variables Example Page](./HTML/variables.html).

---

## 30. CSS Specificity

**CSS Specificity** is the set of rules browsers use to determine which style declaration is applied to an element when multiple conflicting rules exist. The more specific a selector is, the higher its precedence.

### Specificity Hierarchy (Highest to Lowest)
1.  **Inline Styles** - `style="..."`
2.  **IDs** - `#my-id`
3.  **Classes, Attributes, Pseudo-classes** - `.my-class`, `[type="text"]`, `:hover`
4.  **Elements, Pseudo-elements** - `p`, `::before`

### The `!important` Rule
Adding `!important` to a style declaration makes it override all other declarations, regardless of specificity. It should be used with extreme caution as it can make debugging difficult.

### ✅ Example:
```css
/* Low specificity */
p {
  color: blue;
}

/* Higher specificity */
.my-paragraph {
  color: green;
}

/* Highest specificity */
#main-paragraph {
  color: red;
}

/* This will be applied regardless of the ID selector */
p.important {
    color: purple !important;
}
```

---

## 31. CSS Float

The **float** property is one of CSS's traditional layout mechanisms that specifies how an element should float, allowing text and inline elements to wrap around it. While modern layout techniques like Flexbox and Grid are now preferred for complex layouts, float remains useful for specific scenarios.

### 🔑 Key Concepts:

- **Float Values:** The float property can take values like `left`, `right`, `none`, and `inherit`.
- **Document Flow:** Floated elements are removed from the normal document flow.
- **Container Collapse:** Containers with only floated elements collapse to zero height.
- **Clearing Floats:** The `clear` property controls how elements behave around floated items.

### 🧹 The Clear Property:

The `clear` property specifies which sides of an element cannot be adjacent to earlier floating elements:

- `clear: left` - Element appears below left-floated elements
- `clear: right` - Element appears below right-floated elements
- `clear: both` - Element appears below both left and right-floated elements
- `clear: none` - Default value, allows floating elements on both sides

### 🛠️ The Clearfix Hack:

When a container has only floated elements, it collapses to zero height. The "clearfix" is a common solution:

```css
/* Modern clearfix using ::after pseudo-element */
.clearfix-container::after  {
  content: "";
  display: block;
  clear: both;
}
```

---

## 32. CSS Media Queries

CSS **Media Queries** are a powerful feature that allows you to apply different styles based on device characteristics like screen size, resolution, orientation, and user preferences. They're the foundation of responsive web design, enabling websites to adapt to different viewing environments.

### 🔑 Key Concepts:

- **Responsive Design:** Media queries enable content to adapt to different screen sizes and devices.
- **Conditional Styling:** Apply CSS only when specific conditions about the user's device or preferences are met.
- **Mobile-First Approach:** Start with styles for small screens, then enhance for larger screens.
- **User Preference Detection:** Adapt to user preferences like dark mode or reduced motion.

### 📱 Media Query Syntax:

```css
@media [media-type] [and/not/only] ([media-feature]) {
  /* CSS rules to apply when conditions are met */
}
```

## 33. CSS Container Queries

**CSS Container Queries** allow you to apply styles to elements based on the size of their containing element, rather than the viewport. This enables truly modular, component-based responsive design.

### 🔑 Key Concepts:
- **Component-Based Design:** Style elements based on their parent container's size
- **Reusable Components:** Create components that adapt to any context they're placed in
- **Modular Layouts:** Build layouts that respond to their available space
- **Reduced Complexity:** Simplify responsive design by focusing on components, not just viewport

### 📝 Syntax
```css
.container {
  container-type: inline-size;
  width: 100%;
  resize: horizontal;
  overflow: auto;
}
.card {
  padding: 1rem;
  background: #f0f4ff;
  border-radius: 8px;
}
@container (max-width: 400px) {
  .card {
    background: #e74c3c;
    color: white;
    padding: 0.5rem;
  }
}

.sidebar {
  container-type: inline-size;
  container-name: sidebar;
}
@container sidebar (max-width: 300px) {
  .widget {
    background: #3498db;
    color: white;
  }
}
```
### 🧩 Container Query Components
- container-type: Establishes a containment context ( size , inline-size , normal )
- container-name: Optional name for the container
- @container: The at-rule that begins a container query
- Container Features: Conditions about the container dimensions ( width , height , aspect-ratio )
- Logical Operators: and , not , or to combine conditions

### ✅ Example: Basic Container Query
```
.container {
  container-type: inline-size;
  width: 100%;
  resize: horizontal;
  overflow: auto;
}
.card {
  padding: 1rem;
  background: #f0f4ff;
  border-radius: 8px;
}
@container (max-width: 400px) 
{
  .card {
    background: #e74c3c;
    color: white;
    padding: 0.5rem;
  }
}
```
### 📏 Container Query Units
- cqw: 1% of a query container's width
- cqh: 1% of a query container's height
- cqi: 1% of a query container's inline size
- cqb: 1% of a query container's block size
- cqmin: The smaller value of cqi or cqb
- cqmax: The larger value of cqi or cqb
```
.cq-heading {
  font-size: calc(1rem + 2cqi);
}
```
### 📊 Container Queries vs. Media Queries
Feature Container Queries Media Queries Target Container size Viewport size Use Modular components Page layout Example

```
@container (min-width: 400px) 
{ .card { display: flex; } }
@media (min-width: 768px) { 
.card { display: flex; } }
```
### 💡 Best Practices
- Use for component-level responsiveness
- Combine with media queries for full flexibility
- Prefer inline-size for internationalization
- Be mindful of performance with deep nesting
- Provide fallbacks for unsupported browsers
### 🔗 Further Reading
- MDN: CSS Container Queries
- W3C: CSS Containment Module Level 3
- Can I Use: CSS Container Queries

## 34. CSS Inheritance & Cascade

### What is Inheritance in CSS?
Inheritance is the process by which some CSS property values applied to a parent element are automatically passed down to its children. Not all properties are inherited. Commonly inherited properties include `color`, `font-family`, and `line-height`. Properties like `margin`, `padding`, and `border` are not inherited by default.

#### Example:
```css
.parent {
  color: #3498db;
  font-family: 'Segoe UI', Arial, sans-serif;
}
.child {
  font-size: 1.2em;
}
```
### What is the Cascade in CSS?
The cascade is the algorithm that determines which CSS rule applies when multiple rules could apply to the same element. It considers:

- Importance ( !important )
- Specificity (how specific the selector is)
Source Order (which rule comes last)
```css
.box {
  background: #f0f4ff;
  color: #222;
}
#special {
  color: #e74c3c;
}
.box {
  color: #3498db !important;
}
```
### 🔑 Key Points:
- !important overrides all other styles
- Specificity determines the winner
- Source order determines the winner
- Inline styles have the highest specificity
- The cascade is a powerful tool, but it can also make debugging complex
- Use it judiciously and test thoroughly

### Best Practices
- Use inheritance to reduce repetition
- Be mindful of the cascade and specificity
- Use inherit , initial , and unset for explicit control
- Avoid overusing !important

### Further Reading
- MDN: CSS Inheritance
- MDN: CSS Cascade
- CSS-Tricks: Specifics on CSS Specificity

## 35. CSS `backdrop-filter`

### What is `backdrop-filter` in CSS?
The `backdrop-filter` property applies graphical effects (such as blurring or color shifting) **to the area behind an element**. It works like placing a frosted glass over content, letting you create stylish UI effects like **glassmorphism**.

It only works on elements with a **transparent background** (or `background-color` with opacity) and usually in combination with `background` and `positioning` styles.

#### Example:
```css
.glass-box {
  backdrop-filter: blur(10px) brightness(0.9);
  background-color: rgba(255, 255, 255, 0.3);
  border-radius: 10px;
  padding: 1rem;
}
```

### Supported Filter Functions:
- `blur(px)`
- `brightness(%)`
- `contrast(%)`
- `grayscale(%)`
- `hue-rotate(deg)`
- `invert(%)`
- `opacity(%)`
- `saturate(%)`
- `sepia(%)`

You can also use **multiple filters** separated by a space.

```css
backdrop-filter: blur(5px) contrast(120%);
```

### 🔑 Key Points:
- Only affects the **background content behind the element**
- Needs a **semi-transparent** or **transparent background**
- Requires **browser support** (ensure fallback for older browsers)
- Often used with **fixed or absolute positioning**
- Works well in **modern UI design** (glassmorphism, modals, popups)

### Best Practices
- Use `backdrop-filter` sparingly—heavy filters can affect performance
- Combine with a `rgba` or semi-transparent background
- Always provide a **fallback** for unsupported browsers
- Consider accessibility—strong blur or contrast may reduce readability

### Compatibility
- Supported in most modern browsers (Chrome, Edge, Safari)
- **Not supported** in Firefox without enabling experimental settings
- Consider using feature detection via `@supports`

#### Example:
```css
@supports (backdrop-filter: blur(5px)) {
  .frosted {
    backdrop-filter: blur(5px);
  }
}
```

### Further Reading
- MDN: [`backdrop-filter`](https://developer.mozilla.org/en-US/docs/Web/CSS/backdrop-filter)
- CSS-Tricks: [Backdrop Filter Basics](https://css-tricks.com/almanac/properties/b/backdrop-filter/)
- CSS-glass: [Creating Glassmorphism Effects in CSS](https://css.glass/)

