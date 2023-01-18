#Designing webpages with CSS

###What is CSS?

**css is Cascading style sheet**, a simple syntax language to mark up HTML files and *bruches* up the professionalism to an extent..

HTML is the most common file however there is:

- SVG (Scalable Vector Graphics)  > Scalable Vector Graphics is an XML-based vector image format for defining two-dimensional graphics, having support for interactivity and animation.
- XML(Extensible Markup Language) > Extensible Markup Language is a markup language and file format for storing, transmitting, and reconstructing arbitrary data. It defines a set of rules for encoding documents in a format that is both human-readable and machine-readable.

The file is presented via a medium such as chrome, firefox or ~~edge~~ for users on the web, projectors or printers.

### CSS Syntax

Css is a rule based language, it gives rules to existing files - e.g. .container p would mean within the file container, a paragraph
will be affected by the rules specified, such as **colour**, *format*, font, sizing et cetera.

        h1 {
         color: red;
         font-size: 5em;
        }
        
        p {
         color: black;
         }
        
        
        
 Selector in the above text is "H1" e.g. a header, with this - css colours it red, and changes its' font size. So In HTML it could be plain black and white, CSS rewrites some of it's rules to become red and differently sized.
 
 Curly braces are used to contain the new rule declarations, each line ending with a semi colon > ;
 
 For P, paragraph, the writing is changed to >Black
 
 There is a documentation for CSS in [MDN web docs](https://developer.mozilla.org/en-US/docs/Web/CSS), fairly useful to go through while using CSS.
 
 ## How to add CSS
 
 within the HTML file you add:
                                > <head>
                                > <link rel="stylesheet" href="mystyle.css">
                                > </head>
                                
The above is **External** which can be edited in any text editor but it's ideal to use an IDE, as indenting, code autocompletetion and such can be a pain to manually do.

 
 **Internal CSS** is where css exists within the HTML file, inside <style> tags like so:
                                        > <style>
                                        >  body {
                                        >        background-color: linen;
                                        >        }

                                        >  h1 {
                                        >        color: maroon;
                                        >        margin-left: 40px;
                                        >        }
                                        > </body>
                                        > </style>
        
**Inline CSS** is internal, but where used - e.g. not requiring slectors:

                                        > <body>      
                                        > <h1 style="color:blue;text-align:center;">This is a heading</h1>
                                        > <p style="color:red;">This is a paragraph.</p>
                                        > </body>
                                        
It is definitely possible to mix and match all of the above, I personally have only done External as of writing this study note page. If multiple style sheets apply to the same attribute, the most recently read one will be applied.

**Cascading order** Is the virtual ruling of CSS where Inline has highest priority, then External/Internal then browser default.
        
## CCS Colour
Css can define colours by a variety of value types such as:
- HEX (#92a9d1)
- RBG (201, 76, 76);
- RGBA (201, 76, 76, 0.6);
- HSL (89, 43%, 51%);
- hsla (89, 43%, 51%, 0.6);

Values can be initalised e.g. brought back to default, or inherit from any parent nodes.

## Things I want to learn about

- I want to understand specs more
- I didn't know what the a extension on rbg and hsl meant
