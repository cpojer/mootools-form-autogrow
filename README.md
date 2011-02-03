Form AutoGrow
=============

Automatically resizes textareas based on their content.

This Plugin is part of MooTools [PowerTools!](http://cpojer.net/PowerTools).

* [Build PowerTools!](http://cpojer.net/PowerTools)
* [Fork PowerTools!](https://github.com/cpojer/PowerTools)

Build
-----

Build via [Packager](http://github.com/kamicane/packager), requires [MooTools Core](http://github.com/mootools/mootools-core) and [MooTools Class-Extras](http://github.com/cpojer/mootools-class-extras) to be registered to Packager already


	packager register /path/to/form-autogrow
	packager build Form-AutoGrow/* > form-autogrow.js

To build this plugin without external dependencies use

	packager build Form-AutoGrow/* +use-only Form-AutoGrow > form-autogrow.js

Demo
----

See Demos/index.html

How To Use
----------

Create a new instance of Form.AutoGrow for your TextArea-Element

	new Form.AutoGrow('myTextarea');

Options
-------

* minHeightFactor (number, defaults to *2*): The minimum textarea height based on the font-size
* margin (number, defaults to *0*): A margin to be added (subtracted) to the calculated textarea height

CSS Tips
--------

Use the following CSS-Styles to get most out of Form.AutoGrow.

Hide the vertical scrollbar that sometimes appears in Webkit while resizing

	textarea {
		overflow-y: hidden;
	}

Hide the resize handle in Webkit

	textarea {
		resize: none;
	}

Animate the height via CSS-Transforms

	textarea {
		-moz-transition-duration: 250ms;
		-webkit-transition-duration: 250ms;
		-o-transition-duration: 250ms;
		transition-duration: 250ms;
		-webkit-transition-property: height;
		-moz-transition-property: height;
		-o-transition-property: height;
		transition-property: height;
	}