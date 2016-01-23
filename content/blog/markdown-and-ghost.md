+++
date = "2016-01-23T13:59:05+01:00"
draft = true
title = "markdown and ghost"

+++

##What is markdown
It's a plain text formating syntax, which is easy to read, optionally it can be converted to HTML.

##Why use it
Because it is really easy, fast and powerfull. Without markdown one can use basically text editor and **mouse** to format text, the other option is to write text in pure HTML to format it nicely, but it's much harder (nobody really want to type those ugly tags).

##Syntax
###Headers
```
H1 header
=========
H2 header
---------

or as a alternative
#H1
##H2
###H3
####H4
#####H5
######H6

```
H1 header
=========
H2 header
---------
#H1
##H2
###H3
####H4
#####H5
######H6

###Emphasis
```
Italics, with *asterisks* or _underscores_.

Bold, with **asterisks** or __underscores__.

Combine bold with italics **asterisks and _underscores_**.

Strikethrough uses two tildes. ~~Scratch this.~~
```
Italics, with *asterisks* or _underscores_.

Bold, with **asterisks** or __underscores__.

Combine bold with italics **asterisks and _underscores_**.

Strikethrough uses two tildes. ~~Scratch this.~~
###Unordered lists
```
* Unordered list can use asterisks
- minuses
+ or pluses
```
* Unordered list can use asterisks
- minuses
+ or pluses

Use whichever suits you best, personaly I like to asterisks.

###Ordered Lists
```
1. First ordered list item
2. Another item
 * Unordered sub-list.
1. Actual numbers don't matter, just that it's a number
 1. Ordered sub-list
 4. And another item.
  Paragraphs within list items, just start with the leading space

  To have a line break without a paragraph, you will need to use two trailing spaces.  
  Note that this line is separate, but within the same paragraph.  
```

### Links

```
[click github](https://www.github.com)
[click github](https://www.github.com "Github's Homepage Hint")
```
[click github](https://www.github.com)

[click github with hint](https://www.github.com "Github's Homepage Hint")

### Images

```
Inline-style:
![alt text](https://ghost.org/assets/logos-d976c73a12a1a34a3db6be321db81f71.png "Logo Title Text 1")

Reference-style:
![alt text][logo]

[logo]: https://ghost.org/assets/logos-d976c73a12a1a34a3db6be321db81f71.png "Logo Title Text 2"
```
### Code and Syntax Highlighting

Code blocks are part of the Markdown spec, but syntax highlighting isn't. To add highlighting into ghost read [in this blog post](http://blog.davebalmer.com/adding-syntax-highlighting-to-ghost/ "Add highlighting to Ghost blog")

### Tables
At the moment Ghost does not support tables. Hopefully it will in the near future.

### Blockquotes

```
> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote.
```

> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote.
### Horizontal Rule


### Inline HTML

Using HTML is very simple in markdown

```
<ul>
 <li>Item 1</li>
 <li>Item 2</li>
 </ul>
```
<ul>
 <li>Item 1</li>
 <li>Item 2</li>
</ul>

### Line Breaks
To manipulate line breaks use *space* and *Enter*
```
Lorem ipsum dolor sit amet enim. Etiam ullamcorper.

Suspendisse a pellentesque dui, non felis. Maecenas malesuada elit lectus felis, malesuada ultricies.
Curabitur et ligula. Ut molestie a, ultricies porta urna.

Vestibulum commodo volutpat a, convallis ac, laoreet enim. Phasellus fermentum in, dolor. Pellentesque facilisis. Nulla imperdiet sit amet magna. Vestibulum dapibus, mauris nec malesuada fames ac turpis velit, rhoncus eu, luctus et interdum adipiscing wisi. Aliquam erat ac ipsum. Integer aliquam purus. Quisque lorem tortor fringilla sed, vestibulum id, eleifend justo vel bibendum sapien massa ac turpis faucibus orci luctus non, consectetuer lobortis quis, varius in, purus. Integer ultrices posuere cubilia Curae, Nulla ipsum dolor lacus, suscipit adipiscing. Cum sociis natoque penatibus et
```

Lorem ipsum dolor sit amet enim. Etiam ullamcorper.

Suspendisse a pellentesque dui, non felis. Maecenas malesuada elit lectus felis, malesuada ultricies.
Curabitur et ligula. Ut molestie a, ultricies porta urna.

Vestibulum commodo volutpat a, convallis ac, laoreet enim. Phasellus fermentum in, dolor. Pellentesque facilisis. Nulla imperdiet sit amet magna. Vestibulum dapibus, mauris nec malesuada fames ac turpis velit, rhoncus eu, luctus et interdum adipiscing wisi. Aliquam erat ac ipsum. Integer aliquam purus. Quisque lorem tortor fringilla sed, vestibulum id, eleifend justo vel bibendum sapien massa ac turpis faucibus orci luctus non, consectetuer lobortis quis, varius in, purus. Integer ultrices posuere cubilia Curae, Nulla ipsum dolor lacus, suscipit adipiscing. Cum sociis natoque penatibus et
