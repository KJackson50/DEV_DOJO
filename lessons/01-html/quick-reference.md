# HTML Quick Reference

## Document Skeleton

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Page Title</title>
  </head>
  <body>
    <!-- visible content goes here -->
  </body>
</html>
```

## Common Elements

```html
<h1>Main Heading</h1>
<h2>Section Heading</h2>
<p>Paragraph text.</p>
<a href="/about">Link text</a>
<img src="photo.jpg" alt="Description of image">
<ul>
  <li>List item</li>
</ul>
<ol>
  <li>Numbered item</li>
</ol>
<div>Generic container</div>
<span>Inline container</span>
```

## Element Pattern

```html
<tag attribute="value">content</tag>
```

- Opening tag: `<p>`
- Content: `Hello`
- Closing tag: `</p>`

## Core Attributes

```html
<a href="https://example.com">Visit site</a>
<img src="cat.jpg" alt="Orange cat sitting on a chair">
<html lang="en">
```

- `href`: link destination
- `src`: file or resource source
- `alt`: text description for images
- `lang`: document language
- `charset`: character encoding

## Head vs Body

- `<head>`: metadata, title, charset, linked CSS, scripts
- `<body>`: headings, paragraphs, links, images, lists, forms

## Semantic Reminder

- Use `<h1>`-`<h6>` for headings
- Use `<p>` for paragraphs
- Use `<a>` for links
- Use `<img>` for images
- Pick tags by meaning, not appearance

## Gotchas

- `<!doctype html>` belongs at the top
- Most elements need both opening and closing tags
- `<a>` uses `href`, not `src`
- `<img>` uses `src` and should include `alt`
- Browsers can guess around mistakes, but valid structure is easier to maintain
