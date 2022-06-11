[<=== Back](README.md)

# [JavaScript Canvas](https://www.javascripttutorial.net/web-apis/javascript-canvas/)

The element `<canvas>` allows the user to draw 2D graphics using JavaScript, and requires at least two attributes: width and height to specify size. Width and height of the canvas can be accessed via the canvas's DOM properties.

`<canvas>` requires a closing tag, and any content inside the tags will display only if the browser doesn't support canvas. This is called 'fallback content'.

> The `<canvas>` element features the `getContext()` method that returns a render context object. This method takes one argument: the type of context, for example '2D'.

```
  let canvas = document.querySelector('#canvas');
  let ctx = main.getContext('2D');
```

## The 2D context

> The 2D drawing context features methods for drawing simple 2D shapes such as paths, rectangles, and arcs. The coordinates in a 2D context begin at the upper-left of the `<canvas>` element, which is point (0,0) as shown in the following image:

[JavaScript Canvas](img/JavaScript-Canvas.png)

Fill and Stroke are basic operations, which use `.fillStyle` and `.strokeStyle` respectively.
- Fill: fills in the shape with a specified style or color
- Stroke: adds color to the edges of the shape

# [Chart.js Documentation](https://www.chartjs.org/docs/latest/)

To use Chart.js, you need the script for the chart included in your page, and a single `<canvas>` node to render the chart.

I see that I can use this to insert my data chart into my Odd Duck project to represent the times an image has been clicked. 

Types of charts that can be created: area, bar, bubble, doughnut/pie, line, mixed, polar, radar, and scatter

# [Easily Create Stunning Animated Charts with Chart.js](https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/)

Advantages of displaying a chart over a table:
- Tables create a more dynamic visual experience
- Easier to look at
- Easier to convey data quickly

To create a chart:
1. Create the canvas element in HTML
2. Write a script that will retrieve the context of the canvas (add to the bottom of HTML body)
3. In the same script tag (HTML), create data

### Bookmarks for consideration:

[Drawing Shapes With Canvas](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes)

[Applying Style and Colors - Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors)

[Drawing Text - Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text)