## Table of Contents

- [What is HTML](#what-is-html)
- [Intro to HTML](#intro-to-html)
  - [Some HTML Tags](#some-html-tags)
  - [Project Structure](#project-structure)
  - [Debugging](#debugging)
- [The Big Beautiful World of CSS](#the-big-beautiful-world-of-css)
  - [Working with CSS](#working-with-css)
  - [Selectors](#selectors)
    - [Inline CSS](#inline-css) 
    - [Selecting by ID anc Class](#selecting-by-id-and-class)

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

### Project Structure
Basic HTML websites have a fairly simple structure that is built with tags like the ones we've already seen. Let's get started by setting up our repo: create a directory called `html-tutorial`, and within that directory, add a file named `index.html`. Let's also add `about.html` and `blog.html`, and another folder within this director named `images`.

Thus, your file structure should look something like this: 
```
html-tutorial/
	index.html
	about.html
	blog.html
	images/
```

Let's get started on actually writing some HTML code. Open up your `index.html` file and copy and paste the following code:
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

All html files are denoted via the .html filetype. Okay, that's great, but what's going in here? 

`<!DOCTYPE html>` 

Tells your browser to interpet the following file as HTML. Every HTML page should start with this tag. Unlike other tags, there is not closing tag for this first tag. 

`<html>`

This tag encapsulates all of your HTML codes. In other words, every other element is a child this tag. 

`<head>`

The head tag denotes the header section of the html document-- this content is not rendered by the browser to the page, but simply contains information that tells the browser how the page should be produced. Typically, this is where you would link JavaScript scripts, cdn connections, and CSS stylesheets-- all of which we will discuss further on. Note that there is closing `</head>` tag. 

`<title>Hello world!</title>`

The title tag declares the title of this html document. When you opened your html page, you might have noticed that this title was the name of the tab in your browser. Note that this tag is a child of the `<head>` tag. 

`<body>`

The body tag describes the content of the body of this HTML page. The bulk of your content will go here. 

`<!-- Put all content here. -->`

This tag describes a comment-- comments are not rendered by the browser, and are merely meant to help the programmer. It's good to get in the habbit of commenting your code-- it will help you keep better track of your work, and will also make it easier for others to collobrate with you.

Note that `<head>` has exactly two children: `<head>` and `<body>`, but all other tags can have as many children as you desire them to have!

Not so bad, right? As we move on to some more HTML and combine it with other things like CSS and JavaScript, we'll come across more tags that we haven't already discussed-- fear not! You now have a solid intution of how HTML tags work. 

### Debugging
No matter what kind of programming you get into, debugging is a process you want to get intimately familiar with. Programming fundamentally boils down to problem solving, and in order to solve problems you need to able to identify them first. Debugging helps you identify problems in your code so you can fix them. Debugging is as much an art as it is a science, and does require some practice to get good at-- luckily, there are some tools within your browser than can help you debug your HTML code. 

If you use google chrome, you can open up the developer tools by clicking `More tools > Developer Tools`. When you open up the developer tools, you'll see a bunch of really cool stuff, but what should look awfully familar is the HTML code of whatever page you opeend the developer tools with. If you open the developer tools with the `index.html` page we created a little while ago, you should see the HTML code that you wrote!

The great thing about this tool is that it can make your life alot easier. You might conceivably run into a situation where your page doesn't look like what you think it should look like, and you have no idea why. It might be that you forgot a pesky `>` closing bracket, or just misformed an HTML tag is such a way that it impacted the way the browser rendered the page. If you open up the Chrome dev tools, you can easily track where you went wrong-- isn't that awesome?

Debugging tools like the Chrome dev tools are a tremendously imporant tool for all programmers, and you'll find similar tools within whatever domain or framework you graduate on to. Getting better at debugging code is something that requires a lot of writing bad code, and taking the time to understand why your code is bad. 

To learn more about debugging, check out https://rubberduckdebugging.com/. 

###possible short projcect? For fun? 


## The Big Beautiful World of CSS
CSS stands for "Cascading Style Sheets"-- these files essentially help you style your HTML websites. You might have noticed that our basic example in our `index.html` is pretty drab right now, but CSS gives us the power to make our page look really cool. Disclaimer: there are a lot of really awesome things you can theoretically do with CSS-- I'm no artist, and I'm not entirely sure how some people manage to make the stuff that they do make, but this guide can give you some insight into how CSS works and provide you with a basis into how to do some cooler stuff.

If you are intersted in seeing what some baller frontend work with CSS looks like, check out https://codepen.io/2016/popular/pens/. (Some of these examples include JavaScript and other framworks, but most of them are very CSS heavy.)

### Working with CSS
At the core, CSS basically allows you to style HTML elements. As we've already seen, HTML documents are entirely composed of elements, so CSS will let us modify the look of every element in our document.

If you wanted to style all the paragraph tags in your HTML document, you might write something like this: 
```css
p {
    color: red;
    text-align: center;
    text-transform: uppercase;
    letter-spacing: 4px;
}
```

Much like the HTML code we've been looking at, CSS code has a fairly simple to follow syntatic structure. As you might have guessed, this CSS code would format all the text within `<p></p>` tags to have the color red, be aligned to the center, with letters in uppercase and spaced out by 4 pixels. 

You chan change a lot more if you would like-- we will cover a few things in this workshop, but you should feel free to explore on your own to modify your websites in whatever way you want!

A few other text based properties:

`direction`: Speciefies the direction the text is written.

`text-indent`: Describes the indentiation spacin of the first line of the text block.

`text-shadow`: Add a shadow effect to the text.

`word-spacing`: Descibes how words should be spaced out. 

For a comprehensive list on how you could modify text with CSS-- check out: https://www.w3schools.com/css/css_text.asp.

### Selectors 
CSS allows you style an HTML page via selectors. 

In general, this is the pattern you will be following: 

```
selector {
  property: value;
  [You can specify as many property/value pairs as you want]
}
```

The selector can come in a variety of formats-- you can select a group of elements by spceifying a specific tag:

For example, as we've seen, the following modifies any text within `<p></p>` tags:
```css
p {
    color: red;
    text-align: center;
    text-transform: uppercase;
    letter-spacing: 4px;
}
```

### Inline CSS
If you want to modify an HTML tag, and have it be a one off change (maybe you only want to modify a single tag), you can use *inline css*. How does it work? 

To specify an inline style for an element, you would do the following `<tag style="property:value"> </tag>`
In you look at your `index.html` file, let's modify the header using inline css. 

```html
<!-- This is the only line we're changing right now. The rest of the file is the same. -->
<h1 style="color:blue">Woah, this is really cool!</h1>
```
Now if you open up `index.html` with your browser again, you should see:
![Alt text](html-tutorial/images/inline-css.png?raw=true) 

In general, inline css is defined within the opening tag of whatever element it is you want to specify. Inline CSS isn't a great choice, mainly because it makes your code much more difficult to follow. If you have a large HTML file and every element is styled using inline css, that would mean you would need to painstakingly go through every element to modify their styles. This isn't ideal, to say the least. Luckily, there are ways to make your styling more modular.

### Selecing by ID and class
Another way to specify the tag is to select a group of elements by `id`. How does this work? Well, let's revist the code in our `index.html`. 

So far this is what it looks like 
### `index.html`
```html
<!DOCTYPE html>
<html>
    <head>
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

In order to add an `id` attribute to an html tag, you would do the following: `<tag id="someIdValue"> blah blah blah </tag>`, where tag can be any tag you want to identify with the id value. 

Now, let's add an `id` attribute to the header tag. 
```html
<!-- This is the only line we're changing right now. The rest of the file is the same. -->
<h1 id="coolID">Woah, this is really cool!</h1>
```

Great! You just specifed the that particular `<h1>` tag to be identified by that particular id value. Note: this doesn't specify *all* `<h1>` tags. Instead, it only specifies tags that have the same `id` value. 

Now that we have a way to directly identify that particular tag, let's use CSS to modify it. This is what our `index.html` looks like following the addition of our CSS. (Note, we took out the inline styling from the previous example to illustrate selecting by `id`.)
```html
```html
<!DOCTYPE html>
<html>
    <head>
        #coolID {
          color:blue;
        }
        <title>Hello world!</title>
    </head>
    <body>
        <!-- Put all content here. -->
        <div>
        	<h1 id="coolID">Woah, this is really cool!</h1>
        	<p>This is my very first HTML Project!</p>
        </div>
    </body>
</html>
```

If you open up `index.html` with your browser again, you should see the same styling from the previous example. 

Why is the better? It looks like this is more lines of code than our inline example. While that is true, this has produced more llnes of code, this code is much more readably than our previous example. If you a large HTML file, having your styles specified in one place let's you make changes by directing your attention to a single place, as opposed to having to comb through your code to find the element style that needs modification. 

Modular code is better code! 











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
