
## JS
* ### Error Handling & Debugging
**The JavaScript interpreter uses the concept of execution contexts. There is one global execution context; plus, each function creates a new new execution context. They correspond to variable scope.**

* * _EXECUTION CONTEXT & HOISTING_

Each time a script enters a new execution context, there are two phases of activity:

1: PREPARE

â€¢ The new scope is created

â€¢ Variables, functions, and arguments are created

â€¢ The value of the this keyword is determined

2: EXECUTE

â€¢ Now it can assign values to variables

â€¢ Reference functions and run their code

â€¢ Execute statements

* * _UNDERSTANDING SCOPE_
 
**In the interpreter, each execution context has its own va ri ables object. It holds the variables, functions, and parameters available within it. Each execution context can also access its parent's v a ri ables object.**

If a variable is not found in the variables object for the current execution context, it can look in the `variables` object of the parent execution context. But it is worth knowing that looking further up the stack can affect performance, so ideally you create variables inside the `functions` that use them. If you look at the example on the left, the inner functions can access the outer functions and their variables. For example, the `greetUser()` function can access the time variable that was declared in the outer `greeting()` function. Each time a function is called, it gets its own execution context and va r i ables object. Each time an outer function calls an inner function, the inner function can have a new variables object. But variables in the outer function remain the same. Note: you cannot access this variables object from your code; it is something the interpreter is creating and using behind the scenes. But understanding what goes on helps you understand scope.

* * _UNDERSTANDING ERRORS_

If a JavaScript statement generates an error, then it throws an **exception**. At that point, the interpreter stops and looks for exception-handl ing code.

If you are anticipating that something in your code may cause an error, you can use a set of statements to handle the error (you meet them on p480). This is important because if the error is not handled, the script will just stop processing and the user will not know why. So exception-handling code should inform users when there is a problem.

Whenever the interpreter comes across an error, it will look for error-handling code. In the diagram below, the code has the same structure as the code you saw in the diagrams at the start of the chapter. The statement at step 1 uses the function in step 2, which in turn uses the function in step 3. Imagine that there has been an error at step 3.

* *  _ERROR OBJECTS_

**Error objects can help you find where your mistakes are and browsers have tools to help you read them.**

* *  _HOW TO DEAL WITH ERRORS_

1: DEBUG THE SCRIPT TO FIX ERRORS If you come across an error while writing a script (or when someone reports a bug), you will need to debug the code, track down the source of the error, and fix it.

2: HANDLE ERRORS GRACEFULLY You can handle errors gracefully using try, catch, throw, and f i na 1 ly statements.