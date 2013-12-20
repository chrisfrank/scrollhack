ScrollHack
==========
Native scrolling in an iOS web app works great, almost. When you get to the top or bottom of an element with <code>-webkit-overflow-scrolling: touch</code>, your entire UI bounces, just like a regular old web page.

I suspect Apple will fix this problem someday. Until then, use scrollhack.js to make your web apps feel more native.

The hack watches scrollable elements, and adjusts their scroll position by one pixel when you touch them. This tricks iOS into thinking you're scrolling from somewhere other than the top or bottom, so <code>touchmove</code> events never propogate all the way to the document <code>body</code>.

![ScrollHack Illustrated](http://chrisfrank.github.io/scrollhack/scrollhack.jpg)
Installation
------------
Include <code>scrollhack.js</code> anywhere in your document.
Style some elements (or just one) with <code>-webkit-overflow-scrolling: touch</code>

Dependencies
------------
None.

FAQ
---
### Will it work with elements insterted into the DOM after the script is initialized?
Yep.
