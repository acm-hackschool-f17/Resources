# Hack-Session-1-README

## Table of Contents

- <a href="#HS1-html-setup">HTML Setup</a>
- Useful HTML Tags
  - <a href="#HS1-div">div</a>
  - <a href="#HS1-headers">h1, h2, h3, ...</a>
  - <a href="#HS1-p">p</a>
  - <a href="#HS1-img">img</a>
  - <a href="#HS1-input">input</a>
  - <a href="#HS1-a">a (Links/Anchor Tags)</a>
  - <a href="#HS1-lists">ol, ul, li (Lists)</a>
  - <a href="#HS1-biu">b, i, u</a>
  - <a href="#HS1-span">span</a>
- Useful CSS Syntax
  - <a href="#HS1-including-your-css">Including your CSS</a>
  - <a href="#HS1-css-general-syntax">CSS General Syntax</a>
- Useful CSS Properties
  - <a href="#HS1-background-and-border-properties">Background and Border Properties</a>
    - <a href="#HS1-color">color</a>
    - <a href="#HS1-opacity">opacity</a>
    - <a href="#HS1-background-color">background-color</a>
    - <a href="#HS1-background-image">background-image</a>
    - <a href="#HS1-background-size">background-size</a>
    - <a href="#HS1-border">border</a>
    - <a href="#HS1-border-sides">border-bottom, border-top, border-left, border-right</a>
  - <a href="#HS1-basic-box-properties">Basic Box Properties</a>
    - <a href="#HS1-float">float</a>
    - <a href="#HS1-width-height">width, height</a>
    - <a href="#HS1-margin">margin</a>
    - <a href="#HS1-margin-sides">margin-bottom, margin-top, margin-left, margin-right</a>
    - <a href="#HS1-padding">padding</a>
    - <a href="#HS1-padding-sides">padding-bottom, padding-top, padding-left, padding-right</a>
  - <a href="#HS1-text-properties">Text Properties</a>
    - <a href="#HS1-text-align">text-align</a>
    - <a href="#HS1-text-decoration">text-decoration</a>
  - <a href="#HS1-font-properties">Font Properties</a>
    - <a href="#HS1-font">font</a>
    - <a href="#HS1-font-family">font-family</a>
    - <a href="#HS1-font-size">font-size</a>
    - <a href="#HS1-font-weight">font-weight</a>
  - <a href="#HS1-miscellaneous">Miscellaneous</a>
    - <a href="#HS1-cursor">cursor</a>
    - <a href="#HS1-flexboxes">Flexboxes</a>
      - <a href="#HS1-creating-a-flexbox">Creating a Flexbox</a>
      - Useful Flexbox Properties
        - <a href="#HS1-flex-direction">flex-direction</a>
        - <a href="#HS1-justify-content">justify-content</a>
        - <a href="#HS1-align-items">align-items</a>
- Classes and IDs
  - <a href="#HS1-classes">Classes</a>
  - <a href="#HS1-ids">IDs</a>
- <a href="#HS1-creating-a-navigation-bar">Creating a Navigation Bar</a>
  - <a href="#HS1-navigation-bar-equals">Navigation Bar = List of Links</a>
  - <a href="#HS1-creating-clickable-blocks">Creating Clickable Blocks</a>
  - <a href="#HS1-changing-color-on-hover">Changing Color on Hover</a>
  - <a href="#HS1-making-the-bar-horizontal">Making the Bar Horizontal</a>
  - <a href="#HS1-fixed-navigation-bars">Fixed Navigation Bars</a>

---

## <a name="HS1-html-setup">HTML Setup</a>

```
<!DOCTYPE html>
<html>
<head>
	<title>Landing page</title>
</head>
<body>
	// Stuff will go here!
</body>
</html>
```

- \<!DOCTYPE html> lets the browser know it’s an HTML doc
- \<html> and \</html> tags denote where the content of HTML goes
- \<head> tag includes information that isn’t displayed, such as the title of the webpage
- \<title> tag defines a title for the page used in the browser toolbar and search results
- \<body> tag surrounds all visible content.



## Useful HTML Tags

### <a name="HS1-div">\<div></a>

- The **div** tag is the most generic tag used to hold any content
- Used to divide the website into different sections

#### Example

```
<div>
	Content goes here.
</div>
```

<img src="https://lh4.googleusercontent.com/gvtDD-gCq4wpm7_OScu0UQhW1TIOc_QsqXALtynb8pKmaHeJHzhgUdnz6LKVChWXBcd8iOw-D5AaNiKccJZn-94OiMjvxYlul3PnFvIJ1tk_ECrydVdQtwvw3bFyCVgVPTksgf1F" width="200px">

---

### <a name="HS1-headers">\<h1>, \<h2>, \<h3>, ... (Headers)</a>

- A **header** tag can be from 1-6, with 1 being the most important/largest, to 6 being the least important/smallest.
- Use header tags to express section headers and other important information.

#### Example

<img src="https://lh4.googleusercontent.com/77DiON_TfywT5RQgmB2PgeGSdWl8-CMQCulWn9D4o-U-A8r5qONych2FiSThZ1SBBO1JGB1ewQ4s55tCj6sDg9Fddu2XKCh4gTz5tD2OJzp-lfT0q-c5Mnt2uxer7PCRi52AD76FPls" align="center" width="200px"/>

---

### <a name="HS1-p">\<p></a>

- A **p** tag is a paragraph tag used to hold text, even if it’s just a small line.

<u>Example</u>

```
<p>Here is some text</p>
```

<img src="https://lh5.googleusercontent.com/WDp6zOr5EQhbrh-LVKkydt_k7o8ktnW36htxEnphG7xRfQHZt60R-36B-_T3kn--hNdvAlyzzJ1A5naPECve-023somagxWFQptjLdROrcQmIBcT7a88VnFnoDiE_rGLACcsB8dA" width="200px"/>

---

### <a name="HS1-img">\<img></a>

- An **img** tag is an image tag, and it is used to insert images.
- img tags generally have a src attribute, whose value is a URL to an image.

#### Example

```
<img src="https://i.ytimg.com/vi/ZHgtIyZX_q8/maxresdefault.jpg"/>
```

<img src="https://i.ytimg.com/vi/ZHgtIyZX_q8/maxresdefault.jpg" width="300px"/>

---

### <a name="HS1-input">\<input></a>

- The \<input> tag is used to gather input from users.
- It has an attribute (type) with a value of “text”, “number”, or “submit” based on what you want the user to input.
- You can also have a placeholder.
- Note that there are many ways to handle input; some ways are more appropriate than others in certain situations.

#### Example

```
<input type="text" placeholder="input stuff here">
```

<img src="https://lh6.googleusercontent.com/RiWsuVfuU-oJRiEJiUupGrKBFXYztDNc-g48e6njwsTtXCV5XAUKbxAy-rgT2AAypAJnc6gbKPpKR97JADqQiMWoiMqeywzYhBGWQdbprYR2buptLFGmQ0xYOGD1HRlbtHKdrwGKHgo" width="200px"/>

---

### <a name="HS1-a">\<a> (Links/Anchor Tags)</a>

- An **anchor** is a piece of text which marks the beginning and/or the end of a hypertext link. 
- The text between the opening **tag** and the closing **tag** is either the start or destination (or both) of a link.

#### Linking Web URLs

- To link a web address, simply use the href attribute and assign it the URL.

##### Example

```
<a href="www.google.com">Click Here to go to Google</a>
```

<img src="https://lh3.googleusercontent.com/-MR5GH1teD2a48f4vlbeGiuF0GvLzq7uRETIOzu4_-2Ps8FIS6fHK5kKZqrR50Co3WeLQ-_7wLfJQloRgcsOnu-_N26CpiJRrD-_CDHeJbsYnOMCn31DWVk8ZMXxh29j6htAJGkkB64" width="200px"/>

##### Linking to a Place on your Website

- To link to a certain line on your page you need to use <a href="#HS1-ids">IDs</a>.

---

### <a name="HS1-lists">\<ol>, \<ul>, \<li> (Lists)</a>

- An **u**nordered **l**ist (ul) has no numbers, just bullets. It is contained within \<ul> and \</ul> tags.


- An **o**rdered **l**ist (ol) is used for ordering, and it automatically numbers list items.


- To populate our list, we use \<li>\</li> tags, which stand for **l**ist **i**tems.

#### Examples

```
<ol>		
	<li>First list item</li>
	<li>Second list item</li>
</ol>
```

<img src="https://lh6.googleusercontent.com/H6JbFg-tFCryLOap8AwKOFVQZkB8BW853oqud_NoKJpfS9O45TrCsqCDffm93Q2i1T4PLKB2bgf6ElCm6UOGovd-rvoBhiRKa5eHnkbOnGWTkef95FGgVe7VRWnaDz1KLRWet9to0dE" width="200px"/>

```
<ul>
	<li>Rock Climbing</li>
	<li>Cooking</li>
	<li>ACM</li>
</ul>
```

<img src="https://lh4.googleusercontent.com/uE34mFhdRGMVmkpSbF4P1PxPMt7iVJyGohJ94kxptugcrejGBULE_B_Tc7mlmNOyRDNRU1UiMOFIrdK3LokB6lnsL_gXI0aZawSFyEADQl9cSYFMqWmO_FHvY6sFLcNCuosYWF22Xbg" width="200px"/>

---

### <a name="HS1-biu">\<b>, \<i>, \<u></a>

- Use \<b> to **bold** text
- Use \<i> to *italicize* text
- Use \<u> to <u>underline</u> text
- Refer to the <a href="#HS1-CSS">CSS</a> section for more styling.

#### Example

```
<b>This text is bolded.</b>
<u><i>This text is underlined and italicized</i></u>
```

<img src="https://lh5.googleusercontent.com/ychGE6cA-9jgw9qtdw34sCu1n0RMkdSr0Dq1XcnIdYWTGcddXCc4BkBIVOi_dsARNSWQp3KNnTVI19IZj9cBjuYdVsOWIwVLhfvRkYmGZzJbjaMmeBWcR6_I8LJq75JXPiJkGpxM" width="500px"/>

---

### <a name="HS1-span">\<span></a>

- The \<span> tag is used to group inline-elements in a document.
- The \<span> tag provides no visual change by itself.
- The \<span> tag provides a way to add a hook to a part of a text or a part of a document.

#### Example

```
<p>My mother has <span style="color:blue">blue</span> eyes</p>
```

<img src="https://lh3.googleusercontent.com/G0fxHQDJ6qjYMoW9aSyaUXgEHOQ4DFhfX-aM4JvF5F8br6_j8DBQmfASTWXrOKJUvFdVDKMNjgHOiDzWurq3KNJF6WjkCYwHNhGeH-u_Lp77NTOe1CtZox563yr7M-I_2y0fsAkC" width="200px"/>

---

## <a name="HS1-CSS">CSS</a>

- CSS stands for Cascading Style Sheets, and it can be used to add color, change element sizes, and format your page.
- Main idea: select a particular element or a group of elements to apply styling to
- ie. make all \<h1> tags blue, give all \<p> tags a border and change their font size, etc.



## Useful CSS Syntax

### <a name="HS1-including-your-css">Including your CSS</a>

In your HTML file after your \<title> tag in your \<head>, add the following line:

```
<head>
	<title>Landing page</title>
	<link rel="stylesheet" type="text/css" href="style.css"/
</head>
```

---

### <a name="HS1-css-general-syntax">CSS General Syntax</a>

- property: value

#### Example

```
p {
    text-align: center;
    color: red;
}
```



## Useful CSS Properties and Values

### <a name="HS1-background-and-border-properties">Background and Border Properties</a>

### <a name="HS1-color">color</a>

- Sets the color of text

  - Sample Values:

    - Black
    - Blue
    - Brown
    - DarkGray
    - A list of more legal names can be found at: https://www.w3schools.com/colors/colors_names.asp

  - Hexadecimal Colours:

    - A hexadecimal color is specified with: #RRGGBB, where the RR (red), GG (green) and BB (blue) **hexadecimal** integers specify the components of the color. All values must be between 00 and FF.

    - <u>Example</u>

      ```
      color: #ff0000;   /* red */
      color: #00ff00;   /* green */
      color: #0000ff;   /* blue */
      ```

  - RGBA Colours:

    - An RGBA color value is specified with: rgba(red, green, blue, alpha).

    - The parameters red, green, and blue define the intensity of the color and each can be an integer between 0 and 255 or a percentage value (from 0% to 100%).

    - The alpha parameter is a number between 0.0 (fully transparent) and 1.0 (fully opaque).

    - <u>Example</u>

      ```
      color: rgba(255, 0, 0, 0.3);/* red with 30% opacity */
      color: rgba(0, 255, 0, 0.3); /* green "  "     " */
      color: rgba(0, 0, 100%, 0.3); /* blue "  "     " */
      ```


---

### <a name="HS1-opacity">opacity</a>

- Sets the opacity (transparency) level for an element
- Decimal number ranging between 0.0 and 1.0

#### Example

```
opacity: 0.5;
```

---

### <a name="HS1-background-color">background-color</a>

- Sets the background color of a single element
- Legal colors can be found above under the **color** section

#### Example

```
body {
    background-color: yellow;
}

h1 {
    background-color: #00ff00;
}

p {
    background-color: rgb(255,0,255);
}
```

---

### <a name="HS1-background-image">background-image</a>

- Sets one or more background images for an element
- By default, a background-image is placed at the top-left corner of an element, and **repeated** both vertically and horizontally.
- **Tip:** Always set a background-color to be used if the image is unavailable.
- To reference an image url in a .css file, use the syntax url(*your file path here*)

#### Example

```
body {
    background-image: url("paper.gif");
    background-color: #cccccc;
}
```

---

### <a name="HS1-background-size">background-size</a>

- Specifies the size of the background images

#### Example

```
div {
    background: url(img_flwr.gif);
    background-size: 80px 60px;
    background-repeat: no-repeat;
}
```

---

### <a name="HS1-border">border</a>

- Sets all the border properties in one declaration
  - Sample Border Styles:
    - solid
    - dotted
    - dashed
    - double
    - none
    - A list of more legal names can be found at: https://www.w3schools.com/css/css_border.asp

#### Example

```
p {
    border: 5px solid red;
}
```

---

### <a name="HS1-border-sides">border-bottom, border-top, border-left, border-right</a>

- Sets the border properties of a specific side in one declaration

#### Example

```
p {
    border-bottom: 5px double #ff0000;
}
```

---

### <a name="HS1-basic-box-properties">Basic Box Properties</a>

### <a name="HS1-float">float</a>

- Specifies whether or not a box (an element) should float

#### Example

```
img {
    float: right;
}
```

<img src="https://lh5.googleusercontent.com/yPF_bD21zdDlu5btqN1JLDTvaV84qYxXDbi7W_rvYhAwEwuBEt2aMEfV3vRlTEinQ21taSY5djmyZritcUB9Q_FfKNFJV5pOVL98FXPvmBjVxDtqUrMSWg8-R58kRk5tHC5O5NXo" width="700px">

---

### <a name="HS1-width-height">width, height</a>

- Sets the width and height of an element

#### Example

```
p.ex {
    height: 100px;
    width: 100px;
}
```

<img src="https://lh4.googleusercontent.com/gqY3YSTKcQdD7fDHIIRJr7e2DuAFCdrK6Kc7kxyz8kdqfdtY61-1gfppkDhYlzvHU6HUtdeckhZGZ_qLP-zqJ_3_1EhtUPYEHPUbbNq-w7MmgQONFF_HQhhkMJMrw06gg7iwx_Jh" width="100px"/>

---

### <a name="HS1-margin">margin</a>

- Sets all the margin properties in one declaration. 
- This property can have from one to four values.
- **Note:** Negative values are allowed (might be used to hide things)

#### Examples

```
p {
    margin: 2cm 4cm 3cm 4cm;
}
```

- top margin is 2cm
- right margin is 4cm
- bottom margin is 3cm
- left margin is 4cm

```
margin: 10px 5px 15px;
```

- top margin is 10px
- right and left margins are 5px
- bottom margin is 15px

```
margin: 10px 5px;
```

- top and bottom margins are 10px
- right and left margins are 5px

```
margin: 10px;
```

- all four margins are 10px


---


### <a name="HS1-margin-sides">margin-bottom, margin-left, margin-right, margin-top</a>

- Sets the margin property of a specific side in one declaration

#### Example

```
p {
    margin-bottom: 2cm;
}
```

---

### <a name="HS1-padding">padding</a>

- Sets all the padding properties in one declaration

#### Examples

```
p {
    padding: 2cm 4cm 3cm 4cm;
}
```

```
padding: 10px 5px 15px;
```

```
padding: 10px 5px;
```

```
padding: 10px;
```

- Refer to the above section on <a href="HS1-margin">**margin**</a> for the meaning of the above statements


---


### <a name="HS1-padding-sides">padding-bottom, padding-left, padding-right, padding-top</a>

- Sets the padding property of a specific side in one declaration

#### Example

```
p {
    padding-bottom: 2cm;
}
```

---

### <a name="HS1-text-properties">Text Properties</a>

### <a name="HS1-text-align">text-align</a>

- Specifies the horizontal alignment of text in an element

#### Example

```
h1 {
    text-align: center;
}

h2 {
    text-align: left;
}

h3 {
    text-align: right;
}
```

---

### <a name="HS1-text-decoration">text-decoration</a>

- Specifies the decoration added to text

#### Example

```
h1 {
    text-decoration: overline;
}

h2 {
    text-decoration: line-through;
}

h3 {
    text-decoration: underline;
}
```

<img src="https://lh4.googleusercontent.com/phkTfvGNu-ZMmdm55uj_78F8rV-CqDqIrN9Lfbl2heJwQH-FK4yDs8mb5mR-0ckOjo5b1Ls6oCYVek68SoCjSFar-f_MjJAnCpR6OubYByIsM7XnJh1L26wEH05rdrYSDWfUh1jQ" width="200px"/>

---

### <a name="HS1-font-properties">Font Properties</a>

### <a name="HS1-font">font</a>

- Sets all the font properties in one declaration
- The properties that can be set, are (in order): "font-style font-variant font-weight font-size/line-height font-family"
- The font-size and font-family values are required. If one of the other values are missing, the default values will be inserted, if any.

#### Examples

```
p.ex1 {
    font: 15px arial, sans-serif;
}

p.ex2 {
    font: italic bold 12px/30px Georgia, serif;
}
```

---

### <a name="HS1-font-family">font-family</a>

- Specifies the font for an element
- The font-family property can hold several font names as a "fallback" system. If the browser does not support the first font, it tries the next font.

#### Example

```
p {
    font-family: "Times New Roman", Georgia, Serif;
}
```

---

### <a name="HS1-font-size">font-size</a>

- Sets the size of a font
- Sample sizes:
  - medium
  - small
  - x-small
  - xx-large
  - A full list of legal sizes can be found at: https://www.w3schools.com/cssref/pr_font_font-size.asp

#### Examples

```
h1 {
    font-size: 250%;
}

h2 {
    font-size: 20px;
}

p {
    font-size: 100%;
}
```

---

### <a name="HS1-font-weight">font-weight</a>

-  Sets how thick or thin characters in text should be displayed

#### Examples

```
p.normal {
    font-weight: normal;
}

p.thick {
    font-weight: bold;
}

p.thicker {
    font-weight: 900;
}
```

---

### <a name="HS1-miscellaneous">Miscellaneous</a>

### <a name="HS1-cursor">cursor</a>

- Specifies the type of cursor to be displayed when pointing on an element

#### Example

```
span.crosshair {
    cursor: crosshair;
}

span.help {
    cursor: help;
}

span.wait {
    cursor: wait;
}
```

### <a name="HS1-flexboxes">Flexboxes</a>

<img src="https://lh3.googleusercontent.com/OcbnMeHOpkbyRkKWmjZSAHlG7Uz3DOqmjivdGRNqeE4PYOvb-T7fKV4Cso66WWaGCrQ9_xwRduVsN0bBRnFmVxUtZBKy0y-L1NcHp0KI3W7_unYuL3qbKxmXe8dB4Hx39YEbys-a" style="width: 700px"/>

- The main idea behind the flex layout is to give a container the ability to alter its items' width/height (and order) to best fill the available space (mostly to accommodate to all kind of display devices and screen sizes). 
- A flex container expands items to fill available free space, or shrinks them to prevent overflow.
- **Note**: a comprehensive guide to flexboxes can be found at https://css-tricks.com/snippets/css/a-guide-to-flexbox/

---

### <a name="HS1-creating-a-flexbox">Creating a Flexbox</a>

In your CSS:

```
.class-name {
	display: flex;
}
```

---

### Useful Flexbox Properties

#### <a name="HS1-flex-direction">flex-direction</a>

- Defines the direction flex items are placed in the flex container. 
- Think of flex items as primarily laying out either in horizontal rows or vertical columns.
- Possible values are:
  - row (default)
    - items are left-to-right
  - row-reverse
    - items are right-to-left
  - column
    - items are top-to-bottom
  - column-reverse
    - items are bottom-to-top

#### Example

```
.container {
	flex-direction: column
}
```

---

#### <a name="HS1-justify-content">justify-content</a>

- Defines the alignment of items along the main axis of the box.

- Possible values are:

  <img src="https://lh4.googleusercontent.com/zk3GIwsV-FFRud1GxW-8rhkz1XivUOlQ3hSG6ZDkpTZB_uXmTqg5kIoolYCJE96-B5GZHez8hn4BnWnactINvaVSPr4daduGplYjYmrfYiNe4v3xUw-wi_GTaOb_-uERH4MD0Yog" width="300px"/>

### Example

```
.container {
	justify-content: center;
}
```

------

### <a name="HS1-align-items">align-items</a>

- This defines the default behaviour for how flex items are laid out along the "cross axis" on the current line.

  - Assuming your flex-box is left-to-right, <a href="#HS1-justify-content">justify-content</a> will determine the position of items **horizontally** (like an x-coordinate), whereas align-items will determine the position of items **vertically** (like a y-coordinate).

- Possible values are:

  <img src="https://lh5.googleusercontent.com/nW1Vz4huI8iYNaSlTFFENAXHsCI189noSsatqN3xrjZwfqOxNf3JY57zxvTEaZN_dPA9nChcjsDdMMS0FS1_hrzyEReZ5dvQjkweyPq_S-Q60CinuO4byDiIeb6S00lT6Sc76_X6" width="300px"/>

#### Example

```
.container {
	align-items: center;
}
```

---

## Classes and IDs

### <a name="HS1-classes">Classes</a>

- The class selector selects elements with a specific class attribute
- Classes should be used when you want multiple HTML elements to have the same style.
- To select elements with a specific class, write a period (.) character, followed by the name of the class.

#### Example

```
.center {
    text-align: center;
    color: red;
}

<h1 class="center">Red and center-aligned heading</h1>
<p class="center">Red and center-aligned paragraph.</p> 
```

<img src="https://lh3.googleusercontent.com/OF35-6kLqqyKNATOdq5CvuKykPZS_zupxf6FrGIVPdUAHIom2Z5OW9vUyFD1wesOGkH_ia3dPM3OpYlXsRbhLcS7gxzf7wlpxBA00j2xoBoQLcs-VDvF-wlbH7oQ3qZ5aE_NQg3-" width="500px"/>

---

### <a name="HS1-ids">IDs</a>

- The id selector uses the id attribute of an HTML element to select a specific element.
- The id of an element should be unique within a page, so the id selector is used to select one unique element!
  - e.g. A title or header of a specific section
- To select an element with a specific id, write a hash (#) character, followed by the id of the element.
- **Note:** An id name cannot start with a number!

#### Example

```
#para1 {
    text-align: center;
    color: red;
}

<p id="para1">Hello World!</p>
<p>This paragraph is not affected by the style.</p>
```

<img src="https://lh6.googleusercontent.com/HE0dLP73JdmWGvkx69PYVLX7IXglp54KFlYcPkvkkjd8nJrzLewcBzCbgRoYivy3Vwh3-iDGU2P_emxtOjSfGUkKTSlQ2doFigoYeW-g8HgSTnlJdsPqcSt_tWPEmgWtzxWsCq9J">

## <a name="HS1-creating-a-navigation-bar">Creating a Navigation Bar</a>

Having easy-to-use navigation is important for any web site.

With CSS you can transform boring HTML menus into good-looking navigation bars.

### <a name="HS1-navigation-bar-equals">Navigation Bar = List of Links</a>

A navigation bar is basically a list of links, so using the \<ul> and \<li> elements makes perfect sense.

**In your HTML file**:

```
<ul>
  <li><a href="default.asp">Home</a></li>
  <li><a href="news.asp">News</a></li>
  <li><a href="contact.asp">Contact</a></li>
  <li><a href="about.asp">About</a></li>
</ul>
```

Now we want to remove the bullets and any margins and padding, which we can achieve with CSS.

**In your CSS file**:

```
ul {
	list-style-type: none;
    margin: 0;
    padding: 0;
}
```

- **list-style-type: none** 
  - Removes the bullets.
- **margin: 0; padding: 0;** 
  - Removes any browser default margins.

You should now have a simple navigation bar, looking something like the following:

<img src="https://lh4.googleusercontent.com/Lv5a3zGiSPOCPqds8himJLI2r_vumrYPufIhOV9-SHLJ186xvFdycfjCYUtX648CdzSNSk9nwRDc25JplL-cH_cCJb_3usGgD64lRGaCeoUjmKAnE_iL5v9cKKOQBCoVqjdKpJy-" width="100px"/>

---

### <a name="HS1-creating-clickable-blocks">Creating Clickable Blocks</a>

Currently, the links only work when we click the text. However, what if we want our navigation bar to be made up of stylable and clickable boxes? CSS comes to our rescue once again!

**In your CSS file:**

```
li a {
    display: block;
    width: 60px;
    background-color: #dddddd;
}
```

This code styles the \<a> elements inside of the list.

- **display: block;**
  - Displays the links as block elements which makes the whole link area clickable (not just the text) and allows us to specify any other properties that we want (width, height, padding, margin, etc.).
- **width: 60px;**
  - Sets the width of the block to 60 pixels. Without this, the block would take up the entire width of the webpage (by default).
- **background-color: #dddddd;**
  - Sets the background color of the block to a dark gray (so we can see the blocks).

You should now have something that looks like the following, where all gray areas are clickable:

<img src="https://lh3.googleusercontent.com/8nCpY9Qz2cg6OWPHbXIOeHmBXc4iky4CsNfWD_nCA9y0gMD5jEFHOg5whfLX_L_m9YxSzWR_G_dljHzWIVLeFtmkNIy0ma8CGcfWmV2gW82KJ_x1XrVhyUAV8r2bYoKwn7lUW7dx" width="100px"/>

---

### <a name="HS1-changing-color-on-hover">Changing Color on Hover</a>

Let's change the background color of a link block as the user hovers over it. We can also achieve this with CSS.

First, we should remove the default styling that hyperlinks receive, and add some padding so the text positioning looks nicer.

**In your CSS file:**

```
li a {
	/* stuff from before here */
	color: black;
    padding: 8px 16px;
    text-decoration: none;
}
```

- **color: black;**
  - Sets text color to black, as opposed to blue.
- **padding: 8px 16px;**
  - Adds padding to the text.
- **text-decoration: none**
  - Removes all text-decoration (i.e. removes the underline).

Now, let's edit the styling of a link being hovered over:

**In your CSS file:**

```
li a:hover {
    background-color: #555;
    color: white;
}
```

a:hover is special syntax that specifically styles links that have the cursor on them.

- **background-color: #555;**
  - Sets the background color to a dark gray (when user is hovering over link)
- **color: white;**
  - Changes text color to white (when user is hovering over link)

You should now have something that looks like the following (if your cursor was on "Home"):

<img src="https://lh3.googleusercontent.com/UItn2CGVR8kLOrKobSNk9hz9_4Fv94KGYTX43IhBUqfc5zTFd4IQv9GLabioG3ua_qdXrTV08FDlFodv9y2zdd_i2JIVL2MPbmlMI4IBgbz6gIak7aHv4fHgCzVftdblBDc25-R1" width="200px"/>

---

### <a name="HS1-making-the-bar-horizontal">Making the Bar Horizontal</a>

Making your bar horizontal can be done using a single line in CSS, and involves the float property.

**In your CSS file:**

```
li {
    float: left;
}
```

However, let's restyle some things as well:

**In your CSS file:**

```
ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    background-color: #333;
}

li {
    float: left;
}

li a {
    display: block;
    color: white;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
}

li a:hover {
    background-color: #111;
}
```

- **overflow: hidden;**
  - Added to the \<ul> element to prevent \<li> elements from going outside of the list
- **background-color: #333**
  - Note that this property is added to the \<ul> element. This creates a full-width, charcoal background color.
- **text-align: center**
  - Added to the \<a> elements in \<li> blocks to center link text within the block.

You should now have something that looks like the following:

<img src="https://lh6.googleusercontent.com/hsHpFjrD3PTszOTXwHogeBJ8d0xuD0bhIHsqm4xTvIUUNHkjxqX9zN-_pjaFDgPqyzQHynEcwazwWI0DmX5ZjNjdk7e476hugxlQkoUSVH4U3RbBL_cLWmGkoaSCe615gpPkO9vz" width="600px"/>

---

### <a name="HS1-fixed-navigation-bars">Fixed Navigation Bars</a>

What if we want to fix our navigation bar at the top or bottom of the page, even when the user is scrolling? You guessed it: a little more CSS.

**In your CSS file:**

```
ul {
	/* stuff from before */
  	position: fixed;
    top: 0;
    width: 100%;
}
```

- **position: fixed;**
  - Makes the list fixed from the users point of view/
- **top: 0**
  - top is a property for absolutely positioned (fixed) elements; in this case it positions our bar at the top of the page.
- **width: 100%**
  - Allows the bar to take up all available width.

This will fix the bar at the top of the screen, even when we scroll! To fix it at the bottom:

```
ul {
    position: fixed;
    bottom: 0;
    width: 100%;
}
```

---

Congratulations! You should now have a pretty kick-ass navigation bar. Continue exploring other CSS properties to make it even cooler. :)

