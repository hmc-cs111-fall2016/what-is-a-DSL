# Context Free

##  Who is this programming language for?

This programming language is for anyone who wants to create images using written instructions.

## What is easy to do in this language? Why is it easy?

It's easy to make recursive, fractal-like patterns! 
It's also very easy to change the location, size, color, hue, angle, 
and saturation of any object. 

The syntax of this language was also straightforward. 
It seems that if the user does not specify a 
location, size, color, hue, angle, or saturation of an object, 
the program knows to set the default. 
Thus, one only has to explicitly state if he/she wants to; 
for example, if one only wants to change the color of an object
from the default color to another color, 
and does not have to explicitly specify keeping other elements the default.

Also, it is nice that writing "s 6 b 0.5" is the same thing as "b 0.5 s 6 b". 
I appreciated this flexibility in specifying the features of an object.

## What is hard to do in this language? Why is it hard?

It was hard to make images that look like letters -- 
maybe there is a shortcut I did not realize, but it was a little annoying to 
have to use lines and arcs to create letters, instead of being able to 
type out the letters themselves.

## How did you learn how to program in this language?

I started by modifying the starter file that was an image of "WELCOME" 
with some vines around it. I changed the location, size, color,
hue, angle, and saturation of certain lines and shapes, and then started adding
repeated elements to each object.

I also looked at the documentation site, through which I learned how to add a background color. 

## What is the underlying _computational model_ for this programming language? 
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of what 
happens when a ContextFree program runs._

I think the program reads the written instructions sequentially, beginning
with the background color, if it is specified, and moving to the startshape, which is 
necessary to specify. 
The program encounters rules, in the order that they are written, and executes all the 
components of that rule before moving onto the next rule.

## What do you think is interesting about the ContextFree program you wrote?

I think it's interesting that I found a way to make the stems of the vine
repeat without explicitly writing and placing each one! 
