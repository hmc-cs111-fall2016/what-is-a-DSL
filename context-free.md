# Context Free

##  Who is this programming language for?

This programming language is for people who want to create art or 
images on the computer using code. 

## What is easy to do in this language? Why is it easy?

Of course, it is very easy to create images. More specifically, it is easy to 
create images with repeating components.  By defining rules, it is very easy to 
create individual shapes which can be called and used in other parts of the image. 
Furthermore, since users can call the rules in other parts of the code,
recursion is relatively easy and shapes can be reused in different variations 
again easily. Though saying it is easy to create images is very broad, what 
comes to mind is how much cleaner it is to read in comparison to SVG, which is 
widely used for creating images on the web. 

## What is hard to do in this language? Why is it hard?

It is difficult to get the exact shape and color you want since the shape 
adjustments are done through numerical calculations, especially on the first try.
Getting pretty much any of these variations required some trial and error, which
should not really be the case for anything mathematical or code-based.  Though
code should make it very clear what the outcome is, this principle does not 
translate nicely to visual things such as image adjustments. If there was a way 
to adjust the code using a method that interacts with the image more directly 
(for example, a color slider), it would be much easier and more intuitive to 
learn how to actually write the proper code for certain shapes. 

## How did you learn how to program in this language?
I used the example images and the matching code to get a grasp of the 
syntax, and then referenced the documentation to find out what the variables in
those examples represented.

## What is the underlying _computational model_ for this programming language? 
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of what 
happens when a ContextFree program runs._

When the program runs, it looks for the `startshape`.  If the startshape is made
up of one of the given, primitive shapes, the computer starts rendering that
shape.  Otherwise, if another rule is given, the computer looks at the next rule
and determines whether a primitive shape exists. It continues to do so until a 
primitive shape is found, which is then rendered. This happens for all rules,
so the computer is just recursively searching in rules until it can render a 
basic, primitive shape.  


## What do you think is interesting about the ContextFree program you wrote?

I think my program is interesting because it is created with a single line that
contains a primitive shape.  By using `SQUARE` once in the code, I could create
this image, an abstract piece, but I personally view it as a shooting star 
(largest one on the bottom) zooming into the distance with its trail behind it. 
