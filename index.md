# Le Wagon JS cheatsheat for beginners

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
var last_p_on_page = els[els.length-1]

var third_p_el = els[2];
```

The syntax is different 😱
but the concepts are all the same 🤗

## AJAX & HTTP

What are the HTTP requests?

- `GET request`: get content (I want to read comments/images/..)
- `POST request`: send new data (Here are my email and password, I want to sign up!)

What's AJAX?

- Allows to load data in the page without refreshing it!
- Let Javascript handle **HTTP** requests

How to do AJAX?

- **$.ajax()** with jQuery
- **fetch()** is more modern

**Example of GET request with fetch():**

```javascript

var url = 'https://some.api.com'

fetch(url)
  .then(
    function(response) {

      if(!response.ok) console.log('something went wrong!', response);

      // Examine the text in the response from the API
      response.json().then(function(data) {

        // We have succesfully fetched data!!
        console.log(data);

      });
    }
  )
  .catch(function(err) {
    console.log('Fetch Error :-S', err);
  });
```

**Example of POST request with fetch():**

```javascript

var url = 'https://some.api.com'
request_body_object = { "description":"Demo string" };
var json_string = JSON.stringify(request_body_object);

fetch(url,{method:"POST",body:json_string})
  .then(
    function(response) {

      // Examine the text in the response from the API
      response.json().then(function(response_body_object) {

        // We have succesfully posted data!!
        console.log(response_body_object);

      });
    }
  );
```




