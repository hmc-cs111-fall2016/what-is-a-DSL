(*Note: I'm adding a second DSL description, of something that
takes a bit more effort to see and describe as a DSL*)

# Language
_What is the name of the language? Link the name to its webpage 
(if appropriate)._

[Melodica](https://itunes.apple.com/us/app/melodica-free/id338223055?mt=8)

_Click below to see a video:_

[![Melodica video](https://img.youtube.com/vi/wVZMaXMNz-0/0.jpg)](https://www.youtube.com/watch?v=wVZMaXMNz-0)

# Domain
_Describe the language's domain in five words._

Compose simple music with ease.

# Computational model
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of 
what happens when a program in your DSL runs._

A user writes program by toggling squares on a grid. Each square is a musical
tone. The higher the square, the higher the tone. When a program runs, it plays
the tones in the first (leftmost) column of the grid, then the second column, 
and so on. When it reaches the end, it loops back around to play the tones from
the beginning.

# DSL-ness
_Fowler writes about a spectrum of languages, from general-purpose languages to 
"purely" domain-specific. Where does the DSL you chose fall on this spectrum, 
and why?_ 

Melodica is purely domain-specific. The domain is music, and the user can
create only music loops. (I suppose it's also possible to draw pictures on the
grid, with no thought about the music; but that would be domain-specific, too).

Programs in Melodica are also purely data. There's no way to create
new kinds of data, and there are no control-flow constructs to choose from.

# Internal or external?
_Is the language implemented as an internal or external DSL? 
Justify your answer._

Melodica is an external DSL. The touch-based interface probably modifies a 
custom data structure, which Melodica interprets as a tone and plays it.

# Host language
_What language(s) was (were) used to implement the DSL?_

I can't find any first-hand information (the developer's 
[website](http://candycaneapps.com/) seems to be defunct), but since it was 
written for an iPhone in 2009, it was probably written in Objective C.

# Benefits
_Identify one potential benefit of the DSL: how is a programmer's life or a 
company's bottom line made easier by the existence of this language?_

Melodica is fun, and it makes it easy to play with and create music.

# Drawbacks
_Identify one potential drawback of the DSL: what does a programmer or company 
lose by using this DSL instead of a general-purpose language?_

Melodica's simplicity is also a shortcoming, if I care about creating more 
complex music. Melodica has fixed number of tones, which limits my 
expressiveness. As a result, it can't grow very well with me, as I get better
at (or bored with) the music I'm making.

(Of course, this is exactly the kind of tradeoff we make in language design:
expressiveness _vs._ ease-of-use. I don't really consider it a drawback to 
Melodica.)
