# HTML

## What it is

HTML stands for HyperText Markup Language. It is the structure layer of a webpage: the part that says "this is a heading," "this is a paragraph," "this is a link," "this is an image," and "this group of content belongs together."

HTML is not a programming language. It does not make decisions or run logic by itself. It marks up content so a browser can understand the document and display it.

Smallest useful example:

```html
<h1>My first page</h1>
<p>Hello from HTML.</p>
```

The browser reads the tags and turns them into visible page content.

## How it works

HTML uses elements. Most elements have an opening tag, content, and a closing tag.

```html
<p>This is a paragraph.</p>
```

In that example:

- `<p>` opens the paragraph element
- `This is a paragraph.` is the content
- `</p>` closes the paragraph element

Some elements also have attributes. Attributes add extra information to an element.

```html
<a href="https://developer.mozilla.org/">Read MDN</a>
```

Here, `<a>` creates a link and `href` tells the browser where the link should go.

A full HTML document usually starts with this shape:

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>My first page</title>
  </head>
  <body>
    <h1>My first page</h1>
    <p>Hello from HTML.</p>
  </body>
</html>
```

`<!doctype html>` tells the browser to use modern standards mode. The `<head>` holds metadata about the document. The `<body>` holds the content people actually see.

## Why it exists / benefits

HTML gives web content a shared structure that browsers, search engines, screen readers, and other tools can understand.

Good HTML makes a page easier to:

- Render in a browser
- Style with CSS
- Make interactive with JavaScript
- Navigate with assistive technology
- Discover through search engines

## Where it's used

HTML is used anywhere web pages are rendered:

- Static websites
- Web apps
- Documentation sites
- Blog posts and articles
- Forms, dashboards, and admin tools
- Emails, with a more limited HTML feature set

Every later frontend topic in this dojo sits on top of HTML.

## How to use it

Start with the document skeleton, then add meaningful elements inside `<body>`.

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Profile Card</title>
  </head>
  <body>
    <h1>Ada Lovelace</h1>
    <p>Mathematician and early computing pioneer.</p>
    <a href="https://en.wikipedia.org/wiki/Ada_Lovelace">Read more</a>
  </body>
</html>
```

For now, focus on choosing tags by meaning. Use a heading for a heading, a paragraph for paragraph text, and a link for navigation.
