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

Interpreted vs Compiled
Interpreted Language
Runs directly from source code.
JavaScript is mainly interpreted.
Compiled Language
Converted into machine code before running.
Examples:
C
C++

Modern JavaScript engines use Just-In-Time (JIT) Compilation to improve speed.


Client-side vs Server-side JavaScript

Client-side
Runs in the browser. buttons, animation, etc.

Server-side
Runs on the server.
Example:
Node.js
Used for:
Databases

Dynamic vs Static Websites

Static Website
Same content for every user.
Doesn't change automatically.
Dynamic Website
Content changes based on:
User actions
Database data
Time
Server responses



Adding JavaScript to HTML
{
    <script>
        console.log("Hello");
    </script>
}
before = </body>

External JavaScript (Recommended)
{
    <script type="module" src="script.js"></script>
}

Inline JavaScript (Not Recommended)
{
    <button onclick="hello()">
}


Event Listeners = Preferred way to handle events.
{
    button.addEventListener("click", function(){
        console.log("Clicked");
    });
}