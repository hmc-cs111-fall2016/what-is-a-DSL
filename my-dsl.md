# Language
_What is the name of the language? Link the name to its webpage 
(if appropriate)._

[POV-Ray](http://www.povray.org/)
([Source-code](https://github.com/POV-Ray/povray))

# Domain
_Describe the language's domain in five words._

Creates images using ray tracing

# Computational model
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of 
what happens when a program in your DSL runs._

POV-Ray contains a _front-end_ and a _back-end_.  A user specifies various
fields such as a light source, camera, shape, background, etc.  The front-end
locates the files and gives them to the back-end to parse and compute the
image data.  The back-end then sends the information back to the front-end,
which writes the image data to a file. [Source](https://github.com/POV-Ray/povray/blob/master/source-doc/architecture.md)

# DSL-ness
_Fowler writes about a spectrum of languages, from general-purpose languages to
"purely" domain-specific. Where does the DSL you chose fall on this spectrum,
and why?_ 

POV-Ray is closer to the domain-specific side, since it is purely used to 
generate images.  However, I would hesitate to say that it is "purely"
domain-specific, because it supports loops and macros that make it
Turing-complete.  Regardless, the intended use is for creating graphics.


# Internal or external?
_Is the language implemented as an internal or external DSL? 
Justify your answer._

It is an **external** DSL because POV-Ray uses a seperate syntax from its host 
language, C++. The code is also compiled in its host language, which is common
for an external DSL. 

# Host language
_What language(s) was (were) used to implement the DSL?_

C++

# Benefits
_Identify one potential benefit of the DSL: how is a programmer's life or a 
company's bottom line made easier by the existence of this language?_

The language is much more specific to rendering images, and so it is much
easier to read the code and figure what the programmer is intending than it
would be without POV-Ray.  Also, this language keeps the programmer from
doing the complicated calculations that come with rendering and optimizing 3D
graphics based on camera position, light source, etc.  

# Drawbacks
_Identify one potential drawback of the DSL: what does a programmer or company 
lose by using this DSL instead of a general-purpose language?_

According to their [docs](http://www.povray.org/documentation/3.7.0/u1_1.html#u1_1), you cannot edit objects on the screen with a 
point-and-click interface".  This could be a drawback for a company that is
more interested in building images interactively than from a text file.  There
are many other DSLs that have such interfaces built in.  However, POV-Ray 
claims that supporting interactivity causes has its drawbacks for "absolute 
control of the scene".
