## Table of Contents

- [What is HTML](#what-is-html)
- [Intro to HTML](#intro-to-html)
  - [Some HTML Tags](#some-html-tags)
  - [Project Structure](#project-structure)
  - [Debugging](#debugging)
- [The Big Beautiful World of CSS](#the-big-beautiful-world-of-css)

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
