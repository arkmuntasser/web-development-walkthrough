# HTML

The foundation of every website is HTML. HTML is what gives our sites, apps, and content form, meaning, and structure.

To build a website, you only need HTML. Files in folders.

## Syllabus:

1. Creating your first HTML document
2. `<html>`, `<head>`, `<body>`
3. Semantic HTML
4. Adding images to your page
5. Accessibility
6. Making multiple pages
7. Linking pages
8. Using classes and BEM-notation to better organize and refine your HTML

## Exercises

By the end of the these exercises are to be done in the `/exercise` folder we should end up with something similar to what is seen the `/demo` folder.

If you get stuck, you can always reference the code in the demo folder as needed. If you learn better be seeing the solution first, then by all means do so. This is your resource; use it in the manner that works best for you.

### Creating your first HTML document

To kick us off, we're going to need a file to work in for our homepage.

> *Create a new file called `index.html` inside the `/exercise` folder.*

Why is this file called 'index'? Why not 'home' or 'homepage' or 'my-cool-site'? Well, it very well could be those things if you wanted it to be. It's not a strict rule that you have to call the homepage HTML file 'index', but your life as a web developer will be a lot easier if you do.

By default, every web server is setup to expect an `index.html` file. And because of this, if you were to host this file at 'www.my-cool-site.com' you would be able to just type in that URL as is and see your page. But if your homepage was called `my-site.html` then you would need to enter the URL 'www.my-cool-site.com/my-site.html' which is fine, but not as nice looking or easy to remember. You could modify the configuration of your server to make it work with a filename other than `index.html`, but you would be breaking with an understood best practice and some hosting providers wont let you make this type of change.

So let's keep it at `index.html`.

### `<html>`, `<head>`, `<body>`

Now that we have our HTML file, open it up in your text editor of choice. I prefer [VS Code](https://code.visualstudio.com/), but you can use whichever editor you're most comfortable with.

Any worthwhile text editor will have an autocomplete suggestion if you start type 'html'. Highlight the suggestion with the arrow keys and hit either `tab` or `enter` depending on how your editor is configured.

You should get something similar to this:

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta http-equiv="X-UA-Compatible" content="ie=edge">
	<title>Document</title>
</head>
<body>
	
</body>
</html>
```

If your editor did not provide you an autocomplete suggestion, you can copy/paste the code above.

Let's break down what we've got going on here.

#### `<!DOCTYPE html>`

The doctype test the browser what version of HTML we're going to be using. Technically, we are on version 5 at the moment, but HTML no longer really has a version like it did in the past. HTML5 was meant to be the last major version.

This doesn't mean that HTML wont change or it wont get anything added to it, quite the opposite actually! With the move to HTML5 there is now just HTML: a living spec that can be added to and evolved as the web evolves.

#### `<html>`

This formally starts the HTML document defining our page. You'll notice the `lang="en"` attribute. This informs the browser and visitor that the language of this page is English. If you will be using a different language than English, you can update the "en" with the appropriate [locale string for your desired language](https://www.science.co.il/language/Locale-codes.php).

#### `<head>`

This tag is where we define a number of items pertaining to the page such as whether it's responsive, the title of the page, any resources you may need for styles or functionality and fonts.

#### `<meta>`

With these tags we can define a number of different things about the page. Let's breakdown the 3 in the example above:

##### `<meta charset="UTF-8">`

Here we define the character encoding we want to use for the page. [UTF-8 is the Unicode character](https://en.wikipedia.org/wiki/UTF-8) set that encompasses pretty much every character you could want to type. You don't need to change this.

##### `<meta name="viewport" content="width=device-width, initial-scale=1.0">`

With this, we are ensuring that the site is responsive.

This defines the viewport to have a width equal to the device width. Here 'device width' is a bit confusing as it makes it sound like it's referring to physical hardware like a phone or tablet, but it actually means the size of the browser window.

Next it sets the initial scale to 1. You can think of this as the zoom level of the page like when you pinch-to-zoom on a page. By default, we want everything visible and not zoomed in our out so we set it to 1.

##### `<meta http-equiv="X-UA-Compatible" content="ie=edge">`

This is to help ensure compatibility with older version of Internet Explorer. If you don't need to support Internet Explorer, you can actually delete this line, but leaving it in wont hurt anything.

#### `<title>`

This controls the title of the page; specifically it controls the text that shows in the tab in your browser.

#### `<body>`

Finally, the body tag is where the actual content of the page will live and where we'll be doing all of our work for the remainder of this section covering HTML.

### Semantic HTML

