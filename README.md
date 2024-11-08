# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

Do some research on semantic and non-semantic elements and share your findings. Your response should include:

- Examples of semantic and non-semantic tags
- The differences between semantic and non-semantic tags
- The benefits of using semantic tags (when possible)

### Response 1

## **Semantic vs Non-Semantic Tags in HTML**

**Semantic tags** provide meaning and structure to content, while **non-semantic tags** are generic containers.

## **Examples of Semantic and Non-Semantic Tags**

### Semantic Tags

```html
<header>Header content</header>
<nav>Navigation links</nav>
<main>Main content</main>
<section>Section content</section>
<article>Article content</article>
<aside>Sidebar content</aside>
<footer>Footer content</footer>
```

### Non-Semantic Tags

```html
<div>Generic block content</div>
<span>Generic inline content</span>
```

## **Differences Between Semantic and Non-Semantic Tags**

- **Semantic tags:** Provide context and structure, helping browsers and developers understand the content.
- **Non-semantic tags:** Do not inherently provide meaning and often rely on CSS classes or IDs to convey purpose.

## **Benefits of Using Semantic Tags**

- **Accessibility:** Better support for screen readers and assistive technologies.
- **SEO:** Improved structure for search engines, which can boost page ranking.
- **Readability:** Easier to understand and maintain code.
- **Maintainability:** Cleaner, more standardized HTML code.

## Prompt 2

Do some research on accessibility. What are some ways to make your website more accessible? Explain why it is important for developers to create websites that meet accessibility standards.

### Response 2

### Ways to Make An Individual's Website More Accessible

1. **Use Semantic HTML**: Use meaningful tags like `<header>`, `<footer>`, `<nav>`, and `<article>` to provide structure for screen readers.
2. **Provide Text Alternatives**: Add `alt` text for images and transcripts for audio and video content.
3. **Ensure Keyboard Navigation**: Make sure all interactive elements are navigable with the keyboard.
4. **Check Color Contrast**: Ensure sufficient contrast between text and background for better visibility.
5. **Use ARIA Roles**: Improve accessibility by adding ARIA attributes to provide more context for assistive technologies.
6. **Make Forms Accessible**: Label form fields clearly using `<label>` elements.
7. **Responsive Design**: Ensure the site works well across all devices and screen sizes.

---

### Importance of Accessibility for Developers

- **Inclusivity**: Ensures everyone, regardless of ability, can use your site.
- **Legal Compliance**: Helps avoid legal issues related to accessibility.
- **Better SEO**: Improves search engine rankings through better content structure.
- **Improved Usability**: Enhances the experience for all users.

## Prompt 3

It is possible to add "inline" CSS styles to our html elements using the `style` attribute like so:

```html
<p style="color: red;">hello world</p>
```

While this is possible, it is a best practice to instead write styles in a separate CSS file. Provide at least one argument for why it _might_ be considered useful to write inline styles, and then provide a more compelling argument for writing styles in a separate CSS file.

### Response 3

### Inline CSS vs External CSS

- **Why Inline CSS Might Be Useful**:

  - **Quick Testing/Prototyping**: Inline styles are useful for making quick changes without needing to modify an external file, especially during development.
    - In other word it is good for making fast style changes while working on a webpage.

- **Why Use External CSS**:
  - **Maintainability**: Keeps styles separate from content, making it easier to update and manage, especially for large projects.
  - **Reusability**: An external CSS file can be applied to multiple pages, ensuring a consistent design across your site.
  - **Performance**: External stylesheets are cached by browsers, reducing load times on repeat visits.

## Prompt 4

Imagine you are teaching a brand new programmer a brief lesson about the `class` and `id` attributes in HTML as well as how to use them to style elements using CSS. Your lesson should have the following components:

- An explanation of the concept of "classes" and "ids" with an analogy.
- An example of the usage using an HTML code block and a CSS code block.
- An explanation of the syntax using the terms: **attribute**, **selector**

### Response 4

### Understanding `class` and `id` in HTML and CSS

- **Classes**: Think of a class as a **category**. Many elements can belong to the same category and share the same style.
- **IDs**: An ID is like a **specific name** for one element. Each ID is unique and should only be used once on a page.

- **Example Usage**:

  - **HTML**:

    ```html
    <p class="highlight">This is a paragraph with a class</p>
    <p id="uniqueParagraph">This is a paragraph with an id</p>
    ```

  - **CSS**:

    ```css
    /* Styling for the class */
    .highlight {
      color: yellow;
      font-weight: bold;
    }

    /* Styling for the id */
    #uniqueParagraph {
      color: red;
      font-size: 18px;
    }
    ```

- **Explanation**:
  - **Attribute**: The `class` and `id` are HTML attributes used to identify elements.
  - **Selector**: In CSS, to style by **class**, use a **dot (.)**, and for **id**, use a **hashtag (#)**.

## Prompt 5

The Document Object Model (DOM) API provides functions for manipulating HTML documents. It is possible to build an entire website using only JavaScript and the DOM API, however is that the best practice?

When building a website, how can I decide which content I should write using HTML/CSS and which content I should create using the JavaScript and the DOM API?

### Response 5

### Deciding Between HTML/CSS and JavaScript for Website Content

- **HTML/CSS**:  
  I use HTML to define the structure of the website (things like headings, paragraphs, images), and CSS to control its appearance (like colors, layout, and fonts).

- **JavaScript & DOM API**:  
  JavaScript, using the DOM API, is great for adding interactivity or dynamically changing content after the page has loaded. For example, things like form validation, fetching data from APIs, or updating parts of the page without refreshing.

- **Best Practice**:

  - **HTML/CSS for static content**: If the content doesn't need to change or interact with the user, I write it using just HTML and CSS.
  - **JavaScript for dynamic content**: If I need content to change based on user input or update without reloading the page, I'll use JavaScript.

- **Why Not Everything in JavaScript?**
  - **Separation of Concerns**: I keep the structure and design in HTML/CSS, and the behavior in JavaScript. Mixing them all together can make the code messy and hard to maintain.
  - **Performance**: Writing everything in JavaScript can slow down the site, especially for users with slower devices. It’s more efficient to use HTML and CSS for static parts and JavaScript for interactive features.
