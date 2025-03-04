# Direction Auto-Detection Script

This script automatically detects and sets the text direction (RTL or LTR) based on the presence of Persian characters. It applies the appropriate direction and text alignment styles to elements dynamically.

## Features
- Detects Persian characters in text nodes and sets `direction` and `text-align` accordingly.
- Supports inline elements, block elements, and lists.
- Handles `iframe` content by observing changes within.
- Resets unwanted styles set by TinyMCE (`data-mce-style`).
- Observes DOM mutations to adjust direction dynamically.

## Usage


## How It Works
1. **Text Detection:** The script scans elements and their child nodes for Persian characters.
2. **Style Application:** If Persian characters are found, it sets `direction: rtl` and adjusts `text-align`. Otherwise, it sets `direction: ltr`.
3. **Handling Inline Elements:** Ensures inline elements (e.g., `<strong>`, `<a>`) are properly styled while considering their non-inline parents.
4. **List Support:** Properly formats lists (`<ul>`, `<ol>`) and list items (`<li>`) while preserving readability.
5. **Mutation Observer:** Monitors the document and iframes for dynamically added content and applies necessary adjustments.

## Edge Cases
- The script ignores specific elements such as `<code>`, `<script>`, and `<pre>`.
- It ensures list items retain their expected indentation and structure.
- **Mixed Persian and English text** is handled correctly within the same element.

## Compatibility
- Works with dynamic content updates, including TinyMCE editors and iframes.
- This script is written specifically for Confluence v8.5.12

## License
This script is open-source. Feel free to use, modify, and improve it as needed.

---
If you need any modifications or additional features, feel free to ask!

