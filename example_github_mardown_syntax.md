Comments:

>Markdown’s syntax is intended for one purpose: to be used as a format for writing for the web.

>Markdown is not a replacement for HTML, or even close to it. Its syntax is very small, corresponding only to a very small subset of HTML tags. The idea is not to create a syntax that makes it easier to insert HTML tags. In my opinion, HTML tags are already easy to insert. The idea for Markdown is to make it easy to read, write, and edit prose. HTML is a publishing format; Markdown is a writing format. Thus, Markdown’s formatting syntax only addresses issues that can be conveyed in plain text.

>For any markup that is not covered by Markdown’s syntax, you simply use HTML itself.

StackOverflow and Github likely strip out much HTML for security purposes.

Also note this is GFM(Github Flavoured Markdown).

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6

## Text Decoration

Regular Text
**Bold with double asterisk**
__Bold with double underline__
*Italic single asterisk*
_Italic single underline_
_You **can** combine them_
~~Strikethrough with double tilde~~

## Text Colour

<span style="color:blue">some *This is Blue italic.* text</span>
<span style="color:red">some **This is Red Bold.** text</span>

<div style="background-color:rgba(0, 0, 0, 0.0470588); text-align:center; vertical-align: middle; padding:40px 0;">
 <a href="#">TEXT</a>
 </div>
 

## Blockquote

You can quote like this:

> Here is how you spell google
> g-o-o-g-l-e

## Links

Any link such as http://github.com is automatically converted to a clickable link in Github.

http://github.com - automatic!
[GitHub](http://github.com) - square brackets with text, followed by the URL in paranthesis

```
[I'm an inline-style link](https://www.google.com)

[I'm an inline-style link with title](https://www.google.com "Google's Homepage")

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[I'm a relative reference to a repository file](../blob/master/LICENSE)

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself]

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[link text itself]: http://www.reddit.com
```

## Images 

![GitHub Logo](https://www.google.ca/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png)
Format: ![Alt Text](https://www.google.ca/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png)

## Resize Images
Most Markdown implementations have a modified syntax. Github can do image resizing:

![](https://www.google.ca/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png | width=100)

![](https://www.google.ca/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png =25x25)

HTML images do not seem to work in regular markdown, but should work on github: <img src="https://www.google.ca/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png" width="200" height="40">

Or could use this html trick, with the `<div>` tag:
<div style="width:50%">![Chilling](https://www.google.ca/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png)</div>

But this one seems to work, though doesn't seem to obey BOTH height and width: 
![test image size](https://www.google.ca/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png){height="100%" width=50%"}

Note that if you're using an image hosted on GitHub, you can resize using the s query param, e.g. s=80

![](https://avatars3.githubusercontent.com/u/31112269?v=4&s=80)

Or if you use a CSS stylesheet:

img[alt=drawing] { width: 200px; }

And a solution using Latex syntax:

\begin{figure}
 \includegraphics[width=300pt, height = 125 pt]{https://www.google.ca/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png}
\end{figure}

You can use `\begin{center}` statement to center the image



###### Relative Images

![GitHub Logo](/images/logo.png)
Format: ![Alt Text](url)


## Ordered List

1. One
	1. sub one
	2. sub two
2. Two
3. Three

## Unordered List

- One
	- sub one
	- sub two
- Two
- Three
* Or use an asterisk
+ Or a plus

## Nested List

Be sure to start the nested list bullet or number directly under the first character of the parent list item:

1. Here is item one
      - the bullet is under the H of Here
        - my third list is under the t of the
2. Here is item two
      - again under the H
        - under the a
        - second item under the a
                

## Task List

- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item

If a task list item description begins with a parenthesis, you'll need to escape it with \:

- [ ] \(Optional) Open a followup issue

## Inline code

In your text you can add html tags like this:
`<addr>` element or perhaps to show the img tag without
actually rendering the image tag:
`<img src="https://www.google.ca/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png">` 

You can also use these `backticks` to simply highlight a `word`.

## Tables

Tables aren't part of the core Markdown spec, but they are part of GFM.

First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

```
Colons can be used to align columns.

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned |  |
| col 2 is      | centered      |    |
| zebra stripes | are neat      |     |

The outer pipes (|) are optional, and you don't need to make the raw Markdown line up prettily. You can also use inline Markdown.

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3
```

Colons can be used to align columns.

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned |  |
| col 2 is      | centered      |    |
| zebra stripes | are neat      |     |

The outer pipes (|) are optional, and you don't need to make the raw Markdown line up prettily. You can also use inline Markdown.

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3

## Syntax Highlighting

This uses triple backticks:

```javascript
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```
OR you can indent your code like with python style four spaces like so:

    function fancyAlert(arg) {
      if(arg) {
        $.facebox({div:'#foo'})
      }
    }
    

## Line Breaks and Spacing

Be sure to hit `Enter` to . GFM usually just needs one line break to start a new paragraph.

Other MD implementations often need 2 new lines, created by hitting `Enter` twice.

To add space between lines, use `<br />` tags.
<br /><br /><br /><br /><br /><br />

Notice all the space above?


## Supress Comments

Use HTML comments to suppress text from the rendered output

`<!-- Does not show up -->`

Nothing to see here --> <!-- does this show up --> <--


## Horizontal Line

Use three hyphens (dashes), asterisks, or underscores

---
***
___

Each of the following lines will produce a horizontal rule:

```
* * *
***
*****
- - -
---------------------------------------
_ _ _
```


## Spacing

When writing MD, adding a newline after each statement will help ensure the following text isn't accidentally renderd with the previous MD syntax.

Also be sure to add a trailing space after some markdown statements. This can sometimes help ensure that the statement is "closed off".



## Emoji icons

You can add emoji to your writing by typing :EMOJICODE:

Github supports emoji's. Example of thumbs up:  :+1:

https://help.github.com/articles/basic-writing-and-formatting-syntax/#using-emoji

## Ignoring Markdown

You can tell GitHub to ignore (or escape) Markdown formatting by using \ before the Markdown character.

Let's rename \*our-new-project\* to \*our-old-project\*.


## References

Learn more about Markdown on Github:

https://help.github.com/articles/basic-writing-and-formatting-syntax/

https://guides.github.com/features/mastering-markdown/

https://sindresorhus.com/github-markdown-css/

https://help.github.com/articles/working-with-advanced-formatting/


