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


Desmos is transforming the way that math is taught and experienced in the college classroom. 


## What Can the Desmos Calculator do?

Let's take a look at some of the popular calculator features. 

Below is the graph of a parabola with it's vertex at the origin. 
<p><div id="calculator1" style="width: 700px; height: 400px; margin: auto;"></div></p>

  <script >
    var elt = document.getElementById('calculator1');
    var calculator = Desmos.GraphingCalculator(elt);
    calculator.setExpressions([
      {id:'graph1', latex:'y=ax^2'},
      {id:'slider1', latex:'a=2', sliderBounds: {min: -3, max: 8, step: 1}}
    ]);
  </script> 

The vertical scale factor $a=2$ is set as a default, but $a$ is a slider, so clicking the play button next to $a$ will let you see the effect that $a$ has on the graph. Notice that the format is very inviting for students to experiment and try things. It's easy to type in your own formulas into the blank cells to experiment to get a better feel for how a parabola can be transformed by a parameter (e.g. $y=x^2+a$, $y=(x-a)^2$, or $y=(ax)^2$).


















-----------------

Just playing around.


Here is a bunch of text to see if it is getting all the way to the end of the page. Something seems to be amiss here, and I'm not sure what the problem is.




<div>

<p><div id="calculator2" style="width: 700px; height: 400px;"></div></p>

<script >
    var elt = document.getElementById('calculator2');
    var calculator = Desmos.Calculator(elt);
    calculator.setExpression({id:'graph1', latex:'y=x^2 \\left\\{0<x\\right\\}'});
    
    calculator.setExpression({
  id: '2',
  latex: 'y=x + 1',
  color: '#662225'
});

    calculator.setExpression({
  id: '3',
  latex: 'y=x + 2',
  color: '#B51D0A'
});

    calculator.setExpression({
  id: '4',
  latex: 'y=x + 3',
  color: '#EAD39C'
});

    calculator.setExpression({
  id: '5',
  latex: 'y=x + 4',
  color: '#7D5E3C'
});

    // Set initial axis labels in the calculator
    calculator.setGraphSettings({
      xAxisLabel: 'Time',
      yAxisLabel: 'Distance'
    });

    var xAxisLabelElt = document.getElementById('x-axis-label');
    var yAxisLabelElt = document.getElementById('y-axis-label');

    function onXAxisLabelUpdate () {
      xAxisLabelElt.textContent = calculator.graphSettings.xAxisLabel;
    }

    function onYAxisLabelUpdate () {
      yAxisLabelElt.textContent = calculator.graphSettings.yAxisLabel;
    }

    // Whenever the axes labels are changed by the user, call the appropriate
    // callback to synchronize the external labels.
    calculator.graphSettings.observe('xAxisLabel', onXAxisLabelUpdate);
    calculator.graphSettings.observe('yAxisLabel', onYAxisLabelUpdate);

    // Initial synchronozation with external and internal labels
    onXAxisLabelUpdate();
    onYAxisLabelUpdate();
  </script>

<p><div id="calculator3" style="width: 700px; height: 400px;"></div></p>
<script >
    var elt = document.getElementById('calculator3');
    var calculator = Desmos.Calculator(elt);
    calculator.setExpression({id:'graph1', latex:'y=x^2 \\left\\{0<x\\right\\}'});
    
    calculator.setExpression({
  id: '2',
  latex: 'y=x + 1',
  color: '#882426'
});

    calculator.setExpression({
  id: '3',
  latex: 'y=x + 2',
  color: '#CDBEA7'
});

    calculator.setExpression({
  id: '4',
  latex: 'y=x + 3',
  color: '#323030'
});

    calculator.setExpression({
  id: '5',
  latex: 'y=x + 4',
  color: '#C29545'
});

  </script>
  
  </div>
