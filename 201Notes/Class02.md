# Class 02 of 201

## Basics of HTML CSS and JS

### Introduction to HTML:

*HTML is a mark up language, used to make the structure of a website, it is usually very bland looking and contains the basics
such as paragraphing, imagery titles and any other contents a website may have. At this stage any decoration and interactivity is
very limited.*

``` <head> ```

Contains information about the website that isn't displayed and any links to scripts used et cetera. 

``` </head> ```

``` <a src=LinkwouldLeadhere.com>```
This is a hyper Link, where the information here would be shown to the user
``` </a> ```

- Semenatic is important as it boosts our SEO and ensures that the structure of the website is proper and allows for easier
  readability when viewing the code and the website in two different senses.
  
- There are 6 levels of html headings, h1 to h6, where h6 is smallest and h1 is largest.

- ```<sup>``` makes a text smaller and held higher than the base line text, like cubed would be held, ```<sub>``` is the same, but lower instead.
  
- ``` <abbr> ``` must be closed by ``` </abbr> ``` in order to be used correctly.
  
## How is CSS Structured? 

CSS and JS can be used **internally** (e.g. alongside HTML), within the head and style tags.

``` <style>
      h1 {
        color: blue;
        background-color: yellow;
        border: 1px solid black;
      }

      p {
        color: red;
      }
    </style> ```
  ```
  
Css can also be used **externally** , in an external .css file and referenced within the ``` <head> </head> ```

```   <link rel="stylesheet" href="styles.css" /> ``` 

The CSS code in .css would reference elements and change them in a similar style to Internally.

``` p::first-letter {
    color: red;
} ```
```
The above makes the first letter of a paragraph Red.

The third and final style is called **in-line** styling which is alongside the HTML in the ``` <body> ```
    ```
    <body>
    <h1 style="color: blue;background-color: yellow;border: 1px solid black;">
      Hello World!
    </h1>
    <p style="color:red;">This is my first CSS example</p>
  </body> ``` 
  
 

### Selectors

To style a specific text, or object from html - we use **Selectors**, there are different types:

- Attribute selector: selects based on attributes
- + ``` .red-center {
    color: red;
    text-align: center;
} ```
- Element selector: selects specific elements
- + ``` p {
  /* Styles here */
} ```
- Class selector: Selects specific classes
- + ``` .selected {
  /* Styles here */
} ```
- ID selector: Selects based on names given
- + ``` #unique {
  /* Styles here */
} ```

### properties and values:

**properties** are human readable identifiers that show what features are changed e.g. ```p {
  color: blue;
} ```
**Values** give how to style that.

*In CSS, a property is a keyword that specifies the aspect of an HTML element that you want to change or modify. A value is the information or setting that you want to apply to the property. Together, a property and its value make up a CSS declaration, which is used to change the presentation of an HTML element.

For example, the property "color" specifies the text color of an element, while the value "red" sets the text color to red. The CSS declaration would look like this:

color: red;

This declaration would be used to change the text color of an HTML element to red.*

## Functions:

Functions are recallable code, that can be reused and generally take in input, to return some sort of output. Some are premade as part of the css library.

e.g. ``` width: calc(90% - 30px); ```

e.g. ``` transform: rotate(0.8turn); ```

### rules:

@ is the symbol for rules in css, for showing how the css should behave and guidelines...
```@import "secondCSS.css"; ```

### shorthands:

Shorthands are properties that can define many values in a single line e.g. 

```padding: 10px 15px 15px 5px;```

``` background: red url(bg-graphic.png) 10px 10px repeat-x fixed; ```

### Questions answered:

- What are ways we can apply CSS to our HTML?
- + Inline styles: adding the style attribute to individual HTML elements
    Internal stylesheet: using a <style> tag in the head of the HTML document to define styles for the entire page
    External stylesheet: linking to a separate .css file from the HTML document
- Why should we avoid using inline styles?
- + it is generally considered best practice to avoid using inline styles as they can make the HTML more cluttered and         harder to maintain. It is better to separate the presentation (CSS) from the structure (HTML) for the sake of          
    organization and to make the code more reusable.
- Review the block of code below and answer the following questions:
- + What is representing the selector?
- + Which components are the CSS declarations?
- + Which components are considered properties?

  ``` 2 {
     color: black;
     padding: 5px;
   } ```
  
In the block of code provided, the "h2" is representing the selector. The CSS declarations are "color: black;" and "padding: 5px;". The components "color" and "padding" are considered properties.
  

## Making decisions in your code - conditionals

If else statements - This is on the basis **If you are mean, I dont like you.. else, I like you** 
 in programming this is important as otherwise programs would be fairly linear and not as functional.
  
example: 
  
  ``` if

  

  



