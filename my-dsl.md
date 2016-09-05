# Language
_What is the name of the language? Link the name to its webpage 
(if appropriate)._

AWK, http://www.cs.princeton.edu/~bwk/btl.mirror/

# Domain
_Describe the language's domain in five words._

Text processing and data extraction

# Computational model
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of 
what happens when a program in your DSL runs._

AWK runs on pattern-action pairs, written as `pattern { action }`. The pattern 
is typically an expression, and the action is a series of commands. As an AWK 
script runs, it tries to match each pattern with the data or text it is run 
with. If there are any matches, AWK will run the action that is paired with the 
pattern.

# DSL-ness
_Fowler writes about a spectrum of languages, from general-purpose languages to 
"purely" domain-specific. Where does the DSL you chose fall on this spectrum, 
and why?_ 

AWK was originally designed to process text and manipulate data. Thus, it is 
mostly used in one-liner scripts/programs that do these domain-specific things. 
However, since AWK is Turing-complete, it can be used like a general-
purpose language and has been used to create large AWK programs. 

On the spectrum of languages, it sits between general-purpose and purely domain-
specific languages, leaning towards purely domain-specific. This is because its 
intended use was for text manipulation, and it is most often used in one-liner 
scripts inside larger applications or as part of a programmer's workflow. 
However, as mentioned above, it is Turing-Complete and it is capable of doing 
much more than purely text processing and data extraction, so it can be used as 
a general-purpose language. Fowler argues that languages that are Turing-
complete should not be considered DSLs. However, Fowler also argues that the 
way a language is used also matters. AWK is mostly used to do text processing, 
so it is definitely more on the domain-specific side of things.

# Internal or external?
_Is the language implemented as an internal or external DSL? 
Justify your answer._

It is an external DSL. AWK is usually used as small scripts in larger programs 
that use languages other than AWK. Since Fowler defines external DSLs as 
a language separate from the main language of the application it works with, 
AWK fits the bill.


# Host language
_What language(s) was (were) used to implement the DSL?_

It was written in C.

# Benefits
_Identify one potential benefit of the DSL: how is a programmer's life or a 
company's bottom line made easier by the existence of this language?_

If a programmer is fluent in AWK, some interesting text manipulations or data 
extractions can be very easy. AWK was used widely to put together reports, so 
used in those domains AWK can save the programmer and their company time and 
therefore money. Also, since AWK is widely available on UNIX distributions, 
it saves even more time because people do not need to waste time downloading 
installing software.

# Drawbacks
_Identify one potential drawback of the DSL: what does a programmer or company 
lose by using this DSL instead of a general-purpose language?_

AWK is an old language and largely succeeded by Perl and other scripting 
languages. That is because AWK has a very specialized and different syntax that 
is just not worth the time and effort to learn and memorize. So a potential 
drawback of using the DSL is lack of results from learning and knowing it. If 
a programmer is pretty good with Perl or Python, they can do relatively the 
same things AWK can in relatively the same time. In that case, learning AWK is 
a waste of time in terms of productivity.
