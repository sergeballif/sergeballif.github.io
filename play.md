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
title: Desmos in the College Classroom
desmos: true
---

## What is Desmos?

Desmos is the graphing calculator I could only dream of having when I went through high school. It has a beautiful layout, it solves equations (numerically), it works with lists, and it can plot implicit functions and inequalities. Best of all, it's freely available to use in a web browser or as a mobile app. How good do I think it is? Well, if you gave me the option of a $\$100$ TI calculator or the free Desmos app for my phone, I would certainly chose the Desmos app.

In this post I will highlight some of my favorite capabilities of Desmos. Throughout these examples, be sure to notice that calculator just begs for you to experiment and make changes as you go.

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

The second equation shows an error because of the unknown variable $a$. Click "add slider" to give $a$ a value. Then clicking the play button next to $a$ will let you see the effect that $a$ has on the graph. Notice that the format is very inviting for students to experiment and try things. It's easy to type in your own formulas into the blank cells to experiment or to get a better feel for how a parabola can be transformed by a parameter (e.g. $y=x^2+a$, $y=(x-a)^2$, or $y=(ax)^2$).

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

Each of the table columns in the example above are lists. We can also define a  list of 

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
Most curves in the plane are not functions in the traditional sense because they fail the vertical line test. However we can write the variables $x$ and $y$ as functions of a third variable $t$. Below we look at the plot of the parametric function
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
Desmos will plot the formula for 

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
  id:'1', latex:'A(x)=\\int_{2}^{x}\\left(\\cos(t)+sin(3t)\\right)dt',
 hidden: 'true'}); 
</script>

Drag the black point around to see how it is glued to the curve $y=f(x)$. You'll notice that I have included some shading using inequalities. Desmos has it's own special notation for conditionally restricting output: place the condition insided of curly braces such as $\{2<x < a\}$ in the graph above. 

If you scroll to the bottom of the expression list you will see a function $A(x)$ that is disabled. Click on the circle to the left of this function to enable it. (Calculus students will recognize the function $A(x)$ as a net signed-area function whose output is purple area minus yellow area.) The ability to hide plots is particularly useful for large projects.




$'y_1\sim ax_1^2+bx_1+c$








Desmos is transforming the way that math is taught and experienced in the college classroom. 



