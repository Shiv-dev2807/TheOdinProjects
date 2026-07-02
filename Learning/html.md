HyperText Markup Language

element = openingtag  content  closingtab -> <p>hi</p> {tag = <p>}

void elements = no content {ex: <br>, <img>}
self closing tags = {ex: <br />, <img />}

{
    
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>My First Webpage</title>
  </head>

  <body>
    <h1>Hello World!</h1>
  </body>
</html>

}



.html
homepage = index.html

<!DOCTYPE html> -> Tells the browser to use HTML5. (always use this)
<html>  -> root element -> Everything on the page goes inside it.
<html lang="en"> -> Specifies the page language. (improves accessibility)
<head> -> Contains metadata
<meta charset="UTF-8"> ->Sets character encoding. Ensures special characters and different languages display correctly.
<title> -> Sets the title shown in the browser tab. (<title>My First Webpage</title>)
<body> Contains everything the user sees{
    Headings
    Paragraphs
    Images
    Links
    Lists
    Buttons
    Forms
}
<p> -> paragraph
headigns = {
    <h1>
    <h2>
    <h3>
    <h4>
    <h5>
    <h6>
}
bold/strong = <strong> <b> //use strong
italic/emphasis = <em> <i>  //use em
nesting structure = HTML elements can be placed inside other elements → called nesting.{
    Parent → outer element
    Child → inside element
    Siblings → elements at the same level
}
ex: {
    <body>
        <p>This is a <strong>bold</strong> word.</p>
    </body>
}
Comments = Used to write notes in code that are not shown in the browser.