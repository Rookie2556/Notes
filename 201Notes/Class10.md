# Debugging

## What Went Wrong? Troubleshooting JavaScript.

Types of errors:
- Syntax, spelling mistakes - will be shown in the debugger, e.g. "cricle does not exist".
- Logic, unintended function - won't show an error code, would require understanding of the functions used and won't be as simple
  to fix.

### Questions:

Name some key differences between a Syntax Error and a Logic Error.
  Syntax is the spelling errors, logic is the coding understanding error, syntax outputs an error, logic likely wouldn't but would
  produce an unexpected output.
List a few types of errors that you have encountered in past lab assignments and explain how you were able to correct them.
  Syntax errors - I had to fix spellings quite often as I tend to mistype quite often so I am used to this
  Logic error - For my baking bad website, I had great difficulty getting the tumbleweed to move correctly and spent hours trouble-
  shooting for me to realise that it was the .gif file moving incorrectly rather than the box in which it was contained.
How will this topic continue to influence your long term goals?
  I will encounter many errors throughout my coding career, as comes with programming comes errors, knowing how to deal with 
  such would aid me massively.

## The Javascript debugger:

All browsers have tools to debug HTML CSS and JS, Devtools.

Devtools is usually opened via an inspect element, a hotkey such as F12 and is easily navigated and generally not too simple to
understand but most programmers will understand it in time.

Inspector would show the public information used to display the page to the reader (you) and help understand the functionality.

DOM inspector allows for deleting nodes, editing "as html" et cetera. 

The above help our undersntading of the website and this course as a whole as messing around with the tools provided can 
help fundamental understanding.

JavaScript debugger usually appears as a exclaimation mark, in which clicking will explain any functionality errors, such as incorrectly called,
inability to do a function etc typically, however we can use it to program Javascript with no persistence.

alert("Hey"); would open a dialog window.
document.querySelector("html").style.backgroundColor = "purple"; would change all html attributes to bg = purple.

### Questions:
How would you describe the JavaScript Debugger tool and how it works to someone just starting out in software development?
  Typically used to show errors in the Js files that create the website, however can be used to program temporary features on the
  site with no persistence.
Define what a breakpoint is.
  A breakpoint is a specific area in a code that the dev wants the code to pause execution.
What is the call stack?
  Mechanism used by JS to keep track of currently being executed functions, when executed - it is removed from the call 
  stack. Mainly to manage resources such as memory or other resources. and to check current state of the program.
