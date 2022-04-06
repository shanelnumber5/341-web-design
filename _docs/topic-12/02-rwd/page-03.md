---
title: Sizing for the Viewport
module: topic-12
permalink: /topic-12/rwd-viewport/
categories: development
tags:
---

<div class="divider-heading"></div>

## Viewport Review 
Remember, a browser’s viewport is the area of web page in which the content is visible to the user. The viewport does not have the same size, it varies with the variation in screen size of the devices on which the website is visible. For a laptop, the viewport has a larger size as compared to a smartphone or tablet.

This is why we include the following `<meta>` element in our HTML pages:

```html
<meta name="viewport" content= "width=device-width, initial-scale=1.0"> 
```

This is the common setting of viewport used in various mobile-optimized websites. The width property governs the size of the viewport. It is possible to set it to a specific value `“width=600”` in terms of CSS pixels. Here it is set to a special value `width= device-width”` which is the width of the device in terms of CSS pixels at a scale of 100%. The initial-scale property governs the zoom level when the page is loaded for the first time.


### Size Content to The Viewport
Users are used to scroll websites vertically on both desktop and mobile devices - but not horizontally!

So, if the user is forced to scroll horizontally (or zoom out) to see the whole web page it results in a poor user experience.

Some additional rules to follow:

1. **Do NOT use large fixed width elements** - For example, if an image is displayed at a width wider than the viewport it can cause the viewport to scroll horizontally. Remember to adjust this content to fit within the width of the viewport.

2. **Do NOT let the content rely on a particular viewport width to render well** - Since screen dimensions and width in CSS pixels vary widely between devices, content should not rely on a particular viewport width to render well.

3. **Use CSS media queries to apply different styling for small and large screens** - Setting large absolute CSS widths for page elements will cause the element to be too wide for the viewport on a smaller device. Instead, consider using relative width values, such as width: 100%. Also, be careful of using large absolute positioning values. It may cause the element to fall outside the viewport on small devices.

<a href="https://www.w3schools.com/css/css_rwd_viewport.asp" target="_new"><em>Reference</em></a>
