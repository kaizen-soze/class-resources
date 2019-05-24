# HTML Tags
HTML is a language specification that defines how text on a web page should be annotated. The following tags are a small taste of what's available. If you want to do a deep dive, check out the [Mozilla Developer Network's documention on HTML](https://developer.mozilla.org/en-US/docs/Web/HTML).

## Paragraph element

The paragraph element is meant for displaying text, and comes with space around it by default. [Click here](https://kaizen-soze.github.io/html5-template/p.html) for an example.

### Syntax
```
<p>This is a paragraph element</p>
```

## Image element
The `<img>` tag is used to display images. [Click here](https://kaizen-soze.github.io/html5-template/img.html) for an example.

### Syntax

```
<img src="cat.jpg" />
<img src="myImageFolder/ferret.jpg" />
```

One interesting thing to note about the image tag is that it's self-closing. Rather than typing `<img> </img>`, you simply close the tag by including a slash at the end.

## Header elements

Header elements set content apart by being visually distinct. They are larger and bolder than the text inside a paragraph element. [Click here](https://kaizen-soze.github.io/html5-template/h.html) for an example.

### Syntax
There are 6 header tags. `<h1>` is the largest and `<h6>` is the smallest.
```
<h1>H1 Header</h1>
<h2>H2 Header</h2>
<h3>H3 Header</h3>
<h4>H4 Header</h4>
<h5>H5 Header</h5>
<h6>H6 Header</h6>
```

## Link element
The `<a>` tag links to another element, typically another web page. You can also create e-mail links and references to other content on the same page. [Example](https://kaizen-soze.github.io/html5-template/a.html)

### Syntax
```
<a href="index.html">Home</a>
<a href="mailto:spammeplease@example.com">E-Mail Link</a>
<p>A <a href="#bookmark">bookmark</a> links to content on the same page.</p>
```

The `href` attribute stands for "hyperlink reference".

## Horizontal rule
The `<hr>` tag is intended to signify a "thematic" change in content. [Example](https://kaizen-soze.github.io/html5-template/hr.html)

### Syntax
```
<hr>
```

## Line break element
The line break adds additional space between elements. [Example](https://kaizen-soze.github.io/html5-template/br.html)

### Syntax
```
<br />
```

Note that this tage is also a self-closing element.

## Span element
The `<span>` element represents a block of content without line breaks. If a `<span>` element is inside of a paragraph element, the text inside `<span>` will appear to be part of the paragraph. [Example](https://kaizen-soze.github.io/html5-template/spandiv.html)

### Syntax
```
<span>This is a span element</span>
```

## Div element
The `<div>` element represents a block of content that includes line breaks. If a `<div>` element is inside of a paragraph element, the text inside `<div>` will appear to be part of a separate paragraph. [Example](https://kaizen-soze.github.io/html5-template/spandiv.html)

In modern web development, `<div>` tags are used extensively for laying out and arranging content.

### Syntax
```
<div>This is a div element</div>
```

## Unordered list element
The `<ul>` tag is used to create an unordered list. [Example](https://kaizen-soze.github.io/html5-template/ul.html)

### Syntax
```
<ul>
    <li>List item</li>
    <li>List item</li>
</ul>
```

## Ordered list element
The `<ul>` tag is used to create an ordered list. [Example](https://kaizen-soze.github.io/html5-template/ul.html)

### Syntax
```
<ol>
    <li>List item</li>
    <li>List item</li>
</ol>
```

## Table element
Tables are used for displaying tabular data. [Example](https://kaizen-soze.github.io/html5-template/tables.html)

### Syntax
```
<table>
    <tr>
        <td>1</td>
        <td>2</td>
        <td>3</td>
        <td>4</td>
        <td>5</td>
    </tr>
  </table>
```

The `<table>` element is meant to work in concert with the `<tr>` and `<td>` tags. `<tr>` represents a row of data, and each column is represented by `<td>`

## Head element
The `<head>` element contains information about the html page that is not intended to be rendered.

### Syntax
```
<head>
</head>
```

A typical head element could look like this:
```
<head>
  <meta charset="utf-8">
  <title>My HTML5 Web Site</title>
  <meta name="description" content="This page contains the essentials for a modern HTML5 web page">
  <meta name="author" content="kaizen-soze">
  <style>
  	.red {
  		background-color: red;
  	}
  </style>

</head>
```

## Title element
You can specify the title of the page with the `<title>` element. The `<title>` element must be included inside the `<head>` element.

### Syntax
```
<head>
  <title>My Web Site Title</title>
</head>
```

## Body element
The `<body>` element contains information about the html page that is intended to be displayed to the user.

### Syntax
```
<body>
</body>
```

## Comments
An HTML content is text that is not meant to be rendered. It can be viewed by any visitor to your web page, so don't include any sensitive information.

### Syntax
```
<!-- This is a comment. -->
```

## Semantic Tags
Semantic HTML tags are meant to give semantic structure to a web page. Instead of a collection of miscellaneous html tags, semantic tags separate HTML into sections that have meaning for a human.

Web browsers don't render semantic tags in any special way; they're meant strictly for humans. Semantic tags can, however, improve search engine rankings and accessibility.

```
<header>
<footer>
<main>
<address>
<article>
<aside>
```

Read more about semantic tags [here](https://seekbrevity.com/semantic-markup-important-web-design/).