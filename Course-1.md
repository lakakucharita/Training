# Bla ... Bla ... Bla ...

## A little bit history (warm up)

### WHATWG was formed to counter W3C's decision [1]

The WHATWG was formed in response to the slow development of World Wide Web Consortium (W3C) web standards and W3C's decision to abandon HTML in favor of XML-based technologies. The WHATWG mailing list was announced on 4 June 2004, two days after the initiatives of a joint Opera–Mozilla position paper had been voted down by the W3C members at the W3C Workshop on Web Applications and Compound Documents.

### W3C adopted WHATWG's HTML5 standard [2]

On 10 April 2007, the Mozilla Foundation, Apple, and Opera Software proposed that the new HTML working group of the W3C adopt the WHATWG’s HTML5 as the starting point of its work and name its future deliverable as "HTML5". On 9 May 2007, the new HTML working group resolved to do that.

### HTML5 was renamed to HTML, as a living standard [3]

HTML formerly known as HTML5 (formerly titled Web Applications 1.0) is the fifth major version of the HTML specification and has been adopted by the W3C as the starting point of the work of the new HTML working group. On 19 January 2011, Ian Hickson announced that the standard would now be called HTML instead of HTML5. The specification for HTML will be a living document that will have continuous changes as necessary.

### How does this effect developers?

It means developers need to keep their knowledge updated all the time for new widely implanted features.

### What are we talking about when referencing HTML5

![HTML5 family](http://upload.wikimedia.org/wikipedia/commons/thumb/f/f7/HTML5-APIs-and-related-technologies-by-Sergey-Mavrody.png/1024px-HTML5-APIs-and-related-technologies-by-Sergey-Mavrody.png)

The meaning varies when the context changes, in our course, the word "HTML5" is referencing mainly the initial WHATWG specification.

### ... HTML5 & CSS3 ...

bla ... bla ... bla ...



## SMACSS, BEM, SASS

### How to organise (SMACSS)?

#### A sample folder structure:

```
/stylesheets/

  ...

  /base/
    _reset.scss
    _typography.scss
  /layouts/
    _grid.scss
    _header.scss
    _footer.scss
  /modules/
    _doormat.scss
    _carousel.scss
    _video_player.scss

  ...

```

#### Base

Base rules are the boilerplate. They are almost exclusively single element selectors but it could include attribute selectors, pseudo-class selectors, child selectors or sibling selectors. Essentially, a base style says that wherever this element is on the page.

Normally, there is `reset.scss` or `normalize.scss`, and some other basic stylesheets depends on your projects.

Code samples:

```scss
@mixin font-family($family) {
  font-family: '#{$family}', sans-serif;
}

strong {
  @include font-family('univers-bold');
}
```

```css
strong {
  font-family: 'univers-bold', sans-serif;
}
```

#### Layouts

Layout rules divide the page into sections. Layouts hold one or more modules together (Containers).

Normally, there is `_grid.scss` holds the grid system to build the layouts, unless there is another grid system, like you have got Susy or Bootstrap.

Sample codes:

```scss
.main-content {
  @include columns(6);
}
```

```css
.main-content {
  float: left;
  width: 47.541%; /* span 6 columns */
  margin-right: 1.639%;
}
```

#### Modules

Modules are the reusable, modular parts of our design. They are the callouts, the sidebar sections, the product lists and so on. Sometimes, the folder is also called components, usually there is lots of files, your site should be mostly composed of tiny modules.


### How to name (BEM)?

Sample codes:

```scss
.author {
  color: #333;
}

author-name {
  font-weight: bold;
}

author-avatar {
  border: 2px solid #333;
}

author-avatar-size-small {
  width: 100px;
  height: 100px;
}
```

BEM stands for "Block, Element, Modifier".

#### What's a "Block"?

A block is an independent entity, a "building block" of an application. A block can be either simple or compound (containing other blocks).

In above sample, `author` is a block.

##### Block Independence

As projects grow, blocks tend to be added, removed, or moved around the page. To make this process easier, blocks must be independent.

An independent block is implemented in a way that allows arbitrary placement — anywhere on the page, including nesting inside another block.

From the CSS point of view it means that

1. A block (or an element) must have a unique "name" (a CSS class) that could be used in a CSS rule.
1. HTML elements must not be used in CSS selectors (.menu td) as such selectors are inherently not context-free.
1. Cascading selectors should be avoided.

##### Blocks Reiteration

Blocks may appear more than once on a page.

In CSS related terms, it means

1. ID-based CSS selectors must not be used.
  * Only class selectors satisfy our non-uniqueness requirement.

On the JavaScript side it means:

1. Blocks with similar behavior are detected unequivocally: they have the same CSS classes
  * Using CSS class selectors allow picking all blocks with a given name to apply the required dynamic behavior.

#### What's an "Element"?

An element is a part of a block that performs a certain function. Elements are context-dependent: they only make sense in the context of the block they belong to.

In above sample, `name`,`avatar` are elements.

#### What's a "Modifier"?

A modifier is a property of a block or an element that alters its look or behavior.

A modifier has a name and a value. Several modifiers can be used at once.

In above sample, `size-small` is a modifier for `avatar` element.

## References

1. What is the WHATWG? http://wiki.whatwg.org/wiki/FAQ#What_is_the_WHATWG.3F
2. Proposal to Adopt HTML5 http://lists.w3.org/Archives/Public/public-html/2007Apr/0429.html
3. HTML is the new HTML5 http://blog.whatwg.org/html-is-the-new-html5
