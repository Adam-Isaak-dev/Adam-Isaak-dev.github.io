---
layout: post
title:  "HTML and CSS"
date:   2020-11-24 17:15:00 -0600
categories: blog-post writing-task
image: /assets/20-11-24/code.png
image.thumbnail: /assets/20-11-24/HTML_CSS_logos.svg
---
 
Have you ever wondered what is behind the websites you visit? HTML (HyperText Markup Language) and CSS (Cascading Style Sheets) form the backbone of the websites you visit daily on a daily basis. Here is a short overview of how HTML and CSS work. 
 
---
## HTML 
HTML provides the structure and meaning to websites. The building blocks of HTML are its elements. Elements can range from boxes of text, images, to website links. Each element is defined by a tag. Tags define what kind of building block is to be used in displaying the website.

Here's an example of an HTML element wrapped by the paragraph tag:
``` html     
<p>Hello World!</p>
```
 
Here is an example of the of a basic website made using HTML:
``` html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
  </head>
  <body>
    <p>Hello World!</p>
  </body>
</html>
```

It's output would look like the following:
 
>  Hello World!
 
### A little more detail
 
There are two types of HTML elements a block element, and an inline element. A block has line breaks around it (i.e. a paragraph). In contrast, an inline element stays within the line (i.e. Bolded text). 

Finally, there are HTML attributes. Attributes can be used for linking other files like images, to adding classes and id’s to elements so they can be individually manipulated.
 
---
## CSS 
In contrast to HTML, CSS provides the visual style and formatting of websites. CSS works by selecting an HTML element and adding some rules and assigning a value to it the rule. Let's break down that process. 
A CSS selector is a name that identifies an HTML element/s that you want to 'select'. This can be in the form of the elements tag, class, or id. Next, there are CSS rules that you want to set for the selected element/s. They vary from changing the font size to text colour, to many other things. Finally, there are CSS values. Values are the value assigned to a rule, that you want to change the element to.

Here is an example of CSS changing the style of paragraph elements to font-height of 25px, red text, and a sans-serif font.
``` css
p {
  font-size: 25px;
  color: red;
  font-family: sans-serif;
}
```

---
## Conclusion
That wraps up a basic overview of HTML and CSS. Hopefully, you now understand the fundamentals behind them and you can move on to greater things. Check out some of the linked resources below if you wish to learn more.
 
* [W3Schools for all your web development learning needs](https://www.w3schools.com/)
* [MDN for a comprehensive reference to the code behind the web.](https://developer.mozilla.org/en-US/)
* [CSS tricks for excellent tips and tricks to make your website look great.](https://css-tricks.com/)
 
## Citations
>CSS. (2020, October 30). Retrieved November 01, 2020, from https://en.wikipedia.org/wiki/CSS
 
>HTML. (2020, October 29). Retrieved November 01, 2020, from https://en.wikipedia.org/wiki/HTML
 
>HTML: HyperText Markup Language. (n.d.). Retrieved November 01, 2020, from https://developer.mozilla.org/en-US/docs/Web/HTML