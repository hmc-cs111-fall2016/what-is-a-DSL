# Language
_What is the name of the language? Link the name to its webpage
(if appropriate)._

[Dockerfile Command Language](https://docs.docker.com/engine/reference/builder/)

# Domain
_Describe the language's domain in five words._

Efficient portable software runtime environments.

# Computational model
_We don't yet have a great definition of the term "computational model".
For now, try to come up with the clearest, most concise explanation of
what happens when a program in your DSL runs._

A user describes the overall build of a container&mdash;a sort of lightweight
virtual appliance&mdash;in a text file called a Dockerfile with limited text
commands. When a user builds an image from the Dockerfile, the text commands are
parsed and with each step a partial container is built representing the state of
the machine&mdash;the Docker commands are converted to lower-level system
commands as needed. After the final command, the user can use the built machine
just as they would a virtual appliance without worrying about the intermediate
steps. If the Dockerfile is edited, the image builder will find the modified
line, and only rebuild and commit images that came from commands with and after
that line.

# DSL-ness
_Fowler writes about a spectrum of languages, from general-purpose languages to
"purely" domain-specific. Where does the DSL you chose fall on this spectrum,
and why?_

The Dockerfile Command Langauge is "purely" domain-specific. It serves one
purpose: to describe and build reproducible Docker containers/images. While it
looks a bit like a scripting language, the commands are extremely limited for
the purposes of readability, reproducibility, and commitability. The langauge
itself is certainly not Turing-complete&mdash;Fowler's litmus test for generic
DSLs.

While I definitely think the Dockerfile's commands are a DSL&mdash;the
documentation even goes as far as refering to it as a DSL&mdash;it verges on the
line of simply being a configuration file which Fowler would likely not count
as a DSL. The reason I'd argue it is not simply a configuration file is there
needs to be a logical ordering of steps that are user determined.

# Internal or external?
_Is the language implemented as an internal or external DSL?
Justify your answer._

The Dockerfile Command Language is an **external** DSL since it does not make
use (and cannot be used) in a more generic langauge. The Dockerfile must be
parsed and turned into another language/code. (Lucky for us all of this parsing
business is open source!)

# Host language
_What language(s) was (were) used to implement the DSL?_

Looking through the [source code](https://github.com/docker/docker) of the
whole Docker infrastructure, the parser and builder are written in Golang (and
some supporting C) which are used to essentially take the English  text commands
in the Dockerfile and turn them into the lower-level commands to eventually
build a final container. Docker commands wrap system commands and logical build
steps under more general, limited commands.

# Benefits
_Identify one potential benefit of the DSL: how is a programmer's life or a
company's bottom line made easier by the existence of this language?_

Since the Dockerfile Command Language includes a limited set of build commands,
it makes the overall configuration and process of the final image easier to
decipher. A developer is forced to compartmentalize the machines build steps
into Docker commands.

If you go onto the [Dockerhub](https://hub.docker.com/) you can view other
peoples Dockerfiles. Reading through them, it is pretty easy to get a general
sense of the goals of building each image.

# Drawbacks
_Identify one potential drawback of the DSL: what does a programmer or company
lose by using this DSL instead of a general-purpose language?_

Dockerfile's do not allow custom commands&mdash;instead people will have a
simple Docker command call to a complex script making it a bit of a scavenger
hunt to find what exactly is happening from the top-level. It would be nice if a
user could add custom commands to encapsulate common actions.

For example, let's say I want to have a part of my build that is functionally
used to seed data (a common occurrence when building images). Instead of writing

```
RUN './seed-script'
```

it would be nice to write

```
SEED data destination
```

which has a more human-friendly style to it.

> Although I make the suggestion that Docker adds custom commands, it could
> have the potential to make the Dockerfile Command Langauge too generic and
> bash-like which Fowler would likely say is a bad thing for something that
> claims to be a DSL.
