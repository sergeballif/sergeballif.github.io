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

In this post I will highlight some of my favorite capabilities of Desmos.

## What Can the Desmos Calculator do?

Let's take a look at some of the popular calculator features. 

### Sliders

Below is the graph of a parabola with it's vertex at the origin. 

<p><div id="calculator" style="width: 700px; height: 400px; margin: auto;"></div></p>

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

<p><div id="calculator2" style="width: 700px; height: 400px; margin: auto;"></div></p>
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

<p><div id="calculator3" style="width: 700px; height: 400px; margin: auto;"></div></p>
<script>
    var elt = document.getElementById('calculator3');
    var calculator = Desmos.Calculator(elt);
    calculator.setMathBounds({
  left: 0,
  right: 6,
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





Desmos is transforming the way that math is taught and experienced in the college classroom. 



