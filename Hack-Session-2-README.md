# Hack-Session-2-README

## Table of Contents

- Getting Started
- Creating a Bootstrap Navbar
- Implementing a Meme Generator
- Useful JavaScript Syntax
  - jQuery

## Getting Started

Ensure that **in your HTML file**, inside your `<head>` `</head>` tags you include the following lines:

```
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
```

- The first link tag is similar to how we linked our **style.css** file to our HTML file. This time, however, the element fetches a CSS file from MaxCDN.
- The second `<script>` tag is used exclusively to include .js, or JavaScript files.

## Creating a Bootstrap Navbar

**Note:** This tutorial is not compatible with Bootstrap 4.0.0 beta.

In <a href="https://github.com/acm-hackschool-f17/Resources/blob/master/Hack-Session-1-README.md#HS1-creating-a-navigation-bar">Hack Session 1</a>, we showed how to make your own Navigation Bar by using and styling `<ul>`, `<li>`, and `<a>` tags.

This time, however, we'll showcase Bootstrap's Navigation Bar. With Bootstrap, a navigation bar can extend or collapse, depending on the screen size.

---

### Getting Started

**In your HTML file**, inside your `<body>` `</body>` tags, add:

```
<nav class="navbar navbar-default">
</nav>
```

- The `<nav>` tag defines a set of navigation links.
- Notice that NOT all links of a document should be inside a `<nav>` element. The `<nav>` element is intended only for major block of **navigation links**.

In Bootstrap, a standard navigation bar is created with `<nav class="navbar navbar-default">`.

**In your HTML file**, inside those `<nav>` tags, add:

```
<div class="container-fluid">
    <div class="navbar-header">
      <a class="navbar-brand" href="#">[Your Name Here]'s Website</a>
    </div>
    <ul class="nav navbar-nav">
      <li class="active"><a href="#">Home</a></li>
      <li><a href="#">Page 1</a></li>
      <li><a href="#">Page 2</a></li>
      <li><a href="#">Page 3</a></li>
    </ul>
</div>
```

- The `.container-fluid` class provides a container that spans the entire width of the space available.
- Inside this container, we use the Bootstrap classes `.navbar-header` and `.navbar-brand` to specify a title (which is a hypertext link that usually links to the home page of your website).
- As before, we then use `<ul>`, `<li>`, and `<a>` tags (along with some Bootstrap classes) to add links to our navbar.

**Save your HTML file**, then open it in a browser to see what we have:

<img src="https://lh3.googleusercontent.com/JLeBwpYyYqPT1JoCvAT6ZhHidXAO5nrDAPn4nLUA8I0Y1oY-7qMDby4HOCB7RUAmtN8zK_7gVdV99hwmIM_dt5Wrt09gWx8gziOVtZH6tslbUpgTham9El-nLBOf5GXOGhYJ5QIZ" width="700px"/>

Neat! But what if we wanted a sleeker design?

**In your HTML file**, replace the `.navbar-default` class in our `<nav>` tag with `.navbar-inverse`:

```
<nav class="navbar navbar-inverse">
```

**Save your HTML file** and refresh:

<img src="https://lh4.googleusercontent.com/G8y2wF1X0YIOr4JmB4i_sTHCgo-GA9DFO69pUmXfihOZDDkWJKyJ77R_JGw2uLd-dEGKZqGfFO8_r7U95MmFjx7Z6WMzjpSmXU2IbQCSTd86EaLs7F8t_-6mFG2NOAAJdgluGhRR" width="700px"/>

Nice! 

**Notice what happens when we resize our window to the point where the links no longer fit:**

<img src="https://lh4.googleusercontent.com/r3sw0DPEy64dYgBh-L4pDMe7GoB3IYJQdWE2NE0q-Utmq3_HmE1sJ6I-RxZ4pjmkP0e66QwfbIFMNYbaVpv_nAJh3zk0_jLm9A6m5CixJTG5CjYzXeDm4u_MCGAvjKwPrWGIQWuN" width="700px"/>

The Bootstrap navbar automatically creates a column display for you!

---

### Right-Aligned Links

The `.navbar-right` class is used to right-align navigation bar buttons.

Suppose your site has users. Let's add a "Sign Up" and "Login" button with icons.

**In your HTML file**, add another set of `<ul>` tags: 

```
<nav class="navbar navbar-inverse">
	<div class="container-fluid">
		<div class="navbar-header">
			<a class="navbar-brand" href="#">ACM Hack's Website</a>
		</div>
		<ul class="nav navbar-nav">
			<li class="active"><a href="#">Home</a></li>
			<li><a href="#">Page 1</a></li>
			<li><a href="#">Page 2</a></li>
			<li><a href="#">Page 3</a></li>
		</ul>
		
		<!-- BEGIN new code -->
		
		<ul class="nav navbar-nav navbar-right">
      		<li><a href="#"><span class="glyphicon glyphicon-user"></span> Sign Up</a></li>
      		<li><a href="#"><span class="glyphicon glyphicon-log-in"></span> Login</a></li>
    	</ul>
    	
		<!-- END new code -->
		
	</div>
</nav>
```

- In our `<ul>` tags, we used the `.navbar-right` class.
- We used the `.glyphicon-user` and `.glyphicon-log-in` Bootstrap classes to add some icons before our link text.
  - Note there is a space before "Sign Up" and "Login", otherwise the icons would be touching the text.

**Save your HTML file**, and refresh:

<img src="https://lh6.googleusercontent.com/OMNENghXvhSjMrxCn4998mXVYS6b9WkuqCampQBgi24MEctMc0SL0KSImce_KJO5wDbGIsHUBS5AwVVnBJVIHzff_S_syRgqxpJXLN-7EwMSKHJk1wKWc1Qv38jL3a-2pq8lo_zx" width="900px"/>

---

### Fixing the Navbar

To fix our navbar at the top or bottom of the page, all we have to do is add the Bootstrap class `.navbar-fixed-top` or `.navbar-fixed-bottom` to our `<nav>` tags!

**In your HTML file**, add the `.navbar-fixed-top` in addition to the `.navbar-inverse` class:

```
<nav class="navbar navbar-inverse navbar-fixed-top">
```

**Save your HTML file**, and refresh. If you have scrollable content following your navbar, you'll notice the navbar stays at the top of the screen even while you scroll!

## Implementing a Meme Generator

Arguably, every good website needs a meme generator. Let's build one using the tools at our disposal (HTML, CSS, Javascript)!

---

### Getting Started

Make sure you have the following three files ready to be edited:

- index.**html**
- style.**css**
- script.**js**

Ensure that you have linked jQuery and all of your files to your HTML file in your `<head>` tags

```
<link rel="stylesheet" type="text/css" href="style.css">
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
<script src="script.js"></script>
```

---

### Setting Everything Up

First let's add the HTML elements we'll need for our meme generator.

**In your HTML file,** add:

```
<div id="meme-image">
</div>
<input id="image-input" type="file" accept="image/*"/>
<input id="caption-input" type="text" value="Enter a caption"/>
<input id="submit-button" type="submit"/>
```

- We use `<input>` tags with the attribute `type="file"` to accept a user's files. We can further specify what files to accept using the `accept` attribute.
  - Note that the `accept` attribute only applies to `<input>` tags with `type="file"`

**In your CSS file,** add:

```
#meme-image {
	background-image: url('http://i0.kym-cdn.com/entries/icons/original/000/022/138/reece.JPG');
	background-size: cover;
	width: 500px;
	height: 500px;
	margin-top: 40px;
	margin-left: 40px;
}

#image-input {
	margin: 20px;
	margin-left: 40px;
}

#caption-input {
	margin-left: 40px;
}

#submit-button {
	margin-left: 40px;
}
```

---

### Uploading Images

**In your script.js file**, add:

```
function attachEventHandlers() {
	
}

$('document').ready(function() {
	attachEventHandlers();
});
```

