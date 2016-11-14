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

<p><div id="calculator" style="width: 700px; height: 400px;"></div></p>

<script >
    var elt = document.getElementById('calculator');
    var calculator = Desmos.Calculator(elt);
    calculator.setExpression({id:'graph1', latex:'y=x^2 \\left\\{0<x\\right\\}'});
    
    calculator.setExpression({
  id: '2',
  latex: 'y=x + 1',
  color: '#662225'
});

    calculator.setExpression({
  id: '3',
  latex: 'y=x + 1',
  color: '#B51D0A'
});

    calculator.setExpression({
  id: '4',
  latex: 'y=x + 1',
  color: '#EAD39C'
});

    calculator.setExpression({
  id: '5',
  latex: 'y=x + 1',
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