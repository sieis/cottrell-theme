---
title: "Portfolio"
author: "Eamonn Cottrell"
subtitle: "Building a Hugo Themed Portfolio Site"
date: 2021-11-19T15:05:09-05:00
draft: false
image: "/images/posts/hugo-portfolio.png"
alt: "portfolio banner image"
section: ""
---
## Localhost: 1313

I had a fair amount of success building a template for a niche audience recently: recovery groups in need of a basic, but functional and modern web presence. It ended up being more detailed than I had anticipated, even for the small nature of that template, but I thoroughly enjoyed the process.

I am now in the middle of coding another template for my own portfolio. I'm using #hugo again, and have had a blast building this thing from the ground up.

Yes, there are easier ways to get a portfolio up and running, but I am learning a lot about the structure of Hugo as a static site generator during the process. Also, I have simply not been crazy about many of the available templates. I've always ended up wanting to fiddle with and tweak the ones that I've downloaded and played around with. That's another great way to learn, but I really enjoy building from scratch for something like this.

For my site, I wanted to have a few things available presented in the cleanest way possible:

1. A sharp front page with previews of three main sections.
1. A posts section for blogging and reposting articles like this one on my own page.
1. A projects page to detail the web projects that I work on.
1. A podcast page to highlight the many shows that I produce.

I knew Hugo was still a great choice for this, and after having built one theme from scratch, I had a framework in mind from the very start. I'd create a new theme again, and code the structure of the site's template from within the theme folder. And I'd add custom archetypes, content and images to the respective folders in the root directory.

I am not setting out to hoist this theme up and have it available to download necessarily, but I can always do that if I feel like it down the road. For now, I'm basically using the theme boilerplate to build out all the layout files up front and then going in and customizing them as I go along.

I had constructed a similar landing page for myself using Boostrap5, and I was pretty good with the overall aesthetic. So, I just started chopping it up into the Hugo theme. 

## Sectioned

The three sections (posts, projects and podcasts) are all pretty similar and required only small tweaks between them. For instance, I used some conditional logic to generate links to demos and code for the projects section, and included embedded audio players from my podcast host for the podcast pages. The basic structure, though, remained the same across each section: a folder to hold the individual files ```(/content/{{.SectionName}})``` and then corresponding html layouts ```(/theme/eamonn/layouts/)``` which dictate how to display each piece of content from each section.

Partials made this project particularly nice since I have a lot of experience inefficiently reusing code. By using Hugo, I was able to write pieces of code like the header, the head and the footer once and then insert them into every page that the static site builder would generate.

The biggest headache I've run into so far was a facepalm moment deploying the site onto Netlify. The initial deploys and custom domain was all good until yesterday when I pushed some changes to GitHub. Small details were broken, but not whole pages. A couple hours and a few commit rollbacks later, I was stumped. I hopped on the forums, posted a question (after trying everything I found from previous posts), and was happy to have a kind soul find a stupid mistake in my files.

I'd capitalized the posts, projects and podcasts folders initially when I was building the content folder's structure. I changed these to lowercase a few days ago and edited the layouts' html appropriately so that the local builds were fine. My folders on GitHub did not change, however. Not even sure why. I moved them temporarily, pushed a commit, moved them back, pushed another commit, and voila! All is well again.

As of this afternoon, I'm happy to report that the site is up and running well! I've got clean sections, and a site where I can easily showcase the many things I'm working on.

Several details remain, but they're just that: details. The podcast pages particularly could use a lot of work to get individual episodes over there, but really, the important pieces are in place including the embedded players.

## Thanks!

Hey, thanks for checking out this article. Let me know if you found it useful and/or entertaining. I enjoy writing about tech, and am always happy to meet new folks on [LinkedIn](https://linkedin.com/in/EamonnCottrell) or [Twitter](https://twitter.com/EamonnCottrell).