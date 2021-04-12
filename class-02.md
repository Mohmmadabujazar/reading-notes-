# HTML
```
Chapter 2 (Links to an external site.)
Text (Links to an external site.)
Structural markup:
the elements that you can use to describe both headings and paragraphs

headings

HTML has six “levels” of headings:

(h1) is used for main headings

(h2) is used for subheadings

(h3) element is used If there are further sections under the subheadings

heading tags write between <>
example :

This is a Main Heading
This is a Level 2 Heading (Links to an external site.)
This is a Level 3 Heading (Links to an external site.)
This is a Level 4 Heading (Links to an external site.)
This is a Level 5 Heading (Links to an external site.)
This is a Level 6 Heading (Links to an external site.)
Paragraph

To create a paragraph, surround the words that make up the paragraph with an opening (p) tag and closing (/p) tag.

paragraph tags write between <>
Semantic markup:
which provides extra information; such as where emphasis is placed in a sentence, that something you have written is a quotation (and who said it), the meaning of acronyms, and so on

There are some text elements that are not intended to affect the structure of your web pages, but they do add extra information to the pages — they are known as semantic markup.

Strong
The use of the (strong) element indicates that its content has strong importance. For example, the words contained in this element might be said with strong emphasis.

strong tags write between <>
example :

“<p>Beware: Pickpockets operate in this area.</p>

This toy has many small pieces and is not suitable for children under five years old.

”

Changes to Content
S tag
The (s) element indicates something that is no longer accurate or relevant (but that should not be deleted). Visually the content of an (s) element will usually be displayed with a line through the center.

s tags write between <>
example :

Laptop computer:

Was $995

Now only $375

Auth or Details
(address)
The (address) element has quite a specific use: to contain contact details for the author of the page.

address tags write between <>
example :

homer@example.org

742 Evergreen Terrace, Springfield.
```
# CSS
```
Chapter 10 (Links to an external site.)
Introducing CSS (Links to an external site.)
CSS allows you to create rules that specify how the content of an element should appear. For example, you can specify that the background of the page.

CSS Associates Style rules with HTML elements: (Links to an external site.)
CSS works by associating rules with HTML elements. These rules govern how the content of specified elements should be displayed. A CSS rule contains two parts: a selector and a declaration.
Selectors
indicate which element the rule applies to. The same rule can apply to more than one element if you separate the element names with commas.

Declarations
indicate how the elements referred to in the selector should be styled. Declarations are split into two parts (a property and a value), and are separated by a colon.

How Elements Are Displayed ? (Links to an external site.)
CSS declarations sit inside curly brackets and each is made up of two parts: a property and a value, separated by a colon. You can specify several properties in one declaration, each separated by a semi-colon.
Properties
indicate the aspects of the element you want to change. For example, color, font, width, height and border.

Values
specify the settings you want to use for the chosen properties. For example, if you want to specify a color property then the value is the color you want the text in these elements to be.

HOW Using External CSS ? (Links to an external site.)
link (Links to an external site.)
The (link) element can be used in an HTML document to tell the browser where to find the CSS file used to style the page. It is an empty element (meaning it does not need a closing tag), and it lives inside the <head> element. It should use three attributes:

href
This specifies the path to the CSS file (which is often placed in a folder called css or styles).

type
This attribute specifies the type of document being linked to. The value should be text/css.

rel
This specifies the relationship between the HTML page and the file it is linked to. The value should be styleshee

HOW Usi ng Internal CSS ? (Links to an external site.)
(style) (Links to an external site.)
You can also include CSS rules within an HTML page by placing them inside a (style) element, which usually sits inside the (head) element of the page.
```
# JavaScript
```
Chapter 2 (Links to an external site.)
Basic JavaScript Instructions (Links to an external site.)
GIVING INSTRUCTIONS:

FOR A BROWSER TO FOLLOW Web browsers (and computers in general) approach tasks in a very different way than a human might. Your instructions need to reflect how computers get things done.

STATEMENTS
A script is a series of instructions that a computer can follow one-by-one. Each individual instruction or step is known as a statement. Statements should end with a semicolon.

COMMENTS
You should write comments to explain what your code does. They help make your code easier to read and understand. This can help you and others who read your code.

MULTI-LINE COMMENTS
To write a comment that stretches over more than one line, you use a multi-line comment, starting with the / * characters and ending with the * / characters. Anything between these characters is not processed· by the JavaScript interpreter.

SINGLE-LINE COMMENTS
In a single-line comment, anything that follows the two forward slash characters // on that line will not be processed by the JavaScript interpreter. Singleline comments are often used for short descriptions of what the code is doing.

VARIABLE
A variable is a good name for this concept because the data stored in a variable can change (or vary) each time a script runs.

Expressions
An expression evaluates into (results in) a single value. Broadly speaking there are two types of expressions.

EXPRESSIONS THAT JUST ASSIGN A VALUE TO A VARIABLE
EXPRESSIONS THAT USE TWO OR MORE VALUES TO RETURN A SINGLE VALUE
Operators
Expressions rely on things called operators; they allow programmers to create a single value from one or more values.

Chapter 4 (Links to an external site.)
Decisions and Loops (Links to an external site.)
DECISIONS
Using the results of evaluations, you can decide which path your script should go down.

DECISIONS MAKING

LOOPS
There are also many occasions where you will want to perform the same set of steps repeatedly.

Loops check a condition. If it returns true, a code block will run. Then the condition will be checked again and if it still returns true, the code block will run again. It repeats until the condition returns false. types of loops:

FOR LOOP
If you need to run code a specific number of times, use a for loop. (It is the most common loop.) In a for loop, the condition is usually a counter which is used to tell how many times the loop should run

The For Loop The for loop has the following syntax:

for (statement 1; statement 2; statement 3) {

// code block to be executed

}

Example
for (i = 0; i < 5; i++) {

text += “The number is “ + i + (“br”);

}

WHILE LOOP
If you do not know how many times the code should run, you can use a while loop. Here the condition can be something other than a counter, and the code will continue to loop for as long as the condition is true

The While Loop The while loop loops through a block of code as long as a specified condition is true.

Syntax
while (condition) {

// code block to be executed

}

Example
while (i < 10) {

text += “The number is “ + i; i++;
} 
```