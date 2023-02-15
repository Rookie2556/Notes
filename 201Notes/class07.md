# Object-oreientated Programming, HTML Tables

## Domain Modelling

Domain modeling involves creating a conceptual model in code for a specific problem. The model describes entities, their 
attributes and behaviors, and constraints that govern the problem domain.

To create objects with the same attributes and behaviors, a constructor function can be used. In JavaScript, 
the new keyword instantiates an object, and the constructor function initializes properties using the this variable.

To model the random nature of user behavior, the JavaScript standard library includes a Math.random() function. Methods can 
be added to a constructor function's prototype, which allows shared code between objects.

To model the popularity of epic fail videos, a daily likes calculation can be made using a random number generator and the 
number of viewers. The formula is the number of viewers times the percentage of viewers who'll like a video.

``` var EpicFailVideo = function(epicRating, hasAnimals) {
  this.epicRating = epicRating;
  this.hasAnimals = hasAnimals;
}

var parkourFail = new EpicFailVideo(7, false);
var corgiFail = new EpicFailVideo(4, true);

console.log(parkourFail);
console.log(corgiFail); 

```

new adds a new property to a property.

### Questions

Explain why we need domain modelin

It is an essential part of the software engineering process, that allows for communication and reduces the risk of errors and
inconsistencies. 

## HTML Table Basics

HTML tables are structured sets of data that can be presented on the web. They allow users to quickly and easily look up 
values that indicate some kind of connection between different types of data. Tables are made up of rows and columns and 
are designed for tabular data, but have been misused by people in the past to layout web pages.

When correctly implemented, HTML tables are handled well by accessibility tools such as screen readers, so a successful 
HTML table should enhance the experience of sighted and visually impaired users alike. HTML tables need some styling 
information with CSS to be effective on the web, as well as good solid structure with HTML. In this module, we focus on 
the HTML part and have provided a minimal CSS stylesheet to make tables more readable.

A table is rigid, and information is easily interpreted by making visual associations between row and column headers. 
The layout of tables should not be confused with table layout techniques. CSS layout techniques are preferable as they are 
more accessible to visually impaired users, produce more straightforward markup structures and are automatically responsive. 
Tables should only be used for tabular data.

Creating a simple HTML table requires adding a table container inside the body of the HTML file. A table cell, created by a
td element, is the smallest container inside a table. For a row of four cells, you need to copy these tags three times. 
Every cell added to the row makes it grow longer. To stop the row from growing and start placing subsequent cells on a 
second row, the tr element is used.

Tags	Description
<table>	Defines the start of a table.
<tr>	Defines a row within a table.
<th>	Defines a header cell in a table.
<td>	Defines a standard cell in a table.
<caption>	Defines a caption for a table.
<thead>	Defines a group of header rows in a table.
<tbody>	Defines the body content of a table.
<tfoot>	Defines a group of footer rows in a table.
<col>	Defines a column within a table.
<colgroup>	Defines a group of one or more columns within a table.
<scope>	Specifies whether a header cell is a header for a column, row, or group of columns or rows.

<table>	Defines a table
<tr>	Defines a table row
<td>	Defines a table cell
<th>	Defines a table header cell
<caption>	Defines a table caption
<thead>	Groups the header content in a table
<tbody>	Groups the body content in a table
<tfoot>	Groups the footer content in a table
<colgroup>	Groups one or more columns in a table for formatting
<col>	Defines a column in a table
<rowspan>	Defines the number of rows a cell should span
<colspan>	Defines the number of columns a cell should span
<scope>	Defines the scope of a header cell
<abbr>	Defines an abbreviation or acronym
<th scope="col">	Defines a header cell in a column
<th scope="row">	Defines a header cell in a row

``` <table>
  <colgroup>
    <col />
    <col style="background-color: yellow" />
  </colgroup>
  <tr>
    <th>Data 1</th>
    <th>Data 2</th>
  </tr>
  <tr>
    <td>Calcutta</td>
    <td>Orange</td>
  </tr>
  <tr>
    <td>Robots</td>
    <td>Jazz</td>
  </tr>
</table> ```

### Questions

Why should tables not be used for page layouts?
They can easily become disorted, and unsuitable for a variety of devices with varying screen sizes, increase load times and 
negatively affect SEO.
List and describe 3 different semantic HTML elements used in an HTML <table>.
<thead>: This element is used to group the header content in a table. It is usually used in combination with <th> elements,
which represent table headers. The <thead> element should be used once in a table and should come before any <tbody> 
or <tfoot> elements.
<tbody>: This element is used to group the main content of a table. It should be used after the <thead> element and before 
the <tfoot> element. The <tbody> element can contain multiple rows (<tr>) and cells (<td>) that make up the body of the 
table.
<tfoot>: This element is used to group the footer content in a table. It should be used after the <tbody> element and can 
contain one or more rows and cells. The <tfoot> element is often used to display summary information or totals for a table.

## Introducing Constructors

We've already used this link so erm, moving on.. 

### Questions

- What is a constructor and what are some advantages to using it?
In JavaScript, a constructor is a special method that is called when an object is created. It is used to initialize the object's properties and behavior. The constructor is invoked using the new keyword, and it returns a new instance of the object.

Advantages of using a constructor include:

Encapsulation: The constructor allows you to bundle data and functionality into a single object, keeping related code 
together and preventing it from being accessed outside of the object.
Reusability: The constructor can be used to create multiple instances of an object, saving time and reducing the amount of 
code that needs to be written.
Inheritance: The constructor can be used as a blueprint for creating child objects that inherit its properties and methods.
In JavaScript, the this keyword is used to refer to the current object. When used in an object literal, this refers to the 
object that contains it.

- How does the term this differ when used in an object literal versus when used in a constructor?
When used in an object literal, this refers to the object itself, while when used in a constructor, this refers to the 
instance being created by the constructor. In other words, this in an object literal refers to the object that is being 
defined, while this in a constructor refers to the object that is being instantiated from the constructor.
  
## Object Prototypes Using A Constructor


