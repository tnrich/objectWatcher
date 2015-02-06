##ObjectWatcher

A super simple package to allow you to set watchers/listeners on your javascript variables.

Useful mostly for debugging when you aren't sure where a variable is being set/modified. 

Just slap a watcher on it:

```
var watch = require(object-watcher).watch;

var data = {
     quantity: 0
     , products:  []
}
, watcher = function(propertyName, oldValue, newValue){ 
	console.log("Variable Changed!");
};

watch(data, 'quantity', watcher);
watch(data, 'products', watcher);

data.quantity = 8
// Variable Changed!
```