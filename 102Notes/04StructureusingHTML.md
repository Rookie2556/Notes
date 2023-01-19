# HTML:

### Wireframing, what is it and what do I do?

Wireframing is a practice of designing an estimate for the website in mind, commonly used by UX designers.
It is a great way of getting everyone's concept of the app/software/website to be as similar as possible and avoid conflicting ideologies. **compatibility and easeability**

Wireframes can be done *anywhere* (though I'd bet digitally is the best bet on a professional standard), from pen and paper to using software. 

This was my wireframe for this project: 

![Wireframe](https://user-images.githubusercontent.com/122787483/213161145-493a5a18-8c4b-4f5a-aa5c-6a35f490076e.png)

- I put where I want the information and the images to go, typically alternating sides.
- The title was decided before the wireframe started.
- We then planned out what cakes we wanted to represent and the sizing of the imagery
- I started coding this immediately after in just HTML.

![BakingBadHTMLpic](https://user-images.githubusercontent.com/122787483/213159412-c36546d5-85a0-4742-bdb1-fcef8039ccb1.png)

*the result is not similar yet, but the HTML structure is ready for CSS to change it appropriately*

Typically wireframes can be interactive, multiple pages long to emulate what the user sees after each click etc, or basic like my example! 

There are tools out there that are massively useful, according to https://careerfoundry.com/en/blog/ux-design/how-to-create-your-first-wireframe/#what-is-a-wireframe 

- UXPin, 
- InVision
- wireframe.cc
**are good software to use for wireframing.**

3 priniples to ensure quality wireframes:

1 - Clarity, It stays true to its' purpose
2 - Confidence, the wireframe should increase every individuals confidence towards the end goal
3 - Simple, the wireframe should stick to being a wireframe and in order to do that too much detail is unecessary

### Now we know what our website looks like conceptually now what?

*Glad you asked!* 
We then structure it in HTML, HTML is hypertext markup language.
Markup is essentially just a *little* harder than markdown which we've already covered.
as such a paragraph is (opening)<p> between elements </p>(closing) and **<always have to be closed/>**

Usually, <p> <b> </b> </p> - nesting is fairly useful:

    *<p> paragraphhhhh paragraphhhhhh
    <b> **Paragraphhhhhh** </b>
    paragraphhhhhhh </p>

and the correct syntax is first opened, last closed.

if the element has no content, it is a **void** element!

    <!DOCTYPE html>
    <html lang="en-US">
     <head>
       <meta charset="utf-8" />
       <meta name="viewport" content="width=device-width" />
       <title>My test page</title>
     </head>
     <body>
       <img src="images/firefox-icon.png" alt="My test image" />
     </body>
    </html>

All html files have similar structure, <!doctype html> <html> <head> Title </head> <body> main content of page> </body> </html>

### IMAGES whoooo

Images are done using img src=path alt=if can't load, what text replaces it with < and > on both sides 😢
*github reads the img so I cannot do it correctly here*
![Imglink](https://www.simplilearn.com/ice9/free_resources_article_thumb/adding-html-images.PNG)

### most common html elements:

    - <h1> **huge text** </h1> <h6> <sup><sub>Add your tiny text</sub></sup> </h6> 
    - <p> paragraphs </p>
    - <ul> lists </ul> <ol> ordered </ol>
    - <a> link </a> href would make it like the example given above.
    
* [Home](/102Notes/01MarkDown.md)
* [Prev (03, Revisions and the Cloud)](./03RevisionsAndTheCloud.md)
* [Next (05, Design Web pages with CSS)](./05DesignWithCSS.md)
