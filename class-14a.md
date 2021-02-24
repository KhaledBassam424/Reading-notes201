> Transform

By modifying the coordinate space, CSS transforms change the shape and position of the affected content without disrupting the normal document flow. This guide provides an introduction to using transforms.

CSS transforms are implemented using a set of CSS properties that let you apply affine linear transformations to HTML elements. These transformations include rotation, skewing, scaling, and translation both in the plane and in the 3D space.



> Note 

Only elements positioned by the box model can be transformed. As a rule of thumb, an element is positioned by the box model if it has display: block.

> CSS transforms properties

Two major properties are used to define CSS transforms: transform and transform-origin

1. > transform-origin
Specifies the position of the origin. By default, it is at the center of the element and can be moved. It is used by several transforms, like rotations, scaling or skewing, that need a specific point as a parameter.

2. > transform
Specifies the transforms to apply to the element. It is a space-separated list of transforms, which are applied one after the other, as requested by the composition operation. Composite transforms are effectively applied in order from right to left.


> Rotating

Example: 

```
<img style="transform: rotate(90deg);
            transform-origin: bottom left;"
     src="screen_shot_2016-02-16_at_15.53.54.png">
```    

> Skewing and translating

Example: 
```
<img style="transform: skewx(10deg) translatex(150px);
            transform-origin: bottom left;"
     src="screen_shot_2016-02-16_at_15.53.54.png">
```

> 3D specific CSS properties

Performing CSS transformations in 3D space is a bit more complex. You have to start by configuring the 3D space by giving it a perspective, then you have to configure how your 2D elements will behave in that space.

1. >Perspective
The first element to set is the perspective. The perspective is what gives us the 3D impression. The farther from the viewer the elements are, the smaller they are.

Setting perspective
This example shows a cube with the perspective set at different positions. How quick the cube shrinks is defined by the perspective property. The smaller its value is, the deeper the perspective is.

HTML
The HTML below creates four copies of the same box, with the perspective set at different values.
```
<table>
  <tbody>
    <tr>
      <th><code>perspective: 250px;</code>
      </th>
      <th><code>perspective: 350px;</code>
      </th>
    </tr>
    <tr>
      <td>
        <div class="container">
          <div class="cube pers250">
            <div class="face front">1</div>
            <div class="face back">2</div>
            <div class="face right">3</div>
            <div class="face left">4</div>
            <div class="face top">5</div>
            <div class="face bottom">6</div>
          </div>
        </div>
      </td>
      <td>
        <div class="container">
          <div class="cube pers350">
            <div class="face front">1</div>
            <div class="face back">2</div>
            <div class="face right">3</div>
            <div class="face left">4</div>
            <div class="face top">5</div>
            <div class="face bottom">6</div>
          </div>
        </div>
      </td>
    </tr>
    <tr>
      <th><code>perspective: 500px;</code>
      </th>
      <th><code>perspective: 650px;</code>
      </th>
    </tr>
    <tr>
      <td>
        <div class="container">
          <div class="cube pers500">
            <div class="face front">1</div>
            <div class="face back">2</div>
            <div class="face right">3</div>
            <div class="face left">4</div>
            <div class="face top">5</div>
            <div class="face bottom">6</div>
          </div>
        </div>
      </td>
      <td>
        <div class="container">
          <div class="cube pers650">
            <div class="face front">1</div>
            <div class="face back">2</div>
            <div class="face right">3</div>
            <div class="face left">4</div>
            <div class="face top">5</div>
            <div class="face bottom">6</div>
          </div>
        </div>
      </td>
    </tr>
  </tbody>
</table>
```