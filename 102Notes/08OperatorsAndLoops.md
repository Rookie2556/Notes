# Operators and Loops

## Expressions and Operators

### Comparison operators

*According to google, comparison operators are: *

> Comparison operators
? Returns true if the operands are equal and of the same type. See also Object.is and sameness in JS. Returns true if the    > operands are of the same type but not equal, or are of different type. Returns true if the left operand is greater than    > the right operand.

Comparison operators are *fairly* straight forward however we need to learn their logic and symbols to use them correcly.

| Operator                    |  Description                                                              |
| ----------------------------| --------------------------------------------------------------------------|
| Equal  (=)                  | If operands equal, returns True                                           |
| Not Equal (!=)              | If operands not equal, returns True                                       |
| Strict equal (==)           | If operands are of the same data type e.g. int and equal, returns True    |
| Strict not equal (!==)      | If operands are of the same data type e.g. str and equal, returns True    |
| Greater than (>)            | If left operands is of greater value than the right, returns True         |
| greater than or equal (>=)  | If left operands is of greater value or equal to the right, returns True  |
| Less than (<>               | If left operands is of lesser value than the right, returns True          |
| Less than or equal (>=)     | If left operands is of lesser value or equal to the right, returns True   |

### Assignment operators

*According to google, comparison operators are: *

> Assignment operators. An assignment operator assigns a value to its left operand based on the value of its right operand.  > The simple assignment operator is equal ( = ), which assigns the value of its right operand to its left operand. That is, x > = f() is an assignment expression that assigns the value of f() to x .

Assignment operators is where values are assigned to variables under Const, var or let. Through classes they have stated that the usage of var is redundant as it can cause uneccessary errors in our code, so const and let are the defacto since 2015.

An object is a class of sorts, that can have properties assigned to oneself, e.g. interactive in some sense through methods consisting of its' properties.

* so we can interact with this new class we made * 

**Java script is an object orientated programming language** and so we can expect to use objects quite often! 

``` 
const Plane = {};
    Plane.speed = 100;
    
    console.log(Plane.speed); //Prints 100
    console.log(Plane); //Prints { Speed : 100 } and would list all the properties given to it
    
const colour = "colour ";
Plane[colour] = "yellow";
    
    console.log(Plane[colour]); // Prints Yellow.
    console.log(Plane); //Prints all info we know about Plane, so: { Speed: 100, colour: Yellow}.
  
-------------------------------------------------------------------------------------------------------

const val = 0; 

this is not considered an object as it itself has a value , and so any properties assigned wouldn't stick.

const val = {}
val.x = 3;
val.itself = 0;

console.log(val.x); // prints 3
console.log(val.itself); // prints 0

Had I left it as a non-object, it would produce errors like follows:

const val = 0; 
val.x = 3;

console.log(val.x); // Prints undefined
console.log(val); // Prints 0

```

Objects can prove to be quite useful in programming, some examples are:
+  Summarises problems into smaller parts
+  Like functions, their properties are reusable, editable etc
+  Can help make properties relationships (e.g. object relationships)

Examples of the above being:

- - Car has 3 chunks of code about itself: Speed, colour and name - each property has easy approachability.
- - In a car game, it may be useful to be able to edit values such as ** when engine v2 installed, speed value increases **
- - The name value could be a child of a car brand, e.g. Ford object could be it's parent and use inheritance to gain some of its' properties etc.
- - additionally, the usage of automated constructors to inherit properties is a popular usage of objects. 

e.g. 

```
function Car(maxSpeed, Colour, Name) {
  this.maxSpeed = maxSpeed;
  this.Colour = Colour;
  this.Name = Name;
  }

Makes it much easier to make new objects based along the same properties:

let LightningMcQueen = new Car("200, "Red", "McQueen"); //In Cars 2 He uses the machine that measures his speed
let ChichksHicks = new Car("180, "Green", "Hicks"); //He isn't in cars 2, however mcqueen became faster so my assumption is 
//hicks is slower. No clue actually but irrelevant lol :")

```

## Loops and iteration

*according to google, Loops are:*
> Loops are used in JavaScript to perform repeated tasks based on a condition. Conditions typically return true or false . > A loop will continue running until the defined condition returns false.

In my own definition, Loops is a more efficient manner of repeating the same actions over and over but would go forever unless a condition was set, e.g. the goal was reached. In JavaScript, endless repeating could crash the system, in python not necessarily but could.

### For Loop

A for loop in python would be fomatted as:
[i = 0, For i in range (0 to X), do ACTION then i = i + 1,] (**pseudocode style**)
so a for loop has an initial value of i, typically 0 or counting backwards.. a set amount of loops wanted to be completed (X) and what it does per loop, then increases the counter (i) up to keep track of however loops have been done.

JavaScript does it differently, the format is now:
for ([Initial value of i]; [comparison to X until True], [i change] {
  [ACTION];
}
so a for loop has an initial value of i, typically 0 or counting backwards.. a comparison of i against x to achieve set amount of loops, change to i made then the action per loop.

For loops are great if you know how many loops are required, a set amount that won't change.

### While Loop

While loops are loops where you **don't** specifically know how many loops are needed to reach a goal.

conditionForLoop : False
while conditionforLoop == False
  do action
  if action meets standards: change conditionForLoop to True //if does not, it will start the loop again.

the "False", "True" are interchangable, or other methods such as asking for certain inputs and measuring that input could be interpreted as its' own 'conditionForLoop'.

e.g. 
``` 
while (FaveMovie !== "Cars 2") {
  let FaveMovie = prompt("What is your favourite movie? ")
```

This would keep prompting the user to input a movie they think is a great movie, immediately dismiss them and ask again until their answer is *"Cars 2"* which is One of thousands of popular movies so it is unlikely, furthered by the syntax, they could write _"cars 2"_ _"car 2"_ _"That movie where theres a red car that goes vroom vroom" _ so usually the user should have a good idea of what is needed, and the programmer **(you)** should know what is acceptable, even if your favourite movie is Cars 2.

## Things I want to know more about

- I am curious to learn more about do for while whatever other loops there are
- There was quite alot of content in the MDN web docs we did not cover
- I would love to have more constructor practice, as I'd barely touched them previously.
