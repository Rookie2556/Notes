## HTML Forms:

Webforms are forms that the user inputs information into, and usually the data is stored in some medium such as email et cetera.

A form can be called a widget, and is acting as an interface betweeen client and their targeted audience.
![form-sketch-low](https://user-images.githubusercontent.com/122787483/219885477-560cd659-921b-4059-a24e-2c55836e87aa.jpg)

A form typically looks like this ^

The form would be formmated as such:

``` <form action="/my-handling-form-page" method="post">…</form> ```

Action defines the location in which the data is sent to.
method defines what method is used, usually get or post.

A form consists of:

``` <label> - This is "Name: "
    <input> - where the user would input their name for example
    <textarea> - where multiple lines of text are required to be put on the form
```

``` <form action="/my-handling-form-page" method="post">
  <ul>
    <li>
      <label for="name">Name:</label>
      <input type="text" id="name" name="user_name" />
    </li>
    <li>
      <label for="mail">Email:</label>
      <input type="email" id="mail" name="user_email" />
    </li>
    <li>
      <label for="msg">Message:</label>
      <textarea id="msg" name="user_message"></textarea>
    </li>
  </ul>
</form>
``` 

```<li class="button">
  <button type="submit">Send your message</button>
</li>
``` 

This button would submit the data to the **action**, there are 3 types of buttons:
- Submit - explained above
- Reset - Resets all attributes
- button - does nothing!

``` form {
  /* Center the form on the page */
  margin: 0 auto;
  width: 400px;
  /* Form outline */
  padding: 1em;
  border: 1px solid #ccc;
  border-radius: 1em;
}

ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

form li + li {
  margin-top: 1em;
}

label {
  /* Uniform size & alignment */
  display: inline-block;
  width: 90px;
  text-align: right;
}

input,
textarea {
  /* To make sure that all text fields have the same font settings
     By default, textareas have a monospace font */
  font: 1em sans-serif;

  /* Uniform text field size */
  width: 300px;
  box-sizing: border-box;

  /* Match form field borders */
  border: 1px solid #999;
}

input:focus,
textarea:focus {
  /* Additional highlight for focused elements */
  border-color: #000;
}

textarea {
  /* Align multiline text fields with their labels */
  vertical-align: top;

  /* Provide space to type some text */
  height: 5em;
}

.button {
  /* Align buttons with the text fields */
  padding-left: 90px; /* same size as the label elements */
}

button {
  /* This extra margin represent roughly the same space as the space
     between the labels and their text fields */
  margin-left: 0.5em;
}
``` 
Above helps style a form nicely in CSS. 


### Questions:

Why are forms so important in web development?
    Allow for an interface from client to server, in a simple and easy manner in which the user can take their time and 
    ensure all data is correct without the need of a contact number or such.
When designing a form, what are some key things to keep in mind when it comes to user experience?
    Text input, Buttons and labels are simple and easily understood. 
    As little confusion as possible in regards to filling the form out.
    Feedback to allow the user to feel as the information was dealt with accordingly, or to state errors in their input.
    Organised in a logical way to ensure that the corresponding data is somewhat grouped together.
List 5 form elements and explain their importance.
    - Submit - Needed to send the data to it's processing location
    - Label - allows the user to udnerstand what is being asked of the user
    - input - allows the user to input what is expected in the corresponding box
    - Textarea - allows for the user to put more than a line of information
    - range input - allows for users to select a value within a specified range
  
  ## Learn JS
  
  ### Introduction to events:
  
 For the past ffew days I have been unable to access canvas. 

``` Here is the code learnt from labs 9

<!DOCTYPE html>
<html>
<head> 
    <script src="Lab9.js"></script>
</head>

<body>
        <form id="NewCookieForm">
        <fieldset>
            <legend>Enter new cookies </legend>

            <label for="name-input">Cookie name</label>
            <input name="name" id="name-input" type="text" />

            <label for="number-input">number of cookies</label>
            <input name="number" id="number-input" type="text" />

            <label for="colour-input">colour of cookies</label>
            <input name="colour" id="colour-input" type="text" />
        
            <button id="submit-button" type="submit">Submit :) </button> 
        
        </fieldset>
        </form> 

    </body>
</html>


// Event listeners

const submitButton = document.getElementById("submit-button");

submitButton.addEventListener("submit", function(event) {
    event.preventDefault();

    const cookieNameInput = document.getElementById("name-input").value;
    const cookieNumberInput = document.getElementById("number-input").value;
    const cookieColourInput = document.getElementById("colour-input").value;

    console.log(cookieNameInput, cookieNumberInput, cookieColourInput);

    const newCookie = new Cookie(cookieNameInput, cookieNumberInput, cookieColourInput);
    newCookie.render();

    document.getElementById("NewCookieForm").reset();
}); ``` 
```

An event is something that is happening in the system, e.g. clikcing a button would result an event e.g. loading a new page et cetera.

Some events can be acitvated by :hover, :submit et cetera.

Event listeners are those that react to events, e.g. "click" meaning when this element is clicked, the eventlistener specifies what happens.

```
const btn = document.querySelector("button");

function random(number) {
  return Math.floor(Math.random() * (number + 1));
}

btn.addEventListener("click", () => {
  const rndCol = `rgb(${random(255)}, ${random(255)}, ${random(255)})`;
  document.body.style.backgroundColor = rndCol;
});
```

The above changes the colour of the background when clicked. 

Eventlistener types:
- focus - when the button is in focus, e.g. clicked - can be used to highlight the selected box
- blur - when it stops being focus, e.g. the form can check if there is input in the box previously focused
- dblclick - only if double clicked, an event happens
- mouseover - e.g. if cursor over an element it could get enlarged
- mouseout - the opposite of mouseover

removing listeners - ``` btn.removeEventListener("click", changeBackground); ```
an element can have multiple eventlisteners.

### Event objects:

Event objects are automatically created by the browser when events are done, allowing us to maniplate within the event handlers. e.g. 

``` const buttonElement = document.getElementById('myButton');

buttonElement.addEventListener('click', function(event) {
  console.log(event.target); // logs the button element that was clicked
});
``` 
Allows for further real time eventlistening.

Video player: 

``` <button>Display video</button>

<div class="hidden">
  <video>
    <source
      src="https://interactive-examples.mdn.mozilla.net/media/cc0-videos/flower.webm"
      type="video/webm" />
    <p>
      Your browser doesn't support HTML video. Here is a
      <a href="rabbit320.mp4">link to the video</a> instead.
    </p>
  </video>
</div>
``` 

Event capturing is the process of handling an event starting from the root of the DOM, and moving up the tree hierarchy. Used for checking changes to the document as a whole. 

``` document.addEventListener('click', function(event) {
  console.log('capturing phase', event.target);
}, true);
``` 

Event delegation is the technique used to handle events on multiple elements using a single event listener.

```
const list = document.querySelector('ul');

list.addEventListener('click', function(event) {
  if (event.target.nodeName === 'LI') {
    // handle the click on the list item here
  }
});
```

### Questions

How would you describe events to a non-technical friend?
    Events is the website reacting to actions, actions cause reactions. The website would consider a click as an event and 
    react accordingly
When using the addEventListener() method, what 2 arguments will you need to provide?
    The event to listen for e.g. click()
    The function called when Click() occurs
Describe the event object. Why is the target within the event object useful?
    Is created automatically by the browser when events are being executed, storing information about the event.
    Target is useful as it creates a reference to the element that caused the event. Would come in useful for types of         event targeters such as event bubbling and capturing. 
What is the difference between event bubbling and event capturing?
    Event capturing targets the highest ancestor, then moves down the group 
    Event bubbling targets the target first, then bubbles up the dom group
