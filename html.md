# What is HTML?

**HTML** stands for **HyperText Markup Language**.  
- **HyperText:** Links between pages and sites.
- **Markup Language:** A way to "mark up" or label parts of your content so browsers know how to display it.

**Key Point:** HTML is not a programming language; it’s a markup language that tells the browser how to structure and display content on a web page.

---

# The Basic Structure of an HTML Document

Every HTML document follows a similar structure. Here’s a simple example:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My First Web Page</title>
  </head>
  <body>
    <h1>Welcome to My Website</h1>
    <p>This is a paragraph of text on my website.</p>
  </body>
</html>
```

**Breaking It Down:**
- `<!DOCTYPE html>`: Declares the document as HTML5, the latest standard.
- `<html>`: The root element that wraps all the content on the page.
- `<head>`: Contains meta-information (like the page title, links to CSS files, meta tags for SEO, etc.).
- `<title>`: Sets the title that appears in the browser tab.
- `<body>`: Contains the actual content (text, images, links, etc.) that users see.

---

# Understanding HTML Elements and Tags

HTML is made up of **elements**, which are the building blocks of a webpage.

## Elements and Tags

An **element** usually has:
- An **opening tag** (e.g., `<p>`)
- **Content** (e.g., `This is a paragraph.`)
- A **closing tag** (e.g., `</p>`)

Example:

```html
<p>This is a paragraph.</p>
```

Some elements are **self-closing**, meaning they don’t need a closing tag. Examples include:
- `<br>` (line break)
- `<img>` (image)

---

# Attributes: Adding Extra Information

**Attributes** provide additional details about an element. They are placed inside the opening tag.

Example:

```html
<a href="https://www.example.com">Visit Example.com</a>
```

- **`href`** is an attribute for the `<a>` (anchor) tag that specifies the link destination.

Other common attributes include:
- `src` for images: `<img src="image.jpg" alt="A description of the image">`
- `alt` for images: Provides alternative text if the image cannot be displayed.
- `class` and `id`: Used for styling and scripting.

---

# Common HTML Elements

Here’s a rundown of some frequently used HTML elements:

## Headings
- `<h1>` to `<h6>` define headings.  
  - `<h1>` is the most important (largest) heading.
  - `<h6>` is the least important (smallest).

Example:
```html
<h1>Main Heading</h1>
<h2>Subheading</h2>
```

## Paragraphs
- `<p>` defines a paragraph.
  
Example:
```html
<p>This is a simple paragraph explaining something important.</p>
```

## Links
- `<a>` creates a hyperlink.

Example:
```html
<a href="https://www.example.com">Click here to visit Example.com</a>
```

## Images
- `<img>` displays images. It requires at least a `src` attribute, and it’s best practice to include an `alt` attribute.

Example:
```html
<img src="photo.jpg" alt="A beautiful scenery">
```

## Lists
- **Unordered Lists:** `<ul>` with `<li>` for each list item.
  
Example:
```html
<ul>
  <li>Item One</li>
  <li>Item Two</li>
  <li>Item Three</li>
</ul>
```
- **Ordered Lists:** `<ol>` with `<li>` for each list item.
  
Example:
```html
<ol>
  <li>First Step</li>
  <li>Second Step</li>
  <li>Third Step</li>
</ol>
```

## Tables
- `<table>` creates a table.
- `<tr>` defines a table row.
- `<th>` defines a header cell.
- `<td>` defines a data cell.

Example:
```html
<table>
  <tr>
    <th>Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Alice</td>
    <td>30</td>
  </tr>
</table>
```

## Forms
Forms allow users to input data, which can be sent to a server.

Example:
```html
<form action="/submit-form" method="post">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required>
  <input type="submit" value="Submit">
</form>
```
- **`action`**: The URL where the form data is sent.
- **`method`**: The HTTP method used (usually "GET" or "POST").

---

# Semantic HTML: Making Content Meaningful

**Semantic HTML** means using tags that describe the type of content they contain. This helps both browsers and search engines understand the content better.

Examples of semantic elements:
- `<header>`: Contains introductory content or navigation links.
- `<footer>`: Contains footer information.
- `<nav>`: Contains navigation links.
- `<article>`: Represents a self-contained piece of content.
- `<section>`: Groups related content.
- `<aside>`: Contains content that is tangentially related (like a sidebar).

Using these elements improves accessibility and SEO (search engine optimization).

---

# Adding CSS and JavaScript

While HTML defines the structure and content, **CSS** and **JavaScript** enhance the appearance and interactivity.

## CSS (Cascading Style Sheets)
CSS is used for styling your HTML content. There are three ways to add CSS:
1. **Inline CSS:** Directly in the HTML element.
   ```html
   <p style="color: blue;">This text is blue.</p>
   ```
2. **Internal CSS:** Within a `<style>` tag in the `<head>`.
   ```html
   <style>
     p { color: blue; }
   </style>
   ```
3. **External CSS:** Linked via a `<link>` tag.
   ```html
   <link rel="stylesheet" href="styles.css">
   ```

## JavaScript
JavaScript adds interactive behavior to your web pages.
- **Inline JavaScript:** Inside a `<script>` tag.
  ```html
  <script>
    alert('Hello, world!');
  </script>
  ```
- **External JavaScript:** Linked via a `<script>` tag.
  ```html
  <script src="script.js"></script>
  ```

---

# Multimedia in HTML

HTML supports embedding multimedia elements like images, audio, and video.

## Images
As seen before:
```html
<img src="image.jpg" alt="Description of image">
```

## Audio
Embed audio files using:
```html
<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>
```

## Video
Embed video files using:
```html
<video controls width="320" height="240">
  <source src="video.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
```

---

# HTML Entities: Special Characters

HTML entities allow you to display reserved characters or symbols.

Examples:
- `&lt;` displays as `<`
- `&gt;` displays as `>`
- `&amp;` displays as `&`

Use these when you need to display characters that would otherwise be interpreted as HTML code.

---

# Accessibility and Best Practices

### Accessibility
Making websites accessible means ensuring everyone, including people with disabilities, can use them. Tips include:
- **Use semantic HTML:** This makes content understandable for screen readers.
- **Add alt text to images:** Helps those using screen readers understand the image content.
- **Ensure keyboard navigability:** Users should be able to navigate using the keyboard alone.
- **Use ARIA attributes:** These help enhance accessibility for complex components.

### Best Practices
- **Declare the Doctype:** Always start with `<!DOCTYPE html>` to ensure modern browser rendering.
- **Keep it Clean:** Write well-organized and indented code.
- **Validate Your Code:** Use tools like the [W3C Markup Validation Service](https://validator.w3.org/) to catch errors.
- **Use Semantic Elements:** They make your code more meaningful and accessible.

---

# The Evolution of HTML

HTML has grown and evolved over the years:
- **HTML 4.01:** Established web page structure.
- **XHTML:** A stricter, XML-based version of HTML.
- **HTML5:** The current standard, offering new features like semantic elements, multimedia support, and enhanced APIs for web applications.

HTML5 makes it easier to build modern, interactive, and accessible web applications.

---

# Conclusion

HTML is the backbone of the web—it structures your content and tells browsers how to display it. By learning HTML, you:
- Gain the ability to create web pages.
- Understand how to organize and display content.
- Learn how to integrate with CSS for styling and JavaScript for interactivity.

This guide has covered the basics and some advanced features of HTML, from the basic document structure to semantic elements and multimedia. As you continue learning, try creating small projects and experimenting with these elements. Practice is the best way to solidify your understanding and build your skills.

---

# Additional Resources

- **[MDN Web Docs - HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)**
- **[W3Schools HTML Tutorial](https://www.w3schools.com/html/)**
- **[HTML Living Standard](https://html.spec.whatwg.org/)**

Keep experimenting, and happy coding!
