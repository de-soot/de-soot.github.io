---
layout: post
title: Justify and Hyphenate Text on Websites using CSS
date: 2024-09-07
categories: justify, text-align, jekyll, css
permalink: /justify-text
---

You may have noticed while reading my blog posts that the way the text are aligned are a little different from the usual way the ones from other websites are --- that they always align as blocks of text no matter how you change your browser window's size. This is because I have justified the text on my website using CSS.

# How to Justify

It is actually pretty simple --- to justify your body text, just add this to your CSS style sheet:

```css
body {
    text-align: justify;
}
```

This will justify your text so it all aligns neatly without jagged edges.

# How to Hyphenate

Although there is a way to do this with Javascript using [Hyphenopoly.js][hyphenopoly], hyphenation is a built-in functionality in CSS and it is widely supported by browsers.

To add hyphenation to your body text, simply add the `hyphens` property to your body section in your CSS style sheet and set it to `auto`, like so:

```css
body {
    hyphens: auto
}
```

# Why Hyphenate

So now your text wraps words using hyphens, but why do we need to use hyphens that ruin the perfect edges that justifying makes?

Text justification can make your paragraphs look tidier, but this has the potential side-effect of awkwardly stretching out the whitespace between words --- which can create and worsen an undesirable effect commonly referred to as 'rivers of white', which is known to trip up dyslexic readers and decrease accessibility.

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d2/Typographic_river_marking.svg/1280px-Typographic_river_marking.svg.png" alt="Image from Wikipedia with visual marking around an example of a 'rivers of white' effect.">

This is also a common reason as to why justification is generally [not][applewood] [recommended][max] for text output on the web.

By hyphenating, even though it does not solve it completely, it will reduce the effect dramatically.

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

<script src="https://giscus.app/client.js"
        data-repo="de-soot/de-soot.github.io"
        data-repo-id="R_kgDOK6_5tA"
        data-category="Announcements"
        data-category-id="DIC_kwDOK6_5tM4CflCT"
        data-mapping="title"
        data-strict="0"
        data-reactions-enabled="1"
        data-emit-metadata="0"
        data-input-position="top"
        data-theme="preferred_color_scheme"
        data-lang="en"
        data-loading="lazy"
        crossorigin="anonymous"
        async>
</script>
