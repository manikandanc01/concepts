# Basics of HTML and CSS

## Introduction 

**HTML** (Hypertext Markup Language) and **CSS** (Cascading Style Sheets) are the foundational technologies used to create and design web pages. HTML provides the structure while CSS handles the visual representation.

## HTML Structure 

HTML is the skeleton of a webpage. It consists of a series of elements, each represented by tags, that define the content and layout of the page

### Boilerplate Code

By pressing '!' and enter in an HTML file, it gives a boilerplate code.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

This is the initial structure of the HTML code.

### Boilerplate Code Explanation

- `<!DOCTYPE html>` : This declaration defines the document type and version of HTML 5 being used. 

- `<html lang="en">` : The <html> tag is the root element of an HTML document. The lang="en" attribute specifies the language of the content as English.

- `<head>` : The <head> section contains meta-information about the document, such as the character set, title, and linked resources like CSS stylesheets.

-  `<meta charset="UTF-8">` : This meta tag specifies the character encoding for the document, ensuring that it supports a wide range of characters.

- `<body>` : The <body> tag encloses all the visible content of the webpage, such as text, images, links, and more.

### Encoding 

Character encoding is a system used to represent text data in computers.

#### Fixed-length encoding

- In early times, people used fixed-length encoding and faced some issues decoding the special characters, space, etc..

- Example :

    - **ASCII** : Each character in ASCII is represented in 7 or 8 bits. It doesn't support special characters.

#### Variable-length encoding

- Variable-length encoding assigns a different number of bits to each character, depending on the character's complexity, frequency, or other factors.

- Flexibility : It can handle a vast range of characters from different languages without requiring a fixed, large number of bits for each character.

- Example
    - **UTF-8** : UTF-8 is a variable-length encoding scheme that uses 1 to 4 bytes per character. 

## HTML Elements

- `<h1> to <h6>`: Heading elements (`<h1> to <h6>`) are used to define headings in the document, with `<h1>` being the highest level and `<h6>` the lowest.

    ```html
    <h1>Main Heading</h1>
    <h2>Subheading Level 1</h2>
    <h3>Subheading Level 2</h3>
    ```

- `<p>` : The `<p>` element defines a paragraph of text.

    ```html
    <p>This is a paragraph of text in HTML.</p>
   ```

- `<a>` : The `<a>` element creates a link to another webpage or resource.

    ```html
    <a href="https://www.example.com">Visit Example.com</a>
    ```
- `<img>` : The `<img>` element is used to create an image in the document. The src attribute specifies the image's source URL, and the alt attribute provides alternative text.

    ```html
    <img src="image.jpg" alt="A description of the image">

    ```
- `<ul>` and `<li>`: The `<ul>` element defines an unordered list, and `<li>` elements represent individual list items.

    ```html
    <ul>
        <li>First item</li>
        <li>Second item</li>
        <li>Third item</li>
    </ul>

    ```

- `<div>`: The `<div>` element is a container used to group other HTML elements for styling or scripting purposes.

    ```html
    <div class="container">
        <h2>Section Title</h2>
        <p>This is a section within a div.</p>
    </div>

    ```

- `<span>`: The `<span>` element is used to apply styles or manipulate specific parts of text inline without affecting layout.

    ```html
    <p>This is an <span style="color: red;">important</span> word in the sentence.</p>
    ```
- `<form>`: The `<form>` element defines a form that can contain various input elements like text fields, checkboxes, and submit buttons.

    ```html
    <form action="/submit" method="post">
        <label for="name">Name:</label>
        <input type="text" id="name" name="name">
    
        <input type="submit" value="Submit">
    </form>
    ```
- `<button>`: The `<button>` element represents a clickable button.

    ```html
    <button>Click Me!</button>
    ```

## CSS Basics

CSS (Cascading Style Sheets) is a stylesheet language used to control the presentation of HTML elements on a webpage.

### CSS Syntax

- CSS is composed of selectors and declaration blocks.
- A selector targets the HTML element(s) you want to style.

    ```css
    selector {
        property: value;
    }
    ```
- Example :

    ```css
    p {
        color: blue;
        font-size: 16px;
    }
    ```
### Selectors

CSS selectors are used to "select" the HTML elements you want to style.

- **Element selectors** : Targets all instances of a specific element.

    ```css
    h1 {
        color: red;
    }
    ```
- **Class Selectors** : Targets elements with a specific class attribute. Prefixed with a dot (`.`).
    ```css
    .highlight {
        background-color: red;
    }

    ```
- **ID Selector** : Targets a single element with a specific ID. Prefixed with a hash (#).

    ```css
    #header {
        text-align: center;
    }
    ```
- **Descendant Selector** : Targets elements that are descendants of a specific element.

    ```css
    div p {
        margin: 10px;
    }
    ```

### Box Model

- The CSS box model is essentially a box that wraps around every HTML element. 
- It consists of: content, padding, borders, and margins.

#### Padding :

Space inside the element, between the element's content and its border.

```css
.box {
  padding: 20px;
}
```
#### Margin :

A line is surrounding the padding (if any) and content.
```css
.box {
  border: 2px solid #000;
}

```
#### Border :

Space outside the element's border.
```css
.box {
  margin: 10px;
}

```

### Display Properties

The display property in CSS is one of the most important and widely used properties. It determines how an element is displayed on the web page.

Display : `block`

- An element with display: block; takes up the full width available and starts on a new line.

    ```css
    .block-element {
        display: block;
    }
    ```
Display : `inline`

- An element with display: inline; only takes up as much width as necessary and does not start on a new line.
    ```css
    .inline-element {
        display: inline;
    }
    ```
Display : `inline-block`

- An element with display: inline-block; is like a mix between block and inline. It flows inline with other content but behaves like a block element in terms of width and height.

    ```css
    .inline-block-element {
        display: inline-block;
        width: 150px;
        height: 100px;
    }
    ```
Display : `none`

- An element with display: none; is not displayed on the page at all. It is as if the element does not exist in the document.

    ```css
    .hidden-element {
        display: none;
    }
    ```

Display : `flex`

- An element with display: flex; becomes a flex container, allowing its children to be aligned and distributed within the container using the flexible box model.

    ```css
    .flex-container {
        display: flex;
        justify-content: space-between;
    }
    ```
Display : `grid`

- An element with display: grid; becomes a grid container, allowing for the creation of grid layouts where items can be positioned in rows and columns.

    ```css
    .grid-container {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
    }
    ```

### Pseudo Elements and Pseudo Classes

Pseudo-classes and pseudo-elements allow you to style elements based on their state or specific parts of an element.

- **Pseudo Classes** - Targets elements in a specific state, such as :hover for when a user hovers over an element.
    ```css
    a:hover {
        color: red;
    }
    ```
- **Pseudo Elements** - Targets a specific part of an element, like ::before or ::after.
    ```css
    p::before {
        content: "Hi: ";
    }
    ```

### Responsive Design 

Responsive design ensures that your webpage looks good on all devices, from desktop monitors to mobile phones. This is achieved by using media queries.

Example:
```css
@media (max-width: 600px) {
  .container {
    padding: 10px;
  }
}
```

This media query applies the styles inside it only if the viewport width is 600px or less.

## Conclusion

These elements form the building blocks of HTML and allow you to create structured, meaningful content for the web.

