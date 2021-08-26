# CSS Questions.

## 1. Explain the CSS position property.

**Absolute** To place an element exactly where you want to place it. absolute position is actually set relative to the element's parent. if no parent is available then the relative place to the page itself (it will default all the way back up to the element).

**Relative** "Relative to itself". Setting position: relative; on an element and no other positioning attributes, it will no effect on its positioning. It allows the use of z-index on the element and it limits the scope of absolutely positioned child elements. Any child element will be absolutely positioned within that block. 

**Fixed** The element is positioned relative to the viewport or the browser window itself. viewport doesn't change if you scroll and hence the fixed element will stay right in the same position. 

**Static** Static default for every single page element. The only reason you would ever set an element to position: static is to forcefully-remove some positioning that got applied to an element outside of your control.

**Sticky** Sticky positioning is a hybrid of relative and fixed positioning. The element is treated as relative positioned until it crosses a specified threshold, at which point it is treated as fixed positioned.

**Notes**  
The key points here are that the candidate knows the difference between absolute and relative positioning and how they work together alongside knowing what fixed is.

---

## 2. What is the difference between “display: none” and “visibility: hidden”, when used as attributes to the HTML element.

When we use the attribute “visibility: hidden” for an HTML element then that element will be hidden from the webpage but still takes up space. Whereas, if we use the “display: none” attribute for an HTML element then the element will be hidden, and also it won’t take up any space on the webpage.

**Notes:**  
This mainly shows an understanding of CSS in more detail, this is a common issue with people who don't really _know_ how to use CSS and simply just _use it_ instead of understand it.

---

## 3. What is the Box model in CSS and which CSS properties are a part of it?

A rectangle box is wrapped around every HTML element. The box model is used to determine the height and width of the rectangular box. The CSS Box consists of Width and height (or in the absence of that, default values and the content inside), padding, borders, margin.

- **Content:** Actual Content of the box where the text or image placed.
- **Padding:** Area surrounding the content (Space between the border and content).
- **Border:** Area surrounding the padding.
- **Margin:** Area surrounding the border.

**Notes**  
This is basic CSS, and they should be able to explain this.

---

## 4. What is the difference between inline, inline-block, and block?

**Block Element:**  
The block elements always start on a new line. They will also take space for an entire row or width. List of block elements are `<div>`, `<p>`.

**Inline Elements:**  
Inline elements don't start on a new line, they appear on the same line as the content and tags beside them. Some examples of inline elements are `<a>`, `<span>` , `<strong>`, and `<img>` tags. 

**Inline Block Elements:**  
Inline-block elements are similar to inline elements, except they can have padding and margins added on all four sides.

**Notes**  
This is basic CSS, so this should be understood.

---

## 5. What are a pseudo elements and pseudo-classes and what is the difference?

Pseudo-classes select regular elements but under certain conditions like when the user is hovering over the link.

- `:link`
- `:visited`
- `:hover`
- `:active`
- `:focus`

Example of the pseudo-class, In the below example, the color applies to the anchor tag when it’s hovered.

```css
/* mouse over link */
a:hover {
	color: #FFOOFF;
}
```

A pseudo-element however allows us to create items that do not normally exist in the document tree, for example `::after`.

- `::before`
- `::after`
- `::first-letter`
- `::first-line`
- `::selection`

In the below example, the color will appear only on the first line of the paragraph.

```css
p: :first-line {
	color: #ffOOOO;
	font-variant: small-caps;
}
```

**Notes**  
As long as the candidate can explain examples of the above, so what before or after is, and hover, active, etc, that is enough.

---

## 6. Explain the different box sizing properties?

The box-sizing CSS property sets how the total width and height of an element are calculated.

`content-box`  
The default width and height values apply to the element's content only. The padding and border are added to the outside of the box.

`padding-box`  
Width and height values apply to the element's content and its padding. The border is added to the outside of the box. Currently, only Firefox supports the padding-box value.

`border-box`  
Width and height values apply to the content, padding, and border.

**Notes:**  
This is a common issue when setting up websites for the first time and can affect how margin/padding affect elements, so it's definitely a key item to understand.