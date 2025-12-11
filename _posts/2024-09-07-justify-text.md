---
layout: post
title: Justify and Hyphenate Text on Websites using CSS
date: 2024-09-07
categories: justify, text-align, jekyll, css, static site generator
permalink: /justify-text
---

## For Static-Site-Generator Websites

It is a little bit less straightforward to follow this guide with static site generators like Jekyll (which is what this website also uses) or Hugo, you will have to override the theme's CSS style sheet.

There is a [blog post by Tom Kadwill on how to override your CSS styles in Jekyll][css-blog] you can follow to create your SCSS file, and after which you should get something resembling this:

```css
---
---

@import "minima"; /* replace minima inside the quotes with your Jekyll theme */
```

After this, you can follow all the steps below the same way as it would be done if you were using CSS in a non-static-site-generator instead of SCSS in a static site generator.

## Why Justify Text

It is more of an aesthetic preference than anything. This jaggedness generally does not bother people that much because they have grown used to the popular left-aligned style of text on the web and probably do not know justification even exists on the web, only on printed books and newspapers. But it just looks better to me when all lines are the same length and the right side of text is not jagged. Justifcation is a way of acheiving that aesthetic goal without cutting words off abruptly.

## How to Justify

It is actually pretty simple. To justify your body text, just add this to your CSS style sheet:

```css
body {
    text-align: justify;
}
```

## Why Hyphenate

Text justification can make your paragraphs look tidier, but it has the side-effect of awkwardly stretching out the whitespace between words, which can create and worsen an undesirable effect commonly referred to as 'rivers of white'. This effect is known to make text harder for dyslexic readers to read, decreasing accessibility.

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d2/Typographic_river_marking.svg/1280px-Typographic_river_marking.svg.png" alt="Image from Wikipedia with visual marking around an example of a 'rivers of white' effect.">

This is why justification is generally [not][applewood] [recommended][max] for text output on the web.

By hyphenating, even though it does not solve the problem completely, it will reduce this effect significantly while keeping text not jagged.

Hyphenating text will cut off some words at the end of lines (indicated by an auto-inserted hyphen), but it will do it with an algorithm that tries to make it seamless.

## How to Hyphenate

Although there is a way to hyphenate with Javascript using [Hyphenopoly.js][hyphenopoly], there already is a built-in functionality in CSS to do this and it is [widely supported by browsers](https://developer.mozilla.org/en-US/docs/Web/CSS/hyphens).

To add hyphenation to your body text, simply add the `hyphens` property to your body section in your CSS style sheet and set it to `auto`, like so:

```css
body {
    hyphens: auto
}
```

## Other Blogs That Justify

Here are a list of other blogsites that I know of that use justified text:
- Chris Noxz's [noxz.tech][noxz], which renders static HTML from [`groff`][groff].
- Simon Johnston's [simonkjohnston.life][simon], which does not use hyphenation.
- Kyle Mcdonald's [kylemcdonald.net][kyle], which also does not hyphenate.
- Public Delivery's [publicdelivery.org][pubdeliver], which also justifies without hyphens.
- JPEG XL's [jpegxl.info][jpg], which had fixed its un-hyphenated text.

## Conclusion

f you found this blog post useful, leave a comment down below! Also read how to add reactive dark-mode to your website in my [previous blog post](/dark-mode).

[max]: https://maxwellforbes.com/posts/web-justified-text
[jpg]: https://jpegxl.info 
[noxz]: https://noxz.tech
[kyle]: https://kylemcdonald.net/psac
[simon]: https://simonkjohnston.life
[groff]: https://www.gnu.org/software/groff
[applewood]: https://applewoodinteractive.com/accessibility/rivers-of-white-why-you-should-never-justify-your-text 
[pubdeliver]: https://publicdelivery.org
[hyphenopoly]: https://mnater.github.io/Hyphenopoly
[css-blog]: https://tomkadwill.com/2017/12/16/how-to-override-css-styles-in-jekyll

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
