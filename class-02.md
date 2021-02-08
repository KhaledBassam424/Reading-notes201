**Why we add tags to the contents of the page? **
Those tags provide extra meaning allow browsers to show users the
appropriate structure for the page.

** What are the unpopular tags we work with in html language and the function of each of them and mention an example on each of them ?**

1. <b> tag : by enclosing words in the tags <b> and </b> we can make characters appear bold. 
For example: <p>This is how we make a word appear <b>bold.</b>
</p>

2. <i> tag : By enclosing words in the tags <i> and </i> we can make characters appear italic.
For example: <p>This is how we make a word appear <i>italic</i>. </p>

3. <sup> tag : is used to contain characters that should be superscript such as the suffixes of dates or mathematical concepts like raising a number to a power such
as 22.

4. <sub> tag : is used to contain characters that should be subscript. It is commonly used with foot notes or chemical formulas such as H20.

For example : <p>The amount of CO<sub>2</sub> in the atmosphere
grew by 2ppm in 2009<sub>1</sub>.</p>

5. <br /> tag : is used to add a line break inside the
middle of a paragraph

6. <hr /> : To create a break between themes — such as a change of topic in a book or a new scene in a play — you can add a horizontal rule between sections.

For example : <p>Venus is the only planet that rotates
clockwise.</p>
<hr />
<p>Jupiter is bigger than all the other planets
combined.</p>
   | term     | definition    | 
 |----------|:-------------:|
1. | semantic markup | are some text elements that are not intended to affect the
structure of your web pages, but they do add extra information to the
pages — they are known as semantic markup |

2.  | script |  is a series of instructions that a computer can follow one-by-one.
Each individual instruction or step is known as a statement.
Statements should end with a semicolon.  |


** what are the main semantic markup tags**

1. <strong> tag : The use of the <strong> element indicates that its content has strong importance. For example, the words contained in this element might
be said with strong emphasis. For example
<p><strong>Beware:</strong> Pickpockets operate in
this area.</p>
2. <em> tag : The <em> element indicates emphasis that subtly changes
the meaning of a sentence. 
For example : <p>I <em>think</em> Ivy was the first.</p>


** What are the main idea behind usage of css ?**
CSS allows you to create rules that control the way that each individual box (and the contents of that box) is presented.

CSS works by associating rules with HTML elements. These rules govern
how the content of specified elements should be displayed. A CSS rule
contains two parts: a selector and a declaration.

![selector-declaretion](https://www.w3schools.com/whatis/img_selector.gif)

CSS declarations sit inside curly brackets and each is made up of two
parts: a property and a value, separated by a colon. You can specify
several properties in one declaration, each separated by a semi-colon.

For example: h1, h2 ,h3{
    font family: Arial;
    color: orange ;

}

**How we can connect css to html page?** 
| method   |      details  |   example    |     
|----------|:-------------:|------:|
| Using External CSS, <link> tag |  The <link> element can be used
in an HTML document to tell the
browser where to find the CSS
file used to style the page | <head>
<title>Using External CSS</title>
<link href="css/styles.css" type="text/css"
rel="stylesheet" />
</head>
<body> |
| Usi ng Internal CSS, <style> tag |    You can also include CSS rules
within an HTML page by placing
them inside a <style> element,
which usually sits inside the
<head> element of the page   |  <head>
<title>Using Internal CSS</title>
<style type="text/css">
body {
font-family: arial;
background-color: rgb(185,179,175);}
h1 {
color: rgb(255,255,255);}
</style> |
| inline styling  | <p style="color: red; background-color: gray"> |

** declaring a variable**
we should announce that we want to use a specific variable by declaring it.

var quantity:

**how to assign a value to the variable**
quantity = 3:
 
 ** creating an array in java script**
 II Create the array
var colors = ['white',
'black' ,
'custom'];
c02/ js/ update-array.js
II Update the third item in the array
colors[2] = 'beige ' ;
II Get the element with an id of col ors
var el = document .getElementByid(' colors') ;
II Replace with third item from the array
el .textContent = colors[2];


