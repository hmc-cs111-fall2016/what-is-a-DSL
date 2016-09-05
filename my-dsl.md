# Language
_What is the name of the language? Link the name to its webpage
 (if appropriate)._
The launchd system. 


# Domain
_Describe the language's domain in five words._
Managing processes/scripts for OSX.


# Computational model
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of 
what happens when a program in your DSL runs._
On startup, launchd reads property lists files in certain directories. Then
depending on the property list (`plist`), the process is run at the specified
intervals or otherwise stopped or managed.


# DSL-ness
_Fowler writes about a spectrum of languages, from general-purpose languages to 
"purely" domain-specific. Where does the DSL you chose fall on this spectrum, 
and why?_ 
launchd is "purely" domain-specifice. A launchd property list has less than
20 possible properties. I don't think you can set variables in these `plist`s.
In terms of use, people only use it to manage processes and scripts written
in other languages.


# Internal or external?
_Is the language implemented as an internal or external DSL? 
Justify your answer._
It is an external DSL. The main language that it works with are usually the
bash commands that it runs. It uses another language's syntax (XML) to make the 
`plist`s.


# Host language
_What language(s) was (were) used to implement the DSL?_
The open source [version]
(http://opensource.apple.com/source/launchd/launchd-842.92.1/) Apple provides 
is implemented in C.


# Benefits
_Identify one potential benefit of the DSL: how is a programmer's life or a 
company's bottom line made easier by the existence of this language?_
launchd was designed to replace a number of ways to manage daemons, such as
init and crontab. Instead of using multiple tools to handle different facets
of management, a programmer can now use launchd.


# Drawbacks
_Identify one potential drawback of the DSL: what does a programmer or company 
lose by using this DSL instead of a general-purpose language?_
Since launchd does not store variables, it would be difficult to manage 
recurring processes which takes different arguments each time. One could
handle storing variables in bash as part of the commands it runs, but then
that is handled by bash not launchd.
