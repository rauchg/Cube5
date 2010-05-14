Cube5: A CSS3 animated 3D Cube layout
=====================================

Cube5 is a set of CSS classes that allow you to create a 3D layout similar to that seen in certain OS X applications such as Quicksilver. The 3D effect works only on Webkit nightly for now, but the layout is accessible for every browser.

Click [here](http://screenr.com/xmd) for a screencast of the effect.

Demo [here](http://devthought.com/wp-content/projects/cube5/index.html)

How to use
----------

Cube5 is entirely CSS(3) based, including the animations, so it only requires that you include the CSS snippet `cube5.css`.
The markup should look like this

	<div class="cube-container" id="demo-cube">
	  <div class="cube toFront">      
	    <div class="face top"><h3>Top</h3></div>
	    <div class="face front"><h3>Front</h3></div>
	    <div class="face bottom"><h3>Bottom</h3></div>
	    <div class="face left"><h3>Left</h3></div>
	    <div class="face right"><h3>Right</h3></div>
	    <div class="face rear"><h3>Rear</h3></div>      
	  </div>
	</div>

In order to change the currently shown face, programmatically change the class of the cube from `toFront` to toTop, toBottom, toLeft, toRight or toRear.

In jQuery:

	$('#demo-cube .cube').attr('class', 'cube toRear');

In MooTools

	$$('#demo-cube .cube').set('class', 'cube toRear');

When the class is changed, the cube will transition to the designated face (if -webkit-transform-3d is supported) or simply switch without a transition if the effect is not supported.

Notes
-----

If you change the width of the cube, make sure to adapt the values of `translateZ` to half the width.