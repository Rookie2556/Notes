# First class of 201:

## How the web works -

According to google, the web is defined as:

> web
> /wɛb/
> Learn to pronounce
> noun
> 1.
> a network of fine threads constructed by a spider from fluid secreted by its spinnerets, used to catch its prey.
 
> 2.
> a complex system of interconnected elements.
> "he found himself caught up in a web of bureaucracy"

_The web is a very *large* place_, while the google definition probably means a different type of web, the principle still stands
as the web in our terms, is a series of interconnected pages with some form of communication.

In the main sense, a client is the device side.
and the web page is the server side. 

The client (device) would make a request - in the form of data packets, sent over the internet via routers and such, to the server
telling the server "Hey, Let me in" in a maybe more *computer-y way*.

![connectoins](https://user-images.githubusercontent.com/122787483/214718345-84fbeef1-3f4d-4ecf-824c-a675cbe035e2.jpg)

Imagine another link on the other side of the cloud, leading to their router and their big servers containing the webpages you're requesting.

We Identify devices by IP addresses - Internet protocol addresses, via the internet (there are other ways to identify but we don't need to talk 
about this here).

![Layers Of internet communication](https://user-images.githubusercontent.com/122787483/214718961-2001f0d4-9b58-416b-af52-124f811c88f8.jpg)

Simplified, this means the application e.g. The Http (Hypertext transfer protocol located by it's Domain name like [Google.com](google.com),
would contain assests and code files (e.g. the HTML CSS and Js that makes it presentable).

The client can access the page using an internet connection, sending *so many* data packets to the correct locations via a series of protocols.

## Designing a website: 

### Designing a website is very fun, but how do we go about it?

Planning - We have to have an idea of what we want this website to look like, it's functionality and use to both the designer
and the consumer.

We could create a wireframe which is a very basic diagram, can be done using software or by hand on paper! ** Wireframing **

This wireframe can be as detailed or as basic as the designer sees fit, however it is important that everyone involved has as similar
an idea as possible for the prospects of this website to avoid confusion later on.

![213141378-073b2608-f73c-49af-bcdb-fe40ba2193c0](https://user-images.githubusercontent.com/122787483/214721300-b983761e-b33d-4709-b2d3-edda262cfba0.png)

![213261561-fed91214-c6d6-4634-9d9c-04ca54711342](https://user-images.githubusercontent.com/122787483/214721379-93e1d949-c441-4284-8423-1536c8d40e6f.png)

![Wireframe example.. ](https://user-images.githubusercontent.com/122787483/214721758-0e404479-5ec9-4b37-8187-0fac5747e0ff.jpg)

![Wireframe](https://user-images.githubusercontent.com/122787483/214722028-f5a3ebe8-81a1-4e51-aaba-c837b82e323a.jpeg)

## What Is JavaScript? 

### JavaScript is very important!!!

*JavaScript is a programming language, used to add interactivity to websites and add functionality as well as keep user engagement.*

We add .Js (javascript) files via a script link - .e.g. ``` <script src="directory/name_ofJavaScript.js"> </script> ```

This can interact with our html via selectors, e.g. ``` document.querySelector(<Tag>); and name it as a suitable variable.```

Variables are defined as ``` Let Variable1 == 1; // if the variable is going to change, e.g. maniplated.
                             Const Variable2 == 2; // If the variable is not going to change at all.
                             var variable3 == 3; // Var is avoided generally as it is error causing and has since 2015 been replaced ```


Boolean is anything defined as ``` True ``` or ``` False ```
Array is a list of int, strings or whatever. ``` ['a','b','23','car']; ```
Object is something that can have properties assigned to itself.

## Answering Canvas Questions:

- What is an HTML attribute? 
- + What is contained within a tags, imagery, links et cetera.
- Describe the Anatomy of an HTMl element.
- + ``` <html> Opens the entire HTML
        <head> //Titles amd styles go here
        </head>
        <body>
        <p> contents is stored here </p>
        </body>
        </html> //closes html ```
- What is the Difference between <article> and <section> element tags?
- +  *In the answers section, each answer can be inside an article tag. 
      So, the section is used to define sections of the page, while an article is generally used for wrapping similar
      content, like, each blogpost in a list of blog posts.*
- What Elements does a “typical” website include?
- + HTML H1 P Style Head et cetera.
- How does metadata influence Search Engine Optimization?
- + Influences SEO, makes the website score higher in searches, e.g. more likely to be clicked on by users, more traffic.
- How is the <meta> HTML tag used when specifying metadata?
- + Used to put descriptions, keywords, authors, viewport settings et cetera.





