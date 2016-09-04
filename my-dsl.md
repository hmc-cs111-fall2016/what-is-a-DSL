# Language
The Domain Specific Language I will be discussing
is named [LilyPond](http://lilypond.org).

# Domain
Typesetting musical scores from text.

# Computational model
The DSL will take text input from the user, parse it and generate 
a typeset musical score in a specificed format (such as PDF or PNG).

The input text has syntax which describes the music to be typeset (including
notes, keys, accidentals, and various annotations).  As mentioned on the
[Text input](lilypond.org/text-input.html) page of the website "Notes are
encoded with letters and numbers. Special commands are entered with
backslashes."  This is notably similar to LaTeX, in that there is text which
encodes information about how the final document should appear, which is
then compiled to produce a beautiful document.

For example, the following code, with LaTeX reminiscent syntax:
![input-annotate.png](http://lilypond.org/pictures/text-input-1-annotate.png)
produces the following output:
![output.png](http://lilypond.org/pictures/text-input-1-output.png)

# DSL-ness
LilyPond is on the domain-specific side
_Fowler writes about a spectrum of languages, from general-purpose languages to 
"purely" domain-specific. Where does the DSL you chose fall on this spectrum, 
and why?_ 


# Internal or external?
_Is the language implemented as an internal or external DSL? 
Justify your answer._


# Host language
_What language(s) was (were) used to implement the DSL?_


# Benefits
_Identify one potential benefit of the DSL: how is a programmer's life or a 
company's bottom line made easier by the existence of this language?_


# Drawbacks
_Identify one potential drawback of the DSL: what does a programmer or company 
lose by using this DSL instead of a general-purpose language?_
