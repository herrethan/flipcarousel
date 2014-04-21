jQuery Flip Carousel
====================

Flip Carousel is an alternative to an image/content carousel. Instead of sliding or cross-fading content, it flips like a deck of cards. It will continually append content behind the scenes with respect to the direction you are flipping. It uses lots of cool CSS3 transitions and animations, and *no* JS animation.

Requires:
- jQuery 1.8.1 or above
- HTML5 Shiv for IE < 10 support.

[See a demo here](http://herrmedia.com/projects/flip/)

Features
--------
- Includes a check for inline images and will always preload one page ahead to ensure smooth flipping
- Randomizer for more organic looking flipping
- Graceful degradation for IE8/9 and JS disabled


Usage
-----
The plugin should be invoked on a jQuery array of any like elements, not a container. And not directly on list items (the plugin wraps the cards in list items).

```javascript
$('.content-cell').flipcarousel();
```

Options
-------

- **arrows**  ```boolean```
Whether or not to show the navigation arrows (previous and next).
Default: *true*

- **duration** ```number```
Number of milliseconds for the flip transition to take. 
Default: *500*

- **itemsperpage**  ```integer```
The number of cards to show at once. Can be any number that goes well with your total number of items.
Default: *3*

- **loader** ```boolean```
Whether or not to show the css spinning loader when images are being loaded. 
Default: *true*

- **randomizer** ```number```
For that slightly more staggered look. Deviates from the set flip duration by the magnitude specified. For best results, use a decimal between 0 and 1. When set to 1, the duration will be deviated by -0.5x and +1.5x, and randomly applied to the set of cards on each flip. A delay between 0 and the flip duration will also be randomly applied across the set.
Default: *0*


Events
------
Coming soon


Sample Markup
-------------

```html
<article><h1>Item 1</h1><span>content</span></article>
<article><h1>Item 2</h1><span>content</span></article>
<article><h1>Item 3</h1><span>content</span></article>
<article><h1>Item 4</h1><span>content</span></article>
<article><h1>Item 5</h1><span>content</span></article>
```

```javascript
$('article').flipcarousel({
		loader : true,
		itemsperpage: 3,
		randomizer: 0.7
	});
```

Ideas for the Future
----------
- Add touch events for mobile for thumb-swipability
- Add ability to click on a card and "zoom-in" to the content
- Add pagination dots, ability to jump to any page



- - -
Licensed under the open source MIT License.
http://www.opensource.org/licenses/mit-license.php

&copy; 2014 [Ethan Herr](http://www.herrmedia.com)
