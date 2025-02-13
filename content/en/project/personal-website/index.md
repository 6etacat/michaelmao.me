---
title: "Personal Website"
subtitle: ""
date: 2022-10-07T00:36:54-07:00
draft: false
weight: 2
description: "Personal website built with Hugo"
coverImage: "website.png" # a 5:1 image with important content in the center 1/3 zone for best effect
cardImage: "website.png" # a thin image/video featured on cards
autonumbering: false
katex:
  enable: false
  singleDollarDeliminator: false
---

![Home page layout](website-tall.png "Home page layout")

Links: [GitHub Repo](https://github.com/michaelmyc/michaelmao.me), [Example Blogpost](/blog/example-blogpost)

## Overview

This personal website is made from scratch using [Hugo](https://gohugo.io/) framework. The color scheme is inspired by [Nord theme](https://www.nordtheme.com/) and all code blocks uses Nord color scheme. The website is responsive and is designed for both mobile and desktop, and supports both vertical and horizontal screen orientations. 

### Home Page and Blogging

The website offers a customizable home page or landing page to suit the need of different users. 

The website also includes a complete blogging system, with elaborate markdown support, pagination and grouping by date, tag support, and serie/collection support. See [example blogpost](/blog/example-blogpost) for features that are tested and supported. If you need one-off custom features, the markdown supports HTML mix-in, so directly writing HTML code the markdown file would render the HTML code. 

Please note that the "series" and "tags" pages won't display series or tags that only contain unlisted blog posts. Unlisted blog posts appear as if they have never been written, but you can still access it through the correct URL. 

### Projects

The website also features sections for personal projects and publications. This section feature a card design that supports banner images. Clicking into the cards reveals regular blog posts that can be used to explain the project/publication in more detail. 

### Photography

I also included a photography section that features a 3-column masonry design (if the screen is wide enough) for showcasing images. The ordering of the images are manual and images are allowed to span multiple columns to allow for most optimal visual layout. 

## Adapting This Website

You can easily adapt this website by forking my [GitHub repository](https://github.com/michaelmyc/michaelmao.me). 

### Removing My Contents

To clear out my contents, you should remove all files in `content`. 

`layouts/_index.html` is the home page, and you will likely want to customize it to suit your needs. 

Other things you may want to customize are the footer in `layouts/partials/footer.html`, the favicon, cover image, and CNAME file under `static`. 

### Adding Your Contents

Most of the site is configurable through the `config.toml` file. The settings should be fairly self-explanatory. You should also add your own CNAME, cover image, and favicon in `static`. 

To add a page of a specific type (blog/project/photography), `hugo new [language]/[type]/[name]` will create the page in the `content` folder from the relevant template in the `archetypes` folder. 

### Auto Deploy to GitHub Pages

The repository supports CI with [GitHub Workflows](https://docs.github.com/en/actions/using-workflows). This means any push to the repository will automatically be built and published as GitHub Pages. If you're not using GitHub Pages to host your website, you should remove the `.github` folder. If you want to adapt this feature to your own GitHub Pages, you will need to modify the last few lines of `.github/workflows/deploy-site.yml` according to your setup:

![](gh-workflow.png "Config that needs changes")