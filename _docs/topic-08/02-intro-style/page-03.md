---
title: Inline Styles
module: topic-08
permalink: /topic-08/basic-styling-divs/
---

<div class="divider-heading"></div>

Divs are _block-level_ elements, meaning they fill the page edge-to-edge. If this isn't necessarily what we want, we can easily force changes to the div itself, and how it relates to the elements inside.

What if we want to affect just one `<div>` element and not any others? We can do this with **inline styling**. We can add inline style rules to our HTML elements by adding the `style=` attribute to the inside of an element's opening tag. Then, we specify the style rule as the attribute value, like this: `<div style="font-size: 14px">`

Let's look at more examples of how this works.

## Changing Width
You can easily change the width of a div from 100% using the **width property**. Width values can be in percentages (changing) or pixels (unchanging). For example:
- to be half of the page _at any size_ of the brower window, set to `width: 50%;`
- to be 300 pixels wide _no matter the size_ of the browser window, set to `width: 300px;`

<div class="code-heading">
  <span class="html">HTML</span>
</div>

```html
  <div style="width: 50%;">
```

<div class="external-embed">
  <p data-height="600" data-theme-id="30567" data-slug-hash="dyXooGE" data-default-tab="html,result" data-user="retrog4m3r" data-pen-title="div width" class="codepen"></p>
</div>

## Centering on the Page
Have a div less than full-page and want it placed in the middle? Add the **margin property**, set to `auto` (`margin: auto`). We did this last week in our assignment!

<div class="code-heading">
  <span class="html">HTML</span>
</div>

```html
<div style="margin: auto;">
```
<div class="external-embed">
  <p data-height="600" data-theme-id="30567" data-slug-hash="WNxvvxp" data-default-tab="html,result" data-user="retrog4m3r" data-pen-title="div margin auto" class="codepen"></p>
</div>

## Cushioning From the Edge
Text inside of a div will set along the edges. To override this and give the text some “cushion” for easier-reading, add the **padding property**. Pixel values are best-suited here.

<div class="code-heading">
  <span class="html">HTML</span>
</div>

```html
<div style="padding: 10px;">
```

<div class="external-embed">
  <p data-height="600" data-theme-id="30567" data-slug-hash="dyXooXE" data-default-tab="html,result" data-user="retrog4m3r" data-pen-title="div padding" class="codepen"></p>
</div>

<div class="divider-pg"></div>

Finally, what if we want to use multiple styles in the same style attribute? We can absolutely do this, but we must separate each rule with a `;` again. So, for example: `<div style="width: 50%; margin: auto; padding: 20px;">`

### Example
This final example, puts all of it together using **width**, **margin: auto**, and **padding**.


<div class="external-embed">
  <p data-height="600" data-theme-id="30567" data-slug-hash="LYZVVRv" data-default-tab="html,result" data-user="retrog4m3r" data-pen-title="Basic HTML Div Styling" class="codepen"></p>
</div>
