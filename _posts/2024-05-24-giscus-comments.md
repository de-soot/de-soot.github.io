---
layout: post
title: Comments on Github Pages with Giscus
date: 2024-05-24
categories: comments, giscus, github pages, github discussions, static websites
permalink: /giscus-comments
---

I added a commenting feature for the blog using [giscus][giscus]. Basically, it uses [Github Discussions][discussions-docs] to store comments instead of storing it in its own database on the web server. Since this website is hosted on [Github Pages][pages-docs] and Pages only supports static websites, it cannot host its own databases to store things such as comments.

# Try it
You can test it out yourself in the comments on blog post below by signing into your github account and commenting, or you can comment on the repository's Github Discussions directly and it will show up on the comments section on the website similarly.

# Add it to your own Github Pages website
1) Make sure to enable Github Discussions on your website's Github repository.

2) Navigate to `giscus.app` on your browser's address bar and follow the instructions under the "Configuration" section to configure your `<script>` tag attribute values.

3) After you have done so, you can simply copy and paste it into your webpage!

---

# Note
Giscus finds and links the comments to the Github Discussions by searching through and matching URLs, path names, titles, and other such metadata. If you try to change a page's title without editing the associated Github Discussion accordingly, it may lead to giscus not being able to find and link it to the Github Discussion (this is especially noticible if you set the `<script>`'s `data-strict` attribute value to `"1"`), and hence Giscus will create a new Github Discussion.

Giscus also only creates Discussions when someone comments, so it is easier to go back and edit to fix some things on your post if you do not have any comments yet rather than when your post already has comments in its own Discussion and you have to manually copy across those changes.

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
