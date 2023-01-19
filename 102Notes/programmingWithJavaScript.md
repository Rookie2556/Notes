## MDN Control Flow:

[MDN web docs](https://developer.mozilla.org/en-US/docs/Glossary/Control_flow)

According to Google, Control flow is: 
        In computer science, control flow is the order in which individual statements,
        instructions or function calls of an imperative program are executed or evaluated. 
        The emphasis on explicit control flow distinguishes an imperative programming language 
        from a declarative programming language.
        
It is the order in which a computer completes its' script.
- Usually runs start to end, looping certain areas if specified in the program through a counter system?
- Conditional functions e.g. If forms == Complete, do x, else ask again / highlight error print error.
- Comditional loops, if counter !== 10, loop again!
This concept *isn't exclusive to Java Script*

> if (isEmpty(field)) {
>  promptUser();
> } else {
>  submitForm();
> }

Many programmers have to deal with control structures frequently, it is a core concept of programming through the above.

As part of testing, sometimes programmers may do a control flow diagram, as such emulating the program on paper.
- This proves that either the computer's control structure is flawed.
- Or you have bad understanding of the control structure.

![Control flow diagram](https://media.geeksforgeeks.org/wp-content/uploads/20190515152609/666.jpg)
*Node 6 could be errrrm, a condition to check if all forms have been completed, 7 is the "successfully completed form and 1 
could be "Boohoo, you are crap at fillng forms"*

To emulate this on paper, it is a table stating step 1 through however is needed, and the tester will follow a pseudo diagram
and state what the output should be at every stage. If both the tester and the computer are correct, they should output the same
outputs. If one is incorrect then the program or programmer needs to be fixed!

## Java Script Functions!

### A Js Function is a group of steps in a block to perform a particular task.

**Note to self:** // is for commenting in Js.

> // Function to compute the product of p1 and p2
> function myFunction(p1, p2) {
>  return p1 * p2;
> }

*wherein `function` declares the block as a function, myFunction is declared as the name of the function, p1 and p2
are parameters 1 and 2*, usually functions jobs are to output a value of significance, this is given back in the return and the
code will stop executing.

> function name(parameter1, parameter2, parameter3) {
>   // code to be executed
> }

The myFunction can be called or invoked via an event e.g. buttonPressed, or self invoked. In Python this would be myFunction(), upon further reading - **This is same for JavaScript!** 🍾 👯

| Advantages    | Disadvantages |
| ------------- |:-------------:| 
| Reusability   | Sometimes can be troublesome to create |
| Saves Time    | Only worth if the action will be called more than once |
| Makes Using Buttons feasible | usually conceptually harder to understand during programming | 
| better readability | *Ugh gotta name this function amirite*| 

Functions are **especially** useful for when input/output could differ.

> function toCelsius(fahrenheit) {
>  return (5/9) * (fahrenheit-32);
> }
> document.getElementById("demo").innerHTML = toCelsius(77);

toCelsius is declared as a function, with fahrenheit as a parameter..
return value is fahrenheit converted to celsius (*To be honest I don't really know how to cconvert between the two*)

> function toCelsius(f) {
> return (5/9) * (f-32); }

This is the function in progress when function called..

> document.getElementById("demo").innerHTML = toCelsius;
document.getElementById means for the Js to interact with the HTML, e.g. obtain the result from called demo and that new value is called "toCelsius".

To call toCelsius() means to collect the variable gotten from the function.
to interact with the function toCelsius, one would use "toCelsius(valueToBeConvertedFrom), e.g. let x = toCelsius(15); would produce whatever the conversion is. 

let text = "The Temperature is " + toCelsius(15) + " Celsius"; is a valid way to call and use the return in a single line.

> // code here can NOT use carName
>
> function myFunction() {
>  let carName = "Volvo";
>  // code here CAN use carName
> }
>
> // code here can NOT use carName

*Nested = Local, not nested = Global, any files made from functions are local unless force made otherwise*

## JavaScript Operators

**Assignment is =**
---
**Addition is +**
---
**multiplication is asterisk**

## I want to know more about
- I want to have more practice with "demo").innerHTML = .. type scenarios as I was really testing my confidence and attempted to explain it as simply as I could in attempt to better understand and may not quite understand yet.
