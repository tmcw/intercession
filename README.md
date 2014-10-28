
## hints

* https://help.github.com/articles/markdown-basics
* http://guides.github.com/overviews/mastering-markdown/

quick:

```md
![](urltoimage.png)

[this is a link](http://tothisurl.com)

> this is a quote
```

![](urltoimage.png)

[this is a link](http://tothisurl.com)

> this is a quote


## intersession

I'm teaching an intersession class with my sister at [Millbrook School](http://www.millbrook.org/).
This repository is where I'm going to manage resources, recommendations, and other plans.

The challenge is to get 9th and 10th graders with no previous experience
interested in computing in a creative sense.

## Presentations

* [HTML](https://docs.google.com/presentation/d/1eM7T9WoA76fUBN8RuuuBNuJqFi4d3AIprcM-T0rR0nM/pub?start=false&loop=false&delayms=3000)
* [CSS](https://docs.google.com/presentation/d/1N6Bq7yFdyK1L1y5A3kfw5qn4aS9tP-dug5Ceyl_mfZQ/pub?start=false&loop=false&delayms=3000)
* [JavaScript](https://docs.google.com/presentation/d/1R5Vm_H0wUBjKO-rh2w_UkA1Bv_VCAbfYW1nl3avgvWw/pub?start=false&loop=false&delayms=3000)

## Phases

### Hacking

Let's change how things look first! This means we'll be changing HTML and CSS. Let's talk about them later and mess with them now.

Let's start by hacking. The nice thing about the internet is that pretty much
everything you see, you can see how it works and change how it works. Looking
at other people's work and tweaking it is how lots of people learn.

Let's start by opening up [millbrook.org](http://millbrook.org/) in Google Chrome.
Open up Developer Tools & let's start hacking. Change the text 'Welcome to Millbrook School'
to whatever you like. Then click on the `<body>` tag and change its color to something
else, like `red`.

Okay! Next challenge: let's change **how something works**. Open up

	http://nebez.github.io/floppybird/

And open up your web developer tools, open `main.js` and look at the code. Crazy, right! Anyway, play the game a little. At the top of the code, you can see

```js
var gravity = 0.25;
var velocity = 0;
var position = 180;
var rotation = 0;
var jump = -4.6;
```

Let's mess with these a little. In your Console, type

```js
gravity = 0;
```

And press **enter**. To space! You can do the same with the other stuff, like

```js
jump = 10;
```

### Building

Okay, let's make something simple. First, review your parts:

[HTML Presentation](https://docs.google.com/presentation/d/1eM7T9WoA76fUBN8RuuuBNuJqFi4d3AIprcM-T0rR0nM/pub?start=false&loop=false&delayms=3000)

HTML is the most basic part of a webpage. It's where you put content and structure: HTML has stuff like links, forms, and references to stuff like images, styles, and videos that are combined at the last minute into the fun mishmosh that is the internet.

[CSS Presentation](https://docs.google.com/presentation/d/1N6Bq7yFdyK1L1y5A3kfw5qn4aS9tP-dug5Ceyl_mfZQ/pub?start=false&loop=false&delayms=3000)

CSS makes HTML look good: without CSS, HTML pages look a little blah, with Times New Roman everywhere. CSS basically lets you make rules that every time you add a link or a title in HTML, it'll look like something.

[HTML + CSS (classes)](https://docs.google.com/presentation/d/1qv-ZF-bo9SGfJmQn8clhmqhAgGRDfB8Z7iCyigYFSbE/pub?start=false&loop=false&delayms=3000)

Javascript makes things interactive: unlike HTML & CSS, it's a programming language, and there's a lot more of it. But it's cool.

### HTML

Open up [jsbin](http://jsbin.com/). This looks a lot like your browser's tools except it's made for building things from scratch, not just messing with them. Let's start by making webpages about our favorite things. You can just edit the text 'Make something amazing with the web' but that doesn't look too cool. Let's learn a little HTML.

Okay, so when you open up jsbin, there'll be some HTML that looks like

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>JS Bin</title>
</head>
<body>

</body>
</html>
```

So much `<` and `>`! Let's break it down. An HTML tag is a word between `<` and `>`, and then that word contained by `</` and `>`. Basically these say 'Start' and 'End'. So let's add some stuff in the `body` part of the page, where content goes!

```html
<body>
hi!
</body>
```

Dress it up a bit?

```html
<body>
hi <strong>there</strong>!
</body>
```

Yep, you guessed it - `strong` makes things bold. Try with a few other tags:

* `em`
* `strong`
* `button`

You might notice that you need to change both the starting and ending tag every time. HTML is picky like this: if you have things start and end, they need to start and end in the right order. It's kind of like a book:

```
start BOOK
	start INTRODUCTION
		this is my book
	end INTRODUCTION
	start TEXT
		For sale, baby shoes, never worn
	end TEXT
end BOOK
```
It wouldn't make sense to end the book before the very end, or to end the introduction after you've started the text.

Okay!

### Style

You may have noticed that things don't look all that great. Let's fix that with CSS.

Copy and paste this HTML:

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>JS Bin</title>
  <style>
    body {
      font-family:sans-serif;
    }
  </style>
</head>
<body>
Hello, there.
</body>
</html>
```

See the new addition to this? The `style` tag adds CSS to your page. CSS is a language that styles things in HTML. Basically it reaches out, `selects` something from the page, like `body`, and then applies `rules` to them. So the part that says

```css
body {
```

Is a selector, and

```css
font-family:sans-serif;
```

is a rule. Try adding another rule:

```css
color:red;
```

On the line after `font-family:sans-serif;`. This'll make everything red. Cool! Want more? Check out [cssbasics.com](http://www.cssbasics.com/introduction-to-css/) for more possibilities - there are lots and lots of rules you can try to change pretty much anything about styles.

### Javascript

Okay, let's make the page do something!

```js
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>JS Bin</title>
</head>
<body>
  Hello, there. <button id='hello'>Say hi!</button>
  <script>
    document.getElementById('hello').onclick = function() {
      alert('hi!');
    }
  </script>
</body>
</html>
```

And click the button. This is using **Javascript** to look for the button `document.getElementById('hello')` and every time someone clicks it `.onclick` to alert the user hi! `alert('hi')`. We'll go into more detail about JS in a bit, but first let's round up a bit:

---

So we've learned that HTML contains content, CSS styles it, and Javascript makes it interactive. The three are different languages with different rules, but their interaction is what makes a web page complete - you can have a link written in HTML, styled in CSS, that does something cool with Javascript.
