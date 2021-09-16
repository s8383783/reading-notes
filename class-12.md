## Readings: Chart.js, Canvas
***
### [Chart.js API.](https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/) - Written by Sara Vieira
- > Charts are far better for displaying data visually than tables and have the added benefit that no one is ever going to press-gang them into use as a layout tool. They’re easier to look at and convey data quickly, but they’re not always easy to create. - Sara V.
- Chart.js is a Javascript plugin that uses HTML5's canvas element to draw the graph onto the pages:
  * Setting Up:
    * You start by first downloading [Chart.js](https://github.com/nnnick/Chart.js)
    * Copy the Chart.min.js of the unzipped folder and paste it into the directory you'll be working in.
    * Import the script into your HTML page: `<script src='Chart.min.js'></script>`
  * Drawing a line chart:
    * Add this to your HTML page: `<canvas id="buyers" width="600" height="400"></canvas>`
    * Next, we write our script that retreives the context of the canvas. We then this into the foot of our body element: `<script>
    var buyers = document.getElementById('buyers').getContext('2d');
    new Chart(buyers).Line(buyerData);
</script>`
    * In our script we need to create data in an object like so: `var buyerData = {
	labels : ["January","February","March","April","May","June"],
	datasets : [
		{
			fillColor : "rgba(172,194,132,0.4)",
			strokeColor : "#ACC26D",
			pointColor : "#fff",
			pointStrokeColor : "#9DB86D",
			data : [203,156,99,251,305,247]
		}
	]
}`
  * Drawing a pie or bar chart:
    * Very similar concept but your data structure will look different.
- Conclusion: 
  * > The great things about Chart.js are that it’s simple to use and really very flexible. Plus, once you’ve mastered the basics here, you’ll discover that there are tons of options listed in the [documentation](http://www.chartjs.org/docs/).
  
### Canvas API
- Basic Usage of Canvas - From [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_usage)
  * Initially, a `<canvas>` looks like the `<img>` element, with the only clear difference being that it doesn’t have the `src` and `alt` attributes. The `<canvas>` element only has two attributes and those are `width` and `height`. Those attributes default to 300 px wide and 150 px high when not specified. 
  * MDN further discusses some other important notes to inlude Fallback content, required `</canvas>` tag, the rendering context, and checking for support.
  * You can find skeleton examples from MDN's website.
- Drawing shapes with canvas from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes)
  * > Working with paths is essential when drawing objects onto the canvas and we will see how that can be done. - MDN
  * The Grid:
    * Before you begin drawing, it's important to talk about the canvas grid or coordinate space.
    * 1 unit in the grid normally corresponds to 1 px on the canvas.
    * The origin of the grid is positioned in the top-left corner at coordinate (0, 0).
    * ![alt text](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes/canvas_default_grid.png)
  * Useful material covered in the doc: Drawing rectangles, drawing paths, and path2D objects.
- Applying styles and colors from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors)
  * > In the chapter about drawing shapes, we used only the default line and fill styles. Here we will explore the canvas options we have at our disposal to make our drawings a little more attractive. You will learn how to add different colors, line styles, gradients, patterns and shadows to your drawings.
  * MDN explains deep details towards how to create modify colors, transparency, line styles, gradients, patterns, shadows, and Canvas fill rules.
- Drawing Text from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text)
  * After learning how to apply styles and colors, the next concept is drawing text onto the canvas.
  * The canvas rendering context provides two methods to render text:
    * Fills a given text at the given (x,y) position. Optionally with a maximum width to draw. `fillText(text, x, y [, maxWidth])`
    * Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw. `strokeText(text, x, y [, maxWidth])`
  * Styling Text: There are some more properties which let you adjust the way the text gets displayed on the canvas:
    * `font = value`: This string uses the same syntax as the CSS font property. 
    * `textAlign = value`: Possible values: `start, end, left, right or center`.
    * `textBaseline = value`: Possible values: `top, hanging, middle, alphabetic, ideographic, bottom`. The default value is alphabetic.
    * `direction = value`: Possible values: `ltr, rtl, inherit`. The default value is inherit.  
![alt text](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text/baselines.png)
