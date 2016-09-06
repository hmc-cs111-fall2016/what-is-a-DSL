# Language
_What is the name of the language? Link the name to its webpage 
(if appropriate)._

[Mathematica/Wolfram Alpha](http://www.wolfram.com/mathematica/?source=nav)


# Domain
_Describe the language's domain in five words._

To create mathematical figures/expressions

# Computational model
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of 
what happens when a program in your DSL runs._

When a program runs, a text parser sends statements to be evaluated to a mathematical figure/expression engine, which are then displayed on the screen using graphics. 

# DSL-ness
_Fowler writes about a spectrum of languages, from general-purpose languages to 
"purely" domain-specific. Where does the DSL you chose fall on this spectrum, 
and why?_ 

I feel it is closer to a general-purpose language because it is able to run algorithms. For example, Mathematica does have conditional statements and loops; however, they are only useful for numbers and do not work with strings. The presence of conditional statements and loops definitely brings Mathematica close to the general-purpose side of the spectrum. 

# Internal or external?
_Is the language implemented as an internal or external DSL? 
Justify your answer._

It is an external DSL since it has its own program and does not involve any other general-purpose languages to use. You can actually use c/c++ to run Mathematica code (it sends data to the Wolfram server) but that does not make it an internal DSL in my book since Mathematica is not created to be a c/c++ API.

# Host language
_What language(s) was (were) used to implement the DSL?_

According to this [link](http://progopedia.com/implementation/wolfram-mathematica/) Mathematica was implemented in C but is now implemented in Mathematica and C. 

# Benefits
_Identify one potential benefit of the DSL: how is a programmer's life or a 
company's bottom line made easier by the existence of this language?_

Mathematica is super useful to perform lots of calculations fast. It has automatic multi-threading and is optomized to create amazing 2D or 3D plots/figures and to solve algebraic problems. By using Mathematica, a programmers life is easier because they won't have to develop a way to do calculus or make complex figures in a general purpose language.

# Drawbacks
_Identify one potential drawback of the DSL: what does a programmer or company 
lose by using this DSL instead of a general-purpose language?_

One major drawback is that the Wolfram language used is a little strange to learn at first. For example, here is a list of some of the bizarre characters used in Mathematica [source](http://mathematica.stackexchange.com/questions/18393/what-are-the-most-common-pitfalls-awaiting-new-users):

Function application

- `@, [...], //` [ref] -- `f @ x = f[x] = x // f` (Prefix, circumfix and Postfix operators for function application]
- `~` [ref] -- `x ~f~ y = f[x, y]` (Infix; see Join [ref] for a Basic Example.)
- `/@` [ref] -- `f /@ list = Map[f, list]`
- `@@` [ref] -- `f @@ list = Apply[f, list]`
- `@@@` [ref] -- `f @@@ list = Apply[f, list, {1}]`
- `//@` [ref] -- `f //@ expr = MapAll[f, expr]`
- `@*` [ref] -- `f @* g @* h = Composition[f, g, h]` (new in V10)
- `/*` [ref] -- `f /* g /* h = RightComposition[f, g, h]` (new in V10)
- `~~` [ref] -- `s1 ~~ s2 ~~ ... = StringExpression[s1, s2, ...]`
- `<>` [ref] -- `s1 <> s2 <> ... = StringJoin[s1, s2, ...]`
