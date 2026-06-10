# CSS

## What it is

CSS stands for Cascading Style Sheets. It is the language used to control how HTML looks in the browser.

If HTML provides the structure of a page, CSS provides the presentation. CSS answers questions like:

- What color should this text be?
- How much space should be around this section?
- How wide should this card be?
- Should these items sit on separate lines or next to each other?

Smallest useful example:

```css
h1 {
  color: darkgreen;
}
```

That rule tells the browser: "Find every `<h1>` and make its text dark green."

## How it works

CSS works by matching selectors to HTML elements, then applying declarations to those matched elements.

```css
p {
  color: navy;
  font-size: 18px;
}
```

In that rule:

- `p` is the selector
- `color: navy;` is one declaration
- `font-size: 18px;` is another declaration

Each declaration has:

- A property, like `color`
- A value, like `navy`

CSS can be added three main ways:

1. Inline, directly on an element
2. Inside a `<style>` tag in the HTML file
3. In a separate `.css` file linked from the HTML

For real projects, the separate file approach is usually best.

Example:

```html
<head>
  <meta charset="utf-8">
  <title>My page</title>
  <link rel="stylesheet" href="styles.css">
</head>
```

```css
body {
  font-family: Arial, sans-serif;
}
```

CSS is called "cascading" because more than one rule can target the same element. When rules conflict, the browser resolves that conflict using the cascade: importance, specificity, and source order all matter.

## Why it exists / benefits

CSS exists so structure and presentation can stay separate.

Benefits:

- You can change the look of a page without rewriting the HTML
- One stylesheet can style many pages
- Designs become easier to maintain
- Layout, spacing, colors, and typography become consistent
- You avoid mixing appearance rules into your content structure

Without CSS, pages still work, but they look plain and are harder to control.

## Where it's used

CSS is used anywhere HTML is rendered and needs styling:

- Static websites
- Web apps
- Landing pages
- Dashboards
- Documentation sites
- Email templates, with limited support

Every frontend app you build later will rely on CSS, even if a framework or library helps generate it.

## How to use it

Start by linking a stylesheet, then target simple elements first.

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Profile Card</title>
    <link rel="stylesheet" href="styles.css">
  </head>
  <body>
    <h1 class="name">Ada Lovelace</h1>
    <p>Mathematician and early computing pioneer.</p>
  </body>
</html>
```

```css
body {
  background-color: #f4f7f1;
  color: #1f2937;
}

.name {
  color: #1b5e20;
}
```

For now, focus on these beginner ideas:

- Select an element
- Change its color
- Add spacing with `margin` and `padding`
- Use classes when you want to style some elements differently from others
- Keep styles in a separate CSS file

Later you will learn layout systems, responsive design, and more advanced selectors.
