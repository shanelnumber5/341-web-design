---
title: Opacity
module: topic-09
permalink: /topic-09/opacity/
---

<div class="divider-heading"></div>

In addition to setting the color of background elements and text, we developers may dictate the **opacity** of elements themselves of just the background-color of an element.

Opacity is set as a ratio between 0.0 - 1.0. A value of 0.0 would make the element _invisible_, allowing your user to see any elements behind it, and a value of 1.0 would make the element totally _opaque_.

There are two ways to dictate opacity.


### Background Opacity

In order to change the opacity of the background-color only, you can write `rgba()` (as opposed to `rgb()`).

Like, `rgb()`, `rgba()` takes three numbers to define the ratios of red, green, & blue. However, `rgba()` also take a fourth number, in the range of 0.0-1.0, to define the opacity level.

For example, set a content box to be black, at half-opacity:

<div id="code-heading">CSS</div>
```css
.text-box {
    background-color: rgba(0,0,0,0.5);
}
```

### Element Opacity

If the goal is to change the opacity of an entire element, as well as its contents, then you can use the `opacity: ` property. Like the fourth value you add in `rgba()`, this property takes a single number, between 0.0-1.0, to represent the opacity of an element.

For example, to set the entire contents of a container to be at half-opacity, you would write:

<div class="code-heading">
  <span class="css">CSS</span>
</div>
```css
div.inner-container {
    opacity: 0.5;
}
```

#### Example

The following example creates 4 elements:

1. `.body-1` is the furthest back, and has no opacity values set.
2. `.box-1.inner` is nested within box one. The color is set to green, and CSS specifies the `opacity: ` property be set to 0.5. Notice how both the color of the box, as well as the white text, are effected by the red of `box-1`.
3. `box-2` is a separate element, which has been positioned to overlap the other two boxes. Notice that it uses the `rgba()` property, which allows the background color to allow bleed through, but _NOT_ the text.
4. `image-box` is just a flat graphic.


<div class="codepen-embed">
  <p data-height="600" data-theme-id="30567" data-slug-hash="PoEwVNg" data-default-tab="css,result" data-user="@mart341" data-embed-version="2" data-pen-title="Opacity" class="codepen"></p>
</div>
