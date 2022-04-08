# tAni

## TLDR
This library animates text and works on web browser (Chrome / FireFox / Opera / Safari)
This repository was created for my study.

## Usage
### Include
To use it, you must add the following code within your html header tag.

```html
<link rel="stylesheet" href="lib/text_animation.css">
<script src="lib/text_animation.js"></script>
```

### Set Animation
Add `.text-animation` to the class of the parent element closest to the text to be animated.  

Finally, set up the animation. After all elements have been loaded (`window.onload`), an instance of tAni must be created.

```html
<p id="title" class="text-animation">Hello World!</p>
<script>
window.onload = function(){
    var textAnimation = new tAni({
        id    : 'title',
        speed : 100,
        delay : 400,
        dir   : 'top',
        ran   : false
    });
}
</script>
```
The constructor of tAni has several configuration items that can be set: id of the element to be animated, animation speed, animation delay, animation direction, and random animation direction.

If you set `ran`, it will override the `dir` setting and will not be used.

All time-related setting values are in milliseconds.

## Sample

There is no demo page. Samples can be found in `index.html` in the sample directory.
