# mousewheel

cross-browser `wheel` event handling based on [Mozilla wheel shim](https://developer.mozilla.org/en-US/docs/Mozilla_event_reference/wheel#Listening_to_this_event_across_browser)

## installation

```bash
$ component install ramitos/mousewheel
```

## example

```js
var mousewheel = require('mousewheel');

var onScroll = function (e) {
  console.log(e.deltaX);
  console.log(e.deltaY);
};

setTimeout(function () {
  mousewheel.unbind(document.body, onScroll);
}, 10000);

mousewheel.bind(document.body, onScroll);
```

## api

### .bind(el, callback, [capture])

### .unbind(el, callback, [capture])

## license

MIT