# Context Free

##  Who is this programming language for?

Context Free is for artists iterested in exploring generative art.

## What is easy to do in this language? Why is it easy?

It's easy to generate art that has a lot of symmetry. One of the easiest tricks
for generating an image is to create recursive shape rules, and this tends to
lead to shapes with a recursive structure, which results in symmetry. The
handful of tree-like example programs confirm this.

## What is hard to do in this language? Why is it hard?

It would be hard to replicate a picture of some real object in the language.
Encoding the information in a picture (which probably does not have too much
symmetry) would take a lot of code in this language, whose primary strength is
encoding symmetry in only a few lines.

Obviously, it would also be tremendously difficult to do any sort of
computation or general-purpose programming in this language (although not
impossible; the language has conditionals, loops, variables, functions, and
recursion, so I believe it's Turing-complete).

## How did you learn how to program in this language?
I first read the documentation and tried to form a mental model for how the
language works. Then I looked at the example programs, and tried to understand
how they work, tweak things, and then change my mental model based on the
results. Finally, I started writing a program and experimenting.

## What is the underlying _computational model_ for this programming language? 
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of what 
happens when a ContextFree program runs._

Computation begins with the `startshape`. If this is a primitive, the shape is
drawn and the program terminates. Otherwise, if there is a replacement rule for
the shape, the rule is evaluated, which means the `startshape` is replaced with
the contents of the rule. The result is then evaluated recursively, until there
is nothing left but primitives.

If the program ever encounters multiple rules for the same shape, a rule is
chosen at random with probability proportional to the rule weight.

## What do you think is interesting about the ContextFree program you wrote?

It seems to exhibit some chaotic behavior. There are 3 parameters that
determine the output -- the probability of a line branching, the probability
of a line terminating, and the size decay factor when branching -- which must
be kept in a precise relationship with each other for the program to work well.
This is documented further in the comments.

If the values of the parameters are not satisfactory, the program may render
lines with very little branching, which makes for a boring image. Tweak the
parameters even slightly, though, and suddenly the program continues branching
seemingly forever.

I also find it interesting that, even in the range that usually produces
interesting results and usually terminates, there is a very high variability
in the complexity of the result in different runs of the program with the same
parameters.
