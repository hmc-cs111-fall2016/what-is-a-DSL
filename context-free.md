# Context Free

##  Who is this programming language for?
This programming language is for people who want to create digital art.

## What is easy to do in this language? Why is it easy?
Recursively creating shapes is easy because shapes are created inside rules.

## What is hard to do in this language? Why is it hard?
It was very hard for me to learn it, taking well over an hour.  It requires
memorization of syntax and avaiable rules unlike a simple program such as paint
where you can see what is available for use.  Additional memorization is
required to know what transforamtions you have available for your shape (such
as using hue to color things is less obvious than something like color). Drawing
like one would with a pencil is quite hard because everything has to be
programmed in and cannot be drawn using mouse.

## How did you learn how to program in this language?
Struggled with the documentation and looking at the sample code so I found a
youtube video tutorial, which explained things well but for the incorrect
version.  However after the youtube tutorial, the documentation made more sense.

## What is the underlying _computational model_ for this programming language? 
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of what 
happens when a ContextFree program runs._

Code is written to describe an image and then rendered to an image format of
choice.  Context Free is written in C++ and Objective C++ for mac and uses
libpng for rendering and writing PNG files.


## What do you think is interesting about the ContextFree program you wrote?
Once I got through the struggle of understanding the language it was interesting
that I could pretty simply create a chessboard.  I thought it was interesting
the way I could define a rule and and reuse it with different transformations
in the position and color with ease.