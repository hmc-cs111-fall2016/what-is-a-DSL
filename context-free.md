# Context Free

##  Who is this programming language for?
The language is targeted toward anyone with access to a computer (Windows,
Mac, or Linux).  

## What is easy to do in this language? Why is it easy?
It is easy to create shapes and modify their attributes.  This is because
it provided built in functions for many primitive shapes (such as circles,
triangles, squares, etc.) and color support.  It is also easy to compose
shapes because the grammer allows for the definition of shapes to include
shapes.

## What is hard to do in this language? Why is it hard?
I found it difficult to learn the semantic model of the DSL.
When I initially wanted to use recursion I was uncertain how to
implement it since I did not find an obvious way to check for a base
case or pass arguments to a function.  (Although there is explanation
of pasing parameters to shapes in Version 3, it seems that no such
feature exists in Version 2.)  Eventually I found (not in the documentation)
but in one of the lesson files, `lesson.cfdg`, the following: 
> A shape can use itself so long as it keeps getting smaller.
> The system will stop the recursion when the shapes get too small to see.
The fact that shapes were drawn from the center rather than one endpoint (or
giving the choice of where to draw from) made it difficult in my case for
me to determine without a bit of trial and error exactly how much I wanted to
shift the x and y coordinates.

## How did you learn how to program in this language?
I followed the guide online, looked at the example code that was present in
the Context Free IDE, and I also looked at the [Context Free Art Gallery](
http://www.contextfreeart.org/gallery/index.php).

## What is the underlying _computational model_ for this programming language? 
The computational model is a recursive one in which every base case
is the drawing of a primitive shape (perhaps with modifications) or the
automatic "bottoming-out" when a shape is too small to display. In some ways
it reminds me of Post Script in that any time an element is drawn, the
attributes of the drawn shape depend on the current state (rotation, scaling,
position, etc.) based on the shapes that referenced the current one.

The startshape is analagous to the `main` function of a C/C++ program, since
the only code that is executed is the code that is called by that main shape.
We can think of the entire computation as substiting the call for a given
shape by the code for that shape (perhaps recursively until we have
primitive shapes or shapes that are sufficiently small).

## What do you think is interesting about the ContextFree program you wrote?
I have always liked the recursive structure of the Sierpinski triangle, and
I thought it was interesting to have the colors depend on the direction of the
recursive call.  From the perspective of any given triangle, the recursive
call above will have a lower saturation and hue, the one to the left with have 
a hue and saturation that grow at a similar rate, and the call to the right will
have a hue that grows 15x faster than the saturation.  This gives a nice color
distribution to the final figure.

