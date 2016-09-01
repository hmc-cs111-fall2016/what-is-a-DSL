# Language
_What is the name of the language? Link the name to its webpage_

[Erlang](https://www.erlang.org/)

# Domain
_Describe the language's domain in five words._

Massively scalable real-time systems

# Computational model
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of 
what happens when a program in your DSL runs._

The code is first compiled.  Then it gets run on a C emulator.

# DSL-ness
_Fowler writes about a spectrum of languages, from general-purpose languages to 
"purely" domain-specific. Where does the DSL you chose fall on this spectrum, 
and why?_ 

I think it classifies as a domain specific langauge, but I think it is more on
the general purpose side of the spectrum because it has control structures like
loops which make it have a less limited expressiveness.  However it is still
clearly targeted at specific domains where massive real time scalability is
required.  It has a sense of fluency in the way expressions come together
meeting the language nature requirement, and it is a computer programming
language.

# Internal or external?
_Is the language implemented as an internal or external DSL? 
Justify your answer._

This appears to be an external language since it is seperate from any other
language.  It is not a particular way of using an internal langauge.

# Host language
_What language(s) was (were) used to implement the DSL?_

Originally, author designed an abstract machine to execute Erlang a compiler
from Erlang to his abstract machine in prolog!  However later the prolog was
scrapped in favor of using C.

# Benefits
_Identify one potential benefit of the DSL: how is a programmer's life or a 
company's bottom line made easier by the existence of this language?_

It makes writing code that is scalable much easier and seems to force a
functional programming like style upon the programmer which has many benefits
such as the ability to prove correctness and it makes writing recursive
functions feel very natural.

# Drawbacks
_Identify one potential drawback of the DSL: what does a programmer or company 
lose by using this DSL instead of a general-purpose language?_

The syntax is rather different from most general-purpose languages such as
C/C++, java, and python so there is a cost to learn it.  
