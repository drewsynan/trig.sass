# trig.sass
trig and inverse trig functions in pure sass

Occasionally, I find myself needing trig functions and inverse trig functions in front end code. Compass had a great library of math helper functions (including all kinds of trig functions), but unfortunately, the entirely library has been deprecated.

Rather than porting over the Compass math helper code (which just bootstraps to the math functions available in Ruby Sass), it made sense to me to try and have a pure Sass implementation that would work with both Ruby Sass and libsass. There are lots of great tutorials online that use Taylor series expansions to compute trig functions in Sass, but they can be tricky to get to converge (as well as tricky to get all of the coefficients right). This implementation uses polynomial approximations based on the trig functions found in the netlib version of libm.

*nb*: CSS angle rotations are positive *clockwise* and negative *counterclockwise*, unlike standard math representations.
