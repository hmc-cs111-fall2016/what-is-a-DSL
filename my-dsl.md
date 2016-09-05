# Body Markup Language (BML)

## Language
_What is the name of the language? Link the name to its webpage 
(if appropriate)._

Behavior Markup Language (BML) 
http://www.mindmakers.org/projects/bml-1-0/wiki#BML-10-Standard

## Domain
_Describe the language's domain in five words._
Controlling embodied conversational agents’ behaviors

## Computational model
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of 
what happens when a program in your DSL runs._
BML code specifies the behaviors to be performed by an embodied conversation 
agent - these can include nonverbal facial and body movements as well as 
verbal behaviors. The code is executed through a module called a BML 
Realizer, which may be run as a stand-alone application, embedded as a 
library, or embedded within a game engine. When the BML Realizer is run, an 
embodied conversation agent that is integrated with the BML Realizer performs 
the behaviors. 


## DSL-ness
_Fowler writes about a spectrum of languages, from general-purpose languages to 
"purely" domain-specific. Where does the DSL you chose fall on this spectrum, 
and why?_ 
I would say BML is purely domain-specific because it functions specifically 
as a tool for behavior generation for embodied agents, and it is often used 
in conjunction with other languages to produce more sophisticated 
applications (i.e. using BML to control characters in a game engine like 
Unity, which uses JavaScript or C# scripts).


## Internal or external?
_Is the language implemented as an internal or external DSL? 
Justify your answer._
BML uses the general syntax of XML and consists of fairly extensive set of 
elements and attributes specific to its language. It very much functions as 
an external DSL because it must be processed by a BML realizer, which is 
implemented in a general programming language such as C++, that will 
interpret the language and produce corresponding behaviors in the embodied 
agent.

## Host language
_What language(s) was (were) used to implement the DSL?_
BML uses XML syntax.

## Benefits
_Identify one potential benefit of the DSL: how is a programmer's life or a 
company's bottom line made easier by the existence of this language?_
BML provides a centralized language for controlling and rigging character 
behavior, and because BML realizers can be integrated into different 
platforms, developers have the ability to use this language in developing 
different types of applications that involve some sort of character speech +and movement. 

## Drawbacks
_Identify one potential drawback of the DSL: what does a programmer or company 
lose by using this DSL instead of a general-purpose language?_
As of now, the potential for BML is largely limited by the quality of the BML 
realizers that are available right now. A character’s facial movements and 
locomotion produced by BML may not be exactly what the developer wants. So 
even though BML may one day make a developer’s work much easier, this will 
depend on how much BML realizers can be improved, which will certainly take 
some time. 

