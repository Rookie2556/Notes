# Problem domain, objects and the DOM

## Javascript object basics

JavaScript objects are a collection of related data and/or functionality, consisting of several variables and functions 
called properties and methods. To create an object, we define and initialize a variable with the object literal syntax. 
An object is made up of members with names and values, separated by a colon, and each name/value pair is separated by a comma.

To access an object's properties and methods, we use dot notation, where the object name acts as the namespace and is followed
by a dot, then the item we want to access. An object property can also be an object, and to access these items, we just chain
the extra step onto the end with another dot.

An object literal is very common when we want to transfer a series of structured, related data items in some manner,
for example, sending a request to the server to be put into a database. Sending a single object is much more efficient than
sending several items individually, and it is easier to work with than an array when you want to identify individual items
by name.

An object's members can be pretty much anything, and the value of an object member can be an array, number, or functions 
that allow the object to do something with that data. Functions can be written in a simpler syntax. Instead of bio: function 
(), we can write bio(). An object like this is referred to as an object literal. It is different from objects instantiated 
from classes, which will be looked at later on.

``` Code for Objects is as follows:
        const Object = {
            colour: ["Red", "blue", "Green"],
            shape: ["Circle", "Sphere", "Square"],
            whatAmI: function () {
              console.log(`${this.shape[0]} ${this.shape[1]} is ${this.colour} Colour.`);
                 },
            introduceSelf: function () {
            console.log(`Hi! I'm ${this.colour[0]}.`);
            },};
           
        object.colour;
        object.shape; ``` 
        
 ``` To interact with this: 
      object.colour;
      object.colour[2];
      object.introduceSelf(); ``` 
      
      
### Questions:

### How would you describe an object to a non-technical friend you grew up with?
An object is more so of a container, it contains information in form of properties and such that define the object.
### What are some advantages to creating object literals?
Easy organisation, and easier to interact/ easily put into arguments and functions/ get values returned.
### How do objects differ from arrays?
An object uses a key system, an array uses linear, objects can store any data type and represent real world entities usually,
arrays are accessed using an index, (so are objects).
### Give an example for when you would need to use bracket notation to access an object’s property instead of dot notation.
Where the name of a property contains a space or number as first character.
### Evaluate the code below. What does the term this refer to and what is the advantage to using this?
``` const dog = {
  name: 'Spot',
  age: 2,
  color: 'white with black spots',
  humanAge: function (){
    console.log(`${this.name} is ${this.age*7} in human years`);
  }
} ``` 
It refers to an object, which is a dog, whose properties are its name, age colour and a function to calculate its age equal to
human age.
It can be extended to include more than one dog fairly easily.

## DOM

The Document Object Model (DOM) is a programming interface for web documents that represents the web page so that programs 
can change the document structure, style, and content. The DOM is built using multiple APIs that work together, with the 
core DOM defining the entities describing any document and the objects within it. The HTML DOM API adds support for 
representing HTML documents to the core DOM, while the SVG API adds support for representing SVG documents.

The DOM is not a programming language, but it provides an object-oriented representation of the web page that can be 
modified with a scripting language such as JavaScript. The DOM is not part of the JavaScript language but is instead a 
Web API used to build websites. Even though most web developers will only use the DOM through JavaScript, implementations 
of the DOM can be built for any language.

To access the DOM, you can use the API directly in JavaScript from within a script. You can immediately begin using the API
for the document or window objects to manipulate the document itself or any of the various elements in the web page.

The DOM defines entities as nodes and objects that are organized into objects for manipulating and creating web pages. 
Fundamental data types in the DOM include Document, which represents the root document object itself; elements, which 
represent the various elements in the web page; and attributes, which represent the various attributes of an element.

``` <!DOCTYPE html>
<html>
  <head>
    <title>To-Do List</title>
  </head>
  <body>
    <h1>To-Do List</h1>
    <form id="add-task-form">
      <input type="text" id="task-input" placeholder="Enter task">
      <button type="submit">Add</button>
    </form>
    <ul id="task-list"></ul>

    <script>
      // Get references to the form, input and list elements
      const form = document.getElementById('add-task-form');
      const input = document.getElementById('task-input');
      const list = document.getElementById('task-list');

      // Add a new task to the list
      const addTask = (event) => {
        // Prevent the default form submission behavior
        event.preventDefault();

        // Create a new list item element
        const li = document.createElement('li');

        // Set the text of the list item to the value of the input
        li.textContent = input.value;

        // Add the list item to the list
        list.appendChild(li);

        // Reset the input value
        input.value = '';
      };

      // Attach the addTask function to the form's submit event
      form.addEventListener('submit', addTask);
    </script>
  </body>
</html>
```

## Questions:

What is the DOM?
Document Object model, a form of an api to change the website as you use it.
Briefly describe the relationship between the DOM and JavaScript.
When a web page is loaded in a browser, the browser creates a Document Object Model (DOM) for that page, which represents 
the structure of the document as a tree-like structure of nodes. Each element, attribute, and text node in the HTML is 
represented as a node in the DOM.

JavaScript can be used to access and manipulate the DOM.

        
