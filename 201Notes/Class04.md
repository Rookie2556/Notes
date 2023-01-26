# HTML Links, Js Functions and intro to CSS layout.

*HTML is used for the structure of websites, it is the fundamental to most websites.*

## Creating hyper links:

They oftentimes lead elsewhere, or bring stuff **to** the website. They've been around since the start and massively affect our
websites.

a typical link looks like this:

``` <a href="Link.com"> Leading to a website called Link.com i guess </a> ```

This would be shown as an underlined blue writing saying "Leading to a website called Link,com i guess" that the user can click

Any block level element can also be made into a link, by adding a ``` <a href ...  </a> ``` 

They are also able to link to directories, such as github directories, an example is simply the .html name if it is in the same
directory, or ./.html name if it is in the parent directory of the file you are currently viewing et cetera..

You can link to specific parts of docuements, for example:

``` <h2 id="Mailing_address">Mailing address</h2> ```

This requires an id, so when naming the element you want to link, it will have a ID class applied to it.

**Two types of URLs**:
- Absolute: where if linked aproproiately, you could use this link *anywhere* and it'd work.
- Relative: where if linked, it only works from your directory, or relative to the users' current position.

Links are useful to keep the user on your website, while giving the user relevant information and tidies up the website as a whole.

## CSS layout, Normal flow:

*In HTML, elements are laid out in a block formatting context by default. 
This means that elements will take up the full width of their parent container,
and will stack vertically one on top of the other. The width and height of block elements can be controlled using CSS. 
Additionally, elements within the block formatting context will respect the box model, meaning that padding, borders, 
and margins will be added to the total width and height of the element.*

## CSS positioning: 

*Static* positioning is default, *relative* positioning is positioning relative to parameters set - such as top, left, right and
bottom. (usually as such top: 30px, or top: 70%)..

*absolute*, With absolute positioning, an element is positioned relative to its nearest positioned ancestor, 
but instead of using the flow of the document, the element is placed at a specific position defined by the CSS top, 
right, bottom, and left properties. This means that the element is removed from the flow of the document and 
other elements will not be affected by the positioning of the absolute element. The position property must be set 
to "absolute" or "fixed" for the element to be positioned absolutely. This method of positioning is 
often used for specific elements that need to be placed in a specific location on a webpage, such as a pop-up or a link bar.

**z index** allows layering of elements, rather than ensuring that elements never touch, there are instances where
a text could go in front of a picture et cetera. formatted as such: ``` z-index: 1; ```, wherein higher z indexes go on top.

A note to make is that z index 2 and 29999999999999 would have the same effect when they are the only higher values than the others.

In CSS, there are four types of positioning:

Static positioning: This is the default positioning for elements. Elements are positioned in the order they appear in the HTML document and do not have any special positioning applied to them.

Relative positioning: When an element is set to relative positioning, it is positioned relative to its default static position. This means that if you apply top, right, bottom, or left properties, the element will shift from its default position by the specified amount.

Absolute positioning: When an element is set to absolute positioning, it is positioned relative to its nearest positioned ancestor element. If there is no positioned ancestor, the element will be positioned relative to the initial containing block, which is typically the viewport.

Fixed positioning: When an element is set to fixed positioning, it is positioned relative to the viewport and does not move when the page is scrolled.

Sticky positioning: Elements are positioned based on the normal flow of the document, but as soon as the user scrolls and the element's top or bottom edge crosses a specified threshold, it becomes fixed-positioned relative to the viewport. It will scroll with the page until its edge reaches the specified threshold, at which point it will stop scrolling and become fixed.

In summary, Static positioning is the default, Relative positioning is when an element is positioned relative to its default position, Absolute positioning is when an element is positioned relative to its nearest positioned ancestor and Fixed positioning is when the element is positioned relative to the viewport and does not move when the page is scrolled.

Sticky comes in useful when creating a scrolling index:

``` <h1>Sticky positioning</h1>

<dl>
  <dt>A</dt>
  <dd>Apple</dd>
  <dd>Ant</dd>
  <dd>Altimeter</dd>
  <dd>Airplane</dd>
  <dt>B</dt>
  <dd>Bird</dd>
  <dd>Buzzard</dd>
  <dd>Bee</dd>
  <dd>Banana</dd>
  <dd>Beanstalk</dd>
  <dt>C</dt>
  <dd>Calculator</dd>
  <dd>Cane</dd>
  <dd>Camera</dd>
  <dd>Camel</dd>
  <dt>D</dt>
  <dd>Duck</dd>
  <dd>Dime</dd>
  <dd>Dipstick</dd>
  <dd>Drone</dd>
  <dt>E</dt>
  <dd>Egg</dd>
  <dd>Elephant</dd>
  <dd>Egret</dd>
</dl>
``` Example given.
This ensures that the heading stays in view, which can be useful for tidiness and general functionality.

## Learn Js - Functions (reusable blocks of code) 

There are prebuilt functions that come with libraries, e.g. myCalc(), Math.sqrt(x) et cetera these functions are often well tested
and functioning.
Or the user can make their own functions, such as:

``` function addTen(num) {
  return num + 10;
}

console.log(addTen(5)); // Output: 15
console.log(addTen(-2)); // Output: 8
```

This code adds 10 to the number applied to, and can be applied as many times as needed throughout the website.
*(though admitedly, it is fairly easy to not use this function.)* we use it by invoking it. e.g. addTen() called, some
functions can be self invoking or conditionally. 

A method is one that is associated with an object, accessing any properties given to it.

*In JavaScript, an arrow function (also called a fat arrow function) is a shorthand notation for defining a function. 
It is a more concise syntax for defining a function, and it also has some other differences in behavior
compared to traditional function declarations. The main difference is that arrow functions do not bind their own this,
arguments, super, or new.target. They can be used as an alternative to function expressions,
and are often used in functional programming constructs such as map, filter, and reduce. 
Arrow functions are defined using the "=>" syntax, with the left side indicating the parameters of the function and 
the right side indicating the function body.*

### Scope

The total code is seen as the **global** scope, nested would result in a **local** scope, e.g. values within wouldn't typically
interact with that outside itself. Counters are a perfect example of this (found onlline): 

``` // Global counter
let globalCounter = 0;

for (let i = 0; i < 5; i++) {
    // Local counter
    let localCounter = 0;
    
    // Incrementing both global and local counters
    globalCounter++;
    localCounter++;

    console.log("Global counter: " + globalCounter);
    console.log("Local counter: " + localCounter);
}

console.log("Outside of loop, global counter: " + globalCounter);
console.log("Outside of loop, local counter: " + localCounter);

```
This gives the following: 

![GlocalScope](https://user-images.githubusercontent.com/122787483/214956752-d31f9990-e29e-45b7-8b38-0bb7c20fab45.png)

![Scopes](https://miro.medium.com/max/1400/1*KxHwVbB0zhnSVrhrWtT-gg.jpeg)

## Pair programming:

Where two program together, as such one is the **driver** and one is the **navigator**.

This ensures improvement of listening speaking reading and writing skills relevent to the course. 

- Work environment readiness
- Job interview readiness
- Social skills
- Learning from fellow students
- Engaged collaboration
- Greater efficiency

## Questions time!!!

*HTML*
To create a basic link, we wrap text or other content inside what element?
The href attribute contains what information?
What are some ways we can ensure links on our pages are accessible to all readers?

we wrap it inside a <a> element tag.
the href contains the url or web address of the resource linked.
we can assign an alt to it, to ensure the visually impaired or the internet-ly impaired can still understand what is happening.
(more so the blind tbh).

*CSS*
What is meant by “normal flow”?
What are a few differences between block-level and inline elements?
___ positioning is the default for every html element.
Name a few advantages to using absolute positioning on an element.
What is a key difference between fixed positioning and absolute positioning?

'normal' flow is the default of elements where they aren't specified.
The main differences between block and inline is:
- Block take up the full width of their containers
- can contain other block level and in line elements
- block can have width and height set, inline cannot.
static is default for html elements.
Absolute allows for complete percision, and outside of the normal flow if needed, and ignores scrolling.
A key difference between fixed positioning and absolute positioning is that an element with fixed positioning will 
remain in the same position on the screen, even when the page is scrolled, while an element with absolute positioning 
will be positioned relative to its nearest positioned ancestor.

*JS*
Describe the difference between a function declaration and a function invocation.
What is the difference between a parameter and an argument?

Declaration is the creation, invoking is the using of the function.
parameters are used as a placeholder for an arguement, an argument is used in the function. e.g. parameter is x, argument is 5.

*Pair programming*
Pick 2 benefits to pair programming and reflect on how these benefits could help you on your coding journey.

I choose:

- Social skills
- Learning from fellow students

I generally lack social skills and would require to work on this at any given time to progress as a person in general, 
as well as improve my experiences in a workplace, or social environment.
I am competitive in a sense, and when I can see others' do things I haven't done, It gives me a drive to become better at
programming to better match their standings.

## I would like to learn more about:

- I would love to watch a video about this, as writing doesnt concrete the concept into my mind, If not for my own
  experience, I wouldn't had understood to be honest.



