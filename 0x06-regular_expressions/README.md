###0x06. Regular expression###

RegExp

The RegExp object is used for matching text with a pattern.

For an introduction to regular expressions, read the Regular expressions chapter in the JavaScript guide. For detailed information of regular expression syntax, read the regular expression reference.
Description
Literal notation and constructor

There are two ways to create a RegExp object: a literal notation and a constructor.

    The literal notation takes a pattern between two slashes, followed by optional flags, after the second slash.
    The constructor function takes either a string or a RegExp object as its first parameter and a string of optional flags as its second parameter.

The following three expressions create the same regular expression object:
js

const re = /ab+c/i; // literal notation
// OR
const re = new RegExp("ab+c", "i"); // constructor with string pattern as first argument
// OR
const re = new RegExp(/ab+c/, "i"); // constructor with regular expression literal as first argument

Before regular expressions can be used, they have to be compiled. This process allows them to perform matches more efficiently. More about the process can be found in dotnet docs.

The literal notation results in compilation of the regular expression when the expression is evaluated. On the other hand, the constructor of the RegExp object, new RegExp('ab+c'), results in runtime compilation of the regular expression.

Use a string as the first argument to the RegExp() constructor when you want to build the regular expression from dynamic input.
Flags in constructor

The expression new RegExp(/ab+c/, flags) will create a new RegExp using the source of the first parameter and the flags provided by the second.

When using the constructor function, the normal string escape rules (preceding special characters wit

const re = /\w+/;
// OR
const re = new RegExp("\\w+");
