Cascading Style Sheets -> appearance

Selector → Which element(s) to style.
Property → What to change.
Value → How to change it.

{
    p {
    color: blue;
    font-size: 20px;
    }
}

Use meaningful HTML elements whenever possible.
<h1>Title</h1>
<p>Paragraph</p>
Use <div> only as a generic container when no semantic element fits.

Universal Selector (*) //selects all elements
{
    * {
    color: purple;
    }
}

Type (Element) Selector
{
    div {
    color: white;
    }
}

Class Selector (.)
{
    .alert-text {
    color: red;
    }
} //✅ Multiple classes allowed

ID Selector (#)
{
    #title {
    background: red;
    }
}

Grouping Selector (,)
{
   ->insted of this:

    .read {
        color: white;
    }
    .unread {
        color: white;
    }

   ->we do this:

    .read,
    .unread {
        color: white;
    }
}

Chaining Selectors (No Space)
{
    <div class="subsection header"></div>

    .subsection.header {
        color: red;
    }

    Select elements that have both classes.
    
    ->Also works with IDs:
    
    .subsection#preview {
    color: blue;
    }

    Both must exist on the same element.
}

Descendant Combinator (Space)
{
    <div class="ancestor">
        <div class="contents"></div>
    </div>
    <div class="contents"></div>
    
    .ancestor .contents {
        color: red;
    }
    
    Matches the 1st div contents decendent of ancestor
    dosent match the 2nd dive
}

===========properties===========

color{
    Changes text color.
}
background-color{
    Changes an element's background color.
}
{
| Type    | Example                |
| ------- | ---------------------- |
| Keyword | `red`, `blue`, `black` |
| HEX     | `#ff0000`              |
| RGB     | `rgb(255,0,0)`         |
| HSL     | `hsl(0,100%,50%)`      |
}

font-family{
    Changes the font.
    font-family: "Times New Roman", serif;
    Browser tries fonts left → right.
}

font-size = Changes text size.

font-weight = Controls boldness.

text-align = Aligns text horizontally.

Image Size = use width, height

auto = It keeps the image's original proportions. ration{
    ex: original image = 1000*500 (width*height), ratio is 2:1
        i changed width to 500 therefor auto make height = 250 (500/2)
}

Why Specify Image Width & Height? = Browser reserves space before image loads. Prevents page content from jumping around (layout shift).

Add CSS = External CSS ⭐ (Recommended), Internal CSS, Inline CSS

CSS Priority (Highest → Lowest){
    Inline CSS
    Internal CSS
    External CSS
}

linking css = HTML <link> Tag <link rel="stylesheet" href="styles.css">


Cascade = The cascade is the set of rules that decides which CSS style gets applied when multiple CSS rules target the same element.

Specificity{
    Inline Style
      ↓
    ID Selector (#id)
      ↓
    Class Selector (.class)
      ↓
    Type Selector (div, p, h1)
      ↓
    Universal Selector (*)
}

Inheritance{
    Some CSS properties automatically pass from parent to children.

    Usually inherited:
    color
    font-size
    font-family
    font-weight

    Usually not inherited:
    display
    margin
    padding
    border
    width
    height
}

Rule Order{
    If specificity is exactly the same... The last rule written wins.

    .alert {
    color: red;
    }

    .warning {
        color: yellow;
    }


    final color = yellow
}

{
    Multiple CSS rules
        │
        ▼
    1. Higher Specificity?
        │
      Yes ───► Winner
        │
       No
        ▼
    2. Direct style vs Inherited?
        │
    Direct style wins
        │
        ▼
    3. Same specificity?
        │
        ▼
    Last written rule wins
}

{
    | Selector         | Specificity |
| ---------------- | ----------- |
| Inline style     | Highest     |
| `#id`            | High        |
| `.class`         | Medium      |
| `div`, `p`, `h1` | Low         |
| `*`              | None        |
}

{
    transition
    !important
    animation
    normal
}


Margin
 ┌──────────────────────┐
 │ Border               │
 │  ┌───────────────┐   │
 │  │ Padding       │   │
 │  │ ┌───────────┐ │   │
 │  │ │ Content   │ │   │
 │  │ └───────────┘ │   │
 │  └───────────────┘   │
 └──────────────────────┘

Margin collapses if 2 boxes one with margin 60px and other also 60px distance bwt them will be 60 px only
if 60 px and 70 px (greater one is taken under consideration) that will be 70px

paddin border content all together = width * height 
10 px  30 px  100*100 = 100+ 30*2 + 10*2 = 100+60+20 = 180*180

margin doesnt account in height width of actual element

to make sure widht and heigh doesnt change = box-sizing: border-box; // used all the time, and mostly kept in universal selector 


Outer Display Type

Determines how an element behaves relative to other elements.
display: block;
display: inline;

================================================

Inner Display Type

Determines how children inside the element are laid out.
display: flex; or grid



block, inline, flex, grid

| Element    | Default Display |
| ---------- | --------------- |
| `<div>`    | Block           |
| `<p>`      | Block           |
| `<h1>`     | Block           |
| `<ul>`     | Block           |
| `<span>`   | Inline          |
| `<a>`      | Inline          |
| `<strong>` | Inline          |
| `<em>`     | Inline          |


flex = creates a block-level flex container.
inline-flex = creates an inline flex container.


margin ,border, padding etc = trbl = top right bottom left (short hand) margin: 10px 20px 30px 2px;

1. Box Model Works Fully Only for Block Elements
2. Inline Elements (like <span>){
    ❌ Do NOT respect width and height
    ❌ Top/bottom margins don’t push other elements
    ⚠️ Top/bottom padding & borders don’t push layout (they can overlap text)
    ✅ Left/right margin, padding, border DO affect layout
}
span {
  width: 80px;
  height: 150px;
  margin: 20px 30px;
  padding: 10px 20px;
  border: 7px solid blue;
}

What actually happens:
width/height → ignored
margin-top/bottom → ignored
padding-top/bottom → expands box but overlaps nearby text
border-top/bottom → overlaps text
margin-left/right → works
padding-left/right → works

Solution: inline-block
{
    
    Behaves like inline:
    Stays on the same line
    
    Behaves like block:
    Respects width and height
    Respects all margins, padding, borders
    Pushes other elements properly

}

Result:
[Box] [Box] [Box]

Why inline-block is useful ->

Normally:

Padding may overlap surrounding layout

With inline-block:

Click area increases
Padding behaves correctly
Layout stays clean
==============================================

Navigation bars

Used in menus like:

Navbar links
Buttons
Tags
Pills

Even when ul uses flex:

display: flex;
Each <a> inside is still inline by default.
So padding may:

Visually overlap borders
Not affect layout spacing correctly

Fix:

.links-list a {
  display: inline-block;
}

| Feature                    | Inline  | Inline-block | Block |
| -------------------------- | ------- | ------------ | ----- |
| New line                   | ❌       | ❌            | ✅     |
| Width/height               | ❌       | ✅            | ✅     |
| Padding/margin (all sides) | Partial | Full         | Full  |
| Overlapping text           | Yes     | No           | No    |

auto Keyword

auto lets the browser decide margin automatically.

Most useful case:

Centering horizontally
.container {
  width: 980px;
  margin: 0 auto;
}
Why it works:
fixed width → element has a defined size
left + right margin = auto → remaining space is split equally

Result:

|     container centered     |


CSS Layout? = 
CSS layout controls where elements are placed on a webpage relative to:

Their default position
Other elements
Their parent container
The browser window (viewport)

Normal Flow = If no CSS changes the layout, elements follow Normal Flow.
Source Order = Elements appear in the same order as written in HTML.


Ways to Override Normal Flow{
    display{ Changes how an element behaves.
        display: block;
        display: inline;
        display: inline-block;
        display: flex;
        display: grid;
    }
    float{ Moves an element left or right.
        float: left;
        float: right;
    }
    position{Controls exact placement.
        position: static;    /* default */
        position: relative;
        position: absolute;
        position: fixed;
        position: sticky;
    }
    Flexbox{ Used for 1-dimensional layouts (row OR column).
        Perfect for:
            Navbar
            Centering
            Cards
            Buttons
            Menus
    }
    Grid{Used for 2-dimensional layouts (rows + columns).
        Perfect for:
            Full page layouts
            Dashboards
            Galleries
    }
    Responsive Design{ Makes websites work on different screen sizes.
        Main tool:
        @media
        Example:
        @media (max-width:600px) {
            ...
        }
    }
    Other Layout Methods{
        Less common:
            Table Layout (display: table)
            Multi-column Layout (newspaper-style columns)
    }
}



{center a element
1. display: block
2. must have a width
3. margin-left: auto;
4. margin-right: auto;
}


border: 2px solid red;
border-radius: 30px;

line-height:24px; #sets the height of input field (will be exact same to height: ;)
and more browsers honor.


normal non flex way to center = display inline | text-align: center (parent)

flex = wrap it into a container = display: flex; justify-content: center; to gap = marign left 10px rigth 10px  (scrimba)

justify-content = center, end, start, space-around, space-between