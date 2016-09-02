# Language
_What is the name of the language? Link the name to its webpage 
(if appropriate)._
The name of the language is EasyLanguage. There is documentation
here: http://www.tradestation.com/~/media/Files/TradeStation/Education/University/School%20of%20EasyLanguage/Books/EL_Essentials.ashx

# Domain
_Describe the language's domain in five words._
Financial traders who use TradeStation

# Computational model
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of 
what happens when a program in your DSL runs._

EasyLanguage is compiled to machine code, and then the compiled code is 
executed. 

# DSL-ness
_Fowler writes about a spectrum of languages, from general-purpose languages to 
"purely" domain-specific. Where does the DSL you chose fall on this spectrum, 
and why?_ 

EasyLanguage is designed for people who are not neccessarily programmers but who 
need to make complex statements regarding stock trades. It allows for creating 
functions and it is compiled to machine code. However, users aren't necessarily
 expected to write functions. When used in the way it is intended, EasyLanguage 
 is much simpler than a full language might be. and has very "englishy" syntax. 
 Because that syntax is so clearly intended for the almost-exclusive purpose of 
 finance-related actions, I would argue that it is closer to a pure DSL than a 
 general purpose language.

# Internal or external?
_Is the language implemented as an internal or external DSL? 
Justify your answer._

The language was probably originally an internal DSL as it was based off of pascal.
 However, it now has its own compiler and its own syntax, which means that it is 
 an external DSL. 

# Host language
_What language(s) was (were) used to implement the DSL?_
EasyLanguage was originally based on Pascal

# Benefits
_Identify one potential benefit of the DSL: how is a programmer's life or a 
company's bottom line made easier by the existence of this language?_

Statements in EasyLanguage are very similar to plain English. It was a language
 designed to be useable by non-programmers in order to perform complex trading 
 actions, and it seems to be fairly successful in that goal. It also seems to 
 be one of the selling points for the TradeStation platform. 

# Drawbacks
_Identify one potential drawback of the DSL: what does a programmer or company 
lose by using this DSL instead of a general-purpose language?_

The time and money required to develop and maintain a programming language 
with its own compiler as well as providing documentation sufficient for 
non-programmers to use the language is likely non-trivial. 