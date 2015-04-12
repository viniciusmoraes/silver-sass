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
