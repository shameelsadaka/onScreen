onScreen
========

onScreen is a jQuery plugin that does stuff when the matched elements are visible (as inside the viewport)

The plugin works something like this:
```JavaScript
$('elements').onScreen({
   container: window,
   direction: 'vertical',
   doIn: function() {
     // Do something to the matched elements as they come in
   },
   doOut: function() {
     // Do something to the matched elements as they get off scren
   },
   tolerance: 0,
   toggleClass: true,
   lazyAttr: null,
   lazyPlaceholder: 'someImage.jpg',
   debug: false
});
```

You can checkout the demos [here](http://silvestreh.github.io/onScreen/). And you can download them [here](https://github.com/silvestreh/onScreen/archive/gh-pages.zip).

Options
-------

#### container
`string`. Tells onScreen() to track elements inside a scrollable element.<br>
__default__: `window` (without quotes)
#### direction
`string`. Tells the plugin to work in `horizontal` or `vertical` mode.<br>
__default__: `vertical`
#### doIn
`function`. Is executed whenever the matched elements enter the viewport.<br>
__default__: `null`
#### doOut
`function`. Is executed whenever the matched elements leave the viewport.<br>
__default__: `null`
#### tolerance
`integer`. The `doIn()` method will be executed when the matched element is `N` pixels inside the viewport.<br>
__default__: `0`
#### toggleClass
`boolean`. Tells the plugin to add the `onScreen` class when the elements enter the viewport and remove it when they leave.<br>
__default__: `true`
#### lazyAttr
`string`. onScreen will look for this attribute on `<img>` tags and replace the `src` attribute with this one's.<br>
__default__: `null`
#### lazyPlaceholder
`string`. Image to display while loading. This is applied through CSS as the background of the matched elements.<br>
__default__: A base64 encoded gif file.
#### debug
`boolean`. Spams your console with information about the matched elements and the scroll container.<br>
__default__: `false`.


