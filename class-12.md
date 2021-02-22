> the `<canvas>` element

The HTML `<canvas>` element is used to draw graphics on a web page.

The graphic to the left is created with `<canvas>`. It shows four elements: a red rectangle, a gradient rectangle, a multicolor rectangle, and a multicolor text.

> What is HTML Canvas?

The HTML `<canvas>` element is used to draw graphics, on the fly, via JavaScript.

The `<canvas>` element is only a container for graphics. You must use JavaScript to actually draw the graphics.

Canvas has several methods for drawing paths, boxes, circles, text, and adding images.

> Note

Note: Always specify an id attribute (to be referred to in a script), and a width and height attribute to define the size of the canvas. To add a border, use the style attribute.

> Example:

`<canvas id="myCanvas" width="200" height="100"></canvas>`


> chart.js

Chart.js is an open source JavaScript library on Github that allows you to draw different types of charts by using the HTML5 canvas element. Since it uses canvas, you have to include a polyfill to support older browsers.

> This library supports 8 different types of graphs :

1. Line
2. Bar
3. Doughnut
4. Pie
5. Radar
6. Polar Area
7. Bubble
8. Scatter

>  Steps to create a chart:

1. First include the chart.js in the HTML.

```<head> 
<script src= 
"https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.2/Chart.bundle.js"> 
</script> 
<link rel="stylesheet" type="text/css" href="style.css"> 
</head> 
```

2. Create canvas: To create a chart we need to represent the Chart class. In order to do this, we need to pass jQuery instance or 2d context of the canvas of where we want the place or draw the chart.


3. Type of Chart and Data: Decide what type of chart is required and prepare the data accordingly. Data requires labels, datasets, data values, backgroundColor,borderColor, borderWidth and various other options.
For example:
```
filter_none
brightness_4
labels:[“CS”, “IT” , “ECE” , “EE”, ”ME”, “BE”], 
And datasets:  
    Label: ‘# of students’, 
    Data : [105,124,78,91,62,56], 
    backgroundColor :['rgba(255, 99, 132, 0.2)', 
                'rgba(54, 162, 235, 0.2)', 
                'rgba(255, 206, 86, 0.2)', 
                'rgba(75, 192, 192, 0.2)', 
                'rgba(153, 102, 255, 0.2)', 
                'rgba(255, 159, 64, 0.2)'
], 
  
borderColor: [ 
                'rgba(255,99,132,1)', 
                'rgba(54, 162, 235, 1)', 
                'rgba(255, 206, 86, 1)', 
                'rgba(75, 192, 192, 1)', 
                'rgba(153, 102, 255, 1)', 
                'rgba(255, 159, 64, 1)'
            ] 
```
And finally, we should decide the type of chart from a line, bar, radar, pie, doughnut, polar area, bubble and scatter.

4. Create a graph: After defining what type of graph is to be drawn, pass the data to that graph that we want to visualize. Below is an example:
```
filter_none
brightness_4
var ctx = document.getElementById("chart"); 
var myChart = new Chart(ctx, { 
  type: 'bar', 
  data: { 
    Labels: [“CS”, “IT” , “ECE” , “EE”, ”ME”, “BE”], 
    datasets: [ 
      { 
       label: ‘# of students’, 
    data : [105,124,78,91,62,56], 
    backgroundColor :['rgba(255, 99, 132, 0.2)', 
                'rgba(54, 162, 235, 0.2)', 
                'rgba(255, 206, 86, 0.2)', 
                'rgba(75, 192, 192, 0.2)', 
                'rgba(153, 102, 255, 0.2)', 
                'rgba(255, 159, 64, 0.2)'
], 
  
borderColor: [ 
                'rgba(255,99,132,1)', 
                'rgba(54, 162, 235, 1)', 
                'rgba(255, 206, 86, 1)', 
                'rgba(75, 192, 192, 1)', 
                'rgba(153, 102, 255, 1)', 
                'rgba(255, 159, 64, 1)'
            ], 
borderWidth : 1 
  
} 
      } 
```



> Applying Styles and Colors in canvas:

Up until now we have only seen methods of the drawing context. If we want to apply colors to a shape, there are two important properties we can use: fillStyle and strokeStyle.

fillStyle = color
Sets the style used when filling shapes.
strokeStyle = color
Sets the style for shapes' outlines.
color is a string representing a CSS `<color>`, a gradient object, or a pattern object. We'll look at gradient and pattern objects later. By default, the stroke and fill color are set to black (CSS color value #000000).

Note: When you set the strokeStyle and/or fillStyle property, the new value becomes the default for all shapes being drawn from then on. For every shape you want in a different color, you will need to reassign the fillStyle or strokeStyle property.

The valid strings you can enter should, according to the specification, be CSS `<color>` values. Each of the following examples describe the same color.

// these all set the fillStyle to 'orange'
```
ctx.fillStyle = 'orange';
ctx.fillStyle = '#FFA500';
ctx.fillStyle = 'rgb(255, 165, 0)';
ctx.fillStyle = 'rgba(255, 165, 0, 1)';
```