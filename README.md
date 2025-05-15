# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DOM Manipulation Example</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <header>
        <h1>Welcome to DOM Manipulation</h1>
        <p>Click the buttons below to see the magic happen!</p>
    </header>

    <main>
        <section id="textSection">
            <p id="textContent">This is some text that will change.</p>
            <button id="changeTextBtn">Change Text</button>
        </section>

        <section id="styleSection">
            <p id="styleContent">Watch my color change!</p>
            <button id="changeStyleBtn">Change Style</button>
        </section>

        <section id="elementSection">
            <button id="addElementBtn">Add Element</button>
            <button id="removeElementBtn">Remove Element</button>
            <div id="dynamicElements"></div>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 My Webpage</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>

#js code

// Change text content dynamically
document.getElementById('changeTextBtn').addEventListener('click', function() {
    document.getElementById('textContent').textContent = 'The text has been changed!';
});

// Modify CSS styles via JavaScript
document.getElementById('changeStyleBtn').addEventListener('click', function() {
    document.getElementById('styleContent').style.color = 'blue';
    document.getElementById('styleContent').style.fontSize = '20px';
});

// Add or remove an element when a button is clicked
document.getElementById('addElementBtn').addEventListener('click', function() {
    const newElement = document.createElement('p');
    newElement.textContent = 'This is a new dynamically added paragraph.';
    document.getElementById('dynamicElements').appendChild(newElement);
});

document.getElementById('removeElementBtn').addEventListener('click', function() {
    const dynamicElements = document.getElementById('dynamicElements');
    if (dynamicElements.lastChild) {
        dynamicElements.removeChild(dynamicElements.lastChild);
    }
});

#css

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: white;
    padding: 20px;
    text-align: center;
}

h1 {
    margin: 0;
}

main {
    padding: 20px;
}

section {
    margin-bottom: 20px;
}

button {
    padding: 10px 20px;
    margin-top: 10px;
    cursor: pointer;
}

footer {
    background-color: #333;
    color: white;
    padding: 10px;
    text-align: center;
    position: absolute;
    bottom: 0;
    width: 100%;
}
