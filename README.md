# SilverSASS
Library of Mixins the SASS drinking from a json file for front end. 

####Important: the latest version of gem 'sass', 'sass-rails' and 'sass-json-vars'.

###Installation Full the library
```scss
@import "silversass";
```

###List of Mixins
1. border-radius
2. animation
    * bounce
    * blinker
3. box-shadow
4. text-shadow
5. flex-box
6. box-sizing

### Mixin - Example
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
//Example
$Article-selector		: map-get($articleRadius, selector);
$Article-hash			: map-get($articleRadius, hash);
$Article-radius			: map-get($articleRadius, radius);
```

```scss
//Example
@include border-radius(
	$Article-selector,
	$Article-hash, 
	$Article-radius
);
```

```css
//Example
article {
  /* Safari 3-4, iOS 1-3.2, Android 1.6- */
  -webkit-border-radius: 20%;
  /* Firefox 1-3.6 */
  -moz-border-radius: 20%;
  /* Opera 10.5, IE 9, Safari 5, Chrome, Firefox 4, iOS 4, Android 2.1+ */
  border-radius: 20%; }
```
