The browser's default CSS, often referred to as **user agent styles**, is loaded and applied automatically by the browser **before** any custom CSS (from external files or inline styles) is processed. Here's the sequence in which the browser loads and applies its default CSS:

### 1. **Initial DOM Creation**:
   - When the browser starts parsing the HTML, it creates the **DOM** (Document Object Model) for the page.
   - At this point, the browser applies its **default styles** to the elements. These are the basic styling rules that ensure the page elements have some default appearance (e.g., headers are bold, paragraphs have margins, etc.). Every browser has its own user agent stylesheet for this purpose.

### 2. **Applying Browser Default CSS**:
   - As the DOM is being created, the browser applies its **default stylesheet** to elements like `<body>`, `<h1>`, `<p>`, `<ul>`, `<a>`, and other HTML elements.
   - These default styles ensure that even without any custom CSS, elements display in a readable way (e.g., a header is larger than a paragraph, links are underlined, and lists are indented).
   
   Example of some typical user agent styles:
   ```css
   body {
       margin: 8px;
   }
   h1 {
       font-size: 2em;
       margin: 0.67em 0;
   }
   p {
       margin: 1em 0;
   }
   ul {
       padding-left: 40px;
   }
   a {
       color: blue;
       text-decoration: underline;
   }
   ```

### 3. **Loading and Applying Custom CSS**:
   - Once the HTML parser encounters `<link>` tags for external stylesheets or `<style>` tags with inline CSS, the browser **fetches** and **applies the custom CSS**.
   - The custom CSS rules **override** the default browser styles where specified. This is based on the CSS **cascading** and **specificity** rules (where more specific or important styles take precedence).

### 4. **Recalculation of Styles**:
   - After custom CSS is applied, the browser recalculates the final appearance of the page based on the **combination** of the browser's default CSS, the custom styles, and any inline styles or JavaScript manipulations.
   - For any elements that are not explicitly styled by the user’s custom CSS, the **browser default styles remain in effect**.

### When Does Browser Default CSS Load? 
The browser default CSS is essentially **always present** and loaded by default as soon as the HTML document starts being parsed. It is applied **before** any custom CSS, and remains in effect unless specifically overridden by user-defined styles.

### Important Notes:
1. **Reset and Normalize CSS**: 
   - Many developers use a **CSS reset** (e.g., Reset.css or Normalize.css) to remove or standardize browser default styles across different browsers to ensure consistent appearance. This is because different browsers may have slightly different default styles.
   
2. **Specificity and Cascade**: 
   - Browser defaults have a low specificity, meaning that custom CSS with higher specificity (like element selectors, class selectors, or inline styles) will typically override them easily.

In summary, browser default CSS is applied at the very start, even before any user-defined styles are processed, ensuring that every HTML element has a basic style to make the page presentable.
