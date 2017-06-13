## Table of Contents

- [What is HTML](#what-is-html)
- [Basic Structure](#basic-structure)
  - [Some HTML Tags](#some-html-tags)

## What is HTML
yolo

## Basic Structure
HTML syntax is fairly simple to follow-- all the content is encapsulated within tags: `<tag>Content</tag>`. There are several tags that you should become familar with, but as time goes on and you become more advanced, you'll find that there are many tags that useful in specific situations!

### Some HTML Tags
In every HTML document, all the content is encapsulated within `<html>` tags. The browser won't render your website unless all your subsequent tags are within the HTML tags!

```html
<html> </html>
```

**Headers**
Header tags allow you to format text on your page as, unsuprisignly, headers. The largest header is `<h1>` and the smallest is `<h6>`. We will see later on how you can possible style headers to make them bigger or smaller, and even change their styles. 
```html
<h1>This is the largest header!</h1>
<h2>This is the second largset header!</h2>
<h3>This is the third largest header!</h3>
<h6>... You get the point.</h6>
```

**Paragraphs**
Pargraphs are another very basic formatting construct within html. You invoke a paragraph with the `<p>` tag.
```html
<p> This is a pragraph. It's a great paragraph. It might even be the best paragraph.</p>
```

**Links**
Links are what allow us to link to other pages and other websitese. Links are invoked with the `<a>` tag, but in order to get it to work properly, we'll need to specify the `href` attribute. The `href` attribute is basically what the link should point to.
```html
<a href="https://www.google.com/"> This link points to Google.com!</a>
```




### `Button.js`

```js
import React, { Component } from 'react';

class Button extends Component {
  render() {
    // ...
  }
}

export default Button; // Don’t forget to use export default!
```

class Button extends Component {
  render() {
    // ...
  }
}

export default Button; // Don’t forget to use export default!
```
