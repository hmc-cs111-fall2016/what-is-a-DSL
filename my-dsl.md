# Language
_What is the name of the language? Link the name to its webpage 

Shepherd http://github.hubspot.com/shepherd/docs/welcome/


# Domain
Web pages that require tutorials


# Computational model
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of 
what happens when a program in your DSL runs._

Shepherd is a JavaScript library used to guide users through a web page. It allows informative textboxes to be easily pinned to elements through the use of id’s and class names. Users go through the tutorial sequentially through mouse clicks of two buttons: a “next” button that moves to the next step of the tutorial and either a “back” or “exit” button. It relies on another open-source library, Tether, to position all of its steps. 

# DSL-ness
_Fowler writes about a spectrum of languages, from general-purpose languages to 
"purely" domain-specific. Where does the DSL you chose fall on this spectrum, 
and why?_ 

It’s an internal domain-specific language. Shepherd has some aspects of general-purpose languages like conditionals – to determine whether to go back or forward in the tutorial. But for the most part, has more domain-specific attributes. Code written with Shepherd has a sense of fluency in its structure, and Shepherd’s limited expressiveness means it can only be used in the particular domain of web page tutorials. 

# Internal or external?
_Is the language implemented as an internal or external DSL? 
Justify your answer._

Shepherd is an internal domain-specific language because it is valid code in its host language, JavaScript. 

# Host language
_What language(s) was (were) used to implement the DSL?_

HTML, CSS, and JavaScript

# Benefits
_Identify one potential benefit of the DSL: how is a programmer's life or a 
company's bottom line made easier by the existence of this language?_

Instead of having to manually use HTML, CSS and JavaScript to pin informative textboxes manually on a webpage, programmers can use this framework. To make a tutorial in this style without this framework would require a lot of experimentation with CSS positioning which could be quite time-consuming. 

# Drawbacks
_Identify one potential drawback of the DSL: what does a programmer or company 
lose by using this DSL instead of a general-purpose language?_

One potential drawback of using this DSL to make tutorials is that it only supports a very specific kind of tutorial. Should the company or programmer want to change to a different style, for instance using large ‘jumbotron’ images with overlaying text, the amount of tweaking needed to do this in Shepherd defeats the purpose of a DSL – to improve productivity – leading to what Fowler calls “Blinkered Abstraction” in page 39. 

