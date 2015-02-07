---
layout: default
title: Class Notes
permalink: /class-notes/
---

## Class 5: Introduction to HTML

We covered HTML tags and attributes, Brackets and developer tools.

### What's What?

- Web Design
    + The process of planning, structuring and creating a website.
- Web Development
    + The process of programming dynamic web applications (remember, that just means websites).
- Front End
    + The outwardly visible elements of a website or application.
- Back End
    + The inner workings and functionality of a website.

### Anatomy of an HTML element

- Element
    + An individual component of HTML
    + heading, paragraph, list item, table, image, etc
- Tag
    + Marks the beginning and end of an element (usually)
    + `<tagexample>Stuff n Junk </tagexample>`
- Types of elements
    + Container element
        * A paragraph element contains text <p>some text</p>
- Stand alone element
    + Cannot contain anything else
        * `<br>`
        * `<img src="http://placekitten.com/300/350" alt="what else but a kitten">`
- Attribute
    + Provides additional information about an element
        * Class, ID, style, source
    + Goes inside the opening tag, before the right angle bracket (see the img example above)
    + Global attributes are available to all elements
        * <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes" title="Global Attributes">Global Attributes</a>
- Value
    + The value assigned to an attribute
    + The value is in side the quotation marks
        * `<a href="http://google.com" title="Google">Link to Google</a>` in this case both http://google.com and Google are values assigned to the href and title attributes.

### HTML Structure

<img src="../images/html-structure.png" alt="the basic html layout of a page">

- Everything visible on your page goes between the `<body>` tags.
- Nesting
    + Some elements can nest inside another element
    + The first element to open must be the last to close.
        * `<p>I love <a href="https://www.petfinder.com/" title="Pet Finder">puppies</a> so much!</p>` The `<p>` is the first to open and the last to close.

### HTML Elements

We covered a ton of elements! To see all the elements available to you check out the <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element" title="Mozilla Developer Network">Mozilla Developer Network</a>.

- Important points to remember:
    + HTML tags are *not* presentational. They mean something and should be used to appropriately attribute that meaning to content. <a href="http://codepen.io/e-to-the-m/pen/QwMVRX?editors=110" title="An example about semantic HTML at CodePen">Example</a>
    + `<em>` emphasizes text. If your text doesn't need emphasis but just needs to be italic, we will do that with CSS.

- Elements we covered
    + Paragraph `<p>`
    + Headings `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`
    + Emphasized text `<em>`
    + Important text `<strong>`
    + Anchor `<a>`
        * Learn more about relative and absolute paths
            - <a href="http://www.coffeecup.com/help/articles/absolute-vs-relative-pathslinks/" title="Absolute Vs. Relative Paths/Links">Absolute Vs. Relative Paths/Links</a>
            - <a href="http://css-tricks.com/quick-reminder-about-file-paths/" title="Quick Reminder About File Paths">Quick Reminder About File Paths</a>
    + Images `<img>`
        * Remember that the Internet is made up of <del>cats</del> <ins>squares</ins>. <a href="http://codepen.io/e-to-the-m/pen/zyljo?editors=110" title="An illustrative image experiment in CodePen">See an example</a>.
    + Line Break `<br>`
    + Lists
        * Ordered Lists `<ol>`
        * Unordered Lists `<ul>`
        * List Items (for both ordered and unordered lists) `<li>`
    + <a href="https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Sections_and_Outlines_of_an_HTML5_document" title="Sections and Outlines of an HTML5 Document">Sections and Outlines of an HTML5 Document</a>
        * Header `<header>`
        * Navigation `<nav>`
        * Main `<main>`
        * Section `<section>`
            - A logical or thematic grouping of content that usually contains a heading.
        * Article `<article>`
            - A self-contained piece of content. It would still make sense if it was removed from the context of the page.
        * Footer `<footer>`

### Developer Tools

You can use what works for you, Chrome has built in developer tools as does Firefox, Safari and Internet Explorer. You can also download Firebug for Firefox.

- Developer tools allow you to:
    + See the HTML of a page
    + Edit and rearrange the HTML elements
    + Examine the box model of an element (we'll talk more about box model in next Saturday's class)
    + Edit the CSS
    + And more, all without damaging anything.
- <a href="http://www.html5rocks.com/en/tutorials/developertools/part1/" title="Introduction to Chrome Developer Tools, Part 1">Introduction to Chrome Developer Tools, Part 1</a>

### Accessibility

You all heard me talk about accessibility several times. Now is the time to get in the habit of building your sites with all your users in mind. Remember, the more people that can consume your content, the better. <a href="http://a11yproject.com/" title="The Accessibility Project">The Accessibility Project</a> is a great place to start.

## Class 8: Introduction to CSS (Cascading Stylesheets)

### Tables

- Tables are for tabular data - **only**
- Parts of a table
	+ Table `<table>`
	+ Table Header (row) `<thead>`
	+ Table Body `<tbody>`
	+ Table Footer (row) `<tfoot>`
	+ Table Row `<tr>`
	+ Table Header (cell) `<th>`
	+ Table Data (cell) `<td>` 
	
<img src="../images/table-structure.png" alt="the basic html layout of a table">


[Table Example](http://codepen.io/e-to-the-m/pen/JorgNj)

- Table Attributes
	+ Make a cell span multiple rows `<td rowspan="2">`
	+ Make a cell span multiple columns `<td colspan="2">`
	
- Next Steps
	+ Watch this old (2009) [video](http://css-tricks.com/video-screencasts/61-basic-table-styling/) (you can skip 4:30-6:20 which is basically an add) about styling tables	

### HTML Entities

[Unicode Character Table](http://unicode-table.com/en/)

`<p>I am going to the caf&eacute;.</p>`
<p>I am going to the caf&eacute;.</p>

### What is CSS?

- HTML provides the structure, CSS provides the style
- CSS stands for **C**ascading **S**tyle **S**heets
- CSS Structure `p { font-weight: bold; }`

### CSS Properties + Values = Rules

- In the above example
	+ `p` is the selector
	+ `font-weight` is the property
	+ `bold` is the value
		* property + value = declaration (block)
			- declaration blocks always start with a left curly brace `{` and end with a right curly brace `}`
			- the property is separated from the value by a colon `:`
			- declaration blocks contain one or more declarations separated by a semicolon `;`
		* selector + property + value = rule (also called a rule set)

### What is the Cascade?

- All things being equal (see specificity) the last rule in CSS will be the one that is followed.
- In the example below the text is green because it comes after the rule that calls for the text to be red.

`p { color: red; }`

`p { color: green; }`

<p style="color: green;">I am going to the caf&eacute;.</p>

### Selectors

How do we tell our CSS what to target?

- HTML element

    `p { color: green; }`
    
	+ Give all paragraph elements a text color of green

	`p a { text-decoration: none; }`
	+ Turns off underline for all links (anchors) inside a paragraph.
- Class (remember class is a global HTML attribute and can be used on all HTML elements)

    `<p class="highlight">This is highlighted text.</p>`
    
    `p.highlight { color: yellow; }`
    + Give all paragraphs with a class of highlight a text color of yellow
	+ A page can contain multiple instances of a class
- ID (also a global HTML attribute)

    `<p id="first">This is the first paragraph.</p>`
    
    `p { font-size: 14px; }`
    
    `p#first { font-size: 20px;`
    + Give all paragraphs a font size of 14 pixels, give paragraphs with an ID of first a font size of 20 pixels

### Specificity

How does the CSS know which rules to follow?

1. The Cascade
2. Specificity

[CSS Specifishity](http://www.standardista.com/css3/css-specificity/)

### Great, how do I get CSS on my page?

- Inline (Ugh)
	+ Is an HTML attribute
	+ Only affects the HTML element it is within
	+ Is not maintainable
	
	`<p style="color: blue; font-size: 14px;">This is a paragraph with blue text and a 14 pixel font size.</p>`
- Embedded (Boo)
	+ Goes inside the `<head>` tag
	+ Only lives on that page so must be repeated on every page where you want styling
	
			<!DOCTYPE html>
			<html>
			<head>
				<title>Best Page Evar</title>
				<style type="text/css">
					body {
						color: green;
						font-size: 12px;
					}
				</style>
			</head>
			<body>

- With a `<link>` (Yay!)
	+ Why is this better?
		* Maintainable, all the code lives in one place
		* Global, the styles apply to your site, not your page or a single element
		
		`<link rel="stylesheet" href="path/to/stylesheet.css">`
		* You can build conditions to support IE browsers
		
		`<!--[if lt IE 9]>`	
		
			`<link rel="stylesheet" href="path/to/other-stylesheet.css">`
			
		`<![endif]-->`

### CSS for Typography

- `color`
	+ color name `green`
	+ hexadecimal value `#00ff00`
	+ rgb (red, green, blue) value `rgb(0, 255, 0)`
	+ [ColorHexa](http://www.colorhexa.com/)
- `font-weight`
	+ `normal` or `400`
	+ `bold` or `700` use this instead of strong
	+ `bolder`
		* One font weight darker than the parent element (among the available weights of the font).
	+ `lighter`
		* One font weight lighter than the parent element (among the available weights of the font).
	+ `100`, `200`, `300`, `400`, `500`, `600`, `700`, `800`, `900`
		* If you use a font only has normal and bold weights the 100-500 will be `normal` and 600-900 will be `bold`
-  `font-size`
	+ pixels `14px`
	+ percent `50%`
	+ ems `1em`
- `font-family`
	+ font stacks
	+ `"Gill Sans Extrabold", Helvetica, sans-serif`
	+ [8 Definitive Font Stacks](http://www.sitepoint.com/eight-definitive-font-stacks/)
- `font-style`
	+ `normal`
	+ `italic` use this instead of `<em>`
	+ `oblique`
- `text-decoration`

[Look up more CSS properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)

- Remember you can use dev tools to show the hover state of links

### Pseudo Selectors

- `:hover`
-  `:active`
-  `:visited`

[Pseudo Selectors](http://css-tricks.com/pseudo-class-selectors/) 

### Google Fonts

- To use Google Fonts
	+ Use `@import`
	+ Use `<link>`
	+ Use javascript
	
[Google Fonts](https://www.google.com/fonts)

[Code Pen Example](http://codepen.io/e-to-the-m/pen/siqav)

### @font-face

- Fonts live in a folder, just like your CSS

		@font-face {
	
			font-family: 'Font Name';
		
			src: url('path-to-font.woff') format('woff'),
		
				 url('path-to-font.ttf') format('truetype'),
			 
		}

[Font Squirrel](http://www.fontsquirrel.com/)

[Using @font-face](http://css-tricks.com/snippets/css/using-font-face/)