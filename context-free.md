# Context Free

##  Who is this programming language for?

I think this language is for people that want to make digital art using context-free grammars.

## What is easy to do in this language? Why is it easy?

It is easy to create rules in this language. It is also easy to use primitive shapes and modify them. These kinds of things are easy because they are the bread and butter of the language. Everything needs rules and primitive shapes along with the parameters for the shapes.

## What is hard to do in this language? Why is it hard?

I think it is hard to keep track of all the rules and where everything is going to show up on the screen. Although beautiful, complex diagrams can be created recursively, there are probably times where one will need a lot of rules to make the drawings they want. Rules can quickly become incoherent if the number of rules and dependencies grows large. The coordinate system and sizing of the objects is a bit hard as well. It's hard to think of coordinates and know where they are going to exactly be placed. It would sometimes take several tries to get a shape in the exact desired place. The sizing of the objects is also a bit hard to intuit because the program can resize the drawing to fit the screen. There could be something to stop this from happening, but this is just from my initial experience.

## How did you learn how to program in this language?

I learned the language by starting with the lesson examples in the program and then reading the documentation. The lessons were recommended by the documentation as they had nice comments explaining the basics. The documentation helped with the differences between version 2 and 3 as well as more complicated things like loops.

## What is the underlying _computational model_ for this programming language? 
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of what 
happens when a ContextFree program runs._

Based on the documentation, it looks like the CFDG code is converted into C++ code and then compiled/run. 

## What do you think is interesting about the ContextFree program you wrote?

I think it is interesting that a small amount of code with recursion and a loop can create a "pretty" symmetric image. In my case, this is a awkward attempt at a snowflake. It is also interesting to note that we can do powerful things like recursion and loops in a context for just images.

