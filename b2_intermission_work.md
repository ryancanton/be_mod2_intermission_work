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
  * `<ul>`, `<ol>`, and `<li>`
    `<ul>` is an unordered list that contains `<li>`, or list elements usually separated with bullet points. `<ol>` stands for ordered list, and will contain `<li>` list elements that are numbered or lettered or counted in some other way.
  * `<form>`
  * `<input>`

 ## CSS

1. What is CSS?
1. What is a CSS selector? How do you use the ID selector? The class selector?
1. What are the three ways to include CSS in your HTML documents? What are the pros and cons of each?
1. What is the Box Model? Describe each component of the Box Model.

## SQL

### Jumpstart Lab Tutorial

1. What is a database?
1. What is SQL?
1. What is SQLite3?
1. What is a Table?
1. What is a primary key?
1. What is a foreign key?
1. Explain what each of the following SQL commands do:
  * insert
  * select
  * where
  * order by
  * inner join

### PG Exercises

1. How can you limit which columns you select from a table?
1. How can you limit which rows you select from a table?
1. How can you give a selected column a different name in your output?
1. How can you sort your output from a SQL statement?
1. What is joining? When do you need to join?
1. What is an aggregate function?
1. List three aggregate functions and what they do.
1. What does the `group` statement do?
1. How does the `group` statement relate to aggregates?

## Rails Tutorial: Task Manager

**Copy and Paste the link to your Task Manager repo here:**
**Copy and Paste the link to your Static Challenge here:**

1. Define CRUD.
1. Define MVC.
1. What three files would you need to create/modify for a Rails application to respond to a `GET` request to `/tasks`, assuming you have a `Task` model.
1. What are params? Where do they come from?
1. Check out your routes. Why do we need two routes each for creating a new Task and editing an existing Task?
