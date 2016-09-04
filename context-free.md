# Context Free

##  Who is this programming language for?

Context Free is useful for users who wish to create math-based images with repetited geometric patterns with ease by writing human-readable instructions.  

## What is easy to do in this language? Why is it easy?

In Context Free, it's easy to generate images with repetitive geometric patterns and the user can make the patterns be generated a few times spinning in a direction they specify. This is easy because Context Free lets the user define a "rule" and within the block where they are defining the rule, they can call the rule, making patterns repetitive. 


## What is hard to do in this language? Why is it hard?

Because the coordinates and numbers for things like rotation are very mathematical, and scaled to the output screen in a way that's hard to intuitively grasp without a few trials and errors, it's hard to draw an image that requires a lot of small, complex details. In other words, it's hard for the user to imagine what the "rule" they are writing would end up in the output image. 


## How did you learn how to program in this language?

I skimmed through the documentation on the official website, and then looked through the gallery looking at the example programs and trying to understand how they work line by line. The example images from the gallery helped me picture what outputs would look like when certain code is executed.


## What is the underlying _computational model_ for this programming language? 
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of what 
happens when a ContextFree program runs._

The Context Free program first computes the starting shape, which can be a rule composed of other shapes. If it's a rule, the program computes it line by line. If this rule has just a basic shape, the computation is done. However, if the rule is followed by more rules, it recursively computes those until it reaches nothing but a basic shape.

## What do you think is interesting about the ContextFree program you wrote?

The image my Context Free program produced is a tree, and as a whole, it's hard for one to imagine that it's consisted of merely "SQUARE"s. With a lot of repetitions and rotations, it achieved to produce curvy branches just with squares, which I find very interesting.
