# Hack-Session-1-README

## HTML Setup

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

- <!DOCTYPE html> lets the browser know it’s an HTML doc
- \<html> and \</html> tags denote where the content of HTML goes
- \<head> tag includes information that isn’t displayed, such as the title of the webpage
- \<title> tag defines a title for the page used in the browser toolbar and search results
- \<body> tag surrounds all visible content.



## Useful HTML Tags

### \<div>

- The **div** tag is the most generic tag used to hold any content
- Used to divide the website into different sections

<u>Example</u>

```
<div>
	Content goes here.
</div>
```

<img src="https://lh4.googleusercontent.com/gvtDD-gCq4wpm7_OScu0UQhW1TIOc_QsqXALtynb8pKmaHeJHzhgUdnz6LKVChWXBcd8iOw-D5AaNiKccJZn-94OiMjvxYlul3PnFvIJ1tk_ECrydVdQtwvw3bFyCVgVPTksgf1F" width="200px">



### \<h1>, \<h2>, \<h3>, ... (Headers)

- A **header** tag can be from 1-6, with 1 being the most important/largest, to 6 being the least important/smallest.
- Use header tags to express section headers and other important information.

<u>Example</u>

<img src="https://lh4.googleusercontent.com/77DiON_TfywT5RQgmB2PgeGSdWl8-CMQCulWn9D4o-U-A8r5qONych2FiSThZ1SBBO1JGB1ewQ4s55tCj6sDg9Fddu2XKCh4gTz5tD2OJzp-lfT0q-c5Mnt2uxer7PCRi52AD76FPls" width="200px"/>



### \<p>

- A **p** tag is a paragraph tag used to hold text, even if it’s just a small line.

<u>Example</u>

```
<p>Here is some text</p>
```

<img src="https://lh5.googleusercontent.com/WDp6zOr5EQhbrh-LVKkydt_k7o8ktnW36htxEnphG7xRfQHZt60R-36B-_T3kn--hNdvAlyzzJ1A5naPECve-023somagxWFQptjLdROrcQmIBcT7a88VnFnoDiE_rGLACcsB8dA" width="200px"/>



### \<img>

- An **img** tag is an image tag, and it is used to insert images.
- img tags generally have a src attribute, whose value is a URL to an image.

<u>Example</u>

```
<img src=“https://i.ytimg.com/vi/ZHgtIyZX_q8/maxresdefault.jpg”/>
```

<img src="https://i.ytimg.com/vi/ZHgtIyZX_q8/maxresdefault.jpg" width="300px"/>



### \<input>

- The \<input> tag is used to gather input from users.
- It has an attribute (type) with a value of “text”, “number”, or “submit” based on what you want the user to input.
- You can also have a placeholder.
- Note that there are many ways to handle input; some ways are more appropriate than others in certain situations.

<u>Example</u>

```
<input type="text" placeholder="input stuff here">
```

<img src="https://lh6.googleusercontent.com/RiWsuVfuU-oJRiEJiUupGrKBFXYztDNc-g48e6njwsTtXCV5XAUKbxAy-rgT2AAypAJnc6gbKPpKR97JADqQiMWoiMqeywzYhBGWQdbprYR2buptLFGmQ0xYOGD1HRlbtHKdrwGKHgo" width="200px"/>



### \<a> (Links/Anchor Tags)

- An **anchor** is a piece of text which marks the beginning and/or the end of a hypertext link. 
- The text between the opening **tag** and the closing **tag** is either the start or destination (or both) of a link.

<u>Example</u>

```
<a href=“www.google.com”>Click Here to go to Google</a>
```

<img src="https://lh3.googleusercontent.com/-MR5GH1teD2a48f4vlbeGiuF0GvLzq7uRETIOzu4_-2Ps8FIS6fHK5kKZqrR50Co3WeLQ-_7wLfJQloRgcsOnu-_N26CpiJRrD-_CDHeJbsYnOMCn31DWVk8ZMXxh29j6htAJGkkB64" width="200px"/>



### \<ol>, \<ul>, \<li> (Lists)

- An **u**nordered **l**ist (ul) has no numbers, just bullets. It is contained within \<ul> and \</ul> tags.


- An **o**rdered **l**ist (ol) is used for ordering, and it automatically numbers list items.


- To populate our list, we use \<li>\</li> tags, which stand for **l**ist **i**tems.

<u>Examples</u>

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



### \<b>, \<i>, \<u>

- Use \<b> to **bold** text
- Use \<i> to *italicize* text
- Use \<u> to <u>underline</u> text
- Refer to the CSS section for more styling.

<u>Example</u>

```
<b>This text is bolded.</b>
<u><i>This text is underlined and italicized</i></u>
```

<img src="https://lh5.googleusercontent.com/ychGE6cA-9jgw9qtdw34sCu1n0RMkdSr0Dq1XcnIdYWTGcddXCc4BkBIVOi_dsARNSWQp3KNnTVI19IZj9cBjuYdVsOWIwVLhfvRkYmGZzJbjaMmeBWcR6_I8LJq75JXPiJkGpxM" width="500px"/>



### \<span>

- The \<span> tag is used to group inline-elements in a document.
- The \<span> tag provides no visual change by itself.
- The \<span> tag provides a way to add a hook to a part of a text or a part of a document.

<u>Example</u>

```
<p>My mother has <span style="color:blue">blue</span> eyes</p>
```

<img src="https://lh3.googleusercontent.com/G0fxHQDJ6qjYMoW9aSyaUXgEHOQ4DFhfX-aM4JvF5F8br6_j8DBQmfASTWXrOKJUvFdVDKMNjgHOiDzWurq3KNJF6WjkCYwHNhGeH-u_Lp77NTOe1CtZox563yr7M-I_2y0fsAkC" width="200px"/>



## CSS

- CSS stands for Cascading Style Sheets, and it can be used to add color, change element sizes, and format your page.
- Main idea: select a particular element or a group of elements to apply styling to
- ie. make all \<h1> tags blue, give all \<p> tags a border and change their font size, etc.



## Useful CSS Syntax

### Including your CSS

In your HTML file after your \<title> tag in your \<head>, add the following line:

```
<head>
	<title>Landing page</title>
	<link rel="stylesheet" type="text/css" href="style.css"/></head>
```



### CSS General Syntax

- property: value

<u>Example</u>

```
p {
    text-align: center;
    color: red;
}
```



## Useful CSS Properties and Values

### <u>Background and Border Properties</u>

### color

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



### opacity

- Sets the opacity (transparency) level for an element
- Decimal number ranging between 0.0 and 1.0

<u>Example</u>

```
opacity: 0.5;
```



### background-color

- Sets the background color of a single element
- Legal colors can be found above under the **color** section

<u>Example</u>

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



### background-image

- Sets one or more background images for an element
- By default, a background-image is placed at the top-left corner of an element, and **repeated** both vertically and horizontally.
- **Tip: **Always set a background-color to be used if the image is unavailable.
- To reference an image url in a .css file, use the syntax url(*your file path here*)

<u>Example</u>

```
body {
    background-image: url("paper.gif");
    background-color: #cccccc;
}
```



### background-size

- Specifies the size of the background images

<u>Example</u>

```
div {
    background: url(img_flwr.gif);
    background-size: 80px 60px;
    background-repeat: no-repeat;
}
```



### border

- Sets all the border properties in one declaration
  - Sample Border Styles:
    - solid
    - dotted
    - dashed
    - double
    - none
    - A list of more legal names can be found at: https://www.w3schools.com/css/css_border.asp

<u>Example</u>

```
p {
    border: 5px solid red;
}
```



### border-bottom, border-top, border-left, border-right

- Sets the border properties of a specific side in one declaration

<u>Example</u>

```
p {
    border-bottom: 5px double #ff0000;
}
```



### <u>Basic Box Properties</u>

### float

- Specifies whether or not a box (an element) should float
- <u>Example</u>

```
img {
    float: right;
}
```

![img](https://lh5.googleusercontent.com/yPF_bD21zdDlu5btqN1JLDTvaV84qYxXDbi7W_rvYhAwEwuBEt2aMEfV3vRlTEinQ21taSY5djmyZritcUB9Q_FfKNFJV5pOVL98FXPvmBjVxDtqUrMSWg8-R58kRk5tHC5O5NXo)



### width, height

- Sets the width and height of an element

<u>Example</u>

```
p.ex {
    height: 100px;
    width: 100px;
}
```

<img src="https://lh4.googleusercontent.com/gqY3YSTKcQdD7fDHIIRJr7e2DuAFCdrK6Kc7kxyz8kdqfdtY61-1gfppkDhYlzvHU6HUtdeckhZGZ_qLP-zqJ_3_1EhtUPYEHPUbbNq-w7MmgQONFF_HQhhkMJMrw06gg7iwx_Jh" width="100px"/>



### margin

- Sets all the margin properties in one declaration. 
- This property can have from one to four values.
- **Note:** Negative values are allowed (might be used to hide things)

<u>Examples</u>

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



### margin-bottom, margin-left, margin-right, margin-top

- Sets the margin property of a specific side in one declaration

<u>Example</u>

```
p {
    margin-bottom: 2cm;
}
```



### padding

- Sets all the padding properties in one declaration

<u>Examples</u>

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

- Refer to the above section on **margin** for the meaning of the above statements



### padding-bottom, padding-left, padding-right, padding-top

- Sets the padding property of a specific side in one declaration

<u>Example</u>

```
p {
    padding-bottom: 2cm;
}
```



### <u>Text Properties</u>

### text-align

- Specifies the horizontal alignment of text in an element

<u>Example</u>

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



### text-decoration

- Specifies the decoration added to text

<u>Example</u>

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

### <u>Font Properties</u>

### font

- Sets all the font properties in one declaration
- The properties that can be set, are (in order): "font-style font-variant font-weight font-size/line-height font-family"
- The font-size and font-family values are required. If one of the other values are missing, the default values will be inserted, if any.

<u>Examples</u>

```
p.ex1 {
    font: 15px arial, sans-serif;
}

p.ex2 {
    font: italic bold 12px/30px Georgia, serif;
}
```



### font-family

- Specifies the font for an element
- The font-family property can hold several font names as a "fallback" system. If the browser does not support the first font, it tries the next font.

<u>Example</u>

```
p {
    font-family: "Times New Roman", Georgia, Serif;
}
```



### font-size

- Sets the size of a font
- Sample sizes:
  - medium
  - small
  - x-small
  - xx-large
  - A full list of legal sizes can be found at: https://www.w3schools.com/cssref/pr_font_font-size.asp

<u>Examples</u>

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



### font-weight

-  Sets how thick or thin characters in text should be displayed

<u>Examples</u>

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



### <u>Miscellaneous</u>

### cursor

- Specifies the type of cursor to be displayed when pointing on an element

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



t