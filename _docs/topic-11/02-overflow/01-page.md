---
title: Dealing with Spills
module: topic-11
permalink: /topic-11/overflow-intro/
---

<div class="divider-heading"></div>

<img src="../img/box-model-overflow.gif" alt="example of overflow scrolling" style="width: 350px; margin: 0 auto 30px;" />

When we were learning about <a href="./../box-sizing#combine-size" target="_blank">combining size types</a>, we saw an example where the text inside an element "overflowed" its containing box. We can choose to address this situation in a couple of ways:

1. Ignore it (boo!).
2. Resize our elements so they fit the content.
3. Tell the browser what to do with _extra_ content.

In the latter option, we will use the "overflow" CSS property (`overflow: `). This property takes one of three values:

- `visible`; this is the default.
- `hidden`; overflow content will be hidden.
- `scroll`; scroll bars will be provided for overflow content.
