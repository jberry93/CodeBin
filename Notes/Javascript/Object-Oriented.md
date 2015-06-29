### Scope
So what does this word **scope** mean? [Scope refers to the visibility of variables](http://www.cs.cf.ac.uk/Dave/PERL/node52.html). Scoping allows complete control over the use of variables. Global scope allows access to all variables even across different Javascript files

### Lexical Scope
A lexical scope (or static scope) defines the functionality of variables within the block of code it is defined in. The variables defined in this scope are called private variables ([reference](http://whatis.techtarget.com/definition/lexical-scoping-static-scoping)) 

Example of lexical and global scope:

```Javascript
var pugs = pugSnort();
var meh = function example(){
	var dogs = dogBark();

	/*The variables stored here are 
	considered private variables*/


};


/*Any variables declared outside of
the function enters the global scope*/


```

Question: Which of these variables would be available from within the body of the `example` function?

Answer: All 3 declared variables are accessible within the `example` function

Take note that curly braces from a function statement will create a new scope. Curly braces from a for loop or if statement do not create a new scope!

Also if we were to remove `var` from `var dogs = dogBark();`, `dog` would become a global variable. This may confuse other programmers trying to read your code so it is not good practice to leave out `var`

### Execution Contexts
An execution context is like the environment in which a function is executed in. It begins with the global execution context and stacks up as we introduce more functions

Example:

```Javascript
//global execution context out here

function dream(){
	//another execution context

	function dominickCobb(){
		//another execution context

		function inception(){
			//another execution context
		}
	}

	function malCobb(){
		//another execution context

		function mindF(){
			//another execution context
		}
	}
}
```