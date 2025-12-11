---
layout: default
title: Markdown Formatting Guide
---

# Markdown Formatting Guide

A comprehensive reference for all Markdown formatting options supported by GitHub Pages and Jekyll.

## Table of Contents
- [Headings](#headings)
- [Text Formatting](#text-formatting)
- [Lists](#lists)
- [Links](#links)
- [Images](#images)
- [Code](#code)
- [Tables](#tables)
- [Blockquotes](#blockquotes)
- [Horizontal Rules](#horizontal-rules)
- [Task Lists](#task-lists)
- [Footnotes](#footnotes)
- [Emoji](#emoji)
- [HTML](#html)

---

## Headings

```markdown
# H1 Heading
## H2 Heading
### H3 Heading
#### H4 Heading
##### H5 Heading
###### H6 Heading
```

# H1 Heading
## H2 Heading
### H3 Heading
#### H4 Heading
##### H5 Heading
###### H6 Heading

---

## Text Formatting

```markdown
*Italic text* or _italic text_
**Bold text** or __bold text__
***Bold and italic*** or ___bold and italic___
~~Strikethrough text~~
`Inline code`
```

*Italic text* or _italic text_

**Bold text** or __bold text__

***Bold and italic*** or ___bold and italic___

~~Strikethrough text~~

`Inline code`

---

## Lists

### Unordered Lists

```markdown
- Item 1
- Item 2
  - Nested item 2.1
  - Nested item 2.2
- Item 3

* Alternative syntax
* Using asterisks

+ Or plus signs
+ Also works
```

- Item 1
- Item 2
  - Nested item 2.1
  - Nested item 2.2
- Item 3

### Ordered Lists

```markdown
1. First item
2. Second item
3. Third item
   1. Nested item 3.1
   2. Nested item 3.2
4. Fourth item
```

1. First item
2. Second item
3. Third item
   1. Nested item 3.1
   2. Nested item 3.2
4. Fourth item

---

## Links

```markdown
[Link text](https://example.com)
[Link with title](https://example.com "Title on hover")
[Reference-style link][reference]
[Relative link to file](./another-file.md)

[reference]: https://example.com
```

[Link text](https://example.com)

[Link with title](https://example.com "Title on hover")

[Relative link to file](./Christmas%20Presents.html)

### Automatic Links

```markdown
<https://example.com>
<email@example.com>
```

<https://example.com>

---

## Images

```markdown
![Alt text](image-url.jpg)
![Alt text with title](image-url.jpg "Image title")
```

Example:
```markdown
![GitHub Logo](https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png)
```

### Images with Links

```markdown
[![Alt text](image-url.jpg)](https://link-destination.com)
```

---

## Code

### Inline Code

```markdown
Use `code` in your sentence.
```

Use `code` in your sentence.

### Code Blocks

**With syntax highlighting:**

````markdown
```python
def hello_world():
    print("Hello, World!")
```
````

```python
def hello_world():
    print("Hello, World!")
```

```javascript
function greet(name) {
    return `Hello, ${name}!`;
}
```

```bash
git add .
git commit -m "Update files"
git push origin main
```

**Without language specified:**

````markdown
```
Plain text code block
No syntax highlighting
```
````

---

## Tables

```markdown
| Header 1 | Header 2 | Header 3 |
|----------|----------|----------|
| Row 1    | Data     | Data     |
| Row 2    | Data     | Data     |
| Row 3    | Data     | Data     |

| Left Aligned | Center Aligned | Right Aligned |
|:-------------|:--------------:|--------------:|
| Left         | Center         | Right         |
| Text         | Text           | Text          |
```

| Header 1 | Header 2 | Header 3 |
|----------|----------|----------|
| Row 1    | Data     | Data     |
| Row 2    | Data     | Data     |
| Row 3    | Data     | Data     |

| Left Aligned | Center Aligned | Right Aligned |
|:-------------|:--------------:|--------------:|
| Left         | Center         | Right         |
| Text         | Text           | Text          |

---

## Blockquotes

```markdown
> This is a blockquote
> It can span multiple lines

> Blockquotes can be nested
>> Like this
>>> And even deeper
```

> This is a blockquote
> It can span multiple lines

> Blockquotes can be nested
>> Like this
>>> And even deeper

### Blockquotes with Other Elements

```markdown
> ### Heading in blockquote
> 
> - List item 1
> - List item 2
> 
> **Bold text** in blockquote
```

> ### Heading in blockquote
> 
> - List item 1
> - List item 2
> 
> **Bold text** in blockquote

---

## Horizontal Rules

```markdown
---

***

___
```

---

***

___

---

## Task Lists

```markdown
- [x] Completed task
- [ ] Incomplete task
- [ ] Another incomplete task
  - [x] Nested completed task
  - [ ] Nested incomplete task
```

- [x] Completed task
- [ ] Incomplete task
- [ ] Another incomplete task
  - [x] Nested completed task
  - [ ] Nested incomplete task

---

## Footnotes

```markdown
Here's a sentence with a footnote[^1].

Here's another with a longer footnote[^bignote].

[^1]: This is the footnote.
[^bignote]: Here's one with multiple paragraphs.

    You can include code, lists, and other elements.
```

Here's a sentence with a footnote[^1].

[^1]: This is the footnote.

---

## Emoji

```markdown
:smile: :heart: :thumbsup: :rocket: :tada:

GitHub supports emoji shortcodes!
```

:smile: :heart: :thumbsup: :rocket: :tada:

[Full emoji list](https://github.com/ikatyang/emoji-cheat-sheet)

---

## Definition Lists

```markdown
Term 1
: Definition 1

Term 2
: Definition 2a
: Definition 2b
```

Term 1
: Definition 1

Term 2
: Definition 2a
: Definition 2b

---

## Escaping Characters

```markdown
\* This is not italic \*
\# This is not a heading
\[This is not a link](url)
```

\* This is not italic \*

\# This is not a heading

---

## HTML

You can use raw HTML in Markdown:

```html
<div style="background-color: #f0f0f0; padding: 10px; border-radius: 5px;">
    <p>This is an <strong>HTML</strong> block inside Markdown.</p>
</div>

<details>
<summary>Click to expand</summary>
Hidden content goes here!
</details>
```

<div style="background-color: #f0f0f0; padding: 10px; border-radius: 5px;">
    <p>This is an <strong>HTML</strong> block inside Markdown.</p>
</div>

<details>
<summary>Click to expand</summary>
Hidden content goes here!
</details>

---

## Line Breaks

```markdown
Line 1  
Line 2 (two spaces after Line 1)

Or use a blank line

For a paragraph break
```

---

## Superscript and Subscript

**Using HTML:**

```html
E = mc<sup>2</sup>
H<sub>2</sub>O
```

E = mc<sup>2</sup>

H<sub>2</sub>O

---

## Highlighting

**Using HTML:**

```html
<mark>Highlighted text</mark>
```

<mark>Highlighted text</mark>

---

## Keyboard Keys

```html
Press <kbd>Ctrl</kbd> + <kbd>C</kbd> to copy
Press <kbd>Cmd</kbd> + <kbd>V</kbd> to paste
```

Press <kbd>Ctrl</kbd> + <kbd>C</kbd> to copy

Press <kbd>Cmd</kbd> + <kbd>V</kbd> to paste

---

## Abbreviations

```markdown
The HTML specification is maintained by the W3C.

*[HTML]: Hyper Text Markup Language
*[W3C]: World Wide Web Consortium
```

---

## Special Characters

```markdown
&copy; Copyright symbol
&trade; Trademark symbol
&reg; Registered trademark
&nbsp; Non-breaking space
&lt; Less than
&gt; Greater than
&amp; Ampersand
```

&copy; Copyright symbol

&trade; Trademark symbol

&reg; Registered trademark

---

## Front Matter (Jekyll Specific)

At the top of your Markdown files, you can add YAML front matter:

```yaml
---
layout: default
title: Page Title
date: 2025-12-11
author: Your Name
categories: [category1, category2]
tags: [tag1, tag2]
---
```

This metadata is used by Jekyll to control page layout and behavior.

---

## Tips for Best Results

1. **Add blank lines** between different elements for clarity
2. **Use consistent indentation** (2 or 4 spaces) for nested lists
3. **Preview your Markdown** locally before pushing to GitHub
4. **Check compatibility** - some features work on GitHub but not all Markdown parsers
5. **Use semantic headings** - don't skip levels (H1 → H3)
6. **Add alt text** to all images for accessibility
7. **Keep lines short** (80-100 characters) for better readability in source

---

## Testing Your Markdown

To test locally:

```bash
bundle exec jekyll serve
```

Then visit `http://localhost:4000/Obsidian_to_GitPage_Workflow/`

---

## Resources

- [GitHub Flavored Markdown Spec](https://github.github.com/gfm/)
- [Markdown Guide](https://www.markdownguide.org/)
- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [Kramdown Syntax](https://kramdown.gettalong.org/syntax.html)

---

*Last updated: December 11, 2025*
