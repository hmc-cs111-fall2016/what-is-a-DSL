# Context Free

##  Who is this programming language for?

ContextFree is for people who want to create designs with lots of similar 
geometric images that rely on symmetry.

## What is easy to do in this language? Why is it easy?

It is easy to create symmetrical geometric patterns concisely because 
ContextFree uses recursion to build them in just a few lines of code.

## What is hard to do in this language? Why is it hard?

Displaying words and sentences can be difficult in ContextFree because this 
design cannot take advantage of recursion. For example, in order to create the 
Welcome demo, you need to write rules for each unique letter and then place 
each letter in the correct position. Imagine how much code would be required to 
write a Chinese phrase, with so many characters and strokes.

## How did you learn how to program in this language?

I looked at the examples provided in the program and changed it so that I can 
see what each line does. I also read the ContextFree Wiki on github and looked 
at cool designs on [contextfreeart.org](https://contextfreeart.org/gallery/).

## What is the underlying _computational model_ for this programming language? 
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of what 
happens when a ContextFree program runs._

ContextFree renders an image based on a starting shape with a rule. Rules 
describe how a shape is created (often by rendering a shape and then recursing 
on a smaller shape). Sometimes, a shape can have multiple rules, allowing for 
randomness and variation with each rendering. A shape stops recursing when the 
size is too small or it doesn't call another rule. With the circle, square, and 
triangle as basic shapes, users can build complex and varied geometrical 
images with a little code.

## What do you think is interesting about the ContextFree program you wrote?

Many people use ContextFree to render sophisticated and smooth images, but I 
like how I can also build colorful cartoons. 

My image does not allow for extensive variation from render to render. Instead, 
I focused on building body parts using a variety of colors and shapes. By 
combining distinct shapes created by recursion, I can create a specific image 
with symmetrical elements.

Aesthetically, most shapes have jagged edges, creating an overall cartoonish 
effect. But at the same time, ContextFree can also be used to build "smooth" 
images, like how the eye gradually changes color. 

I also tweaked the code from "ziggy", an example provided in the program, so 
that the horn is not just a zig-zag but a more complex pattern.
