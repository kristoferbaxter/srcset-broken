# Do `srcset` attributes work the way you expect?

This is honest confusion for me: Turns out the final image candidate in a srcset must not have a width descriptor to match what I expected.

From the [WhatWG srcset definition](https://html.spec.whatwg.org/multipage/images.html#srcset-attributes): "If an image candidate string for an element has the width descriptor specified, all other image candidate strings for that element must also have the width descriptor specified."

This doesn't appear to be true! User Agents will provide a default pixel density descriptor. 

Checkout the example in `width-descriptor-image.html` by running `npm run install; npm run serve` in this repository.
