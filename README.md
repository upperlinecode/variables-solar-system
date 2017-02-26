# Using Variables: The Solar System

![solar system](https://s3.amazonaws.com/upperline/curriculum-assets/p5js/solar-system.png)

The code below builds a model of the solar system. It's not a very accurate model though because the planet's are not the correct size in proportion to each other. Also, in the real solar system the planet's are not evenly spaced apart. Pluto, for example, is almost 40 times as far from the sun as Earth is. Considering that Earth is 92.96 million miles from the sun, that's pretty far!!

```javascript
var centerY;

function setup() {
  createCanvas(24000, 600);
  centerY = height/2;
}

function draw() {
  background(0);

  // sun
  stroke(250, 225, 0);
  strokeWeight(50);
  line(0, 0, 0, height);

  noStroke();

  // mercury
  fill(125);
  ellipse(200, centerY, 50, 50);

  // venus
  fill(220, 155, 100);
  ellipse(400, centerY, 50, 50);

  // earth
  fill(0, 100, 200);
  ellipse(600, centerY, 50, 50);

  // mars
  fill(200, 50, 0);
  ellipse(800, centerY, 50, 50);

  // jupiter
  fill(195, 160, 140);
  ellipse(1000, centerY, 50, 50);

  // saturn
  fill(240, 215, 160);
  ellipse(1200, centerY, 50, 50);

  // uranus
  fill(150, 250, 250);
  ellipse(1400, centerY, 50, 50);

  // neptune
  fill(55, 130, 250);
  ellipse(1600, centerY, 50, 50);

  // pluto
  fill(250, 200, 160);
  ellipse(1800, centerY, 50, 50);

}
```

## Your Task

Your task is to alter the code using the chart below so that you can show a more accurate model of the solar system. The chart shows the *Diameter* of each planet in relation to Earth's diameter, and the *Distance from the Sun* of each planet in relation to Earth's distance.

Assume that in the code *the ellipse that represents Earth is in the correct position and the correct size.* Place the other planets in the appropriate position with the appropriate size in relation to Earth.


## Planetary Facts - Ratio to Earth
| MERCURY | VENUS | EARTH | MARS | JUPITER | SATURN | URANUS | NEPTUNE | PLUTO
 --- | --- | --- | --- | --- | --- | --- | --- | --- |
 **Diameter** | 0.4 |	0.9 |	1	| 0.5 | 11.2 | 9.5 | 4.0 | 3.9 |	0.2
 **Distance from Sun** | 0.4 | 0.7 | 1 | 1.5 |	5.2 | 9.6 |	19.2 |	30.1 |	39.5

## Tips
Let's say a new planet was discovered that was 2.6 times the size of Earth.  I could pull out my calculator and multiply Earth's width (50px) by 2.6. Then I could pass the result, 130, to the `ellipse` function.  

This would be really tedious to do for every planet, and why should we do all that math ourselves when the computer can do it for us.  What if you made a variable `earthDiameter` that you could just multiply by 2.6 or whatever each planet's diameter is?

## Additional Goals

You will probably start out by having at least two variables representing Earth's diameter and Earth's distance from the sun.  Can you make additional variables for each planet so that your code is extremely *easy to read* for other programmers?

Rather than hard-coding in Earth's diameter and distance, could you make those values be proportional to the size of the canvas so that the solar system stayed proportional no matter how you changed the canvas size?
