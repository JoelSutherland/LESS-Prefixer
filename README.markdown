# LESS Prefixer

All of the CSS3 fun, none of the prefixes!

## What is it?

LESS Prefixer is a set of [LESS](http://lesscss.org/) mixins that let you use vendor-prefixed CSS properties without the prefixes. It uses some simple conventions and gets out of the way so you can use the CSS you already know, but with less typing.

## How does it work?

As a rule, you can use the CSS properties you would expect just by adding a '.' to start them and putting arguments afterwards.

So you type this:

	div {
		.box-shadow(0px 0px 10px rgba(255,0,0,.5));
	}

and you get this through the beauty of LESS:

	div {
		-webkit-box-shadow: 0px 0px 10px rgba(255,0,0,.5);
		-moz-box-shadow: 0px 0px 10px rgba(255,0,0,.5);
		box-shadow: 0px 0px 10px rgba(255,0,0,.5);
	}

The convention is simple: when shorthand is available, arguments are not parameterized. Learn CSS, not LESS Prefixer.

## What's Supported

A whole bunch. There is a nice Table of Contents in the file so you can look this up quickly while working in your project. Everything is even alphabetized.

Additionally, each mixin uses the correct vendor prefixes as indicated by [CSS3Please.com](http://css3please.com/). They aren't just thrown in there willy-nilly.

* .animation(@args)
	* .animation-delay(@delay)
	* .animation-direction(@direction)
	* .animation-duration(@duration)
	* .animation-iteration-count(@count)
	* .animation-name(@name)
	* .animation-play-state(@state)
	* .animation-timing-function(@function)
* .background-size(@args)
* .border-radius(@args)
* .box-shadow(@args)
	* .inner-shadow(@args) *
* .box-sizing(@args)
	* .border-box() *
	* .content-box() *
* .columns(@args)
	* .column-count(@count)
	* .column-gap(@gap)
	* .column-rule(@args)
	* .column-width(@width)
* .gradient(@default,@start,@stop) *
	* .linear-gradient-top(@default,@color1,@stop1,@color2,@stop2[,@color3,@stop3,@color4,@stop4]) *
	* .linear-gradient-left(@default,@color1,@stop1,@color2,@stop2[,@color3,@stop3,@color4,@stop4]) *
* .opacity(@factor)
* .text-shadow(@args)
* .transform(@args)
	* .rotate(@deg)
	* .scale(@factor)
	* .translate(@x,@y)
	* .translate3d(@x,@y,@z)
	* .translateHardware(@x,@y) *
* .transition(@args)
	* .transition-delay(@delay)
	* .transition-duration(@duration)
	* .transition-property(@property)
	* .transition-timing-function(@function)

## Credits

Credit to [LESS Elements](http://lesselements.com/) for the motivation and to [CSS3Please.com](http://css3please.com/) for implementation.