# RangeTouch
A super tiny library (645 bytes gzipped) to make `<input type="range">` sliders work better on touch devices.

[Checkout the demo](https://rangetouch.com)

## Why?
While building [plyr](https://plyr.io) I noticed how bad the experience was trying to use `<input type="range">` is on a touch device (particularly iOS). Touching the track on a desktop will jump the thumb handle to that point. However on some touch devices this simply focuses the input and to adjust the value you need to touch and drag the handle. This is something that I can't help but feel will eventually be fixed by the browser vendors but for now, you can use RangeTouch to fill that gap.

## Quick setup
To use RangeTouch in it's most basic form, you just need to add `rangetouch.js` (either from the `/dist` (minified) or `/src/js` (unminified) folders) before the closing `</body>` tag like so:
```html
<script src="/path/to/rangetouch.js"></script>
```

You can even use our CDN if you'd like:
```html
<script src="https://cdn.rangetouch.com/0.0.1/rangetouch.js"></script>
```

## Configuration
If you're customizing your range inputs (easily done - see the demo for an example) and you change the size of the thumb handle, you should specify (in pixels) this after including the script:
```javascript
window.rangetouch.set("thumbWidth", 15);
```
This value is used as part of the calculation to determine the value the users selects when touching the range track. Unfortunately as JavaScript can't access the shadow DOM, this value can't be automatically determined. I would recommend customisation (and setting the size of the thumb) given all OS and browser combinations seem to render the control differently (as per usual).

## Issues
If you find anything weird with RangeTouch, please let us know using the GitHub issues tracker.

## Author
RangeTouch is developed by [@sam_potts](https://twitter.com/sam_potts) / [sampotts.me](http://sampotts.me)

## Copyright and License
[The MIT license](license.md).