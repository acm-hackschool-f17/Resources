# HTML/CSS Review

## What is HTML?

HTML stands for **Hyper Text Markup Language** and is used to design and structure websites.

HTML elements are the most basic building blocks for all web pages, and they are represented by **tags**. HTML tags label pieces of content such as "heading", "paragraph", "table", and so on. Browsers do not display the HTML tags, but use them to render the content of the page

## Getting Started

1. Create a folder on your Desktop named "MyWebsite" (or anything else you want)
2. In a text editor (**Sublime Text** recommended), create a new **empty** text file. Name it **index.html**, and save it inside the folder you created in Step 1. 
3. We're ready to start coding!

## HTML Tags

As mentioned above, all HTML elements are represented by tags. Tags have the following form:

```
<tagname>content goes here...</tagname>
```

HTML tags normally come **in pairs** like \<p> and \</p>. 

The first tag in a pair is the **start/opening tag,** and the second tag is the **end/closing tag**. 

The end tag is written like the start tag, but with a **forward slash** inserted before the tag name.

## Creating a Basic HTML Page

All HTML documents begin with the following line:

```
<!DOCTYPE html>
```

It declares your file as HTML. Add this line to your **index.html** file.

---

Next, we are going to define the sections in our file where we will put meta information about the document and the actual visible page content.

Underneath the `<!DOCTYPE html>` line, add:

```
<html>
<head>
	
</head>
<body>

</body>
</html>
```

Let's break each tag down:

- The `<html>` element is the root element of an HTML page. The html tags will surround **all** of the other HTML content that you write.
- The `<head>` element contains meta information about the document. In simplest terms, meta information is **information about information**. In this context, meta information can include a website's description, name, and date it was last modified.
- The `<body>` element contains the visible page content. It will surround all of the HTML elements you want the user to actually see.

---

Let's give our website a name!

Inside the `<head> </head>` tags, add:

```
<title>[Your Name Here]'s Website</title>
```

- The `<title>` element specifies a title for the document and is the text you'll see inside your page's tab on a web browser.

---

Finally, inside your `<body> </body>` tags, add:

```
<h1>My First Heading</h1>
<p>My first paragraph.</p>
```

- The `<h1>` element defines a large heading.
- The `<p>` element defines a paragraph.

## Viewing your Website

Altogether, your **index.html** file should look like this:

```
<!DOCTYPE html>
<html>
<head>
	<title>[Your name here]'s Website</title>
</head>
<body>
	<h1>My First Heading</h1>
	<p>My first paragraph.</p>
</body>
</html>
```

**Save** your index.html file. 

**To view your website:**

- If you're in Sublime Text, you can right click on your document and select "Open in Browser" from the drop-down menu.
- Otherwise, open the folder containing your index.html file in Finder or Windows Explorer and drag the file into your favorite browser.

Voila! You now have a basic web page! From here, there's no limit to what you can build!

**Note: It is very important that you always save your file(s) before reloading or trying to view your page! Most text editors do not autosave, so it will look as if any changes you made to your file did not appear!**

<img src="https://www.w3schools.com/html/img_chrome.png" width="500px"/>

## What is CSS?

CSS stands for **Cascading Style Sheets**. 

CSS describes how HTML elements are to be displayed on screen, paper, or in other media. CSS **saves a lot of work**. It can control the layout of multiple web pages all at once.

## Getting Started

1. In a text editor, create a new **empty** text file and name it **style.css**
2. Save it **inside the same folder** that contains your index.html file.
3. We're ready to start coding!

## CSS Syntax

CSS uses a **property: value** syntax that looks like the following:

```
element {
    property: value;
}
```

Let's break everything down:

- The **element** is the specific HTML element you want to style. If we wanted to style `<p>` tags, we would replace "element" with "p". If we wanted to style `<h1>` tags, we would replace "element" with "h1".
- The **property** is the specific property of the element we want to style. There are hundreds of different properties and it is near impossible to memorize them all, but typical properties include **color**, **text-align**, **font-size**, and **font-family**.
- The **value** is the value we wish to assign to the aforementioned property. Let's say our property is **color**. Some sample values would be **red**, **blue**, **black**, and **brown**.

## Styling our Page

Add the following to **style.css**:

```
h1 {
    color: blue;
    text-align: center;
}

p {
    color: red;
}
```

- We want `<h1>` elements to be blue and centered.
- We want `<p>` elements to be red.

## Linking your CSS to your HTML File

We need to link our two files together so that our HTML can use this external sheet.

In your **index.html** file, inside the `<head> </head>` tags, add:

```
<link rel="stylesheet" href="style.css">
```

**Save both index.html and style.css**, and reopen/refresh your page in a browser of your choice.

<img src="https://lh6.googleusercontent.com/dL7n7j-fB8vIeOCT8L4SxPMj9_y2aA33_3TvPUVFxCruugw3eSGBgy3_Be8j7_SwHQoAeXqA_dBqST2f_6dqW25Wygt0mpWRqXwpDal0HllS_ebWFGBsxuO6Ta62KgLtiWPUxpcP" width="700px">

**And there you go!** You now have the skills necessary to build even the most complex and beautifully designed pages. Happy coding!