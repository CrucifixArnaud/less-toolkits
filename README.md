# Less Toolkits - v1.0

A collection of various useful Less mixins.

## Mixins


### Border Radius:

	.border-radius(@radius)

Result in:

	-webkit-border-radius: @radius;
	   -moz-border-radius: @radius;
		    border-radius: @radius;

	-webkit-background-clip: padding-box;
	   -moz-background-clip: padding;
			background-clip: padding-box;

Default Value: 

	@radius: 3px;
	
### Alt Border radius:

	.alt-border-radius(@topright, @bottomright, @bottomleft, @topleft)
	
Result in:

	-webkit-border-bottom-right-radius: @bottomright;
	 -webkit-border-bottom-left-radius: @bottomleft;
	   -webkit-border-top-right-radius: @topright;
		-webkit-border-top-left-radius: @topleft;
	
	-moz-border-radius-bottomright: @bottomright;
	 -moz-border-radius-bottomleft: @bottomleft;
	   -moz-border-radius-topright: @topright;
		-moz-border-radius-topleft: @topleft;

	border-bottom-right-radius: @bottomright;
	 border-bottom-left-radius: @bottomleft;
	   border-top-right-radius: @topright;
		border-top-left-radius: @topleft;

	-webkit-background-clip: padding-box; 
	   -moz-background-clip: padding; 
		    background-clip: padding-box;


Default Value:

	@topright:	  0;
	@bottomright: 0;
	@bottomleft:  0;
	@topleft:     0;
	
### Box-shadow

	.box-shadow(@shadow);

Result in:

	-webkit-box-shadow: @shadow;
	   -moz-box-shadow: @shadow;
		    box-shadow: @shadow;

Default value:

	@shadow: 0 1px 2px rgba(0,0,0,0.2;
	
### Double Box Shadow

	.double-box-shadow(@shadow1, @shadow2);

Result in:

	-webkit-box-shadow: @shadow1, @shadow2;
	   -moz-box-shadow: @shadow1, @shadow2;
		    box-shadow: @shadow1, @shadow2;

Default value:

	none

### Opacity

	.opacity(@alpha);

Result in:

	-webkit-opacity: @alpha;
	   -moz-opacity: @alpha;
		    opacity: @alpha;

Default value:

	@alpha: 0.5;

### Gradient

#### Vertical Gradient

	.gradient(@startColor, @endColor);

Result in:

	background: @startColor;
	background: -webkit-gradient(linear, left top, left bottom, from(@startColor), to(@endColor));
	background: -webkit-linear-gradient(top, @startColor, @endColor);
	   background: -moz-linear-gradient(top, @startColor, @endColor);
		background: -ms-linear-gradient(top, @startColor, @endColor);
		 background: -o-linear-gradient(top, @startColor, @endColor);
			background: linear-gradient(top, @startColor, @endColor);

Default value:

	none
	
#### Horizontal Gradient

	.gradient(@startColor, @endColor, horizontal);

Result in:

	background: @startColor;
	background: -webkit-gradient(linear, left top, right top, from(@startColor), to(@endColor));
	background: -webkit-linear-gradient(left, @startColor, @endColor);
	   background: -moz-linear-gradient(left, @startColor, @endColor);
		background: -ms-linear-gradient(left, @startColor, @endColor);
		 background: -o-linear-gradient(left, @startColor, @endColor);
			background: linear-gradient(left, @startColor, @endColor);

Default value: 

	none

#### Directional Gradient
	
	.gradient(@startColor, @endColor, @angle);

Result in:

	background: @startColor;
	background: -webkit-linear-gradient(@angle, @startColor, @endColor);
	   background: -moz-linear-gradient(@angle, @startColor, @endColor);
		background: -ms-linear-gradient(@angle, @startColor, @endColor);
		 background: -o-linear-gradient(@angle, @startColor, @endColor);
	 		background: linear-gradient(@angle, @startColor, @endColor);

Default value:

	none
	
### Box Sizing

	.box-sizing(@type);

Result in:

	-webkit-box-sizing: @type;
	   -moz-box-sizing: @type;
			box-sizing: @type;

Default value:

	@type: border-box;

### Animation

	.animation (@name, @duration, @delay, @ease, @direction, @iteration);

Result in:

	-webkit-animation: @name @duration @timing @delay @iterations @direction;
	   -moz-animation: @name @duration @timing @delay @iterations @direction;
		-ms-animation: @name @duration @timing @delay @iterations @direction;
		 -o-animation: @name @duration @timing @delay @iterations @direction;
			animation: @name @duration @timing @delay @iterations @direction;

Default value:

	@name: none;
	@duration: 1000ms;
	@delay: 0; 
	@ease: ease; 
	@direction: normal;
	@iteration: infinite;

### Transition

	.transition (@transition);

Result in:

	-webkit-transition: @transition;
	   -moz-transition: @transition;
		-ms-transition: @transition;
		 -o-transition: @transition;
			transition: @transition;

Default value:

	none
	
### Transform

	.transform(@transformation);

Result in:

	-webkit-transform: @transformation;
	   -moz-transform: @transformation;
		-ms-transform: @transformation;
		 -o-transform: @transformation;
			transform: @transformation;

Default value:

	none

### Transform Origin

	.transform-origin(@origin);

Result in:

	-webkit-transform-origin: @origin;
	   -moz-transform-origin: @origin;
		-ms-transform-origin: @origin;
			transform-origin: @origin;

Default value:

	none

### Rotate

	.rotate (@deg);

Result in:
	
	-webkit-transform: rotate(@deg);
	   -moz-transform: rotate(@deg);
		 ms-transform: rotate(@deg);
		 -o-transform: rotate(@deg);
			transform: rotate(@deg);

Default value:

	none

## Changelog

* **v1.0** Initial Release

## Credits

Created by Crucifix Arnaud ([crucifixarnaud.com](http://crucifixarnaud.com))

This is free and unencumbered software released into the public domain. ([http://unlicense.org](http://unlicense.org))
