# HTML Comprehension Questions


## Q1 - For each of the following HTML documents, is the HTML valid?

Type true/false in the provided [ ].

a) [F ] `<div><span>hello</div></span>`

The <div> should close the line, <span> is nested on the div

<div><span>hello</span></div>

div and span are use for the same porpoise. The difference between span and div is that a span element is in-line and usually used for a small chunk of HTML inside a line (such as inside a paragraph) whereas a div (division) element is block-line (which is basically equivalent to having a line-break before and after it) and used to group larger chunks of code.

b) [F]

```html
<ul>
<li>one</li>
</ol>
```
The unordered list should be closed by </ul>
<ul> = The <ul> tag defines an unordered (bulleted) list.
<li> = The <li> tag is used in ordered lists(<ol>), unordered lists (<ul>), and in menu lists (<menu>).

c) [T] `<ul></ul><img/><ol><li>one</li></ol>`
`<ul></ul> empty unordered list
<img/> empty image tag
<ol>
    <li>one</li> ordered list with one element
</ol>`


## Q2 - What is a screenreader and why should we care about them?

_Feel free to use the powers of Google here, but please provide link(s) to your source(s)_

https://en.wikipedia.org/wiki/Screen_reader
 assistive technology (AT)[1] that renders text and image content as speech or Braille output.

 we should care about them because in order to work it needs proper tags

 E.G <bold> vs <strong>
 https://www.seobility.net/en/wiki/Strong_and_Bold_Tags







## Q3 - For each of the following cases, which tags will be needed?

a) You want to create a webpage with the photos from your latest vacation
<!DOCTYPE html>
<html>
<head>
<title>Page Title</title>
</head>
<body>

<h1>Page Title</h1>
<section> <!--The <section> tag defines sections in a document, such as chapters, headers, footers, or any other sections of the document. --> = container 
<div><img....></div>
<div><img....></div>
<div><img....></div>
.........
</section>

</body>
</html>


b) You want to create a website that lists all the art gallery websites in your city and links to their website.
<!DOCTYPE html>
<html>
<head>
<title>Page Title</title>
</head>
<body>

<h1>Page Title</h1>
<p>Sales speech....</p>
<ul>
    <li><a href=".......">gallery 1</a></li>
    <li><a href=".......">gallery 2</a></li>
    <li><a href=".......">gallery 3</a></li>
    <li><a href=".......">gallery 4</a></li>
</ul>

</body>
</html>

c) You want to sell designer hats. You need to receive orders from the user.


<!DOCTYPE html>
<html>
<head>
<title>Page Title</title>
</head>
<body>

  <h1>Page Title</h1>
  <div class="container">
    <div class="item">
      <input type="checkbox">
      <p><img src="......" alt="Nice black hat" height="42" width="42">Product #1</p>
    </div>
    <div class="item">
      <input type="checkbox">

      <p><img src="......" alt="Nice red hat" height="42" width="42">Product #2</p>
    </div>
    <div class="item">
      <input type="checkbox">
      <p><img src="......" alt="Nice green hat" height="42" width="42">Product #3</p>
    </div>
  </div>
</body>
</html>

## Q4 - Can a button be a child of a button?  No 
Explain your reasoning is not logic

https://stackoverflow.com/questions/39386497/can-i-nest-button-inside-another-button
https://css-tricks.com/use-button-element/
https://html.spec.whatwg.org/multipage/form-elements.html#the-button-element


## Q5 - What is the most generic tag you can use?
the mighty <div>




## Q6 - What do the following acronyms stand for?

a) `a` = anchor

b) `ol` = ordered list

c) `ul` = unordered list

d) `li` = list item

e) `tr` = table row

f) `th` = table header

g) `td` = table data


## Q7 - Usually, `td` elements are children of what kind of elements?

<tr>

## Q8 - What is the difference between td and th?
th = header First Column
td = cells with data about the headers

This distinction gives user agents a means to render such cells distinctly, for instance by using a larger or heavier font for header cells. It is also needed when rendering to speech. 

https://www.w3.org/MarkUp/html3/tablecells.html


## Q9 - Which tag makes the text appear bigger: h1 or h3?
<h1>


## Q10 - In which situation can you use self closing tags?
According to the HTML5 spec, tags that cannot have any contents (known as void elements) can be self-closing*. This includes the following tags:

area, base, br, col, embed, hr, img, input, 
keygen, link, meta, param, source, track, wbr
The "/" is completely optional on the above tags, however, so <img/> is not different from <img>, but <img></img> is invalid.

https://stackoverflow.com/questions/3558119/are-non-void-self-closing-tags-valid-in-html5




## Q11 - What is autofilling and why is it important?
it reduces the time required by the users when filling forms
https://cloudfour.com/thinks/autofill-what-web-devs-should-know-but-dont/

## Q12 - Which attributes are always present in an img element?
<img src="....." alt=".......">
src
alt

## Q13 - Which attribute is always present for an anchor tag?

<a href="......">text</a>
href
