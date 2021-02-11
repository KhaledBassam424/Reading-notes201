> **Choosing images**

A picture can say a thousand words, and great images help make the difference between an average-looking site and a really engaging one.

> **How to add an image to your page ?**

`<img src="URL, OR A PATH OF THE IMAGE" />`

**`<img>`** 

To add an image into the page you need to use an `<img>` element. This is an empty element (which means there is
no closing tag). It must carry the following two attributes:

1. *src* : This tells the browser where it can find the image file. This will usually be a relative URL
pointing to an image on your own site.


2. *alt* : This provides a text description of the image which describes the image if you cannot see it.

3.  *title* :

You can also use the title attribute with the `<img>` element to provide additional information about the image. Most browsers will display the content of this attribute in a tootip when the user hovers over the image.

> **Example on usage of those three different attributes**
```
<img src="images/quokka.jpg" alt="A family of
quokka" title="The quokka is an Australian
marsupial that is similar in size to the
domestic cat." />
```

> **Height and width of images**

*height*

This specifies the height of the
image in pixels.

*width*

This specifies the width of the
image in pixels.

> **example on usage of height and width**
```
<img src="images/quokka.jpg" alt="A family of
quokka" width="600" height="450" />`
```

#CSS


<dl>
<dt>COLOR</dt>
<dd>The color property allows you
to specify the color of text inside
an element. You can specify any
color in CSS in one of three ways</dd>
<dt>RGB VALUES</dt>
<dd>These express colors in terms
of how much red, green and
blue are used to make it up. For
example: rgb(100,100,90</dd>
<dt>HEX CODES</dt>
<dd>These are six-digit codes that
represent the amount of red,
green and blue in a color,
preceded by a pound or hash #
sign. For example: #ee3e80</dd>
<dt>Hue</dt>
<dd>Hue defines pure color in terms of "green", "red" or "magenta". Hue also defines mixtures of two pure colors like "red-yellow" (~ "orange"), or "yellow-green"</dd>
<dt>Saturation</dt>
<dd>Saturation refers to the amount
of gray in a color. At maximum
saturation, there would be no
gray in the color. At minimum
saturation, the color would be
mostly gray.</dd>
<dt>Brightness</dt>
<dd>Brightness (or "value") refers
to how much black is in a color.
At maximum brightness, there
would be no black in the color.
At minimum brightness, the
color would be very dark</dd>

</dl>
 
> **Example on usage these properties**
```
<!DOCTYPE html>
<html>
<head>
<title>Color</title>
<style type="text/css">
body {
background-color: silver;
color: white;
padding: 20px;
font-family: Arial, Verdana, sans-serif;}
h1 {
background-color: #ffffff;
background-color: hsla(0,100%,100%,0.5);
color: #64645A;
padding: inherit;}
p {
padding: 5px;
margin: 0px;}
p.zero {
background-color: rgb(238,62,128);}
p.one {
background-color: rgb(244,90,139);}
p.two {
background-color: rgb(243,106,152);}
p.three {
background-color: rgb(244,123,166);}
p.four {
background-color: rgb(245,140,178);}
p.five {
background-color: rgb(246,159,192);}
p.six {
background-color: rgb(245,176,204);}
p.seven {
background-color: rgb(0,187,136);}
p.eight {
background-color: rgb(140,202,242);}
p.nine {
background-color: rgb(114,193,240);}
p.ten {
background-color: rgb(84,182,237);}
p.eleven {
background-color: rgb(48,170,233);}
p.twelve {
background-color: rgb(0,160,230);}
p.thirteen {
background-color: rgb(0,149,226);}
p.fourteen {
background-color: rgb(0,136,221);}
</style>
```

**text**

The font property is a shorthand property for:

font-style
font-variant
font-weight
font-size/line-height
font-family
The font-size and font-family values are required. If one of the other values is missing, their default value are used.


**Property Values**
> **Property/Value	Description**
<dl>
<dt>font-style</dt>
  <dd>	Specifies the font style. Default value is "normal"</dd>
<dt>font-variant</dt>	
<dd>Specifies the font variant. Default value is "normal"</dd>
<dt>font-weight</dt>
	<dd>Specifies the font weight. Default value is "normal"</dd>
<dt>font-size/line-height</dt>	
<dd>Specifies the font size and the line-height. Default value is "normal"</dd>
<dt>font-family	Specifies the font family. Default value depends on the browser</dt>
<dt>caption</dt>	
<dd>Uses the font that are used by captioned controls (like buttons, drop-downs, etc.)</dd>
<dt>icon</dt>	
<dd>Uses the font that are used by icon labels</dd>

menu	Uses the fonts that are used by dropdown menus
message-box	Uses the fonts that are used by dialog boxes
small-caption	A smaller version of the caption font
status-bar	Uses the fonts that are used by the status bar
initial	Sets this property to its default value. Read about initial
inherit	Inherits this property from its parent element. Read about inherit
</dl>
Example
A demonstration of some of the other font property values.

```<p style="font:caption">The browser font used in captioned controls.</p>
<p style="font:icon">The browser font used in icon labels.</p>
<p style="font:menu">The browser font used in dropdown menus.</p>
<p style="font:message-box">The browser font used in dialog boxes.</p>
<p style="font:small-caption">A smaller version of the caption font.</p>
<p style="font:status-bar">The browser font used in the status bar.</p>
```