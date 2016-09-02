# Language
_What is the name of the language? Link the name to its webpage
(if appropriate)._

[should.js](https://shouldjs.github.io/)

# Domain
_Describe the language's domain in five words._

Descriptive unit tests for Javascript.

# Computational model
_We don't yet have a great definition of the term "computational model".
For now, try to come up with the clearest, most concise explanation of
what happens when a program in your DSL runs._

The language is an internal, fragmentary language, so its computational model
is inherited from its host language Javascript. This means that when tests which
use should.js run, the should.js code is interpreted as valid Javascript code,
often intermixed with general Javascript, and is fed to the JS interpreter to be
executed.

# DSL-ness
_Fowler writes about a spectrum of languages, from general-purpose languages to
"purely" domain-specific. Where does the DSL you chose fall on this spectrum,
and why?_

should.js is purely domain-specific. Its lack of Turing completeness is the
biggest indicator: the langauge does not have variables, conditionals, or
looping constructs (although all of these may be found interspersed with
should.js code in native Javascript, due to the fragmentary nature of the DSL).

The only thing should.js is useful for is making assertions about code in a
self-documenting way.

# Internal or external?
_Is the language implemented as an internal or external DSL?
Justify your answer._

It is internal: should.js code is valid Javascript.

# Host language
_What language(s) was (were) used to implement the DSL?_

Javascript.

# Benefits
_Identify one potential benefit of the DSL: how is a programmer's life or a
company's bottom line made easier by the existence of this language?_

should.js allows the programmer to write unit tests that not only prove the
correctness of the program, but also document what the correct behavior should
be. This is done in a way that is readable even if the reader does not know
anything about the host language. For example,

```javascript
this.obj.should.have.property('id').which.is.a.Number()
this.obj.should.have.property('path')
```

should be understandable so long as the reader knows what 'id' and 'path' refer
to (that is, the reader is familiar with the domain). This makes the language
useful as a tool for communicating with domain experts, one of the benefits of a
DSL which Fowler mentions in chapter 2.

# Drawbacks
_Identify one potential drawback of the DSL: what does a programmer or company
lose by using this DSL instead of a general-purpose language?_

The biggest drawback of should.js may be, ironically, the same as its biggest
strength. The syntax is very close to natural language. This is what makes the
code so reasonable, but it is also what Fowler warns against on page 42. The
large amount of syntactic sugar needed to make the language read this way can
also make it difficult for the programmer to learn, which could slow down
development and make it difficult to bring in new talent.

For example, as described [here](https://shouldjs.github.io/#assertion-be), the
language includes the syntax `be`, `an`, `of`, `a`, `an`, and more, which all
mean the same thing -- nothing.
