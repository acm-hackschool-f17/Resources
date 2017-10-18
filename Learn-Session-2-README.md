# Learn-Session-2-README

## Table of Contents

- <a href="#LS2-what-is-bootstrap">What is Bootstrap?</a>
- <a href="#LS2-why-use-bootstrap">Why Use Bootstrap?</a>
- <a href="#LS2-getting-bootstrap">Getting Bootstrap</a>
  - <a href="#LS2-bootstrap-cdn">Bootstrap CDN</a>
- <a href="#LS2-bootstrap-grid-system">Bootstrap Grid System</a>
  - <a href="#LS2-grid-classes">Grid Classes</a>
  - <a href="#LS2-useful-class-names">Useful Class Names</a>

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

- **container**

  - Fixed width container with widths determined by screen sites. Equal margin on the left and right.

  - ```
    .container {
      padding-right: 15px;
      padding-left: 15px;
      margin-right: auto;
      margin-left: auto;
    }
    ```

- **row**

  - Container for responsive columns.

  - ```
    .row {
      margin-right: -15px;
      margin-left: -15px;
    }
    ```

- **.col-\*-\***

  - Responsive grid (span 1-12 column)
  - The first asterisk is to be replaced by a 