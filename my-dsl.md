# Language
_What is the name of the language? Link the name to its webpage 
(if appropriate)._

The name of the language is CHEM. It is fairly old, so it does not have a webpage. However, a paper that talks about it can be found at this link http://dl.acm.org/citation.cfm?id=315691

# Domain
_Describe the language's domain in five words._

Creates chemical structure diagrams.

# Computational model
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of 
what happens when a program in your DSL runs._

When a program runs, it reads lines and draws something onto the canvas based on what was on the line. It can draw things like benzene and can connect them with things like double bonds. The final output is a chemical structure diagram.

# DSL-ness
_Fowler writes about a spectrum of languages, from general-purpose languages to 
"purely" domain-specific. Where does the DSL you chose fall on this spectrum, 
and why?_ 

CHEM is purely domain-specific. It focuses on drawing chemical structure diagrams and does not support drawing other diagrams. It really cannot do anything else besides draw chemical structure diagrams. Valid code in CHEM is something like "doublebond -135 from Rl.V3 ; 0" and cannot diverge from this kind of writing.

# Internal or external?
_Is the language implemented as an internal or external DSL? 
Justify your answer._

One could argue that this is an external DSL because it is meant to be used stand alone. It also looks like an internal DSL because it takes some operations from the PIC programming language and extends it slightly to make it nice for chemists to use. However, internal DSLs are a subset of their host language, and the host language is typically a general-purpose language (PIC is a DSL). So I would say that CHEM is an external DSL.

# Host language
_What language(s) was (were) used to implement the DSL?_

Awk and PIC were used to implement the DSL.

# Benefits
_Identify one potential benefit of the DSL: how is a programmer's life or a 
company's bottom line made easier by the existence of this language?_

Chemical structure diagrams tend to take a long time to make and can be costly. CHEM saves the programmer time and money as a result.

# Drawbacks
_Identify one potential drawback of the DSL: what does a programmer or company 
lose by using this DSL instead of a general-purpose language?_

Since CHEM is only able to draw diagrams, programmers cannot perform computations on the structures made in CHEM directly. With a general-purpose language, the structures would probably be in some data structure, and the bonds, elements, and other values can be accessed for computational purposes.
