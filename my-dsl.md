# Language
_What is the name of the language? Link the name to its webpage 
(if appropriate)._

[Exhibit](http://www.simile-widgets.org/exhibit3)

# Domain
_Describe the language's domain in five words._

Data-driven, interactive web pages

# Computational model
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of 
what happens when a program in your DSL runs._

An Exhibit program is an HTML page that loads the Exhibit library and specifies
one or more data sources. The HTML page describes, in a declarative way, 
how to display the elements of the data. The Exhibit library takes the HTML page
and data source(s) as input and essentially compiles a new HTML page that lays
out the data visualization and iteractive elements described by the input.

# DSL-ness
_Fowler writes about a spectrum of languages, from general-purpose languages to 
"purely" domain-specific. Where does the DSL you chose fall on this spectrum, 
and why?_ 

It's what I'd call a "practical" domain-specific language. Exhibit has some 
general-purpose language constructs, such as looping and conditionals. Because
it is an internal language, it provides users with an "escape hatch": a user can
always write raw HTML, JavaScript, or CSS to augment the program. Overall, I
think it strikes a very nice balance as a DSL.

# Internal or external?
_Is the language implemented as an internal or external DSL? 
Justify your answer._

This one is harder to classify than I thought! 

On the one hand, Exhibit is an internal language whose host language is HTML: to
specify the visualizations, users write HTML elements with special attributes;
to specify the data, users write a form of JSON (an internal JavaScript DSL).

On the other hand, Exhibit is implemented in JavaScript, which relies on a
parser to pull the attributes out of the HTML and which rewrites that HTML à la
a compiler.

But I'm happy classifying Exhibit as an internal language, where the host
language is HTML+JavaScript(+CSS).

# Host language
_What language(s) was (were) used to implement the DSL?_

HTML+JavaScript(+CSS)

# Benefits
_Identify one potential benefit of the DSL: how is a programmer's life or a 
company's bottom line made easier by the existence of this language?_

It's easy to get some rich visualizations up and running quickly. It's also easy
to create multiple visualizations of the same data.

# Drawbacks
_Identify one potential drawback of the DSL: what does a programmer or company 
lose by using this DSL instead of a general-purpose language?_

(*Note: It's been a little while since I used Exhibit. The current version may 
have addressed some of these drawbacks.*)

I've found it hard to filter data, mostly because there seem to be lots of
hidden features that the documentation doesn't talk about (I had to suss them
out from examples I found on the web.)

The language doesn't make it easy to add new visualizations. If I wanted to
graph some data, that'd be difficult.
