# Context Free

##  Who is this programming language for?
People who want to program art, perhaps for interesting geometric shapes.

## What is easy to do in this language? Why is it easy?
Recursion. We can easily define shapes and recursively create that shape.

## What is hard to do in this language? Why is it hard?
Art that involves randomness is hard to do. Version 2 does not support 
function calls and expressions.

## How did you learn how to program in this language?
Digging around documentation, I found this really helpful
[page](https://github.com/MtnViewJohn/context-free/wiki/Shape-Adjustments). 
Looking at the sample code that came with the program was moderately helpful.
I got help from Sam Andow on understanding loops. Ultimately, what helped me
the most was and lots and lots of trial and error, which I found to be a 
pretty frustrating way to learn a language.

## What is the underlying _computational model_ for this programming language? 
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of what 
happens when a ContextFree program runs._

It reads all the lines and makes sure that it works syntactically.
It draws the rule specified by `startshape`. Then it goes line by line
for each rule.


## What do you think is interesting about the ContextFree program you wrote?
It draws a fractal recursively. It also constructs more complicated shapes,
by defining rules for increasingly complicated shapes, such as defining
rectangles to draw limbs. I really wanted to introduce some randomness to the
program to make it more interesting, but the version we are using doesn't
seem to handle expressions for shapes.

