# Context Free

##  Who is this programming language for?

ContextFree is for people who are interested in making (variations of ) cool 
pictures, with minimal effort.

## What is easy to do in this language? Why is it easy?

It's easy to create complex images from deceptively simple rules, thanks to 
repeated patterns, recursion, and built-in randomness.

## What is hard to do in this language? Why is it hard?

It's hard to have complete control over the layout of a picture.  If you wanted
to write words or draw an image that requires pixel-level precision, you'd have
a hard time. The reason it's hard is because randomness is a key aspect of
ContextFree: the idea is to be able to make many different variations on a theme.
The language encourages play over rigor.

## How did you learn how to program in this language?

I looked at lots of examples, and I read the documentation. When I started to 
write programs, I started by modifying existing programs.

## What is the underlying _computational model_ for this programming language? 
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of what 
happens when a ContextFree program runs._

A program describes a set of rules. Each rule draws a shape, and one rule may
invoke additional rules by name, to continue the drawing. If a program contains
multiple rules defined with the same name, ContextFree randomly chooses which
definition to use. Drawing starts with a specified initial rule and ends when
either (a) no more rules can be invoked or (b) when a rule would draw a shape
whose size is smaller than one pixel (I *think* this is true).

Put another way: A ContextFree program describes a non-deterministic push-down 
automaton. When the program runs, the automaton goes from the start state to an
accepting state, drawing pixels as described by the rules of each state through 
which it passes.


## What do you think is interesting about the ContextFree program you wrote?

I like that it looks almost like a clump of wild grass. I wish the rules were a
bit simpler, and the program definitely takes too long to terminate. But still,
...pretty pictures!
