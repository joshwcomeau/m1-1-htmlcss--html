# HTML Reference

HTML documents are composed of HTML elements. An HTML element has the following characteristics:

- A tag
- Attributes
- Children

For example, there are 2 HTML elements in the following HTML document:

```html
<ul id="foo">
  <li class="bar" id="someid">one</li>
</ul>
```

The first HTML element has a ul tag, an attribute called id with a value of "foo" and one child. The other HTML element has a li tag, an attribute called class with a value of "bar" and another attribute called id with a value of "someid". It has one text child ("one")

Here is another HTML document with an element with two children

```html
<ul>
  <li>one</li>
  <li>two</li>
</ul>
```

An element can have 0 or more attributes, 0 or more children and always has a single tag.

All HTML elements are written the same way:

1. You always start an element with <tagname …>
   - where … denotes the attributes of the element.
2. Then come the children
3. Then you need to close the element with </tagname>

In this course all elements must be closed. No exceptions.

The following HTML document has an error. Can you find it?

```html
<div>
  <div>hello</div>
</div>
```

Different tags are used to to display different user elements. Let's look at some of them in detail.

## Self closing tags

If your element does not have any children, you can open and close it immediately like so

```html
<img src="foobar" />
```

## List of common tags

### `h1`-`h6`

There are 6 heading levels, and they're numbered: `<h1>`, <h2>`, …`<h6>`.

The page should never have more than a single `h1` tag. It is meant to be used as the page's title. You should drop by 1 level for every more-specific or nested heading.

For example:

```html
<html>
<body>

  <h1>My Website</h1>

  <article>
    <h2>Things you can do here</h2>
    <p>Thing 1, thing 2, thing 3…</p>

    <h2>About this website</h2>
    <p>Created by me at a point in time</p>
    <h3>About this website's creator</h3>
    <p>A human from the planet earth</p>

    <h2>Contact me</h2>
    <p>No thanks</p>
  <article>
  <aside>
    <h2 class="small-heading">Table of Contents</h2>
    Stuff here
  </aside>
</body>
</html>
```

Both our main `<section>` and our `<aside>` have headings, and since they're not the page title, they use `<h2>`. The "Table of Contents" heading might be a lot smaller than the `<h2>`s used in the main section, but it's stll an `h2`.

The `About this website` heading covers information about the website, and there's an additional sub-heading that relates to it, `About this website's creator`. Because it's related content, it drops down to an `h3`; if we used an `h2`, it would be considered a "sibling" by assistive technologies, instead of deeper information on the same subject.

## `button`

The button tag is used to display a clickable button. Its descendants cannot be a clickable element (eg: `<button><a href="/foobar"/></button>`)

## `ul`

The ul tag ("Unordered List") is for bullet point lists. The children of a ul element should be li elements

## `li`

The li tag is for list elements. The parent of an li element should be a ul or ol element.

## `ol`

The ol ("Ordered List") tag is for numbered lists. The children of a ol element should be li elements, same as `ul`.

## `select`

The select tag is for drop down selection. It renders option elements.

## `option`

The option tag is for a select option. You can add multiple options by adding option elements as children of the select tag.

## `p`

The p tag is used for text. It displays the text on a new line. By default, some space will be created around the text.

## `div`

The div tag is generic and is used in many situations.

## `span`

The span tag is also used for text. However, it doesn't create a new line. It is only useful when combined with css or event handlers (covered in later chapters)

## `p` vs `div`

Any time you can use a `p`, you could also have used the more generic `div` tag. ~Usually, it doesn't really matter which one you choose.~ IT MATTERS!

### Here are the advantages to using a p tag

It makes your page easier to analyze by screen readers and therefore more accessible to the blind.

`p` tags increase code readability and maintainability.

## `a`

Anchor tags are for links on a website. They always have an href attribute which corresponds to the destination address.

```html
<a href="http://google.com">The googs</a>
```

Its descendants cannot be a clickable element (eg: `<button><a href="/foobar"/></button>`)

## `img`

`img` tags are for images. They always have an src attribute which corresponds to the location of the image on the internet.

The `img` requires an `alt` attribute. It is the title/label of the image. This attribute is used when the image is missing, by screen readers (accessibility) and is just plain good practice.

```html
<img
  src="https://example.com/images/thailand-sunset.png"
  alt="Sunset on the beach in Thailand"
/>
```

## `form`

`form` tags are for forms. They usually contain descendants that are input tags.

## `input`

`input` tags are usually (but not necessarily) found inside a form element. They always have a type attribute that dictates their purpose, how they are displayed and how users interact with them.

For example,

- `type="text"` is for text boxes where users can enter information (eg their username)
- `type="password"` is for text boxes where users can enter their password (which is hidden when they type)

### Why put input elements inside a form?

Pressing enter in an input element submits the form. This is very convenient. Also, forms can be autofilled by your browser, but orphaned input tags can't. Form tags provide an easy way to send information to a server. We will cover this topic in a later chapter.

## `table`

`table` tags are (surprisingly) for tables. They contain rows of data. Each row contains cells.

## `tr` (table row)

`tr` defines a new table row. Its children are td or th elements.

## `td` (table data)

A table cell. It is always the child of a tr element.

## `th` (table head)

A `table` cell. Usually placed in the first row. Indicates that it is the header of the column in the table.

_Please don't use tables. Unless you actually need to render "tabular" data, `table` is the Voldemort of HTML tags._
