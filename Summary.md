# CSS Summary for Revision

A concise reference to revise the essential CSS concepts and best practices while building web projects.

---

## 1. What is CSS?

**CSS (Cascading Style Sheets)** is a style sheet language used to define the presentation and layout of HTML documents. It separates content (HTML) from design, enabling consistent styling across multiple web pages.

### 🔑 Key Concepts:
- **Separation of Concerns:** Structure (HTML) vs. Style (CSS)
- **Cascading Nature:** Multiple rules can apply to an element; the most specific one takes effect.
- **Inheritance:** Certain properties (e.g., `color`, `font-family`) pass from parent to child elements.

### ✅ Example:
```html
<!-- index.html -->
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="style.css">
</head>
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

| Type        | Description | Use Case |
|-------------|-------------|----------|
| **Inline**   | Defined inside an element's `style` attribute | For quick testing or overriding |
| **Internal** | Placed within `<style>` in the HTML `<head>` | For single-page documents |
| **External** | Linked via `<link>` to a `.css` file | Recommended for maintainability and reuse |

### ✅ Example:
```html
<!-- Inline -->
<p style="color: red;">This is inline styled</p>

<!-- Internal -->
<head>
  <style>
    p { color: blue; }
  </style>
</head>

<!-- External -->
<head>
  <link rel="stylesheet" href="styles.css">
</head>
```

---

## 3. CSS Selectors

**Selectors** determine which HTML elements to style.

### 🎯 Common Selectors:
- `element` – Targets all specific elements (e.g., `p {}`)
- `.class` – Targets elements with a specific class
- `#id` – Targets a unique element by its ID
- `[attribute]` – Targets elements by attribute
- `:pseudo-class` – Styles elements in a specific state
- `::pseudo-element` – Styles a part of an element (e.g., `::first-line`)

### 🔢 Specificity (Priority Order):
`Inline Styles > #ID > .Class / [Attr] / :Pseudo-class > Element / ::Pseudo-element`

### ✅ Example:
```css
p { color: navy; }
.highlight { background: yellow; }
#main { border: 1px solid #333; }
input[type="text"] { border-radius: 4px; }
a:hover { color: orange; }
```

---

## 4. Comments in CSS

Comments help document your styles. They're ignored by browsers.

```css
/* This is a single-line comment */

/* Layout Styles */
.container {
  max-width: 1200px;
  margin: 0 auto;
}
```

---

## 5. Colors in CSS

CSS provides several ways to define color:

| Format     | Example                |
|------------|------------------------|
| Named      | `red`, `blue`          |
| Hex        | `#ff0000`, `#333`      |
| RGB        | `rgb(255, 0, 0)`       |
| RGBA       | `rgba(255, 0, 0, 0.5)` |
| HSL/HSLA   | `hsl(0, 100%, 50%)`    |

### 👀 Accessibility Tip:
Ensure **sufficient contrast** between foreground and background colors for better readability.

### ✅ Example:
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

## ✅ Summary Tips
- Use an **external CSS** file for scalability.
- Organize your CSS with **clear comments** and **consistent naming conventions**.
- Always test styles across devices for **responsiveness**.
- Learn and apply **Flexbox** and **Grid** for advanced layouts.
- Use tools like **DevTools** to debug and experiment.

---

_Keep updating this summary as you explore more advanced CSS concepts like animations, transitions, Flexbox, Grid, media queries, and preprocessors (like SASS)._ 🚀