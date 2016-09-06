# Context Free

##  Who is this programming language for?
_This programming language is for artists who want to render images with
repeated patterns and who have some understanding of programming._

## What is easy to do in this language? Why is it easy?
_It's very easy to repeat a single image or a pattern of images. This is
because the rules in Context Free allow for the same pattern to be
copied in one line of code. These rules also allow the user to change the
location, color, and size of the image by only changing parameters._

## What is hard to do in this language? Why is it hard?
_It's hard to make an image that has many individual pieces that are not the
same or a similar image. With those, you have to adjust the small pieces of
the single image, which becomes difficult because it takes 8-10 lines of
code to make a single section and then cannot reuse any of the code because
each section is different._

## How did you learn how to program in this language?
_I looked at the welcome message that popped up when I opened Context Free for
the first time. I tried to use some of the documentation, but I focused on 
using the already written code to see how the language fit together and 
some ideas that other programmers had already written._

## What is the underlying _computational model_ for this programming language? 
_When Context Free runs, it compiles the startshape rule. To do this, it looks
the at the dependencies for the rule in startshape and then recurses on the 
non-primitive ._

## What do you think is interesting about the ContextFree program you wrote?
It focuses on building the images up from different parts. The leaves are a 
separate rule from the tree, which is a separate rule from the orchard, which
is a separate rule from the forest. The flock of birds above uses the ARCL rule
from the welcome message, and tests out the flip and r parameters to see how to
get the arcs to line up to look like bird wings.
