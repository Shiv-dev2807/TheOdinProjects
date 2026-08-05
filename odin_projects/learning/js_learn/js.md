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


Script Loading
JavaScript should run after HTML is loaded.

Methods:

Put <script> before </body>

Use:
<script type="module" src="script.js"></script>

Use:
<script defer src="script.js"></script>


Comments
{
    // This is a comment

    /*
        This is
        a comment
    */
}


alert() // pop up on top

Variable = A variable is a “named storage” for data. We can use variables to store goodies, visitors, and other data.

{
    let message = 'Hello!';
    alert(message);
}

{
    let user = 'John', age = 25, message = 'Hello';

    let user = 'John';
    let age = 25;
    let message = 'Hello';

    let user = 'John',
      age = 25,
      message = 'Hello';
    
    let user = 'John'
      , age = 25
      , message = 'Hello';
}

let
Modern variable.

const
Cannot change.

var
Old JavaScript.

Declaring twice= 

let message = "Hello";
message = "World";


Naming = 
{
    let user;
    let user123;
    let user_name;
    let $money;
}

camelCase = {let myName;}

Case Sensitive

let apple = 5;
let Apple = 10; //both are not same

Reserved Words
Cannot use
let
return
class
function
if
else

Strict Mode Without strict mode 
num = 5;
JavaScript automatically creates the variable.
Bad practice.
{
Use
"use strict";

Then
num = 5;

Error.
}
Correct{
    "use strict";
    let num = 5;
}


Constants

If value never changes
Use
const PI = 3.14159;

Uppercase Constants = Use uppercase only for fixed values known before the program runs.
const COLOR_RED = "#F00";
const MAX_USERS = 100;

good variable names = {
    let studentName;
    let totalMarks;
    let shoppingCart;
    let currentUser;
}

Don't Reuse Variables

Real-Life Example

let userName = "Shiv";
let age = 20;
let isStudent = true;
console.log(userName);
console.log(age);
console.log(isStudent);

summary 
| Keyword | Can Change? | Modern? | Use When           |
| ------- | ----------- | ------- | ------------------ |
| `let`   | ✅ Yes       | ✅ Yes   | Normal variables   |
| `const` | ❌ No        | ✅ Yes   | Fixed values       |
| `var`   | ✅ Yes       | ❌ Old   | Avoid in modern JS |

{
    Use let for values that can change.
    Use const for values that should never change.
    Avoid var in modern JavaScript.
    Give variables meaningful camelCase names (shoppingCart, currentUser).
    Declare a variable only once; after that, update it without let.
}

Number int float

num.toFixed(2) //decimal
"74" 74 not same


string -> number = 
{
    let x = "74";
    x = Number(x);
    x += 3;
    console.log(x);
}

Check type

typeof "74"
// string

typeof 74
// number


Arithmetic Operators

| Operator | Meaning        | Example | Result |
| -------- | -------------- | ------- | ------ |
| `+`      | Addition       | `5+2`   | 7      |
| `-`      | Subtraction    | `5-2`   | 3      |
| `*`      | Multiplication | `5*2`   | 10     |
| `/`      | Division       | `10/2`  | 5      |
| `%`      | Remainder      | `8%3`   | 2      |
| `**`     | Power          | `5**2`  | 25     |

Operator Precedence (Order of Operations)

JavaScript follows normal math rules (PEMDAS/BODMAS).
()
**
* / %
+ -

Increment (++)

let x = 5;
x++;

Prefix ++x Increment first. then returns
Postfix x++ Return current value. Then increment.

Decrement (--)

let x = 5;
x--;

Assignment Operators
x = x + 5; => x += 5;

| Operator | Shortcut   | Meaning |
| -------- | ---------- | ------- |
| `=`      | Assignment | `x=5`   |
| `+=`     | Add        | `x=x+5` |
| `-=`     | Subtract   | `x=x-5` |
| `*=`     | Multiply   | `x=x*5` |
| `/=`     | Divide     | `x=x/5` |

Comparison Operators
| Operator | Meaning               |
| -------- | --------------------- |
| `===`    | Equal                 | (strict compares even the type of data)
| `!==`    | Not equal             | (compares type of data aswell)
| `<`      | Less than             |
| `>`      | Greater than          |
| `<=`     | Less than or equal    |
| `>=`     | Greater than or equal |

==, != (does not compare the datatype)
bool = true and false

Math.random() b/w 0 to 1

Math.floor(5.9) Rounds down.
Math.ceil(5.1) Rounds up.
num.toFixed(2)


operator performs an operation


Unary Operator = Works on one operand.
let x = 5;
-x
op = -5

Binary Operands = 5 - 2 = 3
| Operator | Meaning        | Example  |
| -------- | -------------- | -------- |
| `+`      | Addition       | `5+2=7`  |
| `-`      | Subtraction    | `5-2=3`  |
| `*`      | Multiplication | `5*2=10` |
| `/`      | Division       | `10/2=5` |
| `%`      | Remainder      | `5%2=1`  |
| `**`     | Power          | `2**3=8` |


String Concatenation using +