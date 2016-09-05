# Language
_What is the name of the language? Link the name to its webpage 
-(if appropriate)._
Django--https://www.djangoproject.com/


# Domain
_Describe the language's domain in five words._
Web development for Python users.


# Computational model
_We don't yet have a great definition of the term "computational model". 
-For now, try to come up with the clearest, most concise explanation of 
-what happens when a program in your DSL runs._
Django is compiled through the command line, like other Python programs.After 
that, the code is by default sent to the Django development server, where they 
can view it. Users could also redirect the code to their website when they are 
finished developing.


# DSL-ness
_Fowler writes about a spectrum of languages, from general-purpose languages to 
-"purely" domain-specific. Where does the DSL you chose fall on this spectrum, 
-and why?_ 
Django sits right in the middle of the spectrum. Fowler mentions limited
expressiveness, espeically for internal DSLs. On page 30, he notes that "it's
common to avoid conditions, looping constructs, and variables." Django includes 
conditional statements and relies heavily on variables. Additionally,
everything is broken down into classes and methods, which are rather abstract.
However, Django includes many helpful classes, like models, which allow for the
feel of "putting together full sentences," like Fowler mentions on page 30. For
instance, the class "models" gives methods like DateTimeField, which build in
necessary elements for web development.


# Internal or external?
_Is the language implemented as an internal or external DSL? 
-Justify your answer._
Internal. Everything is written in Python and compiled like a Python script.
Django developers have just added onto Python to add more elements that are web
development specific, like the "models" class mentioned, and made each compiled
program also push to a website.


# Host language
-_What language(s) was (were) used to implement the DSL?_
Python


# Benefits
_Identify one potential benefit of the DSL: how is a programmer's life or a 
-company's bottom line made easier by the existence of this language?_
Python is a relatively easy language to learn and is taught for many other
reasons too. People use Python for Excel macros and in intro computing classes, 
so there are already many people who know how to use it, so they are leveraging
a language people are already comfortable with to do website development.


# Drawbacks
_Identify one potential drawback of the DSL: what does a programmer or company 
-lose by using this DSL instead of a general-purpose language?_
The focus on classes and methods is rather abstract and something that not
everyone who learned Python will know. It may cause more confusion than HTML or
CSS, which do not rely on abstractions.
