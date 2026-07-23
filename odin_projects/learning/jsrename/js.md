JavaScript (JS) is a scripting/programming language used to make web pages interactive and dynamic.

example = 
button.addEventListener("click", updateName);
When the button is clicked, the updateName() function runs.

JavaScript APIs
examples = 
DOM API → Change HTML/CSS
Geolocation API → Get user's location
Canvas/WebGL API → 2D & 3D graphics
Audio & Video APIs → Multimedia support

Third-party APIs

Examples:
Google Maps API
OpenStreetMap API
Bluesky API


{
    HTML → Structure
    CSS → Styling
    JavaScript → Interactivity
}

JavaScript Execution Order

JavaScript usually runs from top to bottom.
example = 

const button = document.querySelector("button");
button.addEventListener("click", updateName);

The variable must be created before it is used, otherwise you'll get errors like:
ReferenceError
