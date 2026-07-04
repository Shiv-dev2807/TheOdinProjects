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