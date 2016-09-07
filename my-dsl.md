# Language
_What is the name of the language? Link the name to its webpage 
(if appropriate)._

[JsonDSL](https://github.com/lift/lift/tree/master/framework/lift-base/lift-json) 
(part of the Liftweb framework for Scala)

# Domain
_Describe the language's domain in five words._

Building name/value data structures

# Computational model
_We don't yet have a great definition of the term "computational model". 
For now, try to come up with the clearest, most concise explanation of 
what happens when a program in your DSL runs._

The code with the JSON's information goes through a parser that builds the JSON. 
The program creates key/value pairs or concatenates when it sees parentheses or 
~'s. Within each pair, implicit methods convert typical Scala types (i.e. Int, 
String) into JSON types (i.e. JInt, JString). Finally, we get a JSON object 
containing the name/value pairs.

# DSL-ness
_Fowler writes about a spectrum of languages, from general-purpose languages to 
"purely" domain-specific. Where does the DSL you chose fall on this spectrum, 
and why?_ 

This DSL is purely domain-specific because it has very limited capabilities. 
It can only build JSONS by parsing through information, narrowing the domain 
focus to strictly this data structure. Moreover, it lacks conditions, loops, 
and variables, a common trait of DSLS according to Fowler (page 30).

# Internal or external?
_Is the language implemented as an internal or external DSL? 
Justify your answer._

I spent a lot of time thinking about this question because JsonDSL isn't 
remarkably different from the Scala language, but at the same time, it's not 
valid Scala code without the parsers provided in the library. Maybe it is 
because Scala is so DSL-heavy. 

Though the lines are blurry, I think JsonDSL is external because it relies on 
parsing custom syntax. In addition, on page 30, Fowler states that "an internal 
DSL should have the feel of putting together whole sentences", but JsonDSL 
does not. 

# Host language
_What language(s) was (were) used to implement the DSL?_

Scala was used to implement this DSL.

# Benefits
_Identify one potential benefit of the DSL: how is a programmer's life or a 
company's bottom line made easier by the existence of this language?_

Programmers can build JSONs concisely without explicitly using parse methods or
the specific JSON types (i.e. JInt, JString)

For example, these three code excerpts produce the same JSON.
With JsonDSL:
```
("name" -> "Pikachu") ~ 
("id" -> 25) ~ 
("moves" -> List("Growl", "Spark", "Thunder", "Agility"))
```

Without JsonDSL:
```
parse("""
{
	"name": "Pikachu",
	"id": 25,
	"moves": ["Growl", "Spark", "Thunder", "Agility"]
}
""")
```

Or if you want to be more explicit:
```
JObject(List(
	JField("name", JString("Pikachu")),
	JField("id", JInt(25)),
	JField("moves", JArray(List(
		JString("Growl"),
		JString("Spark"),
		JString("Thunder"),
		JString("Agility")
	)))
))
```

Thus, JsonDSL builds a JSON with the least code. 

# Drawbacks
_Identify one potential drawback of the DSL: what does a programmer or company 
lose by using this DSL instead of a general-purpose language?_

There is little documentation on how to use this DSL (or the Liftweb framework 
in general). In fact, the API for 
[JsonDSL](http://liftweb.net/api/25/api/net/liftweb/json/JsonDSL.html) 
only displays the implicit methods for converting individual values to the 
correct JSON type, so it can be hard to find resources for learning the DSL.
