# Browser defaults

* They teach you how to reset the browser's default CSS styles. Why?
* Study browser CSS defaults [here](https://chromium.googlesource.com/chromium/blink/+/master/Source/core/css/html.css)
* This CSS file gets applied after the DOM (Document Object Model) is created [here](./defaults.md). (The DOM is a representation of the HTML in memory.)
* What's so cool about it? Children of the `<head>` element all have `display:none` by default.
* So why change the defaults? Why not use them to our advantage?
