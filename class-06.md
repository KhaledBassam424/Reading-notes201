**object**

Objects group together a set of variables and functions to create a model of a something you would recognize from the real world. In an object, variables and functions take on new names. 

> IN AN OBJECT: VARIABLES BECOME KNOWN AS PROPERTIES.

If a variable is part of an object, it is called a
property. Properties tell us about the object, such as
the name of a hotel or the number of rooms it has.
Each individual hotel might have a different name
and a different number of rooms.


> IN AN OBJECT: FUNCTIONS BECOME KNOWN AS METHODS.

If a function is part of an object, it is called a method.
Methods represent tasks that are associated with
the object. For example, you can check how many
rooms are available by subtracting the number of
booked rooms from the total number of rooms.



> Object Properties
The name:values pairs in JavaScript objects are called properties:

Property :	Property Value

firstName :	John
lastName  :Doe
age	    :  50
eyeColor : blue


How can I access and process nested objects, arrays or JSON  using javascript?

JavaScript has only one data type which can contain multiple values: Object. An Array is a special form of object.

(Plain) Objects have the form

{key: value, key: value, ...}
Arrays have the form

[value, value, ...]
Both arrays and objects expose a key -> value structure. Keys in an array must be numeric, whereas any string can be used as key in objects. The key-value pairs are also called the "properties".

Properties can be accessed either using dot notation

const value = obj.someProperty;
or bracket notation, if the property name would not be a valid JavaScript identifier name [spec], or the name is the value of a variable:

// the space is not a valid character in identifier names
const value = obj["some Property"];

// property name as variable
const name = "some Property";
const value = obj[name];
For that reason, array elements can only be accessed using bracket notation:

const value = arr[5]; // arr.5 would be a syntax error

// property name / index as variable
const x = 5;
const value = arr[x];




How to select DOM elements using JavaScript
May 21, 2019  Atta

 TABLE OF CONTENTS ⛱
The Document Object Model (DOM) is a programming interface for HTML and XML documents created by the browser once the document is loaded. A web page is essentially a document represented by the DOM as nodes and objects. It allows programs to manipulate the document's content, structure, and styles.

In this tutorial, we will learn how to use JavaScript to access different nodes (HTML elements) in the DOM. Let us start with the first method: getting element by ID.

Get Element By ID
The document's getElementById() method takes the element ID as input and returns an Element object representing the DOM element. Here is an example:

`<div id="unicorn">🦄</div>`
Now here is how we can get the above `<div>` element by using its ID:

const unicorn = document.getElementById('unicorn');
The ID is case-sensitive and unique across the entire HTML document. So this method always returns a single element. If no matching element is found, it returns null.

Note: Do not put the # sign before the ID string while calling getElementById() method. You will get null instead of the element, and then you might wonder for hours what has gone wrong.

Get Elements By Tag Name
The getElementsByTagName() method is used to access multiple elements. It takes the tag name as input and returns all of the DOM elements that match the tag name as HTMLCollection:
```
<p>🐱</p>
<p>🐰</p>
<p>🐯</p>
<p>🐧</p>
JavaScript code to access all <p> elements:
```
const animals = document.getElementsByTagName('p');
This method searches only one tag name at a time. But if you pass in * as the tag name, you will get all elements in the DOM:

const allNodes = document.getElementsByTagName('*');
Get Elements By Name
The getElementsByName() method is used to get a collection of elements by their name attribute, and returns a NodeList object:
```
<input type="text" name="email">
<input type="tel" name="phone">
<input type="date" name="dob">
Let us get all the elements with the name email:
```
const emails = document.getElementsByName('email');
Note: Unlike the id attribute, which must be unique, multiple HTML elements can have the same name attribute. That's why getElementsByName() returns a collection of nodes.

Get Elements By Class Name
Want to use class attribute to get a list of matching elements? You can use getElementsByClassName() method, just pass it a class name (without .) and it will return an HTMLCollection of all DOM elements that have the given class name:
```
<div class="bird owl">🦉</div>
<div class="bird">🐦</div>
<div class="bird eagle">🦅</div>
<div class="animal cat">🐱</div>
Let us get all the bird's:
```
const birds = document.getElementsByClassName('bird');
This method also accepts multiple class names separated by spaces. Let us get all elements that have both the bird and eagle classes:

const eagle = document.getElementsByClassName('bird eagle');
Query Selector
The querySelector() method is one of the two modern JavaScript methods that allow you to get elements from DOM, based on CSS selectors. Just pass in the CSS selector and you will get the first element that matches the specified selector. If no matches exist, it returns null. Here is an example:

const email = document.querySelector('#signup input[name="email"]');
Query Selector All
Want to select a list of elements that match the specified selectors? Use querySelectorAll() method instead. This method takes multiple CSS selectors as input and returns a NodeList — a list of DOM elements that match the given selectors. Let us select all elements with a class of either bird or animal from the above HTML markup:

const elems = document.querySelectorAll('.bird, .animal');
console.log(elems.length); // 4
































![DOM](https://simplesnippets.tech/wp-content/uploads/2018/10/what-is-document-object-model-in-JS-featured-image.jpg)