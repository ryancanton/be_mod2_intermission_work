# B2 Intermission Work

Answer these Check for Understanding questions as you work through the assignments.

## HTML

1. What is HTML?
  HTML, or HyperText Markdown Language, is a computer language used to create webpages.
1. What is an HTML element?
  An element is a piece of an HTML script that has a start tag and an end tag. For example, `<p>This is a paragraph element</p>`
1. What is an HTML attribute?
  An HTML attribute effects how an element appears on screen. Some examples are color, background color, size, positioning, etc. They are usually called in the in start tag, unless there is a CSS file dedicated to storing the different attribute specifications.
1. What is the difference between a class and an id? When would you use one vs. the other?
  Both a class and an id are identifiers for HTML elements, but a class can be applied to multiple elements while an id can only be applied to one. So, if you had a bunch of links for chapter summaries that send you further down in the web page, ids would be appropriate as each chapter has a unique location on the web page. Conversely, if you had several paragraphs that should be styled the exact same, a class would be appropriate.
1. What HTML would you write to create a form for a new dog with a "name" and an "age"?
  ```
  <form>
    <label for="name">Name:</label><br>
    <input type="text" id="name" name="name"><br>
    <label for="age">Age:</label><br>
    <input type="text" id="age" name="age">
  </form>
  ```
1. What are semantic tags? When would you use them over a `div`?
Semantic tags contain information about the function of the element. `<form>`
is an example, as it signifies that there will be some sort of user input. One
should use them over a div if one of the semantic tags applies directly to its contents. If ambiguous, a div tag will do.
1. Explain what each of the following HTML tags do and when you would use them:
  * `<h1>`, `<h2>`, etc.
    These are headers. They enlarge text with h1 being the largest and h6 the smallest.
  * `<p>`
    This is a paragraph element. It displays the text in between the tags.
  * `<body>`
    The body tag specifies where the webpage starts and ends. It ensures a separation from the `<head>`, which contains the web address.
  * `<a>` and the `href` attribute
    This tag creates an element that acts as a link to another webpage, or a different part of the current webpage. The href attribute explicitly defines where the link should lead.
  * `<img>` and the `src` attribute
    This tag creates and image that is visible on the webpage. The src attribute is the source of the image (sometimes a webpage sometimes stored locally).
  * `<div>`
    The div tag is used to hold other HTML elements, usually for styling purposes. It can have a class or id, but without any elements inside of it, it doesn't do much of anything.
  * `<section>`
    The section tag separates and defines sections of a webpage. From my testing, it intrinsically effects the elements contained inside it, unlike div (My headers always became smaller when inside a section tag).
  * `<ul>`, `<ol>`, and `<li>`.
    `<ul>` is an unordered list that contains `<li>`, or list elements usually separated with bullet points. `<ol>` stands for ordered list, and will contain `<li>` list elements that are numbered or lettered or counted in some other way.
  * `<form>` The form tag indicates a section that takes input from the user. It can be a text box, a radio button, or other forms      
    of accepting input
  * `<input>` The input tag is used after the form to specify how the user will input its data. See above for examples.

 ## CSS

1. What is CSS? CSS, or Cascading Style Sheets, is the language used to style web pages.

1. What is a CSS selector? How do you use the ID selector? The class selector? Selectors are like a code that contains specific styling instructions. Any HTML elements that have the selector will use the specified styling. IDs can only be used on one element, while classes are used for multiple elements.

1. What are the three ways to include CSS in your HTML documents? What are the pros and cons of each? It can be done inline, which is useful for short styling specs, but is bad if you want to use that styling for multiple elements. It can be done internally, with a style tag at the top of an HTML page. This is useful for styling multiple elements the same, but it can drastically increase the length of the HTML document. It can be done externally on a file, which is good for stykeing multiple elements the same without increasing the length of the document, but it can be difficult to tell how the web page is styled just from looking at the HTML doc.

1. What is the Box Model? Describe each component of the Box Model. The box model represents the layout of a webpage. It contains:
Content - The content of the box, where text and images appear
Padding - Clears an area around the content. The padding is transparent, unless styled otherwise
Border - A border that goes around the padding and content
Margin - The transparent area outside the border

## SQL

### Jumpstart Lab Tutorial

1. What is a database? A database is a data grouped by rows and columns. It is similar to an array of objects that all have
the same attribute types.
1. What is SQL? SQL, or Structured Query Language, is a language used to access and manipulate databases.
1. What is SQLite3? SQLite3 is a sub-language of SQL with specific keywords used to create, manipulate, and access databases.
1. What is a Table? A table is a combination of rows and columns that store data.
1. What is a primary key? It is a key that defines a row in a table. It contains unique, non-null values.
1. What is a foreign key? A foreign key is used to show that the value is used on multiple tables.
1. Explain what each of the following SQL commands do:
  * insert - used to create new data in a table with specified values
  * select - used to access rows/columns of a table
  * where - used to limit/specify where select or insert is used
  * order by - used to organize table according to specified order
  * inner join - used to combine multiple tables at specified row

### PG Exercises

1. How can you limit which columns you select from a table? Specify which columns you want returned after keyword SELECT
1. How can you limit which rows you select from a table? After WHERE, make a conditional statement that limits which rows are returned.
1. How can you give a selected column a different name in your output? Use the AS keyword. Ex: cd.faculty.name AS 'Faculty Member'
1. How can you sort your output from a SQL statement? Use the ORDER BY keywords; you can choose which row you want to organize by, in increasing or descending order.
1. What is joining? When do you need to join? Joining is combining two or more tables that have an identical column. It can be used to view how data relates across tables.
1. What is an aggregate function? An aggregate function combines data from a table to create values
1. List three aggregate functions and what they do. COUNT-counts number of columns
SUM-adds values of specified columns
AVG-averages values of specified column
1. What does the `group` statement do? The `group` keyword can be used to separate aggregate functions by a specified column
1. How does the `group` statement relate to aggregates? See above.

## Rails Tutorial: Task Manager

**Copy and Paste the link to your Task Manager repo here:** https://github.com/ryancanton/task_manager
**Copy and Paste the link to your Static Challenge here:** https://github.com/ryancanton/static_challenges

1. Define CRUD. Create, read, update, delete: These are the four base operations of database management, and nearly every application should be able to do them.
1. Define MVC. Model-view-controller is a way of thinking about how an application works. A user interacts with a controller, which changes the model of data, which updates the view for the user.
1. What three files would you need to create/modify for a Rails application to respond to a `GET` request to `/tasks`, assuming you have a `Task` model. You would need to ensure there is a controller for the tasks that defines any methods used in the `GET` request; you will need an html(.erb) file that will update the view from the user, and you will need a route in your routes folder that says where specifically to go and what to do in /tasks.
1. What are params? Where do they come from? Rails takes the parameters that are received from controller requests and turns it into a params object that can be manipulated inside of an application. These parameters can come from HTML forms, i.e. the user.
1. Check out your routes. Why do we need two routes each for creating a new Task and editing an existing Task? We need two routes because they each have a unique HTML, and the edit and create methods do not do the same thing (edit first has to acquire the object from the db before updating it, while create starts from scratch).
