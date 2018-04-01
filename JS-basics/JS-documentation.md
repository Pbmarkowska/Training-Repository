### JS documentation <br>

[link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/A_re-introduction_to_JavaScript)

JS was created in 1995 by Brendan Eich, while he was an enginner at Netscape.

Few facts:
* JavaScript has no concept of input and output, it is designed to run as a scripting language in a host environment (like a browser).
* It's multi-paradigm, dynamic language with types and operators, standard built-in objects, and methods.
* Its syntax is based on Java and C languages.
* It **supports object-oriented programming** with object prototypes, instead of classes.
* It **supports functional programming**: functions are objects giving functions the capacity to hold executable code and be passed around like any other object.

JavaScript programs manipulate values and those values all belong to a type.

Types:

* Number
* String
* Boolean
* Object
  * Function
  * Array
  * Date
  * RegEx
* Symbol
* Undefined
* Null


#### Variables

Variables are declared using one of three keywords:
* **let**: used to declare block-level variables, it is available from the *block* it is enclosed in
* **const**: used to declare variables that are never intended to change, it is available from the *block* it is enclosed in
* **var**: it is available from the *function* it is declared in.

If you declare a variable without assigning any value to it, its type is ``undefined``.

! Blocks do not have a scope; only functions have a scope
