Well, this is truely new for me becasue to be honest, I've never used Canvas in my projects. Let's learn Canvas step by step.

## Canvas related:
### The `<canvas>` element

`
<canvas id="draw" width="800" height="800"></canvas>
`

At first sight a `<canvas>` looks like the `<img>` element. But the `<canvas>` element has only two attributes, `width` and `height`. These are both optional and can also be set using DOM properties. As in this tutorial, we set the width and height of the `<canvas>` element to window's width and height `canvas.width = window.innerWidth; canvas.height = window.innerHeight`

### The rendering context
The `<canvas>` element creates a fixed-size drawing surface that exposes one or more `rendering contexts`, which are used to create and manipulate the content shown. In this tutorial, we focus on the 2D rendering context. Other contexts may provide different types of rendering; for example, WebGL uses a 3D context based on OpenGL ES.

The canvas is initially blank. To display someting, a script first needs to access the rendering context and draw on it. The `<canvas>` element called `getContext()`, used to obtain the rendering context and its drawing functions. `getContext()` takes one parameter, the type of context. For 2D graphics, such as those covered by this tutorial, you specify "2d" to get a `CanvasRenderingContext2CD`
`
const canvas = document.querySelector("#draw")
const ctx = canvas.getContext('2d')
`

### Drawing paths
In this tutorial, we're going to draw paths. A path is a list of points, connected by segments of lines that can be of different shapes, curved or not, of different width and of different color. To make shapes using paths takes some steps:
1. First, you create the path.
2. The you use drawing commands to draw into the path. 
3. One the path has been created, you can stroke or fill the path to render it.
Here are the functions used to perform these steps in this tutorial

`beginPath()`:
Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.

`moveTo()`: After the first path construction, you will almost always want to specifically set your starting position by `moveTo()`

`lineTo(x, y)`: Draws a line from the starting position in the former step to the position specified by `x` and `y`

`stroke()`: Render the path created.

For more information about Canvas, feel free to refer to [Canvas tutorial](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial).

Now let's start the real practice

## Steps

1. Get the `canvas` element, set its width and height.
2. Create and manipulate the content by `const ctx = canvas.getContext('2d')`. And specify its `strokeStyle`, `lineJoin`, `lineCap` and `lineWidth`
3. Add event listeners to start drawing. We need to watch `mousemove` event to catch the track. But we need to specify when to start drawing and when to finish. So we add a `isDrawing` state to note. 
 
    - When we trigger `mousedown`, it means drawing begins. Set the `isDrawing` state to be true
    - When we trigger `mouseup`, it means we've reached the destination, stop drawing here. `isDrawing` shall be false here. Same as `mouseout` event when the mouse moves out of the canvas screen.

4. Let's start `draw` function. To create a complete path we need to know where to start and where to finish. So let's define a `lastX` and `lastY` to always indicate where to start. And update their values when our `mousedown` event begins and `draw` function ends. We use the moving mouse's location `e.offsetX` and `e.offsetY` to indicate where to end the path. 
5. We use hsl to change the stroke color like a rainbow. To see the effect of hsl https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial
6. We also change the `lineWidth`.

Oops, quite a long passage. Need to get a rest and have a digest...