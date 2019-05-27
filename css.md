# CSS Properties
CSS is used to add styling information to an HTML document. The following properties are a small taste of what's available. If you want to do a deep dive, check out [The CSS Handbook](https://medium.freecodecamp.org/the-css-handbook-a-handy-guide-to-css-for-developers-b56695917d11).

## Selectors

A selector is a way of identifiying which part of the HTML document you want to add stylig information to. There are three types of selectors:

* HTML elements (body, p, div, etc)
* Classes (`<p class="myClass">This is a paragraph</p>`)
* IDs (`<p id="my-paragraph">This is a paragraph</p>`)

The general format for a CSS instruction is as follows:

```
selector {
  property: value
}
```

CSS instructions may set multiple properties at a time. Instructions from multiple sources may even overlap; this is where the cascading part of Cascading Style Sheets comes from!

## Types of Stylesheets

### External

External stylesheets are loaded first via the `<link>` tag, which is defined in the `<head>` of an HTML document.

`<link rel="stylesheet" href="external.css">`

### Internal

Internal stylesheets are loaded second. They are contained within the `<style>` tag of an HTML document. Internal stylesheets usually take precedence over what is defined in an external sheet.

### Inline

Inline styles are defined on the actual element itself, and are take precedence over both Inline and External style instructions.

`<p style=”color: red; margin: 10px;”>This is a paragraph</p>`

## Margin property
The margin property adds space around an element. [Click here](https://kaizen-soze.github.io/html5-template/cssExamples/margin.html) for an example.

### Syntax

Set a margin of 10px on each side:
```
margin: 10px;
```

Set a margin of 10px only on the left side:
```
margin-left: 10px;
```

Set a margin of 25% of the page height only on the top:
```
margin-top: 25%;
```

Set the values for the top (1px), right (2px), bottom (3px), and left (4px) all in one line:

```
margin: 1px 2px 3px 4px;
```

The shorthand version of the `margin` property also accepts 2 arguments and 3 arguments.

```
margin: 1px 2px;
margin: 1px 2px 3px;
```

## Padding property
The padding property creates extra space _inside_ an element. [Click here](https://kaizen-soze.github.io/html5-template/cssExamples/padding.html) for an example.

### Syntax

Set a padding of 10px on each side:
```
padding: 10px;
```

Set a padding of 10px only on the left side:
```
padding-left: 10px;
```

Set a padding of 25% of the page height only on the top:
```
padding-top: 25%;
```

Set the values for the top (1px), right (2px), bottom (3px), and left (4px) all in one line:

```
padding: 1px 2px 3px 4px;
```

The shorthand version of the `padding` property also accepts 2 arguments and 3 arguments.

```
padding: 1px 2px;
padding: 1px 2px 3px;
```

## font-weight property
The font-weight property adds (or removes) **emphasis** from text. [Click here](https://kaizen-soze.github.io/html5-template/cssExamples/font-weight.html) for an example.

### Syntax

Increase emphasis on text.
```
font-weight: bold;
```

Normal emphasis on text. You would use this when the surrounding text is bold or light and you want the text to be a normal weight.
```
font-weight: normal;
```

Lighter emphasis on text. This is a relative measurement. If the parent element's text is bold, this instruction will make the affected text slightly less bold.
```
font-weight: lighter;
```

More emphasis on text. This is a relative measurement. If the parent element's text is normal, this instruction will make the affected text slightly more bold.
```
font-weight: bolder;
```

You can also use numbers to specify font-weight. Font-weight begins at 100 for the lightest and end at 900 for the boldest. Not every font has every font-weight number, so be sure to test this before you use it in a finished web site.

```
font-weight: 100;
font-weight: 200;
font-weight: 300;
font-weight: 400;
font-weight: 500;
font-weight: 600;
font-weight: 700;
font-weight: 800;
font-weight: 900;
```

## font-size property
The font-size property changes the size of the affected text. [Click here](https://kaizen-soze.github.io/html5-template/cssExamples/font-size.html) for an example.

### Syntax

There are several different default sizes for font-size.
```
font-size: xx-small;
font-size: x-small;
font-size: medium;
font-size: x-large;
font-size: xx-large;
```

You can also specify sizes in various measurements that CSS understands. You can read more about CSS units [here](https://medium.freecodecamp.org/the-css-handbook-a-handy-guide-to-css-for-developers-b56695917d11).

```
font-size: 15px;
font-size: 15em;
font-size: 15%;
```

## font-family property
The font-family property changes the font of the affected text. [Click here](https://kaizen-soze.github.io/html5-template/cssExamples/font-family.html) for an example.

Be sure to use [Web Safe Fonts](https://www.cssfontstack.com/); they are installed on every computer. If you specify a font that the end user doesn't have installed on their system, the font will not load and the text will simply render in the default font of the web browser.

### Syntax

Serif fonts:
```
font-family: Georgia;
font-family: Palatino;
font-family: Times New Roman;
font-family: Times;
```

Sans-Serif fonts:
```
font-family: Arial;
font-family: Helvetica;
font-family: Verdana;
font-family: Geneva;
font-family: Tahoma;
font-family: Lucida Grande;
font-family: Impact;
font-family: Trebuchet MS;
font-family: Arial Black;

```

Monospace fonts:
```
font-family: Courier New;
font-family: Courier;
font-family: Lucida Console;
font-family: Monaco;
```

It's also possible to use generic names:
```
font-family: sans-serif;
font-family: serif;
font-family: monospace;
font-family: cursive;
font-family: fantasy;
```

These instructions can be combined, and the first font found on the system will be used. If a font isn't found or doesn't load, it will be skipped and the next font will be attempted.

```
font-family: Lucida Grande, Arial, sans-serif;
```

## color property
The color property changes the color of the affected text. [Click here](https://kaizen-soze.github.io/html5-template/cssExamples/color.html) for an example.

Check out this list of [available colors](https://www.w3schools.com/cssref/css_colors.asp) to see what's available.

To generate your own matching color scheme, use [Paletton](https://paletton.com/)

### Syntax

Each line changes the color to red. Use whatever method you are most comfortable with.

```
color: red;
color: #ff0000;
color: #f00;
```

## background-color property
The background-color property changes the background color of the affected element. [Click here](https://kaizen-soze.github.io/html5-template/cssExamples/background-color.html) for an example.

Check out this list of [available colors](https://www.w3schools.com/cssref/css_colors.asp) to see what's available.

To generate your own matching color scheme, use [Paletton](https://paletton.com/)

### Syntax

Each line changes the color to red. Use whatever method you are most comfortable with.

```
background-color: red;
background-color: #ff0000;
background-color: #f00;
```

## width property
The width property changes the maximum width of the affected element. [Click here](https://kaizen-soze.github.io/html5-template/cssExamples/width.html) for an example.

### Syntax

Width can be defined via pixel or percentage.

```
width: 50px;
width: 50%;
```

## height property
The height property changes the maximum height of the affected element. [Click here](https://kaizen-soze.github.io/html5-template/cssExamples/height.html) for an example.

If the content of the element is greater than the specified height, the content will overflow. You can sometimes end up with an element that has more height than you intend as a result.

### Syntax

Height can be defined via pixel or percentage.

```
height: 50px;
height: 50%;
```

## CSS Comments
CSS Comments are ignored by the interpreter.

### Syntax

```
/* This is a CSS comment! */
color: red;
```