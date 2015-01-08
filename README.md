Touch Emulator
========

Emulate multi-touch input on desktop. Triggers touch events as
[specified by W3C](http://www.w3.org/TR/touch-events). Press the `shift` key to pinch and rotate. Customized for specific project.


## How to use
Include the javascript file, and call the `Emulator()` function before any other libraries that do something with the 
touch input. It will set some fake properties to spoof the touch detection of some libraries, and triggers `touchstart`, `touchmove` and `touchend` events on the mouse target.

Also, the script includes polyfills for `document.createTouch` and `document.createTouchList`.

## How it works
It listens to the `mousedown`, `mousemove` and `mouseup` events, and translates them to touch events. If the mouseevent
has the `shiftKey` property to `true`, it enables multi-touch. 