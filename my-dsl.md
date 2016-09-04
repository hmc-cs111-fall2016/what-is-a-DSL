# Language
_What is the name of the language? Link the name to its webpage 
(if appropriate)._

Apache Ant, http://ant.apache.org/

# Domain
_Describe the language's domain in five words._

Automate the application build processes

# Computational model
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of 
what happens when a program in your DSL runs._

Ant Apache is a command-line tool that helps the user build mainly Java applications with ease by automating the processes, providing the user with an interface where they can develop custom tasks. 
The user invokes it from the command line and automates repetitive processes that can be described in terms of targets and tasks. Then, Ant delegates the work to external programs like Java.

# DSL-ness
_Fowler writes about a spectrum of languages, from general-purpose languages to "purely" domain-specific. Where does the DSL you chose fall on this spectrum, 
and why?_ 

Ant, in my view, is closer to being purely domain-specific than general-purpose languages, since it lacks a lot of features and functions that general-purpose languages usually offer, such as the lazy property evaluation in "for" loops. More importantly, Ant's domain is strictly restricted to classic build and test processes. 


# Internal or external?
_Is the language implemented as an internal or external DSL? 
Justify your answer._

Ant is an external DSL, since it has its own custom syntax, but mainly based on the XML's syntax. And it's parsed in the command-line interface, independently of Java, its host general purpose language. 


# Host language
_What language(s) was (were) used to implement the DSL?_

Java

# Benefits
_Identify one potential benefit of the DSL: how is a programmer's life or a 
company's bottom line made easier by the existence of this language?_

Apache Ant is similar to Make, however, it comes with the beneift of 
portability from one platform to the other. Unlike Make, Ant does not require different shell commands for different platforms on which it runs. For example, Make has a Unit-specific command "rm" that is equivalent to "rmdir" in other environments like Microsoft Windows. Ant, on the other hand, lets the user use the same built-in command line "delete" for the same task which is not specific to any one platform. 

# Drawbacks
_Identify one potential drawback of the DSL: what does a programmer or company 
lose by using this DSL instead of a general-purpose language?_

Users who are new to Ant may be confused when treating properties, an essential way to customize a build process. Unlike some general-purpose languages, Ant's properties cannot change once Ant processes the property's name-value pair, and Ant does not even throw an error when the user mistakenly tries to change the value of the properties, allowing properties to be redeclared. In addition, propeties are always global in scope. Treating properties is one of the unusual ways Ant processes, that the user has to keep in mind and get used to. 
