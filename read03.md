


# Using CSS

CSS can be added to HTML documents in 3 ways:

Inline - by using the style attribute inside HTML elements
Internal - by using a <style> element in the <head> section
External - by using a <link> element to link to an external CSS file
The most common way to add CSS, is to keep the styles in external CSS files. However, in this tutorial we will use inline and internal styles, because this is easier to demonstrate, and easier for you to try it yourself.

Inline CSS
An inline CSS is used to apply a unique style to a single HTML element.

An inline CSS uses the style attribute of an HTML element.

The following example sets the text color of the <h1> element to blue, and the text color of the <p> element to red:

Example
<h1 style="color:blue;">A Blue Heading</h1>

<p style="color:red;">A red paragraph.</p>
Try it Yourself » (Links to an external site.)
ADVERTISEMENT


Internal CSS
An internal CSS is used to define a style for a single HTML page.

An internal CSS is defined in the <head> section of an HTML page, within a <style> element.

The following example sets the text color of ALL the <h1> elements (on that page) to blue, and the text color of ALL the <p> elements to red. In addition, the page will be displayed with a "powderblue" background color: 

Example
<!DOCTYPE html>
<html>
<head>
<style>
body {background-color: powderblue;}
h1   {color: blue;}
p    {color: red;}
</style>
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
Try it Yourself » (Links to an external site.)
External CSS
An external style sheet is used to define the style for many HTML pages.

To use an external style sheet, add a link to it in the <head> section of each HTML page:

Example
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="styles.css">
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
Try it Yourself » (Links to an external site.)
The external style sheet can be written in any text editor. The file must not contain any HTML code, and must be saved with a .css extension.

Here is what the "styles.css" file looks like:

"styles.css":
body {
  background-color: powderblue;
}
h1 {
  color: blue;
}
p {
  color: red;
}
Tip: With an external style sheet, you can change the look of an entire web site, by changing one file!

CSS Colors, Fonts and Sizes
Here, we will demonstrate some commonly used CSS properties. You will learn more about them later.

The CSS color property defines the text color to be used.

The CSS font-family property defines the font to be used.

The CSS font-size property defines the text size to be used.

Example
Use of CSS color, font-family and font-size properties:

<!DOCTYPE html>
<html>
<head>
<style>
h1 {
  color: blue;
  font-family: verdana;
  font-size: 300%;
}
p {
  color: red;
  font-family: courier;
  font-size: 160%;
}
</style>
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
Try it Yourself » (Links to an external site.)
CSS Border
The CSS border property defines a border around an HTML element.

Tip: You can define a border for nearly all HTML elements.

Example
Use of CSS border property: 

p {
  border: 2px solid powderblue;
}
Try it Yourself » (Links to an external site.)
CSS Padding
The CSS padding property defines a padding (space) between the text and the border.

Example
Use of CSS border and padding properties:

p {
  border: 2px solid powderblue;
  padding: 30px;
}
Try it Yourself » (Links to an external site.)
CSS Margin
The CSS margin property defines a margin (space) outside the border.

Example
Use of CSS border and margin properties:

p {
  border: 2px solid powderblue;
  margin: 50px;
}
Try it Yourself » (Links to an external site.)
Link to External CSS
External style sheets can be referenced with a full URL or with a path relative to the current web page.

Example
This example uses a full URL to link to a style sheet:

<link rel="stylesheet" href="https://www.w3schools.com/html/styles.css">
Try it Yourself » (Links to an external site.)

Example
This example links to a style sheet located in the html folder on the current web site: 

<link rel="stylesheet" href="/html/styles.css">