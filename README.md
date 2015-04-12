# SilverSASS
Library of Mixins the SASS drinking from a json file for front end. 


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