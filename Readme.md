# Browser defaults

- They teach you to reset the browser defaults. Buy why?
- Study browser css defaults [here](https://chromium.googlesource.com/chromium/blink/+/master/Source/core/css/html.css)
- This css file 👆 gets applied after the dom is created [here](./defaults.md). (dom is a representation of the html in the memory)
- What's so cool about it? children of the <head> element all have display:none 😁
- So why change the defaults? Why not use them to our advantage?
