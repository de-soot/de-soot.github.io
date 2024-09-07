---
layout: post
title: Reponsive Web Text with Auto Justify and Hyphens Using Only CSS
date: 2024-09-07
categories: justify, text-align, jekyll, css
permalink: /justify-text
---

You may have noticed the way the text are aligned in my blog posts are a little different from the usual way other websites normally align them, and that they always align as blocks of text no matter how you change your browser window's size. This is because using CSS, I have justified and hyphenated the text on my website so it looks a whole lot cleaner and easier to read than if I had left it in its default jagged-right form as-is.

# How to Hyphenate
Though there is a way to do this with Javascript using [Hyphenopoly.js][hyphenopoly], hyphenation already has built-in functionality in CSS and it is widely supported by browsers, so its a no-brainer unless your target audience has a user-agent that does not support CSS `hyphens` property for some reason.

To add hyphenation to your body text, simply add the `hyphens` property to your body section in your CSS style sheet and set it to `auto`, like so:

```css
body {
    ...
    hyphens: auto
}
```

# How to Justify
Great! So now your text wraps words using hyphens, but there is still jaggedness on the right due to your text not being aligned properly. To fix this, we can use the `text-align` property and set it to `justify`, like this:

```css
body {
    ...
    text-align: justify;
```

This will justify your text so it all aligns neatly.

# Other Blogs That Use Justify
~~Here are a list of other blogsites that I know of that use justified text:~~

As of right now, I only know of one, and that is:

Chris Noxz's [noxz.tech][noxz], which renders static HTML from [`groff`][groff].

[noxz]: https://noxz.tech
[groff]: https://www.gnu.org/software/groff
[hyphenopoly]: https://mnater.github.io/Hyphenopoly
