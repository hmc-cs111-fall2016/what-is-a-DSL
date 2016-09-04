# Language
_What is the name of the language? Link the name to its webpage._

The Domain Specific Language I will be discussing
is named [LilyPond](http://lilypond.org).

# Domain
_Describe the domain of the language in five words._
Typesetting musical scores from text.

# Computational model
_Fowler writes about a spectrum of languages, from general-purpose 
languages to "purely" domain-specific. Where does the DSL you chose fall on
this spectrum, and why?_

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
_Fowler writes about a spectrum of languages, from general-purpose languages to
"purely" domain-specific. Where does the DSL you chose fall on this spectrum, 
and why?_ 

LilyPond is on the domain-specific side of the spectrum.  Although it can be
used to typeset many forms of music with great generality, its use case is
exclusively the domain of typesetting music, making it _more_ restrictive than
TeX or LaTeX, which we already consider to be a DSL (even thought it
is Turing Complete).


# Internal or external?
_Is the language implemented as an internal or external DSL? 
Justify your answer._

The language is implemented as an external DSL.  Although based on the syntax
I assumed that it was an internal DSL of LaTeX, that provided macros or wrappers
for TikZ commands, it turns out that this was incorrect.  LilyPond is an
external DSL, implemented in a mix of C++ and Lisp, and simply expects its
input text in a format similar to TeX.

# Host language
_What languages were used to implement the DSL?_

As mentioned in the above question, C++ and Lisp were used to implement this
DSL.

# Benefits
_Identify one potential benefit of the DSL: how is a programmer's life or a 
company's bottom line made easier by the existence of this language?_

A programmer need not use TikZ to typeset their notes directly, nor be forced
to make the choice between a simple framework for plotting single notes and a
complex system that covers all the use cases of DSLs.

Of course, this benefit alone could be provided simply by a library, why does
it require its own DSL?  The major benefit of having it be its own language 
is the extra readability and ease of use, since there is no need to learn the
many intricacies of LaTeX, many of which are irrelevant if the only
functionality one is interested in is the ability to typeset music.

A company could clearly experience and improved bottom line, since LilyPond is
free software maintained by the open source community and the clear syntax of
the notes 'c', 'g', and 'a' being represented as `c4 g a` is a certain benefit
for reading and writing.

# Drawbacks
_Identify one potential drawback of the DSL: what does a programmer or company 
lose by using this DSL instead of a general-purpose language?_

It seems as thought the similarity to LaTeX could actually be a drawback in some
situations.  While it might prove helpful for users familiar with LaTeX syntax,
the fact that it is _not_ actually a subset of LaTeX syntax might surprise
some individuals, lured into a false sense of security by the backslash
denoted commands, such as `\clef`.  It might be tempting to throw in a
`\vspace{2pt}` in the code, which will not be recognized as valid by LilyPond.

There may also be the issue that those completely _unfamiliar_ with LaTeX
will also have trouble with the syntax.  `\clef bass` might seem less intuitive
than an assignment, such as `clef <- bass` or `clef:bass`.

