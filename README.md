[Assignment HOWTO]: https://github.com/hmc-cs111-fall2016/hmc-cs111-fall2016.github.io/wiki/Assignment-HOWTO
[Fowler]: https://sakai.claremont.edu/access/content/group/CX_mtg_91991/Fowler_Chapter2.pdf
[markdown]: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
[Pulls]: https://github.com/hmc-cs111-fall2016/what-is-a-DSL/pulls

# What _is_ a DSL?
###### _Submission deadline: Sunday, Sept. 4 at 11:59pm_
###### _Critique deadline: Tuesday, Sept. 6 at 11:59pm_

In this assignment, you'll read an introductory chapter about DSLs, which will 
give us some shared terminology for talking about DSLs and their 
implementations. Then you'll find a DSL "in the wild" and describe its design 
and implementation using terminology from the reading. Finally, you'll write a
program in an interesting DSL: ContextFree.

After this assignment, you should be able to:

- Recognize properties of a DSL and evaluate those properties using common 
terms.
- Write in at least two DSLs (ContextFree and Markdown).
- Use GitHub as a submission system.

## Teamwork
For the technical part of the assignment, you'll work by yourself (though you're
free to talk about the assignment with anyone). For the critique part of the
assignment, you'll pick a partner and review each other's work.

## Read up on the assignment workflow
[This article][Assignment HOWTO] describes how we'll do our assignments on
GitHub. Be sure to read it before you start working on your assignment.

## Read Fowler's introduction to DSLs
Read [Fowler, Chapter 2][Fowler].<sup>1</sup> For the most part, this reading is 
self-contained. In a few places, Fowler references other parts of the book. 
Ignore these references; you can understand the reading without them. It may be 
helpful to know that, in Chapter 1, Fowler described a domain called Miss 
Grant's Controller. You can safely substitute the domain you choose for your DSL 
in place of Miss Grant's Controller. 

_<sup>1</sup> This copy of the reading is for class use only. You should not distribute
 it to anyone outside the class. You should destroy your digital copy when the 
 class is over._

## Find a DSL
Find a DSL—one that you think most other people in the class *won’t* know. 
When picking a DSL, it's good to find one for which you can find a few 
example programs, so you can get a good sense of it. Sometimes it's hard to be 
sure whether or not a language is actually a DSL. That's okay! If you find a 
language that you think *might* be a DSL, but you're not sure, then go with 
it—just assume that it *is* a DSL.

## Describe your DSL
Open the file `my-dsl.md`, read the questions there, and edit the file to
include your answers to those questions. Back up your answers with any evidence 
that you can find about your DSL. Your answers must be formatted in [markdown].
Also, please don't use more than 80 characters per line in your files. It will
make it _much_ easier for people to review your work.

## Learn, use, and critique ContextFree
1. Download ContextFree, a domain-specific language for making art. **You should
download version 2.2**, which is _not_ the current version of the language.
(download: [Windows](http://www.contextfreeart.org/download/ContextFreeInstall2.2.2.exe), 
[Mac](http://www.contextfreeart.org/download/ContextFree2.2.2.dmg),
[Linux](http://www.contextfreeart.org/download/ContextFreeSource2.2.2.tgz)).
_Note: the Mac version is also installed on the CS lab Macs._ The version 2.2
documentation is 
[here](https://github.com/MtnViewJohn/context-free/wiki/Version-2-Syntax).

2. Write an interesting ContextFree program. Save your program in a file called
`firstname_lastname.cfdg` (where you fill in your first and last names, of
course).

3. Export a nice image from your program. (Choose the `Render` menu, then `Save
Image...`) Use a `.png` extension, so your filename should be `
firstname_lastname_variant.png` (where `variant` is the three-letter variant the
uniquely identifies this version of your program).

4. Answer the questions in `context-free.md`.

## Identify your peer-review partner(s)
Your name is on the left side of this table; the person whose work you should
review is on the right side of this table:

| You...      | Should critique...          |
| ----------- | --------------------------- |
| Anna C.     | Justin C.                   |
| Anthony R.  | Linnea N.                   |
| Daniel S.   | Matt B.                     |
| Daniel Z.   | Michael S.                  |
| Farhan A.   | Renata P.                   |
| Jeb B.      | Ross W.                     |
| Jon L.      | Sophia S.                   |
| Julien C.   | Tiffany F.                  |
| Justin C.   | Wokky P.                    |
| Linnea N.   | Anna C.                     |
| Matt B.     | Anthony R.                  |
| Michael S.  | Daniel S.                   |
| Renata P.   | Daniel Z.                   |
| Ross W.     | Farhan A.                   |
| Sophia S.   | Jeb B.                      |
| Tiffany F.  | Jon L.                      |
| Wokky P.    | Julien C.                   |

## Peer-review your partner's work
Once your partner has submitted, you can comment on their work. You should find
their work linked on the [pull request page][Pulls]. Provide feedback on all
aspects of your partner's work, including the information in `my-dsl.md`,
`context-free.md`, their code, and their image. Here are some questions you
might consider / answer when providing feedback:

- Would you answer a question from the assignment differently than your partner
did? For example, do you agree with how your partner described the DSL-ness of
their language?
- Did your partner describe anything that you also experienced? For example, did
you try to do something in ContextFree that was difficult?
- If your partner has raised a question in `my-dsl.md` or `context-free.md`,
try to answer it!
- Did you learn any cool language features (from ContextFree or Markdown) that
might add to your partner's work?

## Grading
Good responses (i.e., responses that receive a 3 out of 4) will:

   + fully respond to every prompt in the starter file, _and_
   + be well-written and easy to read, i.e., clear yet concise using good 
   spelling, grammar, organization, and proper formatting, to convey a 
   well-formed idea, _and_
   + where appropriate, support your thoughts with references to material from
   the reading or from language documentation.

Great responses (i.e., responses that receive a 4 out of 4) will additionally:

   + be particularly insightful, by using concepts from the reading to classify
   aspects of each DSL in the assignment and / or by disagreeing with the
   classification that Fowler might make and by presenting a strong argument for
   a different classification.

## Tasks

- [ ] Read the [Assignment HOWTO]
- [ ] Read Fowler's [introduction to DSLs][Fowler]
- [ ] Find a DSL
- [ ] Describe your DSL's implementation and semantics in `my-dsl.md`
- [ ] Write a ContextFree program in `firstname_lastname.cfdg`
- [ ] Make and save a nice picture in `firstname_lastname_variant.png`
- [ ] Answer the questions in `context-free.md`
- [ ] Submit your work
- [ ] Comment on your critique partner's work
