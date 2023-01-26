# Readings: HTML Lists, Control Flow with JS, and the CSS Box Model 

## Learn HTML

*The most fundamental component of the Web is HTML (HyperText Markup Language). It describes the purpose and organisation of 
web content. The appearance/presentation (CSS) and functionality/behavior (JS) of a web page are typically described 
using technologies other than HTML (JavaScript).

Links that join online pages together, either within a single website or between websites, are referred to as "hypertext." 
An essential component of the Web are links. You can participate actively in the World Wide Web by publishing content
online and linking it to other people's web pages. * 

according to google: 

> HTML
> /eɪtʃtiːɛmˈɛl/
> nounCOMPUTING
> Hypertext Markup Language, a standardized system for tagging text files to achieve font, colour, graphic, and hyperlink effects on World Wide Web pages.
> "an HTML file"

Markup is used to change the basic text to a format, using tags such as:

```
<head>, <title>, <body>, <header>, <footer>, <article>, <section>, <p>, <div>, <span>, <img>, <aside>, 
<audio>, <canvas>, <datalist>, <details>, <embed>, <nav>, <output>, <progress>, <video>, <ul>, <ol>, <li> and many others.
 ```
 
[MDN has great resources for learning HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)

## Ordered and unordered lists

- ``` <ol> ```

Ordered lists are annotated by the above, and represents an ordered list. Accepts global attributes: *Global attributes are attributes common to all HTML elements; they can be used on all elements, though they may have no effect on some elements.* 

**reversed** - can make the list high to low
**start** - can specify what number to start from
**type** - a for lowercase letters
+ A for uppercase letters
+ i for lowercase Roman numerals
+ I for uppercase Roman numerals
+ 1 for numbers (default)

Examples below:

``` <ol>
  <li>Fee</li>
  <li>Fi</li>
  <li>Fo</li>
  <li>Fum</li>
</ol>

``` 

``` <ol type="i">
  <li>Introduction</li>
  <li>List of Grievances</li>
  <li>Conclusion</li>
</ol>

```

``` <ol start="4">
  <li>Speedwalk Stu</li>
  <li>Saunterin' Sam</li>
  <li>Slowpoke Rodriguez</li>
</ol>
```

``` <ol>
  <li>first item</li>
  <li>
    second item
    <!-- closing </li> tag is not here! -->
    <ul>
      <li>second item first subitem</li>
      <li>second item second subitem</li>
      <li>second item third subitem</li>
    </ul>
  </li>
  <!-- Here's the closing </li> tag -->
  <li>third item</li>
</ol>

```

- ``` <ul> ```

*The <ul> HTML element represents an unordered list of items, typically rendered as a bulleted list.*

 Which functions fairly similarly to ordered, however it's attributes are better used in css.
 
 ## Questions for Above: 
 
1 - When should you use an unordered list in your HTML document?
2 - How do you change the bullet style of unordered list items?
3 - When should you use an ordered list vs an unorder list in your HTML document?
4 - Describe two ways you can change the numbers on list items provided by an ordered list?
 
 
 ## Answers:
 
 1 - When items are not required to be ordered, e.g. shopping lists
 2 - css can change the style of unordered lists
 3 - When a order is required, use ordered - when not don't.
 4 - Using css or using html to avhieve the same effect:
 
type = A" in HTML
type = "i" in HTML
 
## Learn CSS
 
### The Box model: 
 
Everything in css is surronded by an invisible box, this section is to better understand this box.
 
There are two types of boxes:
 
 - Block
 - Inline
 
 The two types dictate how the item behaves relative to other items and it's own positioning.
 
 They contain an inner display type and outer display type: 
 
**Inner display types: ** 
 
 **block** Will break onto a new line, width and height is respected.
 Padding margin and border pushes other items around, will occupy its container 100%
 3 examples of this is - paragraphs, lists and spans.
 
**in-line** Won't break onto a new line, width height don't apply.
 padding margin and border pushes some items around.
 2 examples of this is - span, ul.
 
**Inner display types: **
 
 
 
 
 
