---
layout: layout.html
title: You Can Comment Now
date: 2024-05-24 20:28:03 +0800
categories: comments, giscus
permalink: /added-commenting
---

I added the commenting feature on the blog posts using [giscus][giscus]. Basically, it uses [Github Discussions][discussions-docs] to store comments instead of storing it in its own database on the web server. Since this website is hosted on [Github Pages][pages-docs] and Pages only supports static websites - which cannot host their own databases to store things such as comments.

You can try it out yourself by signing into your github account and commenting below, or you can comment on the repository's [Github Discussions][discussions] directly and it will show up on the comments section on the website similarly.

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
        data-strict="1"
        data-reactions-enabled="1"
        data-emit-metadata="0"
        data-input-position="top"
        data-theme="preferred_color_scheme"
        data-lang="en"
        data-loading="lazy"
        crossorigin="anonymous"
        async>
</script>
