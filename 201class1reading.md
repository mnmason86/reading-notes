[<=== Back](README.md)

# HTML & CSS by Jon Duckett
*Summarized*

## Introduction
### How People Access the Web
- Web Browsers: software which allows the user to search for information or websites.
- Web Servers: A computer which is constantly connected to the internet, and "hosts" websites, sending information out when requested.
- Devices: Desktops, laptops, tablets, phones, etc. Different devices have different screen sizes and connection speeds.
- Screen Readers: Programs that read the contents of a computer screen to the user. 

### How Websites Are Created
The visual aspect of a website is produced by the browser receiving HTML and CSS from the server and interpreting it. HTML5 and CSS3 are the latest versions of these languages, and are always being built upon. Other programming languages are used on larger, more complex sites to perform functions and store data. 

### How The Web Works
- The user connects to the web via their Internet Service Provider (ISP), and types a web address into the browser
- The computer contacts a network of servers called Domain Name System (DNS) servers. DNS servers relay information about the IP address it is trying to reach.
- The IP address that is returned allows the browser to connect to the requested server. 
- The web sends the page back to the browser.

## Chapter 1: Structure
p.12-39

Structure refers to the layout of a page or document, appropriate reflecting the hierarchy of information in that page or document.

HTML uses **elements** to describe the structure of web pages.
**Attributes** provide additional information about the contents of an element, appear on the opening tag of the element, and are made of a *name* and a *value*, separated by `=`.

It's never a bad idea to "View Source" for a page to view the HTML!

## Chapter 8: Extra Markup
p.176-199

`<!DOCTYPE html>` is used to tell the browser which version of HTML is being used. Refer to p.181 for examples of different DOCTYPES.

To add a comment that is not visible in the user's browser, wrap the text with `<!-- -->`

The `id` attribute uniquely identifies that element from other elements on the page, while the `class` attribute is used to identify a set of elements as different from the rest of the page.

Block level elements: `<h1>`,`<p>`,`<ul`>,`<li>`    
Inline elements: `<a>`,`<img>`
`<div>` elements allow a set of elements to be grouped together in one box.  
A `<span>` element "acts like an inline equivalent of the `<div>` element.  
`<iframe>` elements are used to embed a window to another page, i.e. Google Maps.  
The `<meta>` element is contained inside the `<head>`, and contains metadata about the page.  

## Chapter 17: HTML5 Layout
p.428-451

Older versions of HTML used the `<div>` tag to group related elements, providing each with an `id=` to differentiate. **HTML5** utilize named elements which describe the type of content found in each, i.e. `<header>`, `<article>`, & `<footer>`.

`<aside>` elements have two purposes
- Inside an article: contains information related to the artical but not essential.
- Outside an article: acts as a container for content that is related to the entire page.

##### Linking Around Block-Level Elements
> "HTML5 allows web page authors to place an `<a>` element around a block level element that contains child elements. This allows you to turn an entire block into a link." (p.441)

## Chapter 18: Process & Design
p.452-475

Important aspects to consider when building a site:
- Who is the site for?
- Why do people visit your site?
- What are your visitors trying to achieve?
- What information do your visitors need?
- How often will people visit your site?

After considering the above questions, create a diagram of the pages utilized within the site and how they will be organized and connected. Then, Wireframe! 

Size, color, and style can help to establish a *visual hierarchy* of information. People tend to "organize visual elements into groups", which can make a design easier to comprehend.

Navigation design should be concise, clear, selective, interactive, consistent, and have context.

# Javascript & JQUERY by Jon Duckett

## Introduction

## JS Chapter 1: The ABC of Programming
p.11-52