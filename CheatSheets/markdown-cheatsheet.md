---
title: Markdown CheatSheet
description: The most commonly used markdown syntaxes are given here.
created: 2022-10-18
---

## Table of Contents

- [Markdown CheatSheet for Developers](#markdown-cheatsheet-for-developers)
  - [Basic Syntax](#basic-syntax)
  - [Extended Syntax](#extended-syntax)
  - [Emphasis](#emphasis)
  - [Lists](#lists)
  - [Images](#Images)

# Markdown CheatSheet for Developers

## Basic Syntax

| Command                                 | Description                                          |
| --------------------------------------- | ---------------------------------------------------- |
| `**bold text**` <br /> `__bold text__`  | Bold                                                 |
| `*italic text*` <br /> `_italic text_`  | Italic                                               |
| `# h1` <br /> `## h2` <br /> `### h3`   | # Heading 1 <br /> ## Heading 2 <br /> ### Heading 3 |
| `[hello google](http://www.google.com)` | Import link                                          |
| `- first` <br /> `- second`             | Unordered list                                       |
| `1. first` <br /> `2. Second`           | Ordered List                                         |
| `---`                                   | Horizontal line                                      |
| `![alt text](image.jpg)`                | Import Image                                         |

**[🔼Back to Top](#table-of-contents)**

## Extended Syntax

| Command                                                                                                   | Description       |
| --------------------------------------------------------------------------------------------------------- | ----------------- |
| `X^2^`                                                                                                    | Superscript       |
| `H~2~O`                                                                                                   | Subscript         |
| `I need to highlight these ==very important words==.`                                                     | ==Highlight==     |
| `That is so funny! :joy:`                                                                                 | Emoji             |
| `~~The world is flat.~~ `                                                                                 | ~~Strikethrough~~ |
| `> blockquote`                                                                                            | > Blockquotes     |
| ` ``` ` <br /> `{ ` <br /> `"First": "1st",` <br /> `"Second": "2nd"` <br /> ` }` <br /> ` ``` `            | Fenced code block |
| ` - [x] task one` <br /> `- [ ] task two` <br /> `- [ ] task three` <br />                                | Task List         |
| `\| col1 \| col2 \|` <br /> `\|------\|------\| ` <br /> `\|data1 \|data2 \|` <br /> `\|data3 \|data4 \|` | Table             |
| `Here's a sentence with a footnote. [^1] ` <br /> `[^1]: This is the footnote.`                           | Footnote          |

## Emphasis
Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.

Strikethrough uses two tildes. ~~Scratch this.~~

## Lists

1. First ordered list item
2. Another item
⋅⋅* Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
⋅⋅1. Ordered sub-list
4. And another item.

⋅⋅⋅You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).

⋅⋅⋅To have a line break without a paragraph, you will need to use two trailing spaces.⋅⋅
⋅⋅⋅Note that this line is separate, but within the same paragraph.⋅⋅
⋅⋅⋅(This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)

* Unordered list can use asterisks
- Or minuses
+ Or pluses

##Images

Here's our logo (hover to see the title text):

Inline-style: 
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

Reference-style: 
![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"



**[🔼Back to Top](#table-of-contents)**
