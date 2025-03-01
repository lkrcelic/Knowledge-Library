# Markdown Style Guide

This document outlines the **markdown conventions** and **best practices** used throughout the project for maintaining a consistent look and feel.

---

## Table of Contents

1. [File Structure & Naming](#file-structure--naming)
2. [Headings & Titles](#headings--titles)
3. [Paragraphs & Line Spacing](#paragraphs--line-spacing)
4. [Lists](#lists)
5. [Code Blocks & Syntax Highlighting](#code-blocks--syntax-highlighting)
6. [Images](#images)
7. [Links & References](#links--references)
8. [Emphasis & Formatting](#emphasis--formatting)
9. [Tables of Contents](#tables-of-contents)
10. [Examples](#examples)

---

## File Structure & Naming

- **File Extension:** Always use `.md` for all markdown documents.
- **File Names:** Use lowercase with words separated by hyphens (e.g., `nginx-architecture.md`, `frontend-deployment.md`).
- **Folders:** Organize files by topic or section when necessary. Avoid deep nesting unless it improves clarity.

---

## Headings & Titles

1. **Main Title (H1)**:

   - Placed at the top of the file.
   - Written in sentence case or title case as appropriate.
   - Example:
     ```md
     # NGINX Architecture
     ```

2. **Section Titles (H2)**:

   - Used for main sections or major topics.
   - Example:
     ```md
     ## Introduction
     ```

3. **Subsections (H3)**:
   - Used for nested topics within a section.
   - Example:
     ```md
     ### Master
     ```
4. **Further Nesting (H4)**:
   - Used only if necessary for clarity. Avoid deep nesting when possible.

**Tip**: Maintain consistent hierarchy (H1, H2, H3, H4) to keep the document scannable.

---

## Paragraphs & Line Spacing

- Separate paragraphs with a single blank line.
- Keep sentences concise. If adding emphasis, use inline formatting like **bold** or _italics_.
- Example:

  ```md
  This is the first paragraph.

  This is the second paragraph.
  ```

---

## Lists

1. **Unordered Lists**:

   - Use `-` or `*` consistently for bullet points.
   - Example:
     ```md
     - Item one
     - Item two
     - Item three
     ```

2. **Ordered Lists**:

   - Use numbers followed by a dot (`1.`, `2.`, `3.`).
   - Example:
     ```md
     1. Step one
     2. Step two
     3. Step three
     ```

3. **Indentation**:
   - When nesting lists, indent by 2 spaces.
   - Example:
     ```md
     - Main item
       - Nested item
     ```

---

## Code Blocks & Syntax Highlighting

- Use fenced code blocks with triple backticks and specify the language when possible:
  ````md
  ```language
  # code or text here
  ```
  ````
- Commonly used languages:
  - **bash** or **shell** for command-line snippets.
  - **dockerfile** for Docker-related code.
  - **json**, **yaml**, **javascript**, **typescript**, etc., depending on context.
- Ensure code blocks are **indented** and **readable**.

**Example**:

```dockerfile
FROM nginx:alpine
COPY build/ /usr/share/nginx/html/
CMD ["nginx", "-g", "daemon off;"]
```

---

## Images

- Use relative paths if images are part of the repository.
- Provide alt text in case the image fails to load or for accessibility.
- Example:
  ```md
  ![nginx-architecture](nginx-architecture.png)
  ```
- Use blank lines before and after images for clarity.

---

## Links & References

- Use inline or reference style links:

  ```md
  [Example Link](https://example.com)

  [1]: https://example.com
  ```

- When referencing, make sure to keep link definitions at the bottom or near relevant sections for maintainability.

---

## Emphasis & Formatting

- **Bold**: for key terms or main points.
- _Italics_: for secondary emphasis or references to other materials.
- `Inline code`: to reference code elements in a paragraph.

Example of emphasis usage:

```md
Nginx is an **open-source** software commonly used as a _web server_, **reverse proxy**, or _load balancer_.
```

---

## Tables of Contents

- Include a table of contents whenever the file is longer than a few screens.
- It should list major sections and optionally subsections for quick navigation.
- Typically placed immediately after the main title or after a short introduction.

**Example**:

```md
## Table of Contents

1. [Introduction](#introduction)
2. [Architecture](#architecture)
3. [Usage & Examples](#usage--examples)
```

---

## Examples

1. **Section Organization**:

   ```md
   # Title

   Brief overview of the topic.

   ## Table of Contents

   1. [Section One](#section-one)
   2. [Section Two](#section-two)

   ## Section One

   Content goes here.

   ### Subsection

   More details here.

   ## Section Two

   Another main topic or feature.
   ```

2. **Code + Explanation**:

   ````md
   # Docker Deployment Example

   Use the following `Dockerfile`:

   ```dockerfile
   FROM nginx:alpine
   COPY build/ /usr/share/nginx/html/
   CMD ["nginx", "-g", "daemon off;"]
   ```
   ````

   This file copies your local `build/` folder to the Nginx directory.

   ```

   ```

---

### Final Notes

Following these guidelines ensures clarity, consistency, and readability across all markdown documents in this project. Adhere to this style for **every .md file** to maintain a polished, cohesive documentation suite.
