# Learn-Session-2-README

## Table of Contents
- **Learn Session 2**
	 - <a href="#LS2-what-is-bootstrap">What is Bootstrap?</a>
	 - <a href="#LS2-why-use-bootstrap">Why Use Bootstrap?</a>
	 - <a href="#LS2-getting-bootstrap">Getting Bootstrap</a>
	   - <a href="#LS2-bootstrap-cdn">Bootstrap CDN</a>
	 - <a href="#LS2-bootstrap-grid-system">Bootstrap Grid System</a>
	   - <a href="#LS2-grid-classes">Grid Classes</a>
	   - <a href="#LS2-useful-class-names">Useful Class Names</a>
	     - <a href="#LS2-container">container</a>
	     - <a href="#LS2-row">row</a>
	     - <a href="#LS2-col">col-\*-\*</a>
	   - <a href="LS2-grid-system-rules">Grid System Rules</a>
	 - Bootstrap Examples (for you to try)
	   - <a href="#LS2-three-equal-columns">Three Equal Columns</a>
	   - <a href="#mobile-and-desktop">Mobile and Desktop</a>
	 - <a href="#LS2-introduction-to-javascript">Introduction to Javascript</a>
	   - <a href="#LS2-using-the-console">Using the Console</a>
	   - <a href="#LS2-variables">Variables</a>
	   - <a href="#LS2-functions">Functions</a>
	   - <a href="#LS2-jquery">jQuery</a>
	     - <a href="#LS2-what-is-jquery">What is jQuery?</a>
	     - <a href="#LS2-using-jquery">Using jQuery</a>
- **Hack Session 2**
  - <a href="#HS2-getting-started">Getting Started</a>
  - <a href="#HS2-creating-a-bootstrap-navbar">Creating a Bootstrap Navbar</a>
    - <a href="#HS2-getting-started-navbar">Getting Started</a>
    - <a href="#HS2-right-aligned-links">Right-Aligned Links</a>
    - <a href="#HS2-fixing-the-navbar">Fixing the Navbar</a>
  - <a href="#HS2-implementing-a-meme-generator">Implementing a Meme Generator</a>
    - <a href="#HS2-getting-started-meme-gen">Getting Started</a>
    - <a href="#HS2-setting-everything-up">Setting Everything Up</a>
    - <a href="#HS2-entering-a-caption">Entering a Caption</a>
  - Useful JavaScript Syntax
    - jQuery

## <a id="LS2-what-is-bootstrap">What is Bootstrap?</a>

Bootstrap is a free front-end **framework** (collection of pre-written code) used for faster and easier web development. 

It includes HTML and CSS-based design templates for typography, forms, buttons, tables, navigation, modals, image carousels and many others, including optional JavaScript plugins.

## <a id="LS2-why-use-bootstrap">Why Use Bootstrap?</a>

Advantages of Bootstrap:

- **Easy to use:** Anybody with basic knowledge of HTML and CSS can start using Bootstrap
- **Responsive features:** Bootstrap's responsive CSS adjusts to phones, tablets, and desktops
- **Mobile-first approach:** In Bootstrap 4, mobile-first styles are part of the core framework
- **Browser compatibility:** Bootstrap is compatible with all modern browsers (Chrome, Firefox, Internet Explorer, Safari, and Opera)

## <a id="LS2-getting-bootstrap">Getting Bootstrap</a>

There are two ways to start using Bootstrap on your own web site:

- Download Bootstrap from getbootstrap.com
- Include Bootstrap from a CDN

For the purposes of Hackschool we will be using the second option.

---

### <a id="LS2-bootstrap-cdn">Bootstrap CDN</a>

A **CDN** is a Content Delivery Network. We can include Bootstrap in our HTML file from a CDN.

**In your HTML file**, in your `<head> </head>` tags include the following code:

```
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta/css/bootstrap.min.css">

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
```

- The first link tag is similar to how we linked our **style.css** file to our HTML file. This time, however, the element fetches a CSS file from MaxCDN.
- The second `<script>` tag is used exclusively to include .js, or JavaScript files. 
  - Bootstrap uses jQuery for JavaScript plugins (like modals, tooltips, etc). We will get to JavaScript later in this README.
  - Note that if you just use the CSS part of Bootstrap, you don't need jQuery.

## <a id="LS2-bootstrap-grid-system">Bootstrap Grid System</a>

Bootstrap's grid system allows up to **12 columns** across the page.

If you do not want to use all 12 columns individually, you can group the columns together to create wider columns:

<img src="https://lh3.googleusercontent.com/mfU_A8E8_kK-QKcjRuJOgw1tw4If1wIgvFa15paEyGVm6E1Zfh8GQrlBSvLin9q2XhiduQVD-QrvlrlRGXzj1RIBYQkDNq5PDtlyTr69C87UkOvhW4KU29d3yz6x99l79e_8QII6" width="600px">

---

### <a id="LS2-grid-classes">Grid Classes</a>

As mentioned above, Bootstrap allows your website to adapt to the screen size of the user. The Bootstrap grid system has four classes it uses to achieve this behavior:

- **xs** (for phones)
- **sm** (for tablets)
- **md** (for desktops)
- **lg** (for larger desktops)

The classes above can be combined to create more dynamic and flexible layouts.

**Note: You do not have to specify a separate website layout for each of the four classes. Classes scale up, meaning if you specify a layout for xs the other three classes will inherit the same layout.**

---

### <a id="LS2-useful-class-names">Useful Class Names</a>

Again, Bootstrap is a **framework**, which is a collection of pre-written code. In particular, it provides us with its own <a href="https://github.com/acm-hackschool-f17/Resources/blob/master/Hack-Session-1-README.md#HS1-classes">classes</a> that we can use to implement the design we want.

Some important class names are:

#### <a id="LS2-container">container</a>

- Fixed width container with widths determined by screen sites. Equal margin on the left and right.

- ```
  .container {
    padding-right: 15px;
    padding-left: 15px;
    margin-right: auto;
    margin-left: auto;
  }
  ```

#### <a id="LS2-row">row</a>

- Container for responsive columns.

- ```
  .row {
    margin-right: -15px;
    margin-left: -15px;
  }
  ```

#### <a id="LS2-col">.col-\*-\*</a>

- Responsive grid (span 1-12 column)
- The **first asterisk** is to be replaced by a <a href="#LS2-grid-classes">grid class</a>, i.e. xs, sm, md, or lg.
- The **second asterisk** is to be replaced by a number between 1-12, interpreted as the amount of columns the element takes up.

---

### <a id="LS2-grid-system-rules">Grid System Rules</a>

- Content should be placed within **columns**.

- Only **columns** may be immediate children of **rows**.

  - The definition of **children** is best described with an example:

    ```
    <div>
    	<p>Hello, World!</p>
    	<a href="www.google.com">Click Here for Google!</a>
    </div>
    ```

    There are three elements in this example: a `<div>` element, a `<p>` element, and an `<a>` element. 

    The `<p>` and `<a>` elements are **children** of the `<div>` element, and the `<div>` element is called the **parent** of the `<p>` and `<a>` elements.

    Child elements can be thought of as "inside of" their parent elements.

- Use **rows** to create horizontal groups of **columns**

- **Rows** must be placed within a **container** (fixed-width) or **container-fluid** (full-width) class for proper alignment and padding.


- Grid columns are created by specifying the number of 12 available columns you wish to span. 
  - For example, three equal columns would use three `.col-sm-4` (as 4+4+4 = 12).

## Bootstrap Examples (for you to try)

Try out the following Bootstrap configurations in your HTML file!

### <a id="LS2-three-equal-columns">Three Equal Columns</a>

```
<div class="container">
	<div class="row">
 		<div class="col-sm-4" style="text-align: center; border: 2px solid black">I take up 1/3 of the page!</div>
  		<div class="col-sm-4" style="text-align: center; border: 2px solid black">So do I!</div>
  		<div class="col-sm-4" style="text-align: center; border: 2px solid black">I do too!</div>
	</div>
</div>
```

<img src="https://lh3.googleusercontent.com/hhC8ZsHLUN-vTRkU6lT885O1QcXrPWU2s6q0-N7so-OaFkZx_2RGQ8S_zgQCjueuj9pGB12vXRAD09RAiQglelHjU1MhrDMt5bWGk73aeNGasocdY5ngxmXoDA3YQBNoVj4dGoeG" width="800px">

---

### <a id="LS2-mobile-and-desktop">Mobile and Desktop</a>

This example will look different depending on whether it is accessed on a computer or a cellphone.

```
<div class="container">
  <h1>Hello World!</h1>
  <p>Resize the browser window to see the effect.</p>
  <div class="row">
    <div class="col-xs-9 col-md-7" style="background-color:red;">.col-xs-9 .col-md-7</div>
    <div class="col-xs-3 col-md-5" style="background-color:lavender;">.col-xs-3 .col-md-5</div>
  </div>
  <div class="row">
    <div class="col-xs-6 col-md-10" style="background-color:lavenderblush;">.col-xs-6 .col-md-10</div>
    <div class="col-xs-6 col-md-2" style="background-color:lightgrey;">.col-xs-6 .col-md-2</div>
  </div>
  <div class="row" style="background-color:lightcyan;">
    <div class="col-xs-6">.col-xs-6</div>
    <div class="col-xs-6">.col-xs-6</div>
  </div>
</div>
```

<img src="https://lh5.googleusercontent.com/6HxkjmpsTH460KYle3rSdgb2HRzsCAH4A4Iqo9yM-hxepegiC9jMYmA1CF_zzT_b8vc8WeABNOjDT1ThG9m0c5jGJSCRfieW6nrssXf0SiVjY2TPElZq2g9U6o6fEFPKo7866ya5" width="800px"/>

---

## <a id="LS2-introduction-to-javascript">Introduction to JavaScript</a>

JavaScript is often referred to as the "programming language of the Internet".

JavaScript is one of the **3 languages** all web developers **must** learn:

1. **HTML** to define the content of web pages.
2. **CSS** to specify the layout of web pages.
3. **JavaScript** to program the behavior of web pages.

### <a id="LS2-using-the-console">Using the Console</a>

The **Console** object provides access to the browser's debugging console. The specifics of how it works vary from browser to browser, but there is a *de facto* set of features that are typically provided.

We will use it as a main tool to teach you JavaScript, so that you can see what each individual line of code does.

To open the Console in **Google Chrome**:

1. Right click on any page.
2. Select "Inspect" on the drop-down menu that appears.
3. If the Inspector (the bar that appears) is not at the bottom of your screen, click on the three vertical dots in the top-right corner of the Inspector. Select the third option (left-to-right) for the **Dock Side** preference.
4. Now that the Inspector is on the bottom of your screen, select the **Console** tab at the top of the Inspector.
5. We're ready to code!

**Note: In the following examples, the string [Enter] will represent you pressing the Enter key!**

---

### <a id="LS2-variables">Variables</a>

Variables are containers for storing data values.

**In the Console, type:**

```
var x = 5; [Enter]
var y = 10; [Enter]
x + y; [Enter]
```

You should see the number 15 printed (ignore the messages that say "undefined")! In this example, both x and y are variables.

In certain languages (like C++) you have to specify the **type** of a variable when you declare it. JavaScript, however, uses **type inference** to determine what type a variable is. Simply type the **var** keyword followed by your variable name to declare a variable.

**Note: To declare a constant variable, you use the let keyword. A constant variable can only be assigned a value once.**

#### Example

```
var a = 5;	// a is an integer!
let b = "cat";	// b is a constant string!
var c = false;	// c is a boolean!
```

---

### <a id="LS2-fucntions">Functions</a>

A JavaScript function is a block of code designed to perform a particular task. This function is executed when "something" invokes it (calls it).

**In the Console, type:**

```
function squareNum(n) { 
	return n * n;
} [Enter]
```

**Note: to add a newline without executing the code, type Shift+Enter**

Now type:

```
squareNum(9);
```

You should see the number 81 printed!

Let's break down the syntax:

**To declare a function:**

- **function** is a keyword that means you are about to declare a function.
- **squareNum** is the name of the function. This name can be whatever you want (within certain naming conventions).
- Parentheses () immediately follow the function name. The parentheses contain the **parameter(s)** of the function.
- Curly braces {} surround the **body** (code/content) of the function.
- When JavaScript reaches a **return statement**, the function will stop executing. If the function was invoked from a statement, JavaScript will "return" to execute the code after the invoking statement. Functions often compute a **return value**. The return value is "returned" back to the "caller".

**To call/invoke a function:**

- Write the name of the function followed by parentheses.
- Inside the parentheses, specify an explicit **value** for each of the function parameters.

---

### <a id="LS2-jquery">jQuery</a>

Now that we have the basic building blocks for JavaScript code, let's apply it to a real website!

1. Go to https://github.com/acm-hackschool-f17/session-2-learn
2. Click the "Clone or download" green button near the right side of the screen
3. Click "Download ZIP"
4. Open the downloaded file in Finder/Windows Explorer (should be a folder called "session-learn-2-master")
5. Navigate to the "final" folder
6. Open the **index.html** file in Google Chrome (drag the file into Google Chrome)
7. All set!

#### <a id="LS2-what-is-jquery">What is jQuery?</a>

**jQuery** is a lightweight, "write less, do more", JavaScript library (a collection of pre-written functions). The purpose of jQuery is to make it much easier to use JavaScript on your website.

jQuery takes a lot of common tasks that require many lines of JavaScript code to accomplish, and wraps them into methods that you can call with a single line of code.

#### <a id="LS2-using-jquery">Using jQuery</a>

Let's try one of these simple functions: **hide()**. Just as its name suggests, hide() will hide the specified element.

**In the index.html you just opened, <a href="#LS2-using-the-console">open the Console</a>:**

Type:

```
$(".image"); [Enter]
```

You should see an **array** of several HTML elements printed out. An array is a collection of similar values (e.g. array of numbers, array of strings).

These are the exact same elements displaying all of the smol kittens on the web page! We have used jQuery to **select** the element. 

Let's break down the syntax:

- jQuery syntax is tailor-made for **selecting** HTML elements and performing some **action** on the element(s).

- Basic syntax is: **$(selector).action()**

  - A $ sign to define/access jQuery
  - A (**selector**) to "query (or find)" HTML elements
  - A jQuery **action**() to be performed on the element(s)

- Examples

  ```
  $("p").hide() - hides all <p> elements.
  $(".test").hide() - hides all elements with class="test".
  $("#test").hide() - hides the element with id="test".
  ```

- **Notably, jQuery uses CSS syntax to select elements!**

Looking back at what we typed above, we used jQuery **to select all elements with class="image"!**

---

Let's select the first image in this array and assign it to a variable.

**In the Console, type:**

```
let firstImage = $(".image")[0]; [Enter]
```

Again, $(".image") will return an array of 12 image elements. We use square brackets [] to access a certain element of the array. Arrays index from 0, meaning [0] accesses the first element of the array, [1] accesses the second element, and so on.

**Now, type:**

```
$(firstImage).hide(); [Enter]
```

The first smol kitten should have disappeared! Let's readd him/her:

**Type:**

```
$(firstImage).show(); [Enter]
```

The smol kitten should have returned. :')

---

# <a id="hack-session-2">Hack Session 2</a>

## Table of Contents

- <a href="#HS2-getting-started">Getting Started</a>
- <a href="#HS2-creating-a-bootstrap-navbar">Creating a Bootstrap Navbar</a>
  - <a href="#HS2-getting-started-navbar">Getting Started</a>
  - <a href="#HS2-right-aligned-links">Right-Aligned Links</a>
  - <a href="#HS2-fixing-the-navbar">Fixing the Navbar</a>
- <a href="#HS2-implementing-a-meme-generator">Implementing a Meme Generator</a>
  - <a href="#HS2-getting-started-meme-gen">Getting Started</a>
  - <a href="#HS2-setting-everything-up">Setting Everything Up</a>
- Useful JavaScript Syntax
  - jQuery

## <a id="HS2-getting-started">Getting Started</a>

Ensure that **in your HTML file**, inside your `<head>` `</head>` tags you include the following lines:

```
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
```

- The first link tag is similar to how we linked our **style.css** file to our HTML file. This time, however, the element fetches a CSS file from MaxCDN.
- The second `<script>` tag is used exclusively to include .js, or JavaScript files.

## <a id="HS2-creating-a-bootstrap-navbar">Creating a Bootstrap Navbar</a>

**Note:** This tutorial is not compatible with Bootstrap 4.0.0 beta.

In <a href="https://github.com/acm-hackschool-f17/Resources/blob/master/Hack-Session-1-README.md#HS1-creating-a-navigation-bar">Hack Session 1</a>, we showed how to make your own Navigation Bar by using and styling `<ul>`, `<li>`, and `<a>` tags.

This time, however, we'll showcase Bootstrap's Navigation Bar. With Bootstrap, a navigation bar can extend or collapse, depending on the screen size.

------

### <a id="HS2-getting-started-navbar">Getting Started</a>

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

------

### <a id="HS2-right-aligned-links">Right-Aligned Links</a>

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

------

### <a id="HS2-fixing-the-navbar">Fixing the Navbar</a>

To fix our navbar at the top or bottom of the page, all we have to do is add the Bootstrap class `.navbar-fixed-top` or `.navbar-fixed-bottom` to our `<nav>` tags!

**In your HTML file**, add the `.navbar-fixed-top` in addition to the `.navbar-inverse` class:

```
<nav class="navbar navbar-inverse navbar-fixed-top">
```

**Save your HTML file**, and refresh. If you have scrollable content following your navbar, you'll notice the navbar stays at the top of the screen even while you scroll!

## <a id="HS2-implementing-a-meme-generator">Implementing a Meme Generator</a>

Arguably, every good website needs a meme generator. Let's build one using the tools at our disposal (HTML, CSS, Javascript)!

------

### <a id="HS2-getting-started-meme-gen">Getting Started</a>

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

------

### <a id="HS2-setting-everything-up">Setting Everything Up</a>

First let's add the HTML elements we'll need for our meme generator.

**In your HTML file,** add:

```
<div id="meme-image">
		<p id="caption">Enter text</p>
</div>
<input id="caption-input" type="text" value="Enter a caption"/>
<input id="submit-button" type="submit"/>
```

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

#caption {
	padding-top: 40px;
	width: 100%;
	text-align: center;
	font: bold 50px Impact, Serif;
	color: white;
	text-shadow:
    -3px -3px 0 #000,
    3px -3px 0 #000,
    -3px 3px 0 #000,
    3px 3px 0 #000; 
}

#caption-input {
	margin: 20px;
	margin-left: 40px;
}

#submit-button {
	margin-left: 40px;
}
```

- We use the `text-shadow` property to make it appear that our text has a border.

------

### <a id="HS2-entering-a-caption">Entering a Caption</a>

**In your script.js file**, add:

```
function attachEventHandlers() {
	$("#submit-button").on('click', updatePhoto);
}

function updatePhoto(event) {
  	// TODO
}

$('document').ready(function() {
	attachEventHandlers();
});
```

- In our "main()" function we call the function attachEventHandlers()
- We add an event handler to our submit button that calls the function `updatePhoto()` after the button is clicked.

Let's write the `updatePhoto()` function!

**In your script.js file**, add:

```
function updatePhoto(event) {
	var caption = $("#caption-input").val();
	$("#caption").html(caption);
}
```

- `#caption-input` grabs our `<input>` element, and the function `val()` gets its value (a user-entered string).
- We use the `.html()` function to alter the raw HTML content inside our `<p>` tags.

Easy at that!

**Save all of your files**, and try it out:

<img src="https://lh4.googleusercontent.com/UP0_ot-L3Nte1drN8Keuhoe8DwnGpjwGNS4DBwUtF5rq57eo4lzg3mbSTxLIgeBvbStYjpij80VLyUl8_M2zGrELVWhGGVFkY3LD3PD3YmDntciLhdMh847eBAM-RCfZ9dD1xco6" width="700px"/>

