# Reading 01 Notes

## Markdown Basic Syntax

### Headings
- Headings are available in six different sizes, by utilizing the '#' symbol, with the largest using one symbol and the smallest using six.
- *For compatibility, always put a space between the symbol and the text.*

### Paragraphs
- Paragraphs are easy. You basically just type as you normally would.
- *To avoid formatting issues, do not indent paragraphs*

### Line Breaks
- To break text into separate lines, the best way is to use two or more spaces.
- If you were taught to type sentences with two spaces at the end, use <br> instead.
- *For compatibility, do not use a backslash*

### Emphasis
#### Bold
- To emphasize by making text **bold**, use two asterisks or two underscores on either side of the text.
- If you need to make letters in the mi**dd**le of a word **bold**, use asterisks for compatibility.

#### Italic
- To emphasize by making text *italic*, use one asterisk or one underscore on either side of the text.
- If you need to make letters in the mi*dd*le of a word *italic*, use asterisks for compatibility.

#### Bold and Italic
- To emphasize by making text **bold** and *italic*, use three asterisks or three underscores on either side of the text.
- If you need to make letters in the mi***ddd***le of a word ***bold and italic***, use asterisks for compatibility.

### Blockquotes
- To create a blockquote, add a 'greater than' > symbol in front of the text you wish to quote.
- If your quote has multiple paragraphs, use the > symbol on the blank lines between paragraphs.
- To nest a block quote within another block quote, use two 'greater than' symbols >>
- Other elements such as headings and ordered lists can be used within a block quote
- *For compatibility, put a blank line before and after block quotes*

### Lists

#### Ordered Lists
- To present items in an ordered list, add items on separate lines, preceded by a number and a period.
- Any number can be used, but the first number *must* be 1!
- *For compatibility, do not use parentheses for list items.*

#### Unordered Lists
- To present items in an unordered list, add items on separate lines, preceded by a dash '-', asterisk '*', or plus sign '+' 
- These symbols are referred to as 'delimiters'.
- *For compatibility, do not combine delimiters in a single list.*

#### Adding Elements in Lists
- Indent added elements by adding four spaces or one tab.
- To add **code blocks**, indent eight spaces or two tabs.

### Code
- To denote a word or phrase as code, enclose it in backticks (`).
- If your text already includes backticks, use double backticks (``)
- To create **code blocks**, indent every line with *at least* four spaces or one tab.

### Horizontal Rules
- To create a horizontal line to separate text, use three asterisks (***), dashes (---), or underscores (___) 
- *For compatibility, put a blank line before and after each horizontal rule*

### Links
- To create a link, enclose the text for the link in brackets [], followed by the URL in parentheses ()
- To add a title to a link (the small box with text that shows when you hover over the text), add your title text in quotation marks after the URL, but still within the parentheses
- To link a URL without text, or link an email address, use angle brackets (<>)
- Links can be formatted as bold, italic, or code, just like text.

#### Reference-style Links
- This style of link, makes URLs easier to read in markdown. The first segment (which is easily readable), makes *reference* to the second segment, the longer URL, which can be embedded anywhere in the markdown.
- First segment: [URL Reference][label]
- Second segment: [label]: <URL> "Optional Title"
- *For compatibility, use '%20' in place of any spaces in the URL text*
  
### Images
  - To add an image, use an exclamation mark in parentheses, followed by alt text in brackets, then the image location in parentheses
  - Optionally, add text in quotation marks for a title.
  - To add a link to the image, enclose the image markdown in brackets, then add the link in parentheses
  - [ ! [Alt text] (image location"Optional title")  ] (URL for image site)
  
### Escaping Characters
  - "Escaping characters" refers to displaying characters that are assumed to be part of the markup
  - Use a backslash to escape a character
  - The following may be escaped: \`*{}<>[]()#+-.!|
  
### HTML
  - Sometimes, markdown applications allow the use of HTML tags. Check your markdown application's documentation!
  
## Markdown Styling
  
  Many features of Markdown styling are similar to the commands in basic syntax.
  Check [Here](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) for more styling and editing features! 
