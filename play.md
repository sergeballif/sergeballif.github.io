---
layout: page
permalink: /play/index.html
title: Serge Ballif
tags: 
  - Serge
  - Ballif

published: true
mathjax: true
featured: false
comments: true
title: What is Desmos?
desmos: true
---


<script type="text/javascript">
 function showhide(id) {
    var e = document.getElementById(id);
    e.style.display = (e.style.display == 'block') ? 'none' : 'block';
 }
</script>


In my [previous post](https://sergeballif.github.io/personal/math/teaching/fun/a-brief-intro-to-desmos) I shared some of my favorite features of the Desmos Graphing Calculator. In this post I want to share how Desmos is changing the way math is taught and experienced in the college classroom. 

### Math for our day

When our students leave college we want them to be fully equipped to handle the math that will come their way. For some students (such as STEM majors) the demands are higher because of the larger role that data and models will play in their careers.  For other students the bar is set lower, but there are some common skills that all college graduates should have. 

* Students should have basic number sense along with the confidence to dive in and try problems.
* Students should be able to accurately use numbers (including units and other appropriate vocabulary) to describe situations and problems.
* Students should be critical thinkers and have at least moderate capabilities in the areas of consumer math and statistics.

If a college graduate hasn't obtained those skills by the time they graduate, then both the school and that student have failed in a key area. This low bar applies regardless of the major.

In his recent article [All the mathematical methods I learned in my university math degree became obsolete in my lifetime](http://www.huffingtonpost.com/entry/all-the-mathematical-methods-i-learned-in-my-university_us_58693ef9e4b014e7c72ee248?timestamp=1483293018441) Keith Devlin describes the math skills needed for today's students in contrast to the skills needed 30 years ago. The ability to carry out procedures and computations is no longer the focus because computers can easily do it for us. Instead we focus more on conceptual understanding, exploiting the tools to solve problems, and creating more meaningful discussions of results.

### The process of doing practical math

The solution to a math problem typically has three components.  

1. __The Setup:__ This is the planning step. We take time to read and comprehend a problem and then translate the problem into a computation to perform or an algebraic expression to solve. Often we draw a picture to clarify the question or introduce variables for unknown quantities. Sometimes we will break a bigger problem into several sub-problems. By the end of this step we have transformed a paragraph of words into concrete math symbols and equations.
2. __Solving:__ In this step we find the numerical answer to the question. Usually this involves some sort of algebraic manipulation and/or arithmetic calculation. Often we complete a procedure of steps that we have memorized.
3. __Interpreting:__ The final part is where we write up the solution. A good interpretation will include units and an explanation of the conclusions reached along with any other information that was requested.




<a href="javascript:showhide('answer1')">
    Click to show/hide.
</a>

<div id="answer1" style="display:none;">
<p>Hmm.</p>

<p><div id="calculator20" style="width: 800px; height: 400px; margin: auto;"></div></p>
  <script >
    var elt = document.getElementById('calculator20');
    var calculator = Desmos.Calculator(elt);

calculator.setExpression({
  type: 'table',
  columns: [
    {
      latex: 'x',
      values: ['1', '2', '3', '4', '5']
    },
    {
      latex: 'y',
      values: ['1', '4', '9', '16', '25'],
      dragMode: Desmos.DragModes.XY
    },
    {
      latex: 'x^2',
      color: Desmos.Colors.BLUE,
      columnMode: Desmos.ColumnModes.LINES
    }
  ]
});
  </script>


</div>

<p>More text here.</p>
 





## What is this calculator I've been hearing about?

Desmos is the graphing calculator I could only dream of having when I went through high school. It has a beautiful layout, it solves equations (numerically), it works with lists, and it can plot implicit functions and inequalities. It can be used for algebra, modeling, statistics, and even calculus. Best of all, it's freely available to use in a web browser or as a mobile app. How good do I think it is? Well, if somebody gave me a free TI graphing calculator I would just sell it on EBay or give it away, because the Desmos app on my phone is superior. The contest isn't even close.

The best way to learn Desmos is to go to [desmos.com](https://www.desmos.com/) and try the calculator out. You'll be amazed at it's capabilities. There are plenty of tutorials to help you on your journey.

In this post I will highlight some of my favorite capabilities of Desmos with minimal explanations. Throughout these examples, be sure to notice that calculator just begs for you to experiment and make changes as you go.

## What Can the Desmos Calculator do?

Let's take a look at some of the popular calculator features. 

### Sliders

Below is the graph of a parabola with it's vertex at the origin. 

<p><div id="calculator" style="width: 800px; height: 400px; margin: auto;"></div></p>

<script>
    var elt = document.getElementById('calculator');
    var calculator = Desmos.Calculator(elt);
    calculator.setExpression({id:'graph1', latex:'y=x^2'});
    
    calculator.setExpression({
  id: '2',
  latex: 'y=ax^2',
  color: '#662225'
});
</script>

The second equation shows an error because of the unknown variable $a$. Click the button by the text "add slider" to give $a$ a value. Then clicking the play button next to $a$ will let you see the effect that $a$ has on the graph. Notice that the format is very inviting for students to experiment and try things. It's easy to type your own formulas into the blank cells to experiment or to get a better feel for how a parabola can be transformed by a parameter (e.g. $y=x^2+a$, $y=(x-a)^2$, or $y=(ax)^2$).

### Tables

Below is a table of data.

<p><div id="calculator2" style="width: 800px; height: 400px; margin: auto;"></div></p>
  <script >
    var elt = document.getElementById('calculator2');
    var calculator = Desmos.Calculator(elt);

calculator.setExpression({
  type: 'table',
  columns: [
    {
      latex: 'x',
      values: ['1', '2', '3', '4', '5']
    },
    {
      latex: 'y',
      values: ['1', '4', '9', '16', '25'],
      dragMode: Desmos.DragModes.XY
    },
    {
      latex: 'x^2',
      color: Desmos.Colors.BLUE,
      columnMode: Desmos.ColumnModes.LINES
    }
  ]
});
  </script>

<p>
Notice that the 2nd column values were entered manually, while the 3rd column values were computed from the 1st column. The points plotted via the 2nd column are set to be draggable, so you can drag them around to change the values. You can add additional values to the first two columns or add another column. Try adding a 4th column with the expression $\left|x-3\right|$ by first clicking inside the table and then clicking inside the top cell of the 4th column.
</p>

### Lists

Each of the table columns in the example above are lists. We can also define a list of values.

<p><div id="calculator3" style="width: 800px; height: 400px; margin: auto;"></div></p>
<script>
    var elt = document.getElementById('calculator3');
    var calculator = Desmos.Calculator(elt);
    calculator.setMathBounds({
  left: -1,
  right: 7,
  bottom: -1.3,
  top: 1.3
});
    calculator.setExpression({id:'graph1', latex:'m=[5,4,3,2,1]'}); 
    calculator.setExpression({
  id: '2',
  latex: 'y=mx',
  color: '#662225'
});
    calculator.setExpression({
  id: '3',
  latex: 'L=[0,0.2,...,6]'
});
    calculator.setExpression({
  id: '4',
  latex: '(L,sin(L))'
});
</script>

Notice how the list $m$ can be used to plot multiple slopes of a line with a single command. The list $L$ is used to plot points on the sine curve. Try plotting the points on a circle by plotting $(\cos(L),\sin(L))$.

### Parametric Curves
Most curves in the plane are not functions in the traditional sense because they fail the vertical line test. However we can write the variables $x$ and $y$ as functions of a third variable $t$. Below we look at the plot of the parametric functions
$$
\begin{align*}
x(t)=\cos(3t), 0\le t \le 2\pi\\
y(t)=\sin(5t), 0\le t \le 2\pi\\
\end{align*}
$$
<p><div id="calculator4" style="width: 800px; height: 400px; margin: auto;"></div></p>
<script>
    var elt = document.getElementById('calculator4');
    var calculator = Desmos.Calculator(elt);
    calculator.setMathBounds({
  left: -2,
  right: 2,
  bottom: -2,
  top: 2
});
    calculator.setExpression({id:'2', latex:'(cos(3at),sin(5at))', domain:{ min: 0, max: 6.28 }, color: Desmos.Colors.BLACK}); 
    calculator.setExpression({id:'3', latex:'a=1', sliderBounds: { min: 0, max: 1}}); 
</script>

I sneeked a parameter $a$ into the calculator so that we can actually watch the curve being drawn. Click the play button to the left of $a$ to see the curve in action.

### Inequalities
Desmos will plot inequalities for you.

  <p><div id="calculator5" style="width: 800px; height: 400px; margin: auto;"></div></p>
  <script >
    var initialState = {"version":1,"graph":{"showGrid":true,"showXAxis":true,"showYAxis":true,"xAxisStep":0,"yAxisStep":0,"xAxisMinorSubdivisions":0,"yAxisMinorSubdivisions":0,"xAxisArrowMode":"NONE","yAxisArrowMode":"NONE","xAxisLabel":"","yAxisLabel":"","xAxisNumbers":true,"yAxisNumbers":true,"polarMode":false,"polarNumbers":true,"degreeMode":false,"projectorMode":false,"squareAxes":true,"viewport":{"xmin":-10,"ymin":-13.54387107276575,"xmax":10,"ymax":13.54387107276575}},"expressions":{"list":[{"id":"2",type:"folder","title":"Click the triangle to my left to reveal the formulas","memberIds":{"3":true,"4":true},"hidden":false,"collapsed":true,"secret":false},{"id":"3","type":"expression","latex":"x^2+y^2\\le a^2","domain":{"min":0,"max":1},"hidden":false,"color":"#4F81BD","style":"normal","residualVariable":"","regressionParameters":{},"isLogModeRegression":false},{"id":"4","type":"expression","latex":"a=[1,2,3,4,5,6]"}]}}

    var elt1 = document.getElementById('calculator5');
    var calculator1 = Desmos.GraphingCalculator(elt1,  {
      administerSecretFolders: false
    });
    calculator1.setState(initialState);
  </script>
  
Open the folder to see the formulas that produced the shaded circles. Try to add a few more circles.

### Draggable Points

Desmos lets you create points that you move. You can even specify that the point should be on a specific curve.

<p><div id="calculator6" style="width: 800px; height: 400px; margin: auto;"></div></p>
<script>
    var elt = document.getElementById('calculator6');
    var calculator = Desmos.Calculator(elt);
    calculator.setMathBounds({
  left: -1,
  right: 7,
  bottom: -2,
  top: 2
});
    calculator.setExpression({
  id: '2',
  latex: 'f(x)=\\cos(x)+sin(3x)',
  color: '#662225'
});
     calculator.setExpression({
  id: '7',
  latex: 'a=1'
});
        calculator.setExpression({
  id: '8',
  latex: '(a,f(a))',
  color: '#000'
});
    calculator.setExpression({
  id: '3',
  latex: '0\\le y \\le f(x)\\left\\{2<x<a\\right\\}',
    color: '#BC8F8F'
});
    calculator.setExpression({
  id: '4',
  latex: '0\\ge y \\ge f(x)\\left\\{a<x<2\\right\\}',
    color: '#BC8F8F'
});
    calculator.setExpression({
  id: '5',
  latex: '0\\le y \\le f(x)\\left\\{a<x<2\\right\\}',
    color: '#FFCC11'
});
    calculator.setExpression({
  id: '6',
  latex: '0\\ge y \\ge f(x)\\left\\{2<x<a\\right\\}',
    color: '#FFCC11'
});
      calculator.setExpression({
  id:'1', latex:'A(x)=\\int_{2}^{x}f(t)dt',
 hidden: 'true'}); 
</script>

Drag the black point around to see how it is glued to the curve $y=f(x)$. You'll notice that I have included some shading using inequalities. Desmos has it's own special notation for conditionally restricting output: place the condition insided of curly braces such as $\{2<x < a\}$ in the graph above. 

If you scroll to the bottom of the expression list you will see a function $A(x)$ that is disabled. Click on the circle to the left of this function to enable it. Calculus students will recognize the function $A(x)$ as a net signed-area function starting at $x=2$ (whose output is the lavender area minus the yellow area). The ability to hide plots is particularly useful for large projects. Try redefining $f(x)$ to be $f(x)=\sin \left(x^2\right)$ to see how it changes the graph.

### Curve Fitting

Desmos makes it easy to come up with models to match a collection of data. The table below shows some points plotted along with the curve that Desmos fit to the points.

<p><div id="calculator7" style="width: 800px; height: 400px; margin: auto;"></div></p>
  <script >
    var elt = document.getElementById('calculator7');
    var calculator = Desmos.Calculator(elt);

 calculator.setExpression({
  id: '2',
  latex: 'y_1~ax_1^2+bx_1+c',
  color: '#662225'
});
calculator.setExpression({
  type: 'table',
  columns: [
    {
      latex: 'x_1',
      values: ['-2','-1','0','1', '2', '3']
    },
    {
      latex: 'y_1',
      values: ['-5', '-2', '0', '1', '1','0'],
    },
  ]
}); 
  </script>

To get the curves we just notice that the points look like they fit a parabola, so we would guess that formula would be of the form $y=ax^2+bx+c$. Then we replace "$y$" with "$y_1$" and "$x$" with "$x_1$" so that Desmos will refer to the table to get its values. Finally we replace "$=$" with "$\sim$" so that Desmos knows you want to fit a curve approximation. That's where we get the code:

$$y_1\sim ax_1^2+bx_1+c$$.

Try changing some of the values in the table to see what parabola gives the best approximation.

### Points of Interest

Desmos is also a great tool for solving equations, finding intercepts, or maximizing or minimizing curves. For example, suppose we wanted to maximize the area of a rectangle in the first quadrant under the green curve below.

<p><div id="calculator8" style="width: 800px; height: 500px; margin: auto;"></div></p> 

  <script >
    var elt = document.getElementById('calculator8');
    var calculator = Desmos.GraphingCalculator(elt);
calculator.setExpression({
  id: '0',
  latex: 'A(x)=xf(x)',
  color: '#91371B',
  hidden: true
});
    calculator.setExpression({
  id: '1',
  latex: 'A(a)',
});
      calculator.setExpression({
  id: '2',
  latex: 'f(x)=.1\\left(x-4\\right)^2\\left\\{0\\le x\\le 4\\right\\}',
  color: '#4A572C'
});
     calculator.setExpression({
  id: '3',
  latex: 'a=1'
});
     calculator.setExpression({
  id: '4',
  latex: '(a,f(a))',
  color: '#000'
});
     calculator.setExpression({
  id: '5',
  latex: '0\\le x \\le a\\left\\{0\\le y\\le f(a)\\right\\}',
  color: '#4A572C'
});
     calculator.setExpression({
  id: '6',
  latex: '0\\le y\\le f(a)\\left\\{0\\le x \\le a\\right\\}',
  color: '#4A572C'
});
    calculator.setMathBounds({
  left: -.2,
  right: 4.5,
  bottom: -1,
  top: 4
});
    calculator.updateSettings({
      projectorMode: true
    });
  </script>
  
The area of each rectangle is base $\times$ height or $x\cdot f(x)$, so we defined the area function $A(x)=x\cdot f(x)$. Drag the black point back and forth along the curve. You can view the actual area by looking at the expression in cell 2. To get the maximum area we can just look at the plot of $A(x)$. click the circle to the left of $A(x)$ to un-hide the graph. Click on the graph of $A(x)$ and you will see some gray dots appear at points of interest (such as intercepts, points of intersection, or maximum values). Click the point on the top to see the maximum possible area of a rectangle under the curve.

Note that the font and line width are larger in this example. That's because the calculator is set to projector mode (using the wrench icon in the upper right corner).

## Just the Tip of the Iceberg

I hope these examples have given you some small appreciation of the features that make Desmos so much fun to use and so effective as a teaching tool. This post could go on for a considerable length describing the cool features of Desmos, but I will stop here and encourage you to go try it out for yourself. Once you have tried out the calculator you'll be ready to learn about [teacher.desmos.com](https://teacher.desmos.com/) and the huge repository of activities that have been created and curated. 

In my next post I plan describe how Desmos is transforming the way that math is taught and experienced in the college classroom. 



