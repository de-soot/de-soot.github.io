---
layout: post
title: Justify and Hyphenate Text on Websites using CSS
date: 2024-09-07
categories: justify, text-align, jekyll, css
permalink: /justify-text
---

You may have noticed while reading my blog posts that the way the text are aligned are a little different from the usual way the ones from other websites are --- that they always align as blocks of text no matter how you change your browser window's size. This is because using CSS, I have justified the text on my website.

# How to Justify

It is actually pretty simple --- to justify your body text, just add this to your CSS style sheet:

```css
body {
    ...
    text-align: justify;
}
```

This will justify your text so it all aligns neatly in a block-like shape.

# How to Hyphenate

Though there is a way to do this with Javascript using [Hyphenopoly.js][hyphenopoly], hyphenation already has built-in functionality in CSS and it is widely supported by browsers, so it is a no-brainer to do it the CSS way, unless your target audience has a `user-agent` that does not support CSS' `hyphens` property for some reason.

To add hyphenation to your body text, simply add the `hyphens` property to your body section in your CSS style sheet and set it to `auto`, like so:

```css
body {
    ...
    hyphens: auto
}
```

So now your text wraps words using hyphens, but why do we need to use hyphens when we can make blocks of text by just justifying?

# Why Hyphenate

Text justification can make your paragraphs look tidier, but this has the potential side-effect of awkwardly stretching out whitespace in between words --- which can create or worsen an often undesirable effect commonly referred to as 'rivers of white,' which are known to trip up dyslexic readers, making your writing less accessible as a result.

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d2/Typographic_river_marking.svg/1280px-Typographic_river_marking.svg.png" alt="Image from Wikipedia with visual marking around an example of a 'rivers of white' effect.">

This is also a highly-cited reason as to why justification is generally [not][applewood] [recommended][max] for text output on browsers and on the web.

# Other Blogs That Justify

Here are a list of other blogsites that I know of that use justified text:
- Chris Noxz's [noxz.tech][noxz], which renders static HTML from [`groff`][groff].
- Simon Johnston's [simonkjohnston.life][simon], which does not use hyphenation.
- Kyle Mcdonald's [kylemcdonald.net][kyle], which also does not hyphenate.
- Public Delivery's [publicdelivery.org][pubdeliver], which also justifies without hyphens.
- JPEG XL's [jpegxl.info][jpg], which had fixed its un-hyphenated text.

[max]: https://maxwellforbes.com/posts/web-justified-text
[jpg]: https://jpegxl.info 
[noxz]: https://noxz.tech
[kyle]: https://kylemcdonald.net/psac
[simon]: https://simonkjohnston.life
[groff]: https://www.gnu.org/software/groff
[applewood]: https://applewoodinteractive.com/accessibility/rivers-of-white-why-you-should-never-justify-your-text 
[pubdeliver]: https://publicdelivery.org
[hyphenopoly]: https://mnater.github.io/Hyphenopoly
