---
layout: post
title: Comments on Github Pages with giscus
date: 2024-05-24
categories: comments, giscus, github pages, github discussions, static websites
permalink: /giscus-comments
---

I added a commenting feature for the blog using [giscus][giscus]. Basically, it uses [Github Discussions][discussions-docs] to store comments instead of storing it in its own database on the web server. Since this website is hosted on [Github Pages][pages-docs] and Pages only supports static websites, it cannot host its own databases to store things such as comments. This guide explains how to add giscus comments to statically-hosted websites, and some quirks and caveats with using Github Discussions as a database for your comments.

# Try it

You can test it out yourself on this blog post in the comments below by signing into your Github account and commenting, or you can comment on the [repository's Github Discussions](https://github.com/de-soot/de-soot.github.io/discussions) directly and it will show up on the comments section on the website similarly.

# Add it to your own Github Pages website

1) Make sure to enable Github Discussions on your website's Github repository.

2) Navigate to `giscus.app` on your browser's address bar and follow the instructions under the "Configuration" section to configure your `<script>` tag attribute values.

3) After you have done so, you can simply copy and paste it into your webpage!

# Note

Giscus finds and links the comments to the Github Discussions by searching through and matching URLs, path names, titles, and other such metadata. If you try to change a page's title without editing the associated Github Discussion accordingly, it may lead to giscus not being able to find and link it to the Github Discussion (this is especially noticible if you set the `<script>`'s `data-strict` attribute value to `"1"`), and hence Giscus will create a new Github Discussion.

Giscus also does not update or sync the posts made on Github Discussions with the blogs on your website, so you may have to manually copy across the changes and edits you make to your blog posts. Luckily, giscus only creates a post on Discussions when there is interaction (reactions or comments) with giscus on your blog post, so it should not be an issue for new blog posts that no one has commented or reacted to yet.

[giscus]: https://giscus.app
[discussions]: https://github.com/de-soot/de-soot.github.io/discussions
[discussions-docs]: https://docs.github.com/en/discussions
[pages-docs]: https://docs.github.com/en/pages

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
