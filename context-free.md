# Context Free

##  Who is this programming language for?

Context Free if for people who want to quickly make random and mathematically
inspired animations and pictures. (Although it may not be entirely intended to
make animations, the slow renderer combined with the time commands make it a
possible use case.)

## What is easy to do in this language? Why is it easy?

It is easy to make pattern filled, recursive, and random images due to the
nature of the language. The loop syntax is especially helpful in making
interesting patterns.

It is also easy, no matter the end picture, to understand the composobility of
shapes if the code chunks are factored appropriately to different "shape" names.
Since we can nest primitive and custom shapes within one another, it makes it
easier to preciesly refer to a part of the picture should someone need to give
feedback or design critiques.

## What is hard to do in this language? Why is it hard?

It is hard to create pictures of non-organic items (or perhaps my artistic
skills and familiarity with the language need more developing). Since
ContextFree is code that starts with primitive shapes, one must try really hard
to mentally divide a non-organic shape into primitive shapes if they want to
draw it accurately. Making adjustments requires a bit of guess and check then
a slow re-render which makes it harder.

## How did you learn how to program in this language?

At first, I began looking through the documentation directly, but quickly
realized learning a DSL destined for visual design was better suited
for experimentation, so I switched to looking at sample images on the Context
Free website.

By looking at and downloading the source and investigating how the
images "worked"&mdash;a combination of reading more of the documentation as
needed and experimentally commenting lines out and adjusting values then
analyzing its effect on the final image&mdash;I was able to (partially) grasp
the language.

## What is the underlying _computational model_ for this programming language?
_We don't yet have a great definition of the term "computational model".
For now, try to come up with the clearest, most concise explanation of what
happens when a ContextFree program runs._

At first, the parser or image builder looks for the top-level shape and then
looks to see what other shapes it is composed of. Once it finally hits a
primitive shape, it renders a unit of the larger shape with the specified
characteristics. As it continues and the sub-shapes are drawn, the larger shapes
naturally come are created. When there are no more loops to evaluate or
primitives to draw it finishes.

Since there is randomness embedded into the renderer, there is almost certainly
a step before the rendering where the builder chooses a seed value for the
"random" selections.

## What do you think is interesting about the ContextFree program you wrote?

Although you cannot observe it in the still PNG image, the iterative nature of
my image makes it especially fun to watch it come to life. As it is being
rendered, there are swirls of color that eventually come together to create the
rainbow sphere. Best of all, I don't think the sphere-like look is obvious until
you watch it.
