## Table of Contents

- [What is HTML](#what-is-html)
- [Intro to HTML](#intro-to-html)
  - [Some HTML Tags](#some-html-tags)
  - [Project Structure](#project-structure)

## What is HTML
yolo

## Intro to HTML
HTML syntax is fairly simple to follow-- all the content is encapsulated within tags: `<tag>Content</tag>`. There are several tags that you should become familar with, but as time goes on and you become more advanced, you'll find that there are many tags that useful in specific situations!

### Some HTML Tags
In every HTML document, all the content is encapsulated within `<html>` tags. The browser won't render your website unless all your subsequent tags are within the HTML tags!

```html
<html> </html>
```

**Headers:**

Header tags allow you to format text on your page as, unsuprisignly, headers. The largest header is `<h1>` and the smallest is `<h6>`. We will see later on how you can possible style headers to make them bigger or smaller, and even change their styles. 
```html
<h1>This is the largest header!</h1>
<h2>This is the second largset header!</h2>
<h3>This is the third largest header!</h3>
<h6>... You get the point.</h6>
```

**Paragraphs:**

Pargraphs are another very basic formatting construct within html. You invoke a paragraph with the `<p>` tag.
```html
<p> This is a pragraph. It's a great paragraph. It might even be the best paragraph.</p>
```

**Links:**

Links are what allow us to link to other pages and other websitese. Links are invoked with the `<a>` tag, but in order to get it to work properly, we'll need to specify the `href` attribute. The `href` attribute is basically what the link should point to.
```html
<a href="https://www.google.com/"> This link points to Google.com!</a>
```


**Images:**

You might want to add images to your website. The `<img>` tag helps you do just that. Just kuje we had to do with links, we have to specify another attribute to let the browser know where the image is located, the `src` attribute allows us to do this. Let's imagine that we have our image in the same directory as our html file. 
```html
<img src="funnycats.jpg">
```

**Divs:**

Divs are used to seperate content into self contained buckets. The `<div>` tag allows you specify content that you want to seperate from everything else. You could have several reasons for this: you want your divs to contain logically different content, you want your divs to have different styles, you want your code to be a bit more modular and organized, etc.
```html
<div class="awesome"> 
	<p>This is a really awesome paragraph</p> 
</div>
<div class="moreAwesome">
	<p>This is an even more awesome paragraph</p>
<div> 
```
For each of these classes, we set a class attribute... but why? We'll get to the importance of classes shortly. I'll let you think about why it might be useful to identify elements by class. 

## Project Structure
Basic HTML websites have a fairly simple structure that is built with tags like the ones we've already seen. Let's get started by setting up our repo: create a directory called `html-tutorial`, and within that directory, add a file named `index.html`. Let's also add `about.html` and `blog.html`, and another folder within this director named `images`.

Thus, your file structure should look something like this: 
```
html-tutorial/
	index.html
	about.html
	blog.html
	images/
```

Let's get started on actually writing some HTML code. Open uo your `index.html` file and copy and paste the following code:
```html
<!DOCTYPE html>
<html>
    <head>
        <!-- This is a comment. -->

        <title>Hello world!</title>
    </head>
    <body>
        <!-- Put all content here. -->
        <div>
        	<h1>Woah, this is really cool!</h1>
        	<p>This is my very first HTML Project!</p>
        </div>
    </body>
</html>
```

If you open your index.html file (with your browser) you should see the following: 
![Alt text](html-tutorial/images/index1.png?raw=true)









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
