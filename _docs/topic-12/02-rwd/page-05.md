---
title: Grid View
module: topic-12
permalink: /topic-12/rwd-gridview/
categories: development
tags:
---

<div class="divider-heading"></div>

## Building a Responsive Grid-View

Let's start building a responsive grid-view. This will make it easier to resize your website for smaller screens.

First, we must ensure that all HTML elements have the box-sizing property set to border-box. This makes sure that the padding and border are included in the total width and height of the elements.

To select all HTML elements, we can use the universal selector, `*`. Add the following code in your CSS stylesheet:

```css
* {
    box-sizing: border-box;
  }
```

The following example shows a simple responsive web page, with two columns. The `menu` class is always going to take up the first 25% of the screen, and the `main` class is always going to take up the other 75% of the screen, no matter how the page is resized by the user.

```css
.menu {
  width: 25%;
  float: left;
  
}
.main {
  width: 75%;
  float: left;
}

.display-inline-block {
    display: inline-block;
}

.menu-item:hover {
    background-color: gold;
    color: #333;
}

p {
  text-align: justify;
}
```


Here is the corresponding HTML:

```html
<div class="menu">
   <div class="menu-item display-inline-block">
      Home
   </div>
   <div class="menu-item display-inline-block">
      Services
   </div>
   <div class="menu-item display-inline-block">
      About
   </div>
   <div class="menu-item display-inline-block">
      Contact
   </div>
</div>

<div class="main">
  <h1>Main Information</h1>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
</div>
```

<div class="codepen-embed">
  <p data-height="600" data-theme-id="30567" data-slug-hash="OJXoqPN" data-default-tab="css,result" data-user="retrog4m3r" data-embed-version="2" data-pen-title="Grid-View 2 Column" class="codepen"></p>
</div>

What if we want to use a responsive grid-view with 12 columns? 12 columns is standard for webpages, because with more columns, we have more control over the web page.

First, we need to calculate the percentage for one column: 100% / 12 columns = 8.33%.

Then, we need to make one class for each of the 12 columns, (`class="col-"`) and add a number so we know which one is which:


```css
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
```

We should also apply the following to all the classes:

```css
[class*="col-"] {
  float: left;
  padding: 15px;
}
```

The strange selector, `[class*="col-"]`, we are using here is a helpful one: it is telling our browser to select all class attributes that has a value that is `col-`. Of course, each of our `col-` classes also have a number added afterward, but so long as the class attributes we add to our HTML elements have `col-` as part of their value, they will be selected. To learn more about this selector, you can view <a href="https://www.w3schools.com/cssref/sel_attr_contain.asp" target="_blank">this page</a> on W3 schools.

Then, we add the `float:` property so that everything is stacked from left to right. Finally, adding some `padding:` will create some space between each column.

Next, we need to think about how we can split our page into <i>rows</i>, too. We can create a class called `row` and apply it to any elements we want to separate into a new row. Then, in our CSS stylesheet, we should add the following:

```css
.row::after {
  content: "";
  clear: both;
  display: table;
}
```

Using the pseudoselector of `::after` here allows us to add styling rules that will happen <i>after</i> a row finishes. Here, we are adding the `content` property, which allows us to automatically add content after the row finishes. It's left empty in this case, to give us a paragraph break and start a new row of content. The `clear` property is related to the `float` property, and dictates how content like images will flow around this element. Finally, displaying the row as a table will help center our content on the page.

See the results below:

<div class="codepen-embed">
  <p data-height="600" data-theme-id="30567" data-slug-hash="dyJQGZB" data-default-tab="css,result" data-user="mart341" data-embed-version="2" data-pen-title="Grid-View 12 Columns" class="codepen"></p>
</div>

In the CSS stylesheet, the following rule was added to resize the images, too: 

```css
div > img {
  max-width: 100%;
}
```

The selector being used here is called the <a href="https://www.w3schools.com/cssref/sel_element_gt.asp" target="_blank">element>element</a> selector. In our case, it selects all `img` elements that are children of a `div` element. Then, we set the `max-width:` of these `img` elements to be 100% of their parent `div` container.

<a href="https://www.w3schools.com/css/css_rwd_grid.asp" target="_new"><em>Reference</em></a>


