# task_management
(HTML Code)
1. <!DOCTYPE html>: This declaration specifies that the document is an HTML5 document type.


2. <html lang="en">: The opening tag of the HTML document, with the "lang" attribute set to "en" (English), indicating the language of the document's content.


3. <head>: The head section of the HTML document, which contains metadata and links to external resources.


4. <title>To-Do List</title>: Sets the title of the web page displayed in the browser's title bar or tab.


5. <meta charset="UTF-8" />: Specifies the character encoding for the document (UTF-8, which supports a wide range of characters and symbols).


6. <meta name="viewport" content="width=device-width" />: Configures the viewport width to match the device's width, providing better responsiveness for various screen sizes.


7. <link rel="stylesheet" href="styles.css" />: Links to an external CSS file named "styles.css" to apply styling to the HTML elements.


8. <body>: The body section of the HTML document, which contains the visible content of the web page.


9. <section class="container">: A section element with the class "container," used to group related content.


10. <div class="heading">: A division element with the class "heading" for the title and image at the top of the page.


11. <img class="heading__img" src="...">: An image element with the class "heading__img" that displays an image of a laptop.


12. <h1 class="heading__title">To-Do List</h1>: A heading level 1 element with the class "heading__title," displaying the text "To-Do List."


13. <form class="form">: A form element with the class "form" for user input.


14. <label class="form__label" for="todo">...: A label for the input field, indicating what the user should input.


15. <input class="form__input" type="text" id="todo" name="to-do" size="30" required>: An input field for the user to enter their to-do item. It has a class "form__input," a unique ID "todo," a name "to-do," a size of 30 characters, and is required.


16. <button class="button"><span>Submit</span></button>: A button element with the class "button," containing the text "Submit."


17. <div>: A division element containing an unordered list (ul) for displaying the to-do list items.


18. <ul class="toDoList">: An unordered list with the class "toDoList," where to-do list items will be added dynamically.


19. <script src="script.js"></script>: Links to an external JavaScript file named "script.js" for adding interactivity and functionality to the web page.


This is the basic structure of our to-do list using HTML, and now we can move on to styling it using CSS.

(CSS Code):

@import: This line imports a Google Fonts stylesheet, making the "Gochi Hand" font available for use on the page.


2. body: This block of code styles the entire body of the webpage. It sets the background color, minimum height, padding, box-sizing, and various other properties to center the content both horizontally and vertically. It also sets the text color and font family to "Gochi Hand" for a cursive font style.


3. @media only screen and (min-width: 500px): Inside this media query, the minimum height of the body is adjusted to take up the full viewport height (100vh) when the screen width is at least 500px.


4. .container: This class styles a container element. It sets the width, minimum and maximum width, background color, border-radius, box shadow, and padding. It also adds a radial gradient background pattern.


5. .heading: This class styles a container for the heading. It aligns the content both horizontally and vertically and adds a margin at the bottom.


6. .heading__title: This class styles the heading title, giving it a rotated appearance, rounded border, background color, and font size. Inside the media query, the font size is increased for larger screens.


7. .form__label: This class styles labels for form inputs, adding a margin at the bottom.


8. .form__input: This class styles form input fields. It sets the box-sizing, background color, padding, border radius, and border style. The focus state adjusts the border color.


9. @media only screen and (min-width: 500px): Inside this media query, the width of the input fields are adjusted for larger screens.


10. .button: This class styles a button element. It sets various properties for the button appearance, including padding, rotation, font family, border radius, box shadow, and background image.


11. .button span: This styles the text inside the button, giving it a background color, padding, border, and border-radius.


12. .button:active, .button:focus: These styles define the appearance of the button when it is active (clicked) or focused (selected).


13. .toDoList: This class styles a to-do list on the webpage, aligning the text to the left.


14. .toDoList li: This class styles individual list items in the to-do list, adding padding.


15. .toDoList li:hover: This style is applied when hovering over a list item, giving it a line-through decoration with a wavy effect and changing the color.
 
 (JavaScript Code):
 1. An Immediately Invoked Function Expression (IIFE) is used to encapsulate the entire code block. This pattern is often used to create a private scope for variables, preventing them from polluting the global scope.


2. Inside the IIFE, several state variables and UI variables are declared and initialized:


    toDoListArray: An array that will store the To-Do list items.
    form, input, and ul: These variables are used to reference specific elements in the HTML structure. form refers to the HTML form element, input refers to the input field within the form, and ul refers to an unordered list where the To-Do list items will be displayed.


3. Two event listeners are set up:


    The first listener is for the form's submit event. When the form is submitted (user presses Enter or clicks the "Submit" button), the function prevents the default form submission behavior (page reloads), generates a unique ID for the To-Do item, retrieves the input value, and then invokes two functions: addItemToDOM() and addItemToArray().
    The second listener is for the unordered list (ul). It listens for click events within the list. When an item within the list is clicked, it checks if the clicked element has a data-id attribute. If it does, it invokes two functions: removeItemFromDOM() and removeItemFromArray().


4. Four functions are defined within the IIFE:


    addItemToDOM(itemId, toDoItem): This function creates a new list item (<li>) element, assigns it a data-id attribute with the provided itemId, sets the inner text of the list item to the provided toDoItem, and appends the list item to the unordered list (ul).
    addItemToArray(itemId, toDoItem): This function adds a new object to the toDoListArray array, where each object represents a To-Do item with its associated itemId and toDoItem text.
    removeItemFromDOM(id): This function finds the list item element with the specified data-id attribute (id) and removes it from the unordered list (ul).
    removeItemFromArray(id): This function filters the toDoListArray to exclude the object with the matching itemId, effectively removing the corresponding To-Do item from the array.


5. The IIFE is immediately invoked by enclosing the entire code block in parentheses and adding () at the end. This ensures that the code within the IIFE is executed as soon as the JavaScript file is loaded.




