# Context Free

##  Who is this programming language for?

This programming language is for anyone who wants to create images using written instructions.

## What is easy to do in this language? Why is it easy?

It's easy to make recursive, fractal-like patterns! 
It's also very easy to change the location, size, color, hue, angle, 
and saturation of any object. 

The syntax of this language was also straightforward. 
It seems that if the user does not specify a 
location, size, color, hue, angle, or saturation of an object, 
the program knows to set the default. 
Thus, one only has to explicitly state if he/she wants to; 
for example, if one only wants to change the color of an object
from the default color to another color, 
and does not have to explicitly specify keeping other elements the default.

Also, it is nice that writing "s 6 b 0.5" is the same thing as "b 0.5 s 6 b". 
I appreciated this flexibility in specifying the features of an object.

## What is hard to do in this language? Why is it hard?

It was hard to make images that look like letters -- 
maybe there is a shortcut I did not realize, but it was a little annoying to 
have to use lines and arcs to create letters, instead of being able to 
type out the letters themselves.

## How did you learn how to program in this language?

I started by modifying the starter file that was an image of "WELCOME" 
with some vines around it. I changed the location, size, color,
hue, angle, and saturation of certain lines and shapes, and then started adding
repeated elements to each object.

I also looked at the documentation site, through which I learned how to add a background color. 

## What is the underlying _computational model_ for this programming language? 
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of what 
happens when a ContextFree program runs._

I think the program reads the written instructions sequentially, beginning
with the background color, if it is specified, and moving to the startshape, which is 
necessary to specify. 
The program encounters rules, in the order that they are written, and executes all the 
components of that rule before moving onto the next rule.

## What do you think is interesting about the ContextFree program you wrote?

I think it's interesting that I found a way to make the stems of the vine
repeat without explicitly writing and placing each one! 









# Language

_What is the name of the language? Link the name to its webpage 
(if appropriate)._

Hibernate Query Language (HQL). Webpage:  
https://docs.jboss.org/hibernate/orm/3.3/reference/en-US/html/queryhql.html

This link describes Hibernate, which is an object-relational mapping framework 
for the Java language. It provides a framework for mapping an 
object-oriented domain model (HQL) to a relational database (SQL).
http://hibernate.org/


# Domain
_Describe the language's domain in five words._

Persistent objects and their properties.


# Computational model
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of 
what happens when a program in your DSL runs._

HQL queries are translated by Hibernate into conventional SQL queries. 
These SQL queries then perform the action on a database.




# DSL-ness
_Fowler writes about a spectrum of languages, from general-purpose languages to 
"purely" domain-specific. Where does the DSL you chose fall on this spectrum, 
and why?_ 

**I think that HQL falls on the "purely" domain-specific end of the spectrum.**

**HQL definitely fits all the criteria of being a DSL:**

1. Computer Programming Language: 
HQL is a database independent query language executable by a computer.

2. Language Nature: 
HQL has a set of syntax that allows its expressions to be composed together.

3. Limited Expressiveness:  
HQL is a database independent query language that is object-oriented, and HQL
understands notions like inheritance, polymorphism and association. Unlike SQL, 
HQL queries involve class names instead of table names, 
and property names instead of column names.

4. Domain Focus: 
HQL is object-oriented and only operates on persistent objects
and their properties.

Unlike XSLT, I don't think that HQL has any particular usages that would make it a
general-purpose language.

Also unlike XSLT, I do not think that there are other tools 
that people use to create HQL files; 
HQL's representation is a human's main way of interacting with objects 
and their properties. 


# Internal or external?
_Is the language implemented as an internal or external DSL? 
Justify your answer._

I argue that HQL is implemented as an external DSL.

The book says that "an external DSL is a language separate from the main language 
of the application it works in. 
A script in an external DSL will usually be parsed by code in the host application 
using text parsing techniques. Examples of external DSLs... include SQL."

HQL seems to be an absttraction of SQL;
HQL queries are translated/parsed by Hibernate into conventional SQL queries, 
SQL being an external DSL itself.


# Host language
_What language(s) was (were) used to implement the DSL?_

Hibernate is an object-relational mapping framework for the Java language. 
It provides a framework for mapping an object-oriented domain model to a relational database. 
Hibernate solves object-relational impedance mismatch problems by replacing direct, 
persistent database accesses with high-level object handling functions.


# Benefits
_Identify one potential benefit of the DSL: how is a programmer's life or a 
company's bottom line made easier by the existence of this language?_

The following are several benefits:

1. Similar to SQL: HQL’s syntax is very similar to that of standard SQL. 
Familiarity with SQL makes it easy to learn HQL. 

2. Fully object-oriented:
HQL does not use real names of table and columns - 
it uses class and property names instead. 
HQL can understand inheritance, polymorphism and association.

3. Case-insensitive for keywords: 
Like SQL, keywords in HQL are case-insensitive. 
That means SELECT, select or Select are the same.

4. Case-sensitive for Java classes and properties: 
HQL considers case-sensitive names for Java classes 
and their properties, meaning Person and person are two different objects.

5. Aides coding: 
HQL helps users conduct more thorough data analysis, 
reduces development time, and ensures more accurate coding.

6. Hides sensitive data:
Since a class defines only the data it needs to be concerned with, 
when an instance of that class (an object) is run, 
the code will not be able to accidentally access other program data. 
This characteristic of data hiding provides greater system security 
and avoids unintentional data corruption.

7. Can be understood by people who cannot code in other languages:
Anyone can quickly learn to write in HQL, 
which is a helpful abstraction of SQL and general database manipulation,
instead of having to learning a more complex and low-level general-purpose language.

8. Simplifies details of database management that one might not need to know:
Database management is complicated, and has been considerably simplified 
by the SQL programming language. SQL is responsible for querying and editing 
information stored in a certain database management system, and HQL makes it even 
easier to manipulate data in the form of class names and property names. 

# Drawbacks
_Identify one potential drawback of the DSL: what does a programmer or company 
lose by using this DSL instead of a general-purpose language?_

1. If one learns how to code in a general-purpose language, one may better 
understand how exactly information is extracted and used. 


















