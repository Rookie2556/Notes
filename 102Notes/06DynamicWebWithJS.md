# Dynamic web pages with JavaScript!

[JavaScript MDN web docs very good for revising](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

Note - Java script and java are comlpetely unrelated 😥

## Intro to JavaScript

JS is a lightweight compiled in real time programming language with *first class functions*

first class functions is, according to google:

> First-class function
> In computer science, a programming language is said to have first-class functions if it treats functions as first-class citizens.

According to Reddit's "Explain like I'm 5": >It's like a toy box where you have different types of toys, like cars, dolls, and balls. You can put a toy in a box, take it out of the box, give it to your friend, and put it back in the box.
> Functions are like toys, you can store them in variables, take them out, and use them when you need them.

> In most popular programming languages like JavaScript, Python, and Ruby, functions are first-class citizens, which means they can be treated like any other data type.

Java Script is the highest level programming language we've encountered so far in this course, and so it is **Not** markdown/markup
It is ``real`` dynamic code!

JavaScript can be used to make API's to interact with other software or websites, *API stands for Application Programming Interface * and usually is used in automation of sorts.* I have plenty of API experience with python and Java 🙂

ref [https://developer.mozilla.org/en-US/docs/Web/JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript) for any assistance during Java script programming. I have experience programming and so think I would be okay to read while I program.

## Introduction to JavaScript - basic output

> Plain JavaScript guide
Once upon a time in ye Olde days, the browser would run the JavaScript client side - e.g. reliant on the users' device - however in modern days, the JavaScript is also kept on the server now.

Runtime evironment -- small operating systems with the required functionality, RTE for short.
- a popular rte is Node.js, I've seen this around..
- another one is io.js, never seen before 😟 deprived from node.js though so 🙂
  - The Language itself is a major part of JavaScript
  - DOM API, *according to Google* > Document Object Model
                                   > The Document Object Model (DOM) is an application programming interface (API) for HTML                                    > and XML documents.
   e.g. like css, used to modify other files...
   - Server API, interaction with other software and programs or server side actions.

Any editor can be used, however for simplicity - it is best to stick to a IDE such as VS code **totally not biased**

Like CSS, they can be External Internal or inline - only they are referred to as ``Embedded`` e.g. Internal/inline or ``Include`` e.g. external where a line in the HTML refers to the js file for documentation. 

A basic script would look like:

        <script language="javascript">
 
        alert("Hello World");
 
        </script>

This creates a file, in JavaScript that will show a popup saying *"Hello World"*!

        First line
        <script>
 
        document.write("<h1>Hello World</h1>");
 
        </script>
        Last line

The content "First line", "Last line" are **not** Js, this is `Embedded` JavaScript. 

        document.write("<h1>Hello World</h1>")

The above is the JavaScript coding, within the file it writes > <h1> Hello World </h1> which in a html file would write a header "Hello World"

        <script>
 
        console.log("Hello World");
 
        </script>

The above would ensure a debugging window to be made, this window is invisible and most browsers have this feature. Where errornaeous Js would output errors, to see the errors you could call console.log() . 

## JavaScript input with prompt and confirm

        <script>
 
        var name = prompt("Your name:", "");
        document.write("Hello ", name);
 
        </script>

This Script brings about a popup window asking the user their name, and collects this input and prints "hello [input]" e.g.
if Thomas was input, "Hello Thomas" would be printed, if no name is given, it prints "Hello null".

        <script>
 
        var name = prompt("Please correct your e-mail address:", "foo@bar.co");
        document.write("Your e-mail address is ", name);
 
        </script>

This script is fairly similar, only in place of name it is email address, "Your email address is [input]" returning null or the user's input. 

`var` is the variable, assigned to 'name' 
`Prompt` Is the popup asking for input, ("What the user sees", "What is already filled into the input box");
`document.write` is the print() function.

        <script>
 
        if (confirm("Shall I print Hello World?")) {
            document.write("Hello World");
        } else {
            document.write("OK, I won't print it.");
        }
        </script>
 
 The above is essentially an 'if x true, do y, else if x false, do z" - Confirm returns pop up value given by the user e.g. `okay` or `Cancel` and reacts accordingly.
 
[all scripts from here](https://code-maven.com/javascript-input-with-prompt-and-confirm)

## Java Script Var (Variables)

There are 4 different ways to declare a variable:
+ var
+ let
+ const
+ Nothing

        var x = 5;
        var y = 6;
        var z = x + y;

New Variable named Z is worked out by adding predefined variables x and y (5 + 6) which is 11.
The programmer usually would do a document.write("Variable Z is, " , z); to show the result of the above.

        let x = 5;
        let y = 6;
        let z = x + y;

The above produces the same results.

        x = 5;
        y = 6;
        z = x + y;

The above produces the same results.

> Var was used from 1995 (beginning) until 2015, then let and const came around in 2015. Now all 3 work 😂

*Generally, Const is the best var declaration if it is unlikely to change, let is best var declaration if it is likely to change.*

        const price1 = 5;
        const price2 = 6;
        let total = price1 + price2;

**const** is applied when the value isn't going to change, price1 or price2 won't change, however - Total is likely to change so it is declared as a **let**!

> "Like algebra" - Let x be 5, let x be 6, z is x + y so z is 11
> let x = 5;
> let y = 6;
> let z = x + y;

Like any other programming language (Not markdown or up), Variables need **unique identifiers so they are uniquely** named.

> The general rules for constructing names for variables (unique identifiers) are:

> Names can contain letters, digits, underscores, and dollar signs.
> Names must begin with a letter.
> Names can also begin with $ and _ (but we will not use it in this tutorial).
> Names are case sensitive (y and Y are different variables).
> Reserved words (like JavaScript keywords) cannot be used as names.

**JS is CaSeSeNsiTivE**

## Assignment operator: (=)

*Like most programming languages, = is given the assignment operator*
> x = x + 5
would mean that x's new value is increased by 5 per time this is looped, unless it is predefined previously in the program.

> x == y
would mean that x is equal to y/

## Data Types!

>Const pi = 3.14;
>let person = "John Doe";
>let answer = 'Yes I am!';

*This is important, as treating variables as the incorrect data type will most likely have an effect on your code,  as such a number being treated as a string, e.g.

> const pi = "3.14"
> const pieces_Of_Pie = 10;
> let Total = pi + pieces_Of_Pie
Would produce 3.1410 as the code sees them as strings, as they are *Letters* (kinda).. If one data type being used **is** in speechmarks, the rest is treated as a string as well!

When the intended result was 13.14 as a number - avoidable if speechmarks weren't used.
Another example is the usage of addition between two datatypes usually won't work, the code may ask you to convert one of the two data types.

# Creating a variable:

To create a variable one would use "var VroomVroomName;" or "let VroomVroomName;", then assign it a value e.g. VroomVroomName = "Volvo"; **This is usually done as one line, " let VroomVroomName = "Volvo"; " It is good practice to declare all variables at the start of the program.

One could declare *Multiple* variables in a single line as such:

> let person = "Ronald macdonald", Resaurant = "Macdonalds", price = 0.99;
The above has 3 variables ready for use, admitedly I don't think they have much use so more variables would be needed..

* if var AFTER defined previously, it doesn't lose its' value.* but let or const will not work.

> let x = 10 + 2 + 14;
The above would work as 10 2 and 14 don't need to be declared result is 26, same goes for strings:
> let unknown_Person = "John" + " " + "Doe";
The above would work as "John" and "Doe" don't need to be declared, the result would be unknown_Person = John Doe.

$ is a valid Js Variable name, I wouldn't use it in other programming languages *to be perfectly honest*..
underscore is another valid Js Variable name, Usually mixed with letters e.g. "_lastName", "full_Name" et cetera..

[This content is from here](https://www.w3schools.com/js/js_variables.asp)!

## I would like to learn more about:

- The Script part, I didn't fully understand what I was reading around this part and would like it explained to me.
- I was not able to run any code personally, so I used the website's "Try me"s to learn coding for the time being, until I am properly introduced to JavaScript.
- > <p id="demo"></p>

  > <script>
  > let carName = "Volvo";
  > document.getElementById("demo").innerHTML = carName;
  > </script>
 **I didn't really understand this.**

