## Animoto
> Javascript utility for animations

![animoto demo](https://raw.github.com/joegesualdo/animoto/master/animoto-demo.gif)

## Install
```
$ npm install --save animoto
```

## Usage
```javascript
var Animoto = require('animoto');

var $square = document.querySelector('#square');

Animoto({
  start: $square.offsetLeft,
  stop: $square.offsetLeft + 300,
  duration: 2000 
})
.on('tick', function(val) {
  var $square = document.querySelector('#square')
  $square.style.left = val + "px";
})

.on('done', function(){
  console.log('done')
})
.begin()
```
