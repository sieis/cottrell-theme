---
title: "SEO"
author: "Eamonn Cottrell"
subtitle: "Adding dynamic meta descriptions and canonical link tags to Hugo sites"
date: 2021-11-23T16:27:02-05:00
draft: false
image: "/images/posts/seo.png"
alt: "Work illustration by Storyset"
section: ""
description: "A quick primer on updating my Hugo site to include custom meta descriptions on each page as well as canonical link tags for each page."
attribute: "Work illustrations by Storyset: https://storyset.com/work"
---
## Meta & Canonical Tags

So I need to do some meta work. I've touched on the Hugo theme that I built for my home page [here]({{< ref "/posts/portfolio.md" >}} "About Us"), but this only covered the very basics of going live. Time to add some details!

I've already added a few meta tags to my head, but I'd like to dynamically generate the meta description depending on which page is being viewed.

I'd also like to add canonical tags to each page. Same deal here--they should be generated uniquely for every page on the site.

I've been checking out a primer on SEO from [Monica Lent](https://monicalent.com/), and implementing some of the basic suggestions she's going through on her weekly videos.

The first suggestions include adding a browser extension to check out several things at a glance. Opening the developer console is the sure fire bet here, but I'm pretty happy for her recommendation of an extension to get a real quick snapshot of some basics like title, description, url, canonical, etc. 

I went with [Detailed](https://detailed.com/extension/).

In Hugo, which I'm using to generate my personal web portfolio, I've currently got the meta description set statically for the whole site, regardless of the page. 

That's not cool.

So, I'm going to add a bit of code to modify that and allow me to include a custom description for each page, if it contains one. Otherwise, it can just have the main site description to fall back on.

Hugo's conditional statement formatting is a little wonky for the unfamiliar, but it was pretty simple once I got the syntax down:


``` go
{{ if .Params.description}}{{.Params.description}}{{else}}{{.Site.Params.Description}}
```

If there's a description in an individual page's front matter, then that'll be used for the meta description. If not, it'll fall back to the site's description which I've got plugged into the config.toml.

I've also added a description field to each of my archetypes so any page I create will have that in the front matter. 

I've added this to the main pages

For URL canonization, I simply added ``` html 
<link rel="canonical" href="{{.Permalink}}">
``` 
to the head template fore every page.

Hugo has some interesting content-management information regarding links, URLS and Canonicalization available in their docs [here](https://gohugo.io/content-management/urls/), but I found that the simple Permalink in each of my pages' head was sufficient for my purposes..


