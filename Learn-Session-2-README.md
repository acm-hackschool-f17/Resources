# Learn-Session-2-README

## Table of Contents

## Bootstrap

Bootstrap is a free front-end **framework** (collection of pre-written code) used for faster and easier web development. 

It includes HTML and CSS-based design templates for typography, forms, buttons, tables, navigation, modals, image carousels and many others, including optional JavaScript plugins.

## Why Use Bootstrap?

Advantages of Bootstrap:

- **Easy to use:** Anybody with basic knowledge of HTML and CSS can start using Bootstrap
- **Responsive features:** Bootstrap's responsive CSS adjusts to phones, tablets, and desktops
- **Mobile-first approach:** In Bootstrap 4, mobile-first styles are part of the core framework
- **Browser compatibility:** Bootstrap is compatible with all modern browsers (Chrome, Firefox, Internet Explorer, Safari, and Opera)

## Getting Bootstrap

There are two ways to start using Bootstrap on your own web site:

- Download Bootstrap from getbootstrap.com
- Include Bootstrap from a CDN

For the purposes of Hackschool we will be using the second option.

### Bootstrap CDN

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

### Bootstrap Grid System

Bootstrap's grid system allows up to **12 columns** across the page.

If you do not want to use all 12 columns individually, you can group the columns together to create wider columns:

<img src="https://lh3.googleusercontent.com/mfU_A8E8_kK-QKcjRuJOgw1tw4If1wIgvFa15paEyGVm6E1Zfh8GQrlBSvLin9q2XhiduQVD-QrvlrlRGXzj1RIBYQkDNq5PDtlyTr69C87UkOvhW4KU29d3yz6x99l79e_8QII6" width="600px">

