# Chart.js, Canvas

## HTML5 Canvas Element

<canvas> allows for 2d drawings using Js, ``` <canvas width="500" height="300" id="canvas"></canvas>
const canvas = document.querySelector('#canvas');
const width = canvas.width;// 500
const height = canvas.height;// 300
  
// dom method:
canvas.width = 600;
canvas.height = 400;  

```

Think of the canvas element like a blank canvas that you can draw on, like a piece of paper. To draw on the canvas, you need to use something called the rendering context. The rendering context is like a set of tools you use to draw on the canvas.

To access the rendering context, you use the getContext() method on the canvas element. The getContext() 
method takes one argument, which tells it what kind of context you want to use. For example, if you want to draw 2D shapes 
on the canvas, you would use the "2d" argument to get a 2D rendering context object.

Once you have the rendering context object, you can use it to draw things on the canvas, like shapes, text, images, 
and other objects. In the example code you provided, the querySelector() method is used to select the canvas element with
the ID of "canvas", and then the getContext() method is called on it to get the 2D rendering context, which is stored in the 
variable named "ctx".
  
``` let canvas = document.querySelector('#canvas');
let ctx = main.getContext('2d');
  ```
![JavaScript-Canvas](https://user-images.githubusercontent.com/122787483/219883661-60a15233-7e5a-4aa3-9c2f-2b128540f635.png)

``` (() => {
    const canvas = document.querySelector('#main');
    if (!canvas.getContext) {
        return;
    }

    // get the context
    let ctx = canvas.getContext('2d');

    // set fill and stroke styles
    ctx.fillStyle = '#F0DB4F';
    ctx.strokeStyle = 'red';

    // draw a rectangle with fill and stroke
    ctx.fillRect(50, 50, 150, 100);
    ctx.strokeRect(50, 50, 150, 100);

})(); ```

### Questions:
  
What does the <canvas> allow a developer to acheive?
  allows for graphics and animations that could respond to user input.
What is the importance of the closing `</canvas> tag?
  so the browser knows when the canvas stops
Explain what the getContext() method does.
  the properties for devlopers to draw lines rectangles et cetera.

## Chart.js Documentation

Chart js is the most popular charting library used, created in 2013 and is open source and permissive licensing.
Chart.js can use popular frames such as React, Vue and Svelte.
Disallows CSS styling.

Well suited for very large data sets, is very actively developed by the community.
  
### Questions
What is Chart.js and how it can be brought into your project?
  Chart js is a very popular opensource library for creating charts and graphs and animations of any sort, imported via a script.
List 3 different Chart types you can create using Chart.js.
  Line, pie and bar charts.
  
## Easily Create stunning animated charts with chart.js

To set up chart js, we need to download, unzip into same directory then use ``` <script src='Chart.min.js'></script> ```

Draw a line:
  
  ``` <canvas id="buyers" width="600" height="400"></canvas> ```

collect context:
  ``` <script>
    var buyers = document.getElementById('buyers').getContext('2d');
    new Chart(buyers).Line(buyerData);
</script> ``` 
  
Animated line graphs:
``` var buyerData = {
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
} ```
  
Pie chart:
  ``` <canvas id="countries" width="600" height="400"></canvas>
  var countries= document.getElementById("countries").getContext("2d");
new Chart(countries).Pie(pieData, pieOptions); ``` 
  
  pie chart data: 
``` var pieData = [
	{
		value: 20,
		color:"#878BB6"
	},
	{
		value : 40,
		color : "#4ACAB4"
	},
	{
		value : 10,
		color : "#FF8153"
	},
	{
		value : 30,
		color : "#FFEA88"
	}
]; ``` 
  
  ``` options are::
  var pieOptions = {
	segmentShowStroke : false,
	animateScale : true
} ``` 
  
Bar chart:
``` <canvas id="income" width="600" height="400"></canvas>
  var income = document.getElementById("income").getContext("2d");
new Chart(income).Bar(barData);
  var barData = {
	labels : ["January","February","March","April","May","June"],
	datasets : [
		{
			fillColor : "#48A497",
			strokeColor : "#48A4D1",
			data : [456,479,324,569,702,600]
		},
		{
			fillColor : "rgba(73,188,170,0.4)",
			strokeColor : "rgba(72,174,209,0.4)",
			data : [364,504,605,400,345,320]
		}

	]
}``` 

### Questions:
What are some advantages to displaying data via a chart over a table?
  It is visually better, more accurate and has higher representation value. 
How could Chart.js aid your previously created applications visually?
  It could aid already existing data to help portray what is being given to the reader in a better manner or to further support it.
 

  


  



  
