# JS

### LocalStorage

Has methods:

- `setItem(key, value)` 
- `getItem(key)` 
- `removeItem(key)` 
- `clear()` 
- `key(index)` 
- `length` 

Syntax:

```js
localStorage.setItem('time',200);
alert(localStorage.getItem('time')); //alerts 200
```

Looping over all stored items:

```js
for(let i=0; i<localStorage.length; i++){
	let key = localStorage.key(i); //index of the ith entry
    alert(key+' : '+localStorage.geItem(key));
}
```

#### Storing objects

Keys and values must be strings. Thus, objects and numbers are automatically converted to strings. To store objects, we can use `JSON`.

```
let car = {'variant':'audi','tyres':'4'};

localStorage.setItem('car',JSON.stringify(car));
let carRecovered = JSON.parse(localStorage.getItem('car'));
alert(car.variant);
```

