---
title: Media Query
module: topic-12
permalink: /topic-12/rwd-mediaquery/
categories: development
tags:
---

<div class="divider-heading"></div>

## Media Query

Media query is a CSS technique introduced in CSS3. It uses the @media rule to include a block of CSS properties only if a certain condition is true.

This is most often used to check the width of a browser window on a device and change the CSS styling accordingly. For example:

```css
@media only screen and (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```

The code here is telling our browser to check the maximum width of the screen. If the browser window is 600px or smaller, the background color will become lightblue.

Please note that all style rules that you want to add if the browser window is 600px or smaller are written with standard CSS syntax, but they must be wrapped in an extra set of `{}` that are associated with the `@media` rule.

As another example, if we want the screen (browser window) to resize when it becomes smaller than 768px across (standard for a phone), we can set each column to have a width of 100%:

```css
/* For desktop: */
.col-1 {width: 8.33%;}
.col-2 {width: 16.66%;}
.col-3 {width: 25%;}
.col-4 {width: 33.33%;}
.col-5 {width: 41.66%;}
.col-6 {width: 50%;}
.col-7 {width: 58.33%;}
.col-8 {width: 66.66%;}
.col-9 {width: 75%;}
.col-10 {width: 83.33%;}
.col-11 {width: 91.66%;}
.col-12 {width: 100%;}

@media only screen and (max-width: 768px) {
  /* For mobile phones: */
  [class*="col-"] {
    width: 100%;
  }
}
```

Here is what our previous example looks like with this rule added:

<div class="codepen-embed">
  <p data-height="600" data-theme-id="30567" data-slug-hash="RwxqaZV" data-default-tab="css,result" data-user="mart341" data-embed-version="2" data-pen-title="12 Columns with Media Query" class="codepen"></p>
</div>



## A Mobile First Approach

If we wanted to take a mobile-first approach, that means we must design (and code!) for mobile before designing for desktop or any other advice. This will also make the page display faster on smaller devices.

This means that we must make some changes in our CSS. Instead of changing styles when the width gets smaller than 768px, we should change the design when the width gets larger than 768px.

```css
/* For mobile phones: */
[class*="col-"] {
  width: 100%;
}

@media only screen and (min-width: 768px) {
  /* For desktop: */
  .col-1 {width: 8.33%;}
  .col-2 {width: 16.66%;}
  .col-3 {width: 25%;}
  .col-4 {width: 33.33%;}
  .col-5 {width: 41.66%;}
  .col-6 {width: 50%;}
  .col-7 {width: 58.33%;}
  .col-8 {width: 66.66%;}
  .col-9 {width: 75%;}
  .col-10 {width: 83.33%;}
  .col-11 {width: 91.66%;}
  .col-12 {width: 100%;}
}
```

One can design for as many screen sizes as they want.

```css
/* For mobile phones: */
[class*="col-"] {
  width: 100%;
}

@media only screen and (min-width: 600px) {
  /* For tablets: */
  .col-s-1 {width: 8.33%;}
  .col-s-2 {width: 16.66%;}
  .col-s-3 {width: 25%;}
  .col-s-4 {width: 33.33%;}
  .col-s-5 {width: 41.66%;}
  .col-s-6 {width: 50%;}
  .col-s-7 {width: 58.33%;}
  .col-s-8 {width: 66.66%;}
  .col-s-9 {width: 75%;}
  .col-s-10 {width: 83.33%;}
  .col-s-11 {width: 91.66%;}
  .col-s-12 {width: 100%;}
}

@media only screen and (min-width: 768px) {
  /* For desktop: */
  .col-1 {width: 8.33%;}
  .col-2 {width: 16.66%;}
  .col-3 {width: 25%;}
  .col-4 {width: 33.33%;}
  .col-5 {width: 41.66%;}
  .col-6 {width: 50%;}
  .col-7 {width: 58.33%;}
  .col-8 {width: 66.66%;}
  .col-9 {width: 75%;}
  .col-10 {width: 83.33%;}
  .col-11 {width: 91.66%;}
  .col-12 {width: 100%;}
}
```


<a href="https://www.w3schools.com/css/css_rwd_mediaqueries.asp" target="_new"><em>Reference</em></a>
