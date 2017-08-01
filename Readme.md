#Le Wagon JS cheatsheat for beginners

## JavaScript ES5

- Callback functions

```javascript
Some_API.register(callback) 
// register your callback

function callback(){
	do_something_else() 
	// this code will run when something happens
}
```

- Objects

Objects have properties.

```javascript
var obj = {some_property_name:"Property Value"}

// example:
var person = {
	first:"Michaeljohn",
	last:"Clement"
	}

// use the property name to return its value:
person.first 
// => "Michaeljohn"

person['first'] 
// => "Michaeljohn"

var property_name = 'first'
person[property_name] 
// => "Michaeljohn"


```


- Arrays

Can store any type of data.

```javascript
// string, integers, functions...
var array = ["a",42,0,7,new Date(),function(x){return x*x}]

// but prefer storing always the same type
var simple_array = ["string","another string"]

// use the index to return a value:
simple_array[0] 
// => "string"

// here's an array of objects... classic structure:
var arr_of_objs = [{x:"y"},{x:"z"},{x:"a"}]

// use the [index] and .property to return a value:
arr_of_objs[2].x
// => "a" 

arr_of_objs.length
// => 3
```

## jQuery


**$()**

Whenever you see this dollar sign... it's jQuery! A powerful **library** of Javascript code. Its helps for cross-browser compatibility.

```javascript
// to select a DOM element, use CSS selectors! 
// .class #id ...
$('.logo')

// to add an event listener:
$('.logo').on('click', callback)

// the dollar sign selects and return a jQuery object
var jQuery_object = $('#some_id')
```

## DOM

What is the DOM?

- A big tree.
- A hierarchical representation of your markup.
- The browser's idea of your HTML in memory.

**The DOM has its own built-in methods, similar to jQuery:**

```javascript
// to select a DOM element
var element = document.querySelector('#some_id')

// to add an event listener:
element.addEventListener('click', callback)

// to select multiple DOM elements:
els = document.querySelectorAll('p')

// to find the last:
els.lastChild
```

The syntax is different 😱 
but the concepts are all the same 🤗