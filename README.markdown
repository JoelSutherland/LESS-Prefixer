# LESS Prefixer

All of the CSS3 fun, none of the prefixes!

## What is it?

LESS Prefixer is a set of [LESS](http://lesscss.org/) mixins that let you use vendor-prefixed CSS properties without the prefixes. It uses some simple conventions and gets out of the way so you can use the CSS you already know, but with less typing.

## How does it work?

First include the less file provided like this:

    @import ".../prefixer.less";

Please note that `...` refers to the location where the file was installed.  If you instaled this package from Bower, replace the ellipsis with `bower_components/less-prefixer`.

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

* .keyframes(@name; @args)
* .animation(@args)
    * .animation-delay(@delay)
    * .animation-direction(@direction)
    * .animation-duration(@duration)
    * .animation-fill-mode(@mode)
    * .animation-iteration-count(@count)
    * .animation-name(@name)
    * .animation-play-state(@state)
    * .animation-timing-function(@function)
* .background-size(@args)
* .border-radius(@args)
* .box-shadow(@args)
    * .inner-shadow(@args) 
* .box-sizing(@args)
    * .border-box() 
    * .content-box() 
* .columns(@args)
    * .column-count(@count)
    * .column-gap(@gap)
    * .column-rule(@args)
    * .column-width(@width)
* .gradient(@default,@start,@stop) 
    * .linear-gradient-top(@default,@color1,@stop1,@color2,@stop2,[@color3,@stop3,@color4,@stop4])*
    * .linear-gradient-left(@default,@color1,@stop1,@color2,@stop2,[@color3,@stop3,@color4,@stop4])*
* .keyframes(@name; @args)
* .user-select(@select)
* .opacity(@factor)
* .transform(@args)
    * .transform-origin(@args)
    * .transform-style(@style)
    * .rotate(@deg)
    * .scale(@factor)
    * .translate(@x,@y)
    * .translate3d(@x,@y,@z)
    * .translateHardware(@x,@y) 
* .text-shadow(@args)
* .transition(@args)
    * .transition-delay(@delay)
    * .transition-duration(@duration)
    * .transition-property(@property)
    * .transition-timing-function(@function)
* Flexbox: 
    * .flex-block()
    * .flex-inline()
         * .flex-flow(@direction: row, @wrap: nowrap)
             * .flex-direction(@direction: row)
             * .flex-wrap(@wrap: nowrap)
    *     .justify-content(@justification)
    *     .align-items(@mode)
    *     .align-content(@alignment)
    *     .flex(@args: none)
             * .flex-grow(@grow: 1)
             * .flex-shrink(@shrink: 1)
             * .flex-basis(@basis: auto)
    *     .order(@num: 0)
    *     .align-self(@align: auto)

## Credits

Credit to [LESS Elements](http://lesselements.com/) for the motivation and to [CSS3Please.com](http://css3please.com/) for implementation.
