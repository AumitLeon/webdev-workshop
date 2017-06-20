This is an Introduction to Web Development workshop that focuses on HTML, CSS, and JavaScript with an eye towards jQuery. This is by no means a comprehensive guide, but hopefully it provides you with a solid foundation with web development. 

No prior programming experience is required. Although, if you have some prior experience with HTML and CSS, you might find this guide to be quite boring. 

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
    - [Selecting by ID](#selecting-by-id)
    - [Selecting by Class](#selecting-by-class)
  - [Linking Style Sheets](#linking-style-sheets)
- [Interactivity with JavaScript](#interactivity-with-javascript)
  - [Basic JavaScript Concepts](#basic-javascript-concepts)
     - [Variables](#variables)
     - [Arrays](#arrays)
  - [JS and jQuery](#js-and-jquery)
   - [Handling Events](#handling-events)
   - [Modifying CSS](#modifying-css)
- [Mini Project](#mini-project)
- [Conclusion](#conclusion)

## What is HTML
HTML stands for *Hypertext Markup Language*, and it is the language that underlies all the websites that you can access via your web browser. HTML is comprised of tags that provide instructions to your browser as to how a particular page should be rendered. Like any other computer/programming language, HTML has a particular syntax that you need to adhere to. 

## Intro to HTML
HTML syntax is fairly simple to follow-- all the content is encapsulated within tags: `<tag>Content</tag>`. There are several tags that you should become familar with, but as time goes on and you become more advanced, you'll find that there are many tags that are useful in specific situations!

### Some HTML Tags
In every HTML document, all the content is encapsulated within `<html>` tags. The browser won't render your website unless all your subsequent tags are within the HTML tags!

```html
<html> </html>
```

**Headers:**

Header tags allow you to format text on your page as, unsuprisignly, headers. The largest header is `<h1>` and the smallest is `<h6>`. We will see later on how you can possibly style headers to make them bigger or smaller, and even change their styles. 
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

Links are what allow us to link to other pages and other websites. Links are invoked with the `<a>` tag, but in order to get it to work properly, we'll need to specify the `href` attribute. The `href` attribute is basically what the link should point to.
```html
<a href="https://www.google.com/"> This link points to Google.com!</a>
```


**Images:**

You might want to add images to your website. The `<img>` tag helps you do just that. Just like we had to do with links, we have to specify another attribute to let the browser know where the image is located: the `src` attribute allows us to do this. Let's imagine that we have our image in the same directory as our HTML file. 
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
Basic HTML websites have a fairly simple structure that is built with tags like the ones we've already seen. Let's get started by setting up our repo: create a directory called `html-tutorial`, and within that directory, add a file named `index.html`. Let's also add `about.html`, `goals.html`, and `experiment.html`, as well as another folder within this directory named `images`.

Thus, your file structure should look something like this: 
```
html-tutorial/
	index.html
	about.html
	goals.html
    experiment.html
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

All html files are denoted via the .html filetype. Okay, that's great, but what's going here? 

* `<!DOCTYPE html>`: Tells your browser to interpet the following file as HTML. Every HTML page should start with this tag. Unlike other tags, there is not closing tag for this first tag. 

* `<html>`: This tag encapsulates all of your HTML codes. In other words, every other element is a child of this tag. 

* `<head>`: The head tag denotes the header section of the html document-- this content is not rendered by the browser to the page, but simply contains information that tells the browser how the page should be produced. Typically, this is where you would link JavaScript scripts and CSS stylesheets-- both of which we will discuss further on. Note that there is closing `</head>` tag. 

* `<title>Hello world!</title>`: The title tag declares the title of this html document. When you opened your html page, you might have noticed that this title was the name of the tab in your browser. Note that this tag is a child of the `<head>` tag. 

* `<body>`: The body tag describes the content of the body of this HTML page. The bulk of your content will go here. 

* `<!-- Put all content here. -->`: This tag describes a comment-- comments are not rendered by the browser, and are merely meant to help the programmer. It's good to get in the habbit of commenting your code-- it will help you keep better track of your work, and will also make it easier for others to collaborate with you.

Note that `<head>` has exactly two children: `<head>` and `<body>`, but all other tags can have as many children as you want!

Not so bad, right? As we move on to some more HTML and combine it with other things like CSS and JavaScript, we'll come across more tags that we haven't already discussed-- fear not! You now have a solid intution of how HTML tags work. 

### Debugging
No matter what kind of programming you get into, debugging is a process you want to get intimately familiar with. Programming fundamentally boils down to problem solving, and in order to solve problems you need to able to identify them first. Debugging helps you identify problems in your code so you can fix them. Debugging is as much an art as it is a science, and does require some practice to get good at-- luckily, there are some tools within your browser than can help you debug your HTML code. 

If you use google chrome, you can open up the developer tools by clicking `More tools > Developer Tools`. When you open up the developer tools, you'll see a bunch of really cool stuff, but what should look awfully familar is the HTML code of whatever page you opeend the developer tools with. If you open the developer tools with the `index.html` page we created a little while ago, you should see the HTML code that you wrote!

The great thing about this tool is that it can make your life alot easier. You might conceivably run into a situation where your page doesn't look like what you think it should look like, and you have no idea why. It might be that you forgot a pesky `>` closing bracket, or just misformed an HTML tag is such a way that it impacted the way the browser rendered the page. If you open up the Chrome dev tools, you can easily track where you went wrong-- isn't that awesome?

Debugging tools like the Chrome dev tools are a tremendously imporant tool for all programmers, and you'll find similar tools within whatever domain or framework you graduate on to. Getting better at debugging code is something that requires a lot of writing bad code, and taking the time to understand why your code is bad. 

To learn more about debugging, check out https://rubberduckdebugging.com/. 

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

* `direction`: Speciefies the direction the text is written.
* `text-indent`: Describes the indentiation spacin of the first line of the text block.
* `text-shadow`: Add a shadow effect to the text.
* `word-spacing`: Descibes how words should be spaced out. 

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

#### Inline CSS
If you want to modify an HTML tag, and have it be a one off change (maybe you only want to modify a single tag), you can use *inline css*. How does it work? 

To specify an inline style for an element, you would do the following `<tag style="property:value"> </tag>`
In you look at your `index.html` file, let's modify the header using inline css. 

```html
<!-- This is the only line we're changing right now. The rest of the file is the same. -->
<h1 style="color:blue">Woah, this is really cool!</h1>
```
Now if you open up `index.html` with your browser again, you should see:
![Alt text](html-tutorial/images/inline-example.png?raw=true) 

In general, inline css is defined within the opening tag of whatever element it is you want to specify. Inline CSS isn't a great choice, mainly because it makes your code much more difficult to follow. If you have a large HTML file and every element is styled using inline css, that would mean you would need to painstakingly go through every element to modify their styles. This isn't ideal, to say the least. Luckily, there are ways to make your styling more modular.

#### Selecting by ID
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

#### Selecting by Class
Although selecting by `id` works well and allows you to write more modular styles for your HTML pages, the `id` selector is ideally used to target specific elements as opposed to an entire class of elements (Note: you can have multiple elements with the same `id`, but CSS has another construct for targetting a group of elements.)

If you want to style a group of elements at once, you can specify the `class` attribute. It also makes more sense semantically to select a group of elements via an attribute called `class` than it does using an attribute called `id`, although both can be used to select a group of elements. 

You specify the `class` attribute the same way you the `id` attribute. Let's make some modifications to our `index.html`:
#### `index.html`
```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            .mainDiv {
            color:blue;
            }
            .secondaryDiv {
                color: red;
            }
        </style>
        <title>Hello world!</title>
    </head>
    <body>
        <!-- Put all content here. -->
        <div class="mainDiv">
        	<h1 id="coolID">Woah, this is really cool!</h1>
        	<p>This is my very first HTML Project!</p>
        </div>
        <div class="secondaryDiv">
            <p>This is cool content.</p>
        </div>
    </body>
</html>
```

We specified that the first div is part of the class `maindDiv` and we added a second div that is part of the `secondaryClass`. If you look at our `style` code now, we've identified the divs by `class` instead of `id`. Note, instead of prepending the name of the attribute with `#` like we did for `id`, we use `.` for classes instead. 

If you reopen your `index.html` with your browser:
![Alt text](html-tutorial/images/select-class.png?raw=true) 

So far, we've illustrated *internal style sheets*, and although they've made things simple to follow, you can imagine a scenario where you have many more elements in your HTML document, and you need to do a lot more styling: your HTML file will become unruly pretty quickly. Luckily, we can add even more modularity to our code. 

### Linking Style Sheets
For the sake of the examples we've been looking at, internal style sheets have worked fine simple because we don't have that much code to work with. But when you start creating your own websites, you'll quickly find that more modulairty would be incredibly helpful. If you have many HTML elements to keep track of and a lot of styling going on within those elements, an internal style sheet would be difficult to work with.

In general, you'll always want to encapsulate various parts of your project in different, well-named files for the sake of being more organized. It also makes sense to have your HTML code seperated from your CSS code-- it is much less confusing to work with when you have larger projects, and it is a good habit to get into. 

To link to a style sheet, you would add the following line within your `<head>` element:
```html
<!-- This is the only line we're changing right now. The rest of the file is the same. -->
<head>
    <link rel="stylesheet" type="text/css" href="styles.css">
<head>
```
Now, when your browser goes to render your html page, it will also link to your `styles.css` style sheet which will provide the styling for your page.

**Note:** We've used the `href` attibute before (when specifying the source for images and links), but it is important to note that must provide the full path of where the particular resource you are linking to is stored. If it's a link, it's the entire link; if it's an image or stylsheet, then you have to specify the path to the source.

For example: if the style sheet is located in the same directory as the HTML file you are linking it to, you can simple use `href="styles.css"`. But if your stylesheet is in a subdirectory called "styling", then you would use `href="styling/styles.css"`. 

Let's add a new subdirectory to our project structure called `styles`, and within this subdirectory add a file called `coolstyles.css`.

Our new file structure should look like this:
```
html-tutorial/
    index.html
    about.html
    goals.html
    experiment.html
    styles/
         coolstyles.css
    images/
```

Add this code to `styles.css`:
#### `styles.css`
```css
.mainDiv {
    color:blue;
}

.secondaryDiv {
    color: red;
 }
#coolID {
    color:blue;
}
```
And let's modify our `index.html`:
#### `index.html`

```html
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" type="text/css" href="styles/coolstyles.css">
        <title>Hello world!</title>
    </head>
    <body>
        <!-- Put all content here. -->
        <div class="mainDiv">
        	<h1 id="coolID">Woah, this is really cool!</h1>
        	<p>This is my very first HTML Project!</p>
        </div>
        <div class="secondaryDiv">
            <p>This is cool content.</p>
        </div>
    </body>
</html>
```

Now, if you reopen `index.html` with your browser, there shouldn't be any changes from the last time we opened it (we simply moved the styling components to a different file.)

You can have as many style sheets as you want, but in order to use them you have to be sure to include the `link` in the `head` portion of your HTML document. 

So far, we've covered the basics of HTML and styling with CSS, but there is a lot more cool styling that can be done with CSS to create awesome webpages. If you're interested in reading more, check out the following: https://www.w3schools.com/css/default.asp

## Interactivity with JavaScript
Now that we have basic functionality of a static website, we can start to focus on more advanced features of static websites using Javascript. JavaScript is an incredibly rich language and many of its features are beyond the scope of this tutorial, but there are specific things that we can do to make our basic websites even more awesome. 

For the purposes of this tutorial, we will turn our attention to **jQuery**, a JavaScript library that focueses on HTML docment manpulation, animation, event handling, and much more. 

When we say that jQuery is a JavaScript library, we simply mean that it contains pre-written JavaScript utilities that come packaged together nicely. JavaScript libraries provide a layer of abstraction from the messy implementation details that support those functionalities. In general, using libraries will save you a bunch of time while letting you do awesome things!

### Basic JavaScript Concepts
Before we dive into using JavaScript libraries, we should get a grasp of some very simple JavaScript syntax and concepts. Unlike HTML, the *hypertext markup language*, JavaScript is an actual programming language with more functionalities and capabilities. 

#### Variables
Let's write some basic Javacript code and see figure out what it does. 
```js
var flavor = "Chocalate";
console.log("The best icecream flavor is: " + flavor);
```
The first line `var flavor = "Chocalate";` is a variable declaration. It sets the value of `flavor` to the string `chocalate`. 

* In declaring a variable, we first wrote `var`, which is a keyword in Javascript that specifies the declaration of a variable. 
* `flavor` is the name of our variable. In general, the names of your variables can contain letters, numbers, dollar signs, or underscores. It is good practice to have descriptive variable names-- this will help you produce more readable code. 
    * **Note on variable names:** Contrary to popular belief, longer variable names don't affect the overal performance of your program (Assembly has no notion of variable names, but that's neither her nor there...). With that in mind, make your variables *descriptive enough* without being too verbose.
* Our variable here is a string, so we write `"chocalate"` with quotation marks around it. 
* Finally, all JavaScript statements are closed with a semicolon. Syntax can be a tricky thing when you're getting started-- don't feel pressure to memarize every little quirk within every language you end up working with. Google is every programmer's long-term auxillary memory!

The second line `console.log("The best icecream flavor is: " + flavor);` will print to the console: `The best icecream flavor is: chocalate`. 

In JavaScript, the `console.log()` function will print to the console. We *concatenated* our string with the variable value we set for `flavor`. But where does console.log() print to? If you open your browser you can open up dev tools (on chrome: `More tools > Developer tools`) and navigate to the `console` tab, you can write in the lines we wrote and see the correct output. Whenever you use `console.log()`, it will write the output to the console. 

**Concatenation** can be a tough conept to follow, so let's look at another example. 
```js
var subject = "Math";

console.log("My favorite class is: " + subject);

var otherSubject = "History";

console.log("I love " + subject + " and " + otherSubject + ".");
```

If you open up the console from your browser and execute the first two lines, the console should print `My favorite class is Math`; if you execute the next two lines, the console should print `I love Math and History.` 

Make note of the spacing we used when adding variables to our `console.log()` statement. We use `+` to concatenate strings with variables, and space accordingly to make the output look like we want it to. Feel free to experiement with spacing to see how it effects the output. 

#### Arrays
Another important featute that you may find useful when using JavaScript (or any other programming language for that matter) is the array.

```js
var testScores = [96, 95, 98, 100, 100, 65];
console.log("My first test score is: " + testScores[0]);
```

If you execute the following lines within the browser's console, you should see `My first test score is: 96`. But wait-- why is it 96 and not 95? Well, JavaScript arrays (and arrays within almost any other programming language you go on to work with) begin at *index 0* as opposed to *index 1*.

If you wanted to access the second element, you would use `testScores[1]`, the third with `testScores[2]`, the fourth with `testScores[3]` and so on and so forth.

You can declare an array like we did above, with instantiated values. In this case we are working with integer values, but you can easily have an array of strings as well: `var sandwiches = ["turkey", "tuna", "pb&j", "blt"];`

Arrays are super useful to encapsualte common data, and accessing various elements within an array is very simple. 

JavaScript is an awesome language that allows you to do many very cool things-- if you want a more indepth introduction, check out https://www.w3schools.com/js/default.asp

### JS and jQuery
Now let's see how we can use jQuery to do some cool stuff on our website. Inserting JavaScript into an HTML page is similar to inserting CSS. Add the following lines to your `index.html` direct below your opening `body` tag. 
```html
<body>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.3/jquery.min.js"></script>
    <script src="/js/index.js"></script>

    <!-- All of your other content remains the same -->
</body>
```
You insert JavaScript by using the `<script>` tag-- you have the specify a source which is where the JavaScript code should exist. We see two examples above. The first sets `src` to a URL, and the second sets it to a a file called `index.js` within a directors called `js`. Both are valid. The first line is actually *importing jquery* via google's hosting service, and the second is serving JavaScript from a local directory. 

#### jQuery Selectors
Just like we saw with CSS, you can specify elements you want to work with in jQuery by using selectors. The syntax for using selectors in jQuery is a little different, here are some basic examples: 

* `$("*")` -- Selects all elements.
* `$("h1")` -- Selects all `<h1>` elements
* `$("#coolName")` -- Selects all elements with id="coolName".
* `$(".coolName")` -- Selects all elements with class="coolName".
* `$(".coolName, .coolerName")` -- Selects all elements with class="coolName" or class="coolerName". 

To read more about various selectors in jQuery, check out: https://www.w3schools.com/jquery/jquery_ref_selectors.asp

When you use a selector like `$("p")`, you return an array of all the paragraph elements in the HTML page. So, as you might've guessed, you can do `$("p:)[0]` to select the first pagraph element, `$("p:)[1]` to select the second element, and so on and so forth. 

Let's experiment with our `index.html` file. Previously we added some lines that ensured our page would be accessing the jQuery library from Google, so if you open up your file with the browser, navigate to the console within the browser dev tools, you can run the following code and see the magic of jQuery.

```js
$('h1').html('lol');
``` 
This should replace the header text with "lol". If you want to revert the changes, just refresh the page. 

You can do even more:
```js
//Append another element to the end of a specified element 
$('p').append(' <a href="https://www.youtube.com/watch?v=bLHL75H_VEM">Click this!</a>');

//Append this HTML snippet after the selected element. 
$('p').after('<p>jQuery is awesome!</p>');
``` 
#### Handling Events
Our goal is to add some interactivity to our basic page, let's figure out how we can do that. Observe the following code: 
```js
$('p').on('click', function () {
    $(this).html('much wow');
});
```
Woah, that's pretty different from anything else we've looked at so far. While there does seem to be a lot going on here, you can figure out what this code does. We select every `<p>` element with `$('p')`, and then use jQuery to specify that when these elements are clicked, change the content to `much wow`. Copy and paste this code in to your `js/index.js` and try it in yor own browser. 

Let's look at this example a little closer: 
* `$('p')` -- Selects all `<p>` elements.
* `.on('Click', function() {...});` -- When a `<p>` element is clicked, run the anonymous function as it's callback.*
* `$(this).html('much wow')` -- When the `Click` event is received, change the content of every `<p>` tag to "much wow".

*An anonymous function is a function without a name. In this case, you see a function being called, but there is no function name. We won't cover functions in JavaScript, but if you would like to learn more, check out: https://www.w3schools.com/js/js_functions.asp 

A callback function is a function that is called immediately after a different funciton is completed running and has returned. In our case, the `on` function checks for the `click` event, and then calls the anonymous function as its callack. Callbacks won't be covered in depth here as they are a bit of a more advanced JavaScript topic, but if you want to learn more, check out: https://www.w3schools.com/jquery/jquery_callback.asp

Some other jQuery events: 
* `dblclick` -- Double click event.
* `mouseenter` -- Event for when mouse enters an element. 
* `mouseleave` -- Event for when mouse leaves an element.
* `keydown` -- Event for when a user presses a button. 
For further reading and more references, check out: https://www.w3schools.com/jquery/jquery_events.asp

#### Modifying CSS
Now that we know how to add some interactivity, let's see how we can go about manipulating the CSS on our page dynamically. 

Look at the following code: 
```js
$('p').on('click', function() {
  $(this).css({
    "color": "green",
    "font-weight": "700",
    "line-height": "40px",
  });
});
```
What's going on with in this snippet? 
We've already covered how the selector is called with the `click` event, and then calls an anonymous function as it's callback. Let's observe what happens within the callback:
`$(this).css({..});` -- Get the CSS of that particular element (`<p>` in this case).

Within the CSS call, we see that we are specifying CSS properties with key/value pairs. Note that each CSS property as well as its value is encapsulated within quotes. 

If you were to run this code, it would modify the stylin for every `<p>` tag when you click on it. 

This isn't an ideal solution since it will only change the style the one time you click the element-- what if you want it to change every time you click on it? 

Add the following to your `styles.css`:
```css
.coolText {
  color: green;
  font-weight: 400;
  line-height: 55px;
}
```
And then add the following snippet to your `index.js` file:
```js
$(document).ready(function() {
    // all custom jQuery will go here
    $('div').on('click', function() {
	  $(this).toggleClass('coolText');
	});
});
```
Now if you open `index.html`, you candan try this out!

Before your JavaScript code can go about using your custom jQuery code, it needs to verify that all the elements in the page have been properly loaded. Thus, in your JavaScript file you use `$(document).ready()` as your first function, and then pass a callback that will contain all your jQuery code. You need to vall `(document).ready()` when linking to jQuery locally and not when running jQuery code from within the console because when you run code in the console, you can be sure that all the elements have already been loaded (you wouldn't be able to use the browser console otherwise). Linking to jQuery within a JavaScript file you wrote yourself needs to wait for the page to load all the lements. 

Effectively, this code will wait for the document to be ready, and then after it verifies that the document is ready, it will call a function that contains all of your jQuery code. 

## Mini Project
Now that we've gone through these web development basics, you're in great shape to get started on your own project. You'll be armed with the basic code we've established in this tutorial, and insight into how to make static HTML web pages! 

Our final file structure: 
```
html-tutorial/
    index.html
    about.html
    goals.html
    experiment.html
    styles/
         coolstyles.css
    images/
```

Let's look at the final version of our files: 

##### `index.html`
```html
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" type="text/css" href="styles/coolstyles.css">
        <title>Hello world!</title>
        <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>        
        <script src="js/index.js"></script>
    </head>
    <body>
        <!-- Basic NavBar -->
        <ul>
          <li><a href="index.html">Home</a></li>  
          <li><a href="about.html">About</a></li>
          <li><a href="goals.html">Goals</a></li>
          <li><a href="experiment.html">Experiment</a></li>
        </ul>  

        <!-- Put all content here. -->
        <div class="mainDiv">
            
            <h1 id="coolID">Woah, this is really cool!</h1>
            <p>This is my very first HTML Project!</p>
        </div>
        <div class="secondaryDiv">
            <p>This is cool content.</p>
        </div>
    </body>
</html>
```

We've added a simple navigation list to travel between various pages.

#####  `about.html`, `goals.html`, `experiment.html`
```html
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" type="text/css" href="styles/coolstyles.css">
        <title>Hello world!</title>
        <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>        
        <script src="js/index.js"></script>
    </head>
    <body>
        <!-- Basic NavBar -->
        <ul>
          <li><a href="index.html">Home</a></li>  
          <li><a href="about.html">About</a></li>
          <li><a href="goals.html">Goals</a></li>
          <li><a href="experiment.html">Experiment</a></li>
        </ul>  
    </body>
</html>
```

##### `coolstyles.css`
```css
.mainDiv {
    color:blue;
}

.secondaryDiv {
    color: red;
 }
#coolID {
    color:blue;
}

.coolText {
  color: green;
  font-weight: 400;
  line-height: 55px;
}
```

##### `index.js`
```js
$(document).ready(function() {
    // all custom jQuery will go here
    $('div').on('click', function() {
	  $(this).toggleClass('coolText');
	});
});
```

**Your mission**: So far, you have a couple of HTML pages that link to eachother, all of which are loaded with jQuery, your `index.js` file, and your CSS styling within your `coolstyles.css`. Your job is to add content to all of these pages that utilizes the core concepts we covered here. That means you can add structured content using HTML tags, style them using CSS, and add interactivity using jQuery. Follow the paradigms we've worked on up to this point as a start, but don't be afraid to explore new ideas and constructs on your own!

Here are the bare minimum requirements of what this completed site should include: 
* In your `index.html`, add a description of what the the site is for. 
* In your `about.html`, include a little bit about yourself. That could mean text, it could mean wacky designs, selfies, or cat videos. 
* In your `goals.html`, reflect on what you've learned, and what you want to pursue next. 
* In your `experiment.html`, go wild. Do whatever you want, just make sure it's awesome. 

Not so bad, right? This mini project is meant to be more fun than it is difficult. I encourage you to explore the ideas we talked about and push yourself to the next level. You can combine a lot of what we covered in some very creative ways to create an awesome site. 

Some things you can try and explore on your own:
* A better looking Navigation bar... our navigation bar is pretty basic right now. For a more thorough look at CSS: https://www.w3schools.com/css/
* Animation with jQuery: http://api.jquery.com/animate/
* Explore awesome fonts from google: https://fonts.google.com/
* We didn't cover Bootstrap, but if you're feeling up to the challenge, you're at a place now where you can look into how to use it: http://getbootstrap.com/css/

## Conclusion
Congrats! You now have the knoweledge to create your own static websites. For some of you, this may be the beginning of your programming journey; for others, this might just be something you're learning for fun. Regardless of your prior experience, I hope this tutorial has inspired you to continue programming and finding new ways to express your creativity. Static websites are cool, but there is so much more to learn out there. 

In the course of working on the mini project my hope is that while this tutorial provided you with a good foundation, you still found yourself googling a million things in the process of building out whatever your vision was. That's good. Endlessely travelling through programming forums (stack overflow more often than not), is part of the growth of all programmers-- it means what you already know isn't sufficient to solve the problem at hand, so you need to strap on your thinking hat and search for clues that can help lead you to the answers you need. 




