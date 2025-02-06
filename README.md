# de-soot.github.io

A place on the internet where I write about my write about things that interest me.

## Usage

### Visit Online

Click [here](https://de-soot.github.io)

### Run Locally

1) [Clone](https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories) this github repository onto your computer by simply downloading the source code from this Github repository, or by using [`git`](https://git-scm.com):
```
git clone https://github.com/de-soot/de-soot.github.io
```
2) Follow [this guide](https://jekyllrb.com/docs/installation) to install the prerequisites for Jekyll for your system if you have not already done so.
3) Once all requirements are installed, run the following command below in a command line terminal:
```
gem install jekyll bundler
```
4) Now that everything's installed and good to go, navigate the terminal to the directory where the you downloaded the copy of the Github repository, like so:
```
cd "{Path of source code folder}"
```
5) Enter this command:
```
bundle exec jekyll serve
```
6) Navigate to http://localhost:4000 in a browser.
7) Profit!

Refer to the [official Jekyll documentation](https://jekyllrb.com/docs) for more information regarding installing and running Jekyll.

### Write a Blog Post

1. Create a markdown (`.md`) file inside `/_posts` with this at the top of the document:

```md
---
layout: post
title:
date: YYYY-MM-DD
categories:
permalink: /...
---
```

2. Write the title of the post after `title:`.
3. Replace `YYYY`, `MM`, and `DD` with the year, month, and day the post is published, respectively.
4. Add any keywords related to the topic of your post after `categories:` separated by commas.
5. Replace the `...` after `permalink:` with the custom path given to the blog post.
