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
 

 A border would simply just make the boxes' width larger, and the height taller. Flex 
 allows elements within a container to be aligned and distributed in a flexible way,

 
 ``` Parts of a box
Making up a block box in CSS we have the:

Content box: The area where your content is displayed; size it using properties like inline-size and block-size or width and height.
Padding box: The padding sits around the content as white space; size it using padding and related properties.
Border box: The border box wraps the content and any padding; size it using border and related properties.
Margin box: The margin is the outermost layer, wrapping the content, padding, and border as whitespace between this box and other elements; size it using margin and related properties.
 ```

![box-model](https://user-images.githubusercontent.com/122787483/215067593-d2b7c627-bb64-4f68-a9e3-fc858b16c4d1.png)
 
 ## Learn Js
 
### Arrays:
 
 An array is a list of values, treated as an object. 
 
 According to google:
 
> array
> /əˈreɪ/
> Learn to pronounce
> See definitions in:
> All
> Military
> Mathematics
> Computing
> Law
> noun
> 1.
> an impressive display or range of a particular type of thing.
> "there is a vast array of literature on the topic"
> 2.
> an ordered series or arrangement.
> "several arrays of solar panels will help provide power"

An array is essentially just a list of values, typically of the same data type but isn't bound to.
 
To **create** an array we use the following:
 
 ``` const shopping = ['bread', 'milk', 'cheese', 'hummus', 'noodles']; ```
 
 This names the list "shopping" and its values are bread, milk, cheese, hummus and noodles.
 
 To find the length of an array we can use the following:
 
 ``` console.log(shopping.length); ``` 
 
 To access and modify we can do the following: 
 
 ``` shopping[0] = 'tahini'; /// adds the value "tahini" as the first value in shopplist
     console.log(shopping[3]); //prints hummus, the 4th item since tahini is now first. ```
 
 You can also have multidimensional arrays, in which arrays can be held within arrays like so:
 
 ``` const random = ['tree', 795, [0, 1, 2]];
     random[2][2]; ``` 
 
 You can also check the index of a specific item in an array like so:
 
``` const shopping = ["ReadysaltedPringles", "cheeseandonionPringles" , "GreenPringles"] 
    console.log(shopping.indexOf('GreenPringles'); //would return 2 ```
 
 We can use the push() function to add to lists, like so:
 
 ``` const letters = ['a','b'];
 letters.push('c'); // the list is now a b c
 letters.push('d','e'); // it is now a b c d e ```
 
push adds it to the end of the array, the unshift() adds it to the start:
 
 ``` letters.unshift('a'); // the list is now a a b c d e ```

to remove an item, from the front - you use pop()
 
 ``` letters.pop(); // the list is now a a b c d ```

to remove an item from the back - you can use shift()
 
 ``` letters.shift(); // a b c d ```
 
 to remove a specific item whose item we know the index of we use splice like so:
 
 ``` const index = letters.indexOf('c'); //returns 2
if (index !== -1) {
  letters.splice(index, 3); //the list is now a b d
} ```

To access each item can be useful, we use a for loop for this instance - 
 
 ``` for (const letter of letters) {
        console.log(letter); } ``` it prints each letter individually, but this can be adjusted to do something else. ```
 
 No idea why you'd want to do this but here goes: map()
 
 ``` const doubled = letters.map(double); // returns aa bb dd ```
 
Filtering a list is useful, especially in a search function type style:
 
 ``` function isLong(city) {
  return city.length > 8;
}
const cities = ['London', 'Liverpool', 'Totnes', 'Edinburgh'];
const longer = cities.filter(isLong);
console.log(longer);  // [ "Liverpool", "Edinburgh" ]
```
 
 ### Expressions and operators
 
*t a high level, an expression is a valid unit of code that resolves to a value. There are two types of expressions: those that have side effects (such as assigning values) and those that purely evaluate.*
 
| Assignment       | x = f()       | x = f()       |
|------------------|---------------|---------------|
| Addition assignment | x += f()    | x = x + f()   |
| Subtraction assignment | x -= f() | x = x - f()   |
| Multiplication assignment | x *= f() | x = x * f()  |
| Division assignment | x /= f()    | x = x / f()   |
| Remainder assignment | x %= f()   | x = x % f()   |
| Exponentiation assignment | x **= f() | x = x ** f() |
| Left shift assignment | x <<= f()  | x = x  << f()  |\n| 
| Bitwise AND assignment | x &= f()  | x = x & f()   |
| Bitwise XOR assignment | x ^= f()  | x = x ^ f()   |
| Bitwise OR assignment  | x |= f()  | x = x | f()   |
| Logical AND assignment | x &&= f() | x && (x = f()) |
| Logical OR assignment  | x ||= f() | x || (x = f()) |
| Nullish coalescing assignment | x ??= f() | x ?? (x = f()) |
 
We can destruct by doing the following to an array called foo:
 
 ``` const [one, two, three] = foo; ```
 
 
