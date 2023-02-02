For the past ffew days I have been unable to access canvas. 

Here is the code learnt from labs 9

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
});
