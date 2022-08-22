[<=== Back](/README.md)

# HTML & CSS by Jon Duckett
*Summarized*

## Chapter 4: Links
p.74-93
> Links are created using the `<a>` element. Users can click on anything between the opening tag and the closing tag. You specify which page you want to link to using the `href` atrribute.

Links to pages within your own page are called **relative URLs**.

To create a link that starts up the user's email, use the `<a>` tag, but start the `href` attribute with `mailto: + useremail`.

## Chapter 15: Layout
p.358-404

> `<div>` elements are often used as containing elements to group together sections of a page.

> Browsers display pages in normal flow unless you specify relative, absolute, or fixed positioning.

> The `float` property moves content to the left or right of the page and can be used to create multi-column layouts. (Floated items require a defined width.)

> Pages can be fixed width or liquid (stretchy) layouts.

> Designers keep pages within 960-1000 pixels wide and indicate what the site is about within the top 600 pixels (to demostrate relevance without scrolling).

> Grids help create professional and flexible designs.

> CSS Frameworks provide rules for common tasks.

> You can include multiple CSS files in one page.


# JavaScript & JQUERY by Jon Duckett
*Summarized*

## Chapter 3: Functions, Methods, and Objects
p.86-99

> Functions let you group a series of statements together to perform a specific task. If different parts of a script repeat the same task, you can reuse the function (rather than repeating the same set of statements).

Functions must be declared by giving it a name, and executed by **calling** the function.

> Sometimes a function needs specific information to perform its task. In such cases, when you declare the function you give it **parameters**. Inside the function, the parameters act like variables.

Example:

```
function getArea(width, height){
  return width * height;
}
```

When a function is called that has parameters, values should be specified in the parentheses that follow its name.

Functions can return single values, or multiple values by using an array.

If a variable is declared within a function, it can only be used within that function - these are called *local variables* and use less memory than global variables.



## "6 Reasons for Pair Programming"
*by: Allie Grampa*

### What is "pair programming"?

Pair programming is when two developers work together on a project - one 'navigating' (doing the actual typing of code), and one 'driving' (speaking to the navigator about ideas, finding solutions, and scanning for errors).

Pair programming fosters greater effeciency, engaged collaboration, learning from fellow students, social skills, job interview readiness, and work environment readiness.  