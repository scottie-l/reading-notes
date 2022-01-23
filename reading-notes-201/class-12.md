# Notes - Day 12

_<a href = "https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/">"Chart.js API"</a>_

Charts are better for displaying data visually than tables.

Chart.js is a JavaScript plugin that uses HTML5's canvas element to draw the graph onto the page. Can use to create bar, line, pie charts and more.

Have to download API first.

For a line chart, add canvas element to html page, then a script tag to point it to the file. Create the data inside the script tags.

canvas API can be used to create charts. A script with a single `<canvas>` node to render the chart.

1) Have canvas on your page, usually in a div for better responsiveness.

2) add the script to link the chart.

3) Render chart using our configuration.

Ex. `<div><canvas id = "myChart"></canvas></div>`

`<script src = "https;//cdn.jsdelivr.net/npm/chart.js"></script>`

const config = {
  type: 'line',
  date: data,
  options: {}
};

`<script>`
var myChart = newChart (
  document.getElementById('myChart'),
  config
);
`</script>`

Chart.js can be integrated with plain JavaScript or with different module loaders.

To create a chart, we need to instantiate the chart class. To do, we need to pass in the node, JQuery instance, or 2d context of the canvas of where we want to draw the chart.

_<a href = "https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_usage">"Basic Usage of Canvas"</a>_

Canvas only has 2 attributes, height & width; Both are optional and can be set using DOM properties. If no attributes, default is 300px wide x 150px tall.

Id isn't required, but good practice. It can be styled in CSS.

Should define some fallback content for unsupported versions. Just insert the alternative inside the canvas element. The closing tag is required, if not present, the rest of the page is considered the fallback.

Use the canvas tag with method called getContext(), used to render the context and its drawing functions. It takes one parameter, the type of context.

First line in script is the node in the DOM representing canvas using the getElementById() method, followed by the getContext().

_<a href = "https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes">"Drawing Shapes with Canvas"</a>_

With canvas we can draw rectangles, triangles, lines, arcs and curves.

Working with paths is essential when drawing objects in the canvas.

Origin of grid placed in top left corner at coordinate (0, 0). All elements are placed relative to this. So the position of the top left corner becomes x pixels from the left and y pixels from the top, at coordinates (x, y).

Canvas only supports two primitive shapes: rectangles and paths = lists of points connected by lines. Other points must be created by combining 1 or more paths.

For a rectangle use fillRect() = draws filled rectangle. strokeRect() = draws outline. clearRect() = makes it fully transparent. Parameters in the parenthesis are (x, y, width, height). All draw immediately to the page.

Path is list of points, connected by segments of lines that can be of different shapes, widths and colors. A path, or even a subpath, can be closed.

To make shapes using paths: 1) create the path. 2) Use drawing commands to create the path. 3) Once created, can stroke or fill path to render.

1: beginPath() = creates new path. Path methods are used to set different paths for objects. closePath() = Adds straight line, going to start of current path. stroke() = draws the shape. fill() = Draws solid shape.

moveTo() = moves to specified coordinates. Helps to draw with lines that won't render on page. Like to draw a smiley face.

lineTo() = method for straight lines

arc(x, y, radius, startAngle, endAngle, counterclockwise) = Draws arc which is centered at x, y position with radius r starting at startAngle, and ending at endAngle. Going counterclockwise as indicated.

arcTo(x1, y1, x2, y2, radius) = Draws arc with given control points and radius, connected to the previous point by a straight line.

Takes 6 parameters = x, y are starting points. startAngle & endAngle are define start and endpoints.

Bezier curves = used to draw more organic shapes.

quadraticCurveTo(cp1x, cp1y, x, y) Draws a quadratic Bézier curve from the current position to the end point specified by x, y using the control point specified by cp1x and cp1y.

bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y) Draws a cubic Bézier curve from the current position to the end point specified by x, y using the control points specified by cp1x, cp1y and cp2x, cp2y.

Also the rect() method, which adds a rectangular path to a currently open path. rect(x, y, width, height) Draws a rectangle whose top-left corner is specified by x, y with specified width and height.

_<a href = "https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors">"Applying Styles & colors"</a>_

fillStyle = color, sets the style used when filling shapes. strokeStyle = color, sets the style for shapes outlines.

In addition to drawing opaque shapes to canvas, can also draw semi-transparent shapes. Done by setting the globalAlpha property, or assigning a semi-transparent color to the stroke and/or fill style.

globalAlpha = transparencyValue, applies the specified transparency value to all future shapes drawn on canvas. Value must be between 0.0 (fully transparent) to 1.0 (fully opaque). This value is 1.0 (fully opaque) by default.

lineWidth = value, sets the width of lines drawn in the future. Default is 1.0 units

lineCap = type, sets the appearance of the ends of lines. 3 values, butt= ends of lines are squared off at the endpoints. round= ends of lines are rounded. square= ends of lines are squared off by adding a box with an equal width and half the height of the line's thickness.

lineJoin = type, sets the appearance of the "corners" where lines meet. 3 values, round= rounds off corners of shape by filling additional sector of disc centered at the common endpoint of connected segments. The radius for these rounded corners is equal to half the line width. bevel= fills additional triangular area between common endpoint of connected segments, and separate outside rectangular corners of each segment. miter= connected segments joined by extending outside edges to connect at single point, with effect of filling an additional lozenge-shaped area. This setting is effected by the miterLimit property.

miterLimit = value, establishes a limit on the miter when two lines join at sharp angle.

getLineDash(), returns the current line dash pattern array containing an even number of non-negative numbers.

setLineDash(segments), sets the current line dash pattern. method accepts a list of numbers that specifies distances to alternately draw a line and a gap.

lineDashOffset = value, specifies where to start a dash array on a line. sets an offset where to start the pattern.

createLinearGradient(x1, y1, x2, y2) = creates linear gradient object with a starting point of x1, y1 and end point of x2, y2.

createRadialGradient(x1, y1, r1, x2, y2, r2) = creates radial gradient. Parameters represent two circles, one with center at x1, y1 and radius of r1, the other with center at x2, y2 with radius of r2.

createConicGradient(angle, x, y) = creates conic gradient object with starting angle of angle in radians, at the position x, y.

We can assign colors to it by using the addColorStop() method.

createPatern(image, type) = image is source in HTML element, and type is type. repeat = tiles the image in both vertical and horizontal directions. repeat-x = tiles the image horizontally but not vertically. repeat-y = tiles the image vertically but not horizontally. no-repeat = doesn't tile the image, used only once.

Shadows: uses 4 properties: shadowOffsetX = float, indicates horizontal distance shadow should extend from object. This value isn't affected by the transformation matrix. The default is 0. shadowOffsetY = float, indicates vertical distance shadow should extend from object. This value isn't affected by the transformation matrix. The default is 0. shadowBlur = float, indicates size of blurring effect; this value doesn't correspond to a number of pixels and is not affected by the current transformation matrix. The default value is 0. shadowColor = color, standard CSS color value indicating the color of shadow effect; by default, it is fully-transparent black.

shadowOffsetX and shadowOffsetY indicate how far shadow extends from the object in the x, y direction.

The shadowBlur property indicates the size of blurring effect.

The shadowColor property is standard CSS color value indicating the color of the shadow effect.

_<a href = "https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text">"Drawing text"</a>_

canvas rendering context provides two methods to render text: fillText(text, x, y [, maxWidth]), fills given text at given x, y position. Optionally with a maximum width to draw. strokeText(text, x, y [, maxWidth]), strokes given text at given x,y position. Optionally with a maximum width to draw.

font = value, the current text style being used when drawing text. String uses same syntax as CSS font property. The default font is 10px sans-serif.

textAlign = value, text alignment setting; Possible values: start, end, left, right or center. The default value is start.

textBaseline = value, baseline alignment setting; Possible values: top, hanging, middle, alphabetic, ideographic, bottom. The default value is alphabetic.

direction = value, directionality; Possible values: ltr, rtl, inherit. The default value is inherit.

measureText(), returns TextMetrics object containing width, in px, that specified text will be when drawn in the current text style.

**<a href = "https://github.com/scottie-l/reading-notes/blob/main/reading-notes-201/README.md">Back</a>**
