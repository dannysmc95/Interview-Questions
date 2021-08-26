# HTML Questions.

## 1. What are void elements in HTML?

HTML elements which do not have closing tags or do not need to be closed are Void elements. For Example `<br />`, `<img />`, `<hr />`, etc.

**Notes:**  
We are really just checking they know that void elements are simply self closing elements, it's not very common, this is more of a question to see if they have heard of it before.

---

## 2. What are HTML Entities?

In HTML some characters are reserved like `<`, `>`, `/`, etc. To use these characters in our webpage we need to use the character entities called HTML Entities. Below are a few mapping between the reserved character and its respective entity character to be used.

| Character | Entity Name | Entity Number |
| :-: | :-: | :-: |
| `<` | `&lt;` | `&#60;` |
| `>` | `&gt;` | `&#62;` |
| `&` | `&amp;` | `&#38;` |

---

## 3. What are the various formatting tags in HTML (list a few)?

HTML has various formatting tags:

- `<b>` - makes text bold.
- `<i>` - makes text italic.
- `<em>` - makes text italic but with added semantics importance (italic).
- `<big>` - increases the font size of the text by one unit.
- `<small>` - decreases the font size of the text by one unit.
- `<sub>` - makes the text a subscript.
- `<sup>` - makes the text a superscript.
- `<del>` - displays as strike out text.
- `<strong>` - marks the text as important (bold).
- `<mark>` - highlights the text.
- `<ins>` - displays as added text.

**Notes:**  
Here you are just checking they understand what these are, and how to use them, the most common ones being `strong`, and `em`.

---

## 4. When to use scripts in the head and when to use scripts in the body?
If the scripts contain some event-triggered functions or jquery library then we should use them in the head section. If the script writes the content on the page or is not inside a function then it should be placed inside the body section at the bottom. In short, follow below three points:

- Place library scripts or event scripts in the head section.
- Place normal scripts that do not write anything on the page, in the head section until there is any performance issue.
- Place scripts that render something on the web page at the bottom of the body section.

**Notes:**  
The main aim of this question is for them to say that scripts loaded in the head will slow down the page load speed, as the page will wait for the scripts to load before it can start rendering the page, whereas when in the body, the page can load faster.

---

## 5. What are Semantic Elements?

Semantic elements are those which describe the particular meaning to the browser and the developer. Elements like `<form>`, `<table>`, `<article>`, `<figure>`, etc., are semantic elements.

**Notes:**  
This is to push for using the semantic elements as much as possible, for example when writing HTML, the developer should be aiming to write code that is clear and easy to understand, using semantic elements will help the developer to understand the code and from a screen reader's perspective, it will make the code more accessible.
