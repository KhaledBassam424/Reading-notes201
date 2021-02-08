**what are the main three types of lists**
1. orederd list: is is created using `<ol>` . it shows the elements using numbers
#### for example

```
<ol>
<li>Chop potatoes into quarters</li>
<li>Simmer in salted water for 15-20
minutes until tender</li>
<li>Heat milk, butter and nutmeg</li>
<li>Drain potatoes and mash</li>
<li>Mix in the milk mixture</li>
</ol>
```
2. unodered list: it is created using `<ul>`. it shows the elements using bullets
#### for example: 
```
<ul>
<li>1kg King Edward potatoes</li>
<li>100ml milk</li>
<li>50g salted butter</li>
<li>Freshly grated nutmeg</li>
<li>Salt and pepper to taste</li>
</ul>
```
3. definition list: The definition list is created with the `<dl>` element and usually consists of a series of terms and
their definitions.
Inside the `<dl>` element you will usually see pairs of `<dt>` and `<dd>` elements.

#### `<dt>`
to contain the term being defined
#### `<dd>`
to contain the definition of the term

#### for example :
```
<dl>
<dt>Sashimi</dt>
<dd>Sliced raw fish that is served with
condiments such as shredded daikon radish or
ginger root, wasabi and soy sauce</dd>
```

<dl>
<dt>nested loop</dt>
<dd>is a loop where we put a list inside a list</dd>
<dt>Padding</dt>
<dd>Padding is the space between
the border of a box and any
content contained within it.
Adding padding can increase the
readability of its contents</dd>
<dt>Margin</dt>
<dd>Margins sit outside the edge
of the border. You can set the
width of a margin to create a
gap between the borders of two
adjacent boxes.</dd>
<dt>border</dt>
<dd>Every box has a border (even if
it is not visible or is specified to
be 0 pixels wide). The border
separates the edge of one box
from another.</dd>
  <dt>White space</dt>
<dd>Designers refer to the space
between items on a page as
white space</dd>
  <dt>array</dt>
<dd>An array is a special type of variable. It doesn't
just store one value; it stores a list of values</dd>
 </dl>



#### example on the nest loop: 
```
<ul>
<li>Mousses</li>
<li>Pastries
<ul>
<li>Croissant</li>
<li>Mille-feuille</li>
<li>Palmier</li>
<li>Profiterole</li>
</ul>
</li>
<li>Tarts</li>
</ul>
```
![Padding, Margin, Border](https://i.ytimg.com/vi/RMNHZsDUZMo/maxresdefault.jpg)


**what is the job of display command?**
The display property allows you to turn an inline element into a block-level element or vice versa, and can also be used to hide an element from the page.
The values this property can take are:
1. > inline
This causes a block-level
element to act like an inline
element.
2. > block
This causes an inline element to
act like a block-level element.
3. > inline-block
This causes a block-level
element to flow like an inline
element, while retaining other
features of a block-level element.

#### Example : 
```
<ul>
<li>Home</li>
<li>Products</li>
<li class="coming-soon">Services</li>
<li>About</li>
<li>Contact</li>
</ul>
li {
display: inline;
margin-right: 10px;}
li.coming-soon {
display: none;}
```
**when should we use the array?**

> You should consider using an array whenever you are working with a list or a set of values that are related to each other.

> Arrays are especially helpful when you do not know how many items a list will contain because, when you create the array, you do not need to specify
how many values it will hold.

> If you don't know how many items a list will contain, rather than creating enough variables for a long list (when you might only use a small percentage
of them), using an array is considered a better solution.

**Example of usage arry**
```
var colors;
colors ['white', 'black', ' custom '];
var el document.getElementByld('col ors');
el . textContent = col ors[O];
```

## The switch statement
is used to perform different actions based on different conditions.

The JavaScript Switch Statement Use the switch statement to select one of many code blocks to be executed.

Syntax
```
switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
```
This is how it works:

The switch expression is evaluated once.
The value of the expression is compared with the values of each case.
If there is a match, the associated block of code is executed.
If there is no match, the default code block is executed.
Example
The getDay() method returns the weekday as a number between 0 and 6.

(Sunday=0, Monday=1, Tuesday=2 ..)

This example uses the weekday number to calculate the weekday name:
```
switch (new Date().getDay()) {
  case 0:
    day = "Sunday";
    break;
  case 1:
    day = "Monday";
    break;
  case 2:
     day = "Tuesday";
    break;
  case 3:
    day = "Wednesday";
    break;
  case 4:
    day = "Thursday";
    break;
  case 5:
    day = "Friday";
    break;
  case 6:
    day = "Saturday";
}
```
The result of day will be:

Monday

![Switch statement](https://kindsonthegenius.com/javascript/wp-content/uploads/2019/03/Switch-Statement-Flowchart.jpg)

