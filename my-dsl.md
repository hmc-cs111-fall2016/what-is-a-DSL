# Language
_What is the name of the language? Link the name to its webpage 
(if appropriate)._

[Selenium Commands - "Selenese"](http://www.seleniumhq.org/docs/02_selenium_ide.jsp#selenium-commands-selenese)

# Domain
_Describe the language's domain in five words._

Automated tests for browser-based applications.

# Computational model
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of 
what happens when a program in your DSL runs._

I assume that each Selenese command is mapped to some equivalent code in another 
language.  For example, `open /downloads/` could be some shell command to open the 
browser and navigate to that URL). So the commands are parsed and the
matching code is run with the parameters entered.  Especially because the
testing is done for applications in the browser, each Selenese command could be
mapped to some Javascript code that is run when the Selenese command is invoked.

# DSL-ness
_Fowler writes about a spectrum of languages, from general-purpose languages to 
"purely" domain-specific. Where does the DSL you chose fall on this spectrum, 
and why?_ 

Selenese is purely domain-specific.  It works only in the Selenium-IDE, which
could be categorized as a langauge workbench. The domain focus is very sharply 
defined: it is used purely for running Selenium tests, with no features 
for wider use. As a result, it is also extremely limited in its expressiveness,
with a defined set of commands and a very specific syntax.

# Internal or external?
_Is the language implemented as an internal or external DSL? 
Justify your answer._

Selenese is an external language. It has its own (limited) syntax of one command
with two parameters for each operation. Perhaps most importantly, it does not
use and is not integrated with a general-purpose, host language.   

# Host language
_What language(s) was (were) used to implement the DSL?_

Java

# Benefits
_Identify one potential benefit of the DSL: how is a programmer's life or a 
company's bottom line made easier by the existence of this language?_

Selenese is extremely simple: each operation is written as the command name
followed by two parameters.  For example, you can open a page, verify you're on
the correct page, and verify text on the page exists by using these three 
commands (this is an [example from the Selenium docs](http://www.seleniumhq.org/docs/02_selenium_ide.jsp#assertion-or-verification):  
```
open /downloads/
assertTitle Downloads
VerifyText //h2 Downloads 
```
Any member of a company could write scripts to test a web app using the Selenium
IDE and Selenese commands because it is extremely human readable. 

# Drawbacks
_Identify one potential drawback of the DSL: what does a programmer or company 
lose by using this DSL instead of a general-purpose language?_

Selenese requires using the Selenium-IDE which is not ideal.  It is probably 
nicer to have the tests written in a general-use programming language rather than having to run them in an IDE.  Selenium has dealt with this by creating Selenium
WebDriver, which allows you to run Selenium tests in your code by using the 
general-purpose host language of your project and interacting through a 
simple API.    
