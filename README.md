# SilverSASS
Library of Mixins the SASS drinking from a json file for front end. 

##Important: the latest version of gem 'sass', 'sass-rails' and 'sass-json-vars'.

### Mixin - border radius
```javascript
{
	"articleRadius": {
		"selectorGold": "wrapper",
		"selector": "article",
		"hash": "id", //Hash: id, class or tag
		"radius": "20%"
	}
}
```

```scss
$Article-selector-gold: map-get($articleRadius, selectorGold);
$Article-selector: map-get($articleRadius, selector);
$Article-radius: map-get($articleRadius, radius);
$Article-hash: map-get($articleRadius, hash);
```

```scss
@include border-radius($Article-hash, $Article-selector-gold, $Article-selector, $Article-radius);
```

```css
#wrapper article {
  /* Safari 3-4, iOS 1-3.2, Android 1.6- */
  -webkit-border-radius: 20%;
  /* Firefox 1-3.6 */
  -moz-border-radius: 20%;
  /* Opera 10.5, IE 9, Safari 5, Chrome, Firefox 4, iOS 4, Android 2.1+ */
  border-radius: 20%; 
}
```

### Mixin - Animation Bounce
```javascript
{
	"messageBounce": {
		"selectorGold": "wrapper",
		"selector": "h1",
		"hash": "id", //Hash: id, class or tag
		"name": "bounce",
		"duration": "1.2s" 
	}
}
```

```scss
$Message-selector-gold: map-get($messageBounce, selectorGold);
$Message-selector: map-get($messageBounce, selector);
$Message-hash: map-get($messageBounce, hash);
$Message-name: map-get($messageBounce, name);
$Message-duration: map-get($messageBounce, duration);
```

```scss
@include animation($Message-hash, $Message-selector-gold, $Message-selector, $Message-name, $Message-duration);
```

```css
#wrapper h1 {
  -webkit-animation: bounce 1.2s ease-out;
  -moz-animation: bounce 1.2s ease-out;
  -o-animation: bounce 1.2s ease-out;
  animation: bounce 1.2s ease-out; 
}

/* Webkit, Chrome and Safari */
@-webkit-keyframes bounce {  
...
```