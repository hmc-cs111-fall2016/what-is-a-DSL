# Context Free

##  Who is this programming language for?

Context Free is useful for people who are interested in creating
computer-generated art.  This could have uses for graphical designs or just
expressing creativity.  Other features in Context Free could interest animators
as well.  

## What is easy to do in this language? Why is it easy?

In Context Free, it is very easy to draw art recursively.  This allows the
creator to make fractals and other patterns with relatively little work.  This
is made possible since shapes can include themselves in their own description, 
so Context Free can make complicated images that would be very difficult to
draw.  In addition, Context Free is good at incorporating randomness in images.
Using the language, it is simple enough to create multiple definitions of a
shape and give it a weight.  It is also easy to draw the same shape with minor
adjustments multiple times, since you can define them and vary parameters.

## What is hard to do in this language? Why is it hard?

It is hard to draw complicated images that do not have much self-similarity 
(for example, drawing an accurate version of the earth).  This is because 
without patterns, you would have to find the end points of each line
individually.  There could be hundreds of unique lines and shapes to fill in,
which would be very tedious work with Context Free.

## How did you learn how to program in this language?

I started by reading the basics about Context Free from the docs on GitHub.
Once I downloaded Context Free, I ran the sample "welcome" program to get an 
idea of how the syntax worked.  I then modified some of the paramters to see 
how it changed the associated picture.  From there, I created a new file and
started experimenting on my own.  When I had questions about what something
meant or whether a feature existed, I checked GitHub for the documentation.

## What is the underlying _computational model_ for this programming language? 
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of what 
happens when a ContextFree program runs._

It seems like when you press Render, Context Free first loads the definitions
of all the shapes you defined.  It then follows all the directions necessary 
to render the start shape.  It seems to follow the steps in order, displaying
shapes as it finds them because when you render a large image, you can see it
gradually processing the smaller shapes. 

## What do you think is interesting about the ContextFree program you wrote?

What I think is most interesting is that it similuates a 3D image by stacking
many 2D shapes on top of each other.  When I first rendered the image, I was
surprised to see the three bright lines trailing from each pyramid, which adds
to the 3D effect.  It seems like this was a convenient consequence of how I
placed the triangles.  The program is also interesting because it is self-
similar and I intensified the saturation as the triangles tailed out.
