# SilverSASS
Library of Mixins the SASS drinking from a json file for front end. 

##Important: the latest version of gem 'sass', 'sass-rails' and 'sass-json-vars'.

##Installation Full the library
```scss
@import "silversass";
```

### Mixin - border radius
```javascript
{
	"articleRadius": {
		"selector": "article",
		"hash": "tag", //Hash: id, class or tag
		"radius": "20%"
	}
}
```

```scss
//Border Radius
$Article-selector		: map-get($articleRadius, selector);
$Article-hash			: map-get($articleRadius, hash);
$Article-radius			: map-get($articleRadius, radius);
```

```scss
@include border-radius(
	$Article-selector,
	$Article-hash, 
	$Article-radius
);
```

```css
article {
  /* Safari 3-4, iOS 1-3.2, Android 1.6- */
  -webkit-border-radius: 20%;
  /* Firefox 1-3.6 */
  -moz-border-radius: 20%;
  /* Opera 10.5, IE 9, Safari 5, Chrome, Firefox 4, iOS 4, Android 2.1+ */
  border-radius: 20%; }
```

### Mixin - Animation Bounce
```javascript
{
	"messageFlash": {
		"selector": "h1",
		"hash": "tag", //Hash: id, class or tag
		"name": "blinker",
		"duration": "1.2s",
		"timing": "linear",
		"iteration": "infinite"
	}
}
```

```scss
//Animation Bounce
$Message-selector		: map-get($messageFlash, selector);
$Message-hash			: map-get($messageFlash, hash);
$Message-name			: map-get($messageFlash, name);
$Message-duration		: map-get($messageFlash, duration);
$Message-timing			: map-get($messageFlash, timing);
$Message-iteration		: map-get($messageFlash, iteration);
```

```scss
//Animation - Bounce
@include animation(
	$Message-selector, 
	$Message-hash, 
	$Message-name, 
	$Message-duration, 
	$Message-timing, 
	$Message-iteration
);
```

```css
h1 {
  -webkit-animation-name: blinker;
  -webkit-animation-duration: 1.2s;
  -webkit-animation-timing-function: linear;
  -webkit-animation-iteration-count: infinite;
  -moz-animation-name: blinker;
  -moz-animation-duration: 1.2s;
  -moz-animation-timing-function: linear;
  -moz-animation-iteration-count: infinite;
  animation-name: blinker;
  animation-duration: 1.2s;
  animation-timing-function: linear;
  animation-iteration-count: infinite; }

  @-moz-keyframes blinker {
  0% {
    opacity: 1.0; }
  50% {
    opacity: 0.0; }
  100% {
    opacity: 1.0; } }
@-webkit-keyframes blinker {
  0% {
    opacity: 1.0; }
  50% {
    opacity: 0.0; }
  100% {
    opacity: 1.0; } }
@keyframes blinker {
  0% {
    opacity: 1.0; }
  50% {
    opacity: 0.0; }
  100% {
    opacity: 1.0; } }
```

### Mixin - Box Shadow
```javascript
{
	"articleBoxShadow": {
		"selector": "wrapper",
		"hash": "class",
		"inset": "inset", //no, inset
		"hLength": "0",
		"vLength": "0",
		"blurRadius": "10px",
		"spread": "10px",
		"colorType": "hex",
		"colorValue": "#00FF00"
	}
}
```

```scss
//Box Shadow
$wrapperShadow-selector		: map-get($articleBoxShadow, selector);
$wrapperShadow-hash			: map-get($articleBoxShadow, hash);
$wrapperShadow-inset		: map-get($articleBoxShadow, inset);
$wrapperShadow-hLength		: map-get($articleBoxShadow, hLength);
$wrapperShadow-vLength		: map-get($articleBoxShadow, vLength);
$wrapperShadow-blurRadius	: map-get($articleBoxShadow, blurRadius);
$wrapperShadow-spread		: map-get($articleBoxShadow, spread);
$wrapperShadow-colorType	: map-get($articleBoxShadow, colorType);
$wrapperShadow-colorValue	: map-get($articleBoxShadow, colorValue);
```

```scss
@include box-shadow(
	$wrapperShadow-selector, 
	$wrapperShadow-hash,
	$wrapperShadow-inset, 
	$wrapperShadow-hLength, 
	$wrapperShadow-vLength,
	$wrapperShadow-blurRadius,
	$wrapperShadow-spread,
	$wrapperShadow-colorType,
	$wrapperShadow-colorValue	
);
```

```css
.wrapper {
  -webkit-box-shadow: inset 0 0 10px 10px #00FF00;
  box-shadow: inset 0 0 10px 10px #00FF00; }
```

### Mixin - Text Shadow
```javascript
{
	"h2TextShadow": {
		"selector": "h2",
		"hash": "tag",
		"hLength": "0",
		"vLength": "0",
		"blurRadius": "10px",
		"colorType": "hex",
		"colorValue": "#00FF00"
	}
}
```

```scss
//Text Shadow
$h2TextShadow-selector		: map-get($h2TextShadow, selector);
$h2TextShadow-hash			: map-get($h2TextShadow, hash);
$h2TextShadow-hLength		: map-get($h2TextShadow, hLength);
$h2TextShadow-vLength		: map-get($h2TextShadow, vLength);
$h2TextShadow-blurRadius	: map-get($h2TextShadow, blurRadius);
$h2TextShadow-colorType		: map-get($h2TextShadow, colorType);
$h2TextShadow-colorValue	: map-get($h2TextShadow, colorValue);
```

```scss
@include text-shadow(
	$h2TextShadow-selector, 
	$h2TextShadow-hash,
	$h2TextShadow-hLength, 
	$h2TextShadow-vLength,
	$h2TextShadow-blurRadius,
	$h2TextShadow-colorType,
	$h2TextShadow-colorValue	
);
```

```css
h2 {
  text-shadow: 0 0 10px #00FF00; }
```