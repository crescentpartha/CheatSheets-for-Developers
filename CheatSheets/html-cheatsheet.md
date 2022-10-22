## Table of Contents

- [HTML CheatSheet for Developers](#html-cheatsheet-for-developers)
  - [Basic Tags of HTML](#basic-tags-of-html)
  - [Tags to Structure Document](#tags-to-structure-document)
  - [Semantic Elements](#semantic-elements)
  - [Links](#links)
  - [Images](#images)
  - [Lists](#lists)
  - [Forms](#forms)
  - [important attributes](#important-attributes)
  - [Tables](#tables)

# HTML CheatSheet for Developers

## Basic Tags of HTML

| Command                | Description                                                                                                                               |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `<html>...</html>`     | Tag can be thought of as a parent tag for every other tag used in the page.                                                               |
| `<head>...</head>`     | Tag is used to specify meta data about the webpage. It includes the webpage’s name,its dependencies (JS and CSS scripts), font usage etc. |
| `<body>...</body>`     | Container for all the contents of the webpage.                                                                                            |
| `<base/>`              | Used to specify the base URL of your site,this tag makes linking to internal links on your site cleaner.                                  |
| `<meta/>`              | Can be useful for mentioning the page’s author,keywords, original published date etc.                                                     |
| `<link/>`              | This is used to link to scripts external to the webpage. Typically utilized for including stylesheets.                                    |
| `<style>...</style>`   | The style tag can be used as an alternative to an external style sheet, or complement it.Includes the webpage’s appearance information.   |
| `<script>...</script>` | Used to add code snippets, typically in JavaScript,to make webpage dynamic. It can also be used to just link to an external script.       |

**[🔼Back to Top](#table-of-contents)**

## Tags to Structure Document

| Command                        | Description                                                                                                                    |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ |
| `<h1..h6> … </h1..h6>`         | Six different variations of writing a heading. `<h1>` Tag has the largest font size, while `<h6>` has the smallest.            |
| `<div>...</div>`               | A webpage’s content is usually divided into blocks, specified by the div tag.                                                  |
| `<span>...</span>`             | This tag injects inline elements, like an image, icon, emoticon without ruining the formatting/styling of the page.            |
| `<p>...</p>`                   | Plain text is placed inside the tag.                                                                                           |
| `<br>`                         | A Line Break for Webpages.It is used when wanting to write a new line.                                                         |
| `<hr/>`                        | In addition to switching to the next line, this tag also drawsa horizontal bar to indicate the end of the section.             |
| `<strike>...</strike>`         | Another old tag, this is used to draw a line atthe center of the text, so as to make it appearunimportant or no longer useful. |
| `<cite>...</cite>`             | Tag for citing author of a quote.                                                                                              |
| `<del>...</del>`               | Pre-formatted, ‘monospace’ text laid out with whitespace inside the element intact.                                            |
| `<ins> … </ins>`               | Denotes text that has been inserted into the webpage.                                                                          |
| `<blockquote> … </blockquote>` | Quotes often go into this tag. Is used in tandem with the <cite> tag.                                                          |
| `<q> … </q>`                   | Similar to the above tag, but for shorter quotes.                                                                              |
| `<abbr> … </abbr>`             | Denotes abbreviations, along with the full forms.                                                                              |
| `<address> … </address>`       | Tag for specifying author’s contact details.                                                                                   |
| `<dfn> … </dfn>`               | Tag dedicated for definitions.                                                                                                 |
| `<code> … </code>`             | This is used to display code snippets within a paragraph.                                                                      |
| `<sub> … </sub>`               | Used for writing a subscript (smaller font just below the mid-point of normal font).                                           |
| `<sup> … </sup>`               | Similar to the above tag, but for superscripting.                                                                              |
| `<small> … </small>`           | Reduces text size. In HTML5, it often refers to redundant or invalid information.                                              | 
| `<strong> … </strong>`         | This element indicates that its contents have strong importance or urgency. Browsers usualy render the contents in bold type.  |
| `<em> … </em>`                 | This tag is used to define emphasized text. The content inside is typically displayed in italic.  |

**[🔼Back to Top](#table-of-contents)**

## Semantic Elements

| Command                          | Description                                                                                 |
| -------------------------------- | ------------------------------------------------------------------------------------------- |
| `<article> ... </article>`       | Defines independent, self-contained content                                                 |
| `<aside> ... </aside>`           | Defines content aside from the page content                                                 |
| `<details> ... </details>`       | Defines additional details that the user can view or hide                                   |
| `<figcaption> ... </figcaption>` | Defines a caption for a `<figure>` element webpage.                                         |
| `<figure> ... </figure>`         | Specifies self-contained content, like illustrations, diagrams, photos, code listings, etc. |
| `<footer> ... </footer>`         | Defines a footer for a document or section                                                  |
| `<header> ... </header>`         | Specifies a header for a document or section                                                |
| `<main> ... </main>`             | Specifies the main content of a document                                                    |
| `<mark> ... </mark>`             | Defines marked/highlighted text                                                             |
| `<nav> ... </nav>`               | Defines navigation links                                                                    |
| `<section> ... </section>`       | Defines a section in a document                                                             |
| `<summary> ... </summary>`       | Defines a visible heading for a `<details>` element                                         |
| `<time> ... </time>`             | Defines a date/time                                                                         |

**[🔼Back to Top](#table-of-contents)**

## Links

| Command                         | Description                                                                                                                    |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| `<a href=””> … </a>`            | Anchor tag. Primarily used for including hyperlinks.                                                                           |
| `<a href=”mailto:”> … </a>`     | Tag dedicated to sending emails.                                                                                               |
| `<a href=”tel:###-###”> … </a>` | Anchor tag for mentioning contact numbers. As the numbers are clickable, this can be particularly beneficial for mobile users. |
| `<a name=”name”> … </a>`        | This tag can be used to quickly navigate to a different part of the webpage.                                                   |
| `<a href=”#name”> … </a>`       | A variation of the above tag, this is only meant to navigate to a div section of the webpage.                                  |

**[🔼Back to Top](#table-of-contents)**

## Images

| Command                  | Description                                                                                                                    |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------ |
| `<img />`                | A tag to display images in the webpage.                                                                                        |
| `src=”url”`              | The URL or path where the image is located on your drive or on the web.                                                        |
| `alt=”text”`             | The text written here is displayed when user hovers mouse over the image. Can be used to give additional details of the image. |
| `height=””`              | Specifies image height in pixels or percentages.                                                                               |
| `width=””`               | Specifies image width in pixels or percentages.                                                                                |
| `align=””`               | The relative alignment of the image. Can change with changes to other elements in the webpage.                                 |
| `border=””`              | Specifies border thickness of the image. If not mentioned, defaults to 0.                                                      |
| `<map> … </map>`         | Denotes an interactive (clickable) image.                                                                                      |
| `<map name=””> … </map>` | Name of the map associated between the image and the map.                                                                      |
| `<area />`               | Specifies image map area.                                                                                                      |
| `shape=””`               | Shape of the area.                                                                                                             |
| `coords=””`              | The coords attribute specifies the coordinates of an area in an image map.                                                     |

**[🔼Back to Top](#table-of-contents)**

## Lists

| Command        | Description                                                 |
| -------------- | ----------------------------------------------------------- |
| `<ol> … </ol>` | Tag for ordered or numbered list of items.                  |
| `<ul> … </ul>` | Contrary to the above tag, used for unorderedlist of items. |
| `<li> … </li>` | Individual item as part of a list.                          |
| `<dl> … </dl>` | Tag for list of items with definitions.                     |
| `<dt> … </dt>` | The definition of a single term inline with body content.   |
| `<dd> … </dd>` | The description for the defined term.                       |

**[🔼Back to Top](#table-of-contents)**

  
## Forms
  
```html
<form method="POST" action="/page">
  <label for="name">Page Name</label>
  <input id="name" type="text" name="page_name" />
  <input type="submit" value="Create" />
</form>
```

#### `<form>`'s Attributes

- **method**: the HTTP verb (method) that the browser uses to submit the form. We use "POST" to stand in for `POST`, `PUT` and `DELETE`.
- **action**: the path of the HTTP request page that processes the information submitted via the form.
- **the _route_**: is the combination of the verb (method) and path, and must be defined on our app for this form to submit data correctly.

```html
<form method="POST" action="/page">
  <input type="hidden" name="_method" value="PUT" />

  ...
</form>
```

We use a hidden input with an attribute `name="_method"`, and then set the value as the HTTP verb we wish to use.
**[🔼Back to Top](#table-of-contents)**

## HTML's Go-To Inputs

| Field Type | HTML Code | Notes |
|:-- |:-- |:-- |
| plain text | `<input type="text">` |  the type attribute can be omitted |
| password field | `<input type="password">` | echoes dots instead of characters |
| text area | `<textarea></textarea>`  | a more customizable plain text area |
| checkbox | `<input type="checkbox">`  | can be toggled on or off |
| radio button | `<input type="radio">` | can be grouped with other inputs |
| drop-down lists | `<select><option>`  | [check here for more info](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select) |
| file picker | `<input type="file">` |  pops up an “open file” dialog |
| hidden field | `<input type="hidden">`   | nothing there!
| submit button | `<input type="submit">` | activates the form's submission <br/>(a `POST` request or <br/>Javascript action) |

  **[🔼Back to Top](#table-of-contents)**
 
  
### Important Attributes

All input types (including `<textarea>`s):

- **`type`**: the type of data that is being input (affects the "widget" that is used to display this
  element by the browser).
- **`name`**: the key used to describe this data in the HTTP request.
- **`id`**: the unique identifier that other HTML elements, JavaScript and CSS use to access this 
  element in the browser.
- **`value`**: the default data that is assigned to the element.
- **`placeholder`**: not a default value, but a useful HTML5 addition of a data "prompt" for an input.
- **`disabled`**: a Boolean attribute indicating that the "widget" is not available for interaction.
  
**[🔼Back to Top](#table-of-contents)**
  
### Radio buttons or checkboxes:

- **`checked`**: a Boolean that indicates whether the control is selected by default (is false unless).
- **`name`**: the group to which this element is connected. For radio buttons, only one element per 
  group (or name) can be checked.
- **`value`**: the data or value that is returned for a specific group (a multi-element control), if 
  this element is checked.

**[🔼Back to Top](#table-of-contents)**

## Tables

| Command                    | Description                                                        |
| -------------------------- | ------------------------------------------------------------------ |
| `<table> … </table>`       | Marks a table in a webpage.                                        |
| `<caption> … </caption>`   | Description of the table is placed inside this tag.                |
| `<thead> … </thead>`       | Specifies information pertaining to specific columns of the table. |
| `<tbody> … </tbody>`       | The body of a table, where the data is held.                       |
| `<tfoot> … </tfoot>`       | Determines the footer of the table.                                |
| `<tr> … </tr>`             | Denotes a single row in a table.                                   |
| `<th> … </th>`             | The value of a heading of a table’s column.                        |
| `<td> … </td>`             | A single cell of a table. Contains the actual value/data.          |
| `<colgroup> … </colgroup>` | Used for grouping columns together.                                |
| `<col>`                    | Denotes a column inside a table.                                   |

**[🔼Back to Top](#table-of-contents)**
