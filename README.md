# [data-scrollmagic]
ScrollMagic data attribute shortcuts

This plugin aims to make ScrollMagic development more agile, by providing ways of creating ScrollMagic scenes via data attributes.

## Availability

```bash
bower install jquery-data-scrollmagic
```

## Installation

Install ScrollMagic as per: https://github.com/janpaepke/ScrollMagic#installation

Then add the jquery-data-scrollmagic plugin:

```html
<script src="bower_components/jquery-data-scrollmagic/jquery.data-scrollmagic.min.js"></script>
```

## Usage

### Pinning feature

```html
<!-- pin element for the duration of viewport height -->
<div data-scrollmagic='{"pin":true,"triggerHook":0,"duration":"100vh"}'></div>

<!-- pin element, pushing all elements below -->
<div data-scrollmagic='{"pin":{pushFollowers:true},"triggerHook":0,"duration":"100vh"}'></div>
```

### Tweening feature

```html
<!-- fade in (single scene) -->
<div data-scrollmagic='{"tween":{"opacity":1},"triggerHook":0.7,"duration":"75vh"}'></div>

<!-- fade in and out (two scenes) -->
<div data-scrollmagic='[{"tween":{"opacity":1},"triggerElement":"#screen-text-1","triggerHook":0.25,"duration":150},{"tween":{"opacity":0},"triggerElement":"#screen-text-2","triggerHook":1,"duration":150}]'></div>
```

### Class-toggle feature

```html
<!-- add class "active, while the element is in the center of the viewport" -->
<div data-scrollmagic='{"class":"active","duration":"100%"}'></div>

<!-- toggle class "active", while the element is in the center of the viewport -->
<div class="inactive" data-scrollmagic='{"class":{"classes":"inactive","toggle":true},"duration":"100%"}'></div>
```

### Mixing features

```html
<!-- when the element reaches screen top, pin it, and tween background color to red, for the duration of viewport height -->
<div data-scrollmagic='{"pin":true,"tween":{"backgroundColor":"#ff0000"},"class":"pinned","triggerHook":0,"duration":"100vh"}'></div>
```

### Options

Same options as for ScrollMagic Scene.

#### duration
**Type:** number or string (percentage or viewport units)  
**Default:** automatically calculated to when the scene exits the viewport  
Notice, that this is different from ScrollMagic.  
Also a percentage value will be translated refering to triggerElement's height or width respectively.  
Use viewport units (vh, vw) refer to viewport height and width.

#### offset
**Type:** number  
**Default:** 0

#### triggerElement
**Type:** string or object or function  
**Default:** the element

#### triggerHook
**Type:** string or number  
**Default:** 0, notice that this is different from ScrollMagic

#### reverse
**Type:** boolean  
**Default:** false

#### loglevel
**Type:** number
