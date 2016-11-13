---
layout: post
published: false
mathjax: true
featured: false
comments: true
title: Intro To College Math
---
## What is Desmos?

<div id="calculator" style="width: 700px; height: 400px;"></div>

<script >
    var elt = document.getElementById('calculator');
    var calculator = Desmos.Calculator(elt);
    calculator.setExpression({id:'graph1', latex:'y=x^2 \\left\\{0<x\\right\\}'});

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