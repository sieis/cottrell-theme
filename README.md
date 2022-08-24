# :boom: My Hugo Portfolio Theme :boom:

[![Netlify Status](https://api.netlify.com/api/v1/badges/a9d21c5e-caac-41e3-93c9-1e98a200465c/deploy-status)](https://app.netlify.com/sites/eamonn/deploys)

![Eamonn](https://github.com/sieis/cottrell-theme/blob/main/static/images/portfolio%20screenshot.png)

I'm using Bootstrap5, FontAwesome and Hugo for my personal site which is live [here](https://eamonncottrell.com).

I've created the theme itself primarily to build a boilerplate for a fresh Hugo site. By running

``` go
hugo new theme theme-name
```

it will construct a theme folder with basic layouts in place. It saves me a hair of time and a little brainpower to do it this way rather than creating those from scratch.

> Some notes in no particular order below

## Layouts

I've modified the layouts as necessary for my site. I added a ```posts.html & podcasts.html``` to the ```/_default/``` layouts in order for those ```list``` pages to render differently. I'll likely add another for ```projects.html``` after further tweaks.

## Index.html

I've got a very straightforward and minimal home page. In a previous iteration I'd built this with just HTML and CSS. This proved unnecessarily lengthy. Thanks to Hugo and some amatuer Go conditionals, I shrunk the index HTML to under 80 lines of code to display the first 3 posts, podcasts and projects and create Bootstrap cards for each.


## Partials

There may be more eventually, but in the interest of keeping things as simple as possible from the outset, I've only used the stock ```footer.html, header.html, and head.html``` partials.

## Config.toml

I'm only using the main config for a few things so far.

1. The theme declaration
1. The menu items for the navbar
1. Some custom params like meta description, subtitle, Google Analytics tag ID, and some images

## Bootstrap 5

I particularly wanted to use the latest iteration of Bootstrap, which at the time of this writing is 5. They chucked JQuery with this release, and with the exception of a small amount for some use cases, no Javascript is required anymore. Even with these improvements, Bootstrap is waaay overkill for what I am doing. However, it's also a quick to market way to get clean CSS. Bulma is another that I enjoy using for this same reason.

## Header

Very basic navbar from Bootstrap components here. And pulling the menu from the config.toml:

``` css
<div class="navbar-nav">
    {{range .Site.Menus.main}}
      <a class="nav-link fs-5" href="{{.URL}}">{{.Name}}</a>
    {{end}}
</div>
```

## Head

I tried to pull a lot of info here from the ```config.toml```. I'm using a cdn for animate.css just because I wanted a quick animation on the title.

``` css
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"/>
```

### Meta Descriptions

I wanted different descriptions for different pages, and the ability to tailor fit those to each individual post if need be. So I did this to allow for tailor-made individual page descriptions, and a fallback site-wide description if one didn't exist at the page level:

``` css
  <meta name="description"
    content="{{ if .Params.description}}{{.Params.description}}{{else if .Params.subtitle}}{{.Params.subtitle}} by Eamonn Cottrell{{else}}{{.Site.Params.Description}}{{end}}" />
```

### Twitter && OG

Hugo has some built in templates that pull from the front-matter of posts, projects or podcasts. Or, it'll pull from the site [params] if there's nothing in the front matter.

```html
  <!-- Twitter Card -->
  {{ template "_internal/opengraph.html" . }}
  <!-- OG tags -->
  {{ template "_internal/twitter_cards.html" . }}
```

### Favicons

I use [realfavicongenerator](https://realfavicongenerator.net/). It's pretty straightforward, and provides easy to follow instructions. Making sure to link these correctly in the head is important.

### Canonical Tag

I opted to create a canonical tag for every page by doing this in the head. This gives me the option to specify a canonical link in the front matter if necessary, and for it to simply be the {{`.Permalink`}} if not.
``` css
<!-- Canonical Tag -->
  <link rel="canonical" href="{{ if .Params.canonical }}{{.Params.canonical}}{{else}}{{.Permalink}}{{end}}">
```

### Google Analytics

I snagged this little piece of code to use the ID from the config.toml:

``` go
{{ $gtag := print "https://www.googletagmanager.com/gtag/js?id=" .Site.Params.gtag }}
```

### Title

I simply did this:

``` go
{{ $title := print .Site.Title " | " .Title }}
{{ if .IsHome }}{{ $title = .Site.Title }}{{ end }}
<title>{{ $title }}</title>
  ```

## Podcasts

I wanted my podcasts to have some different features since I needed to have the podcast players for the trailers and the episodes embedded. This is as simple as creating a ```/layouts/podcasts/single.html``` file which will override the ```/_default/single.html``` according to Hugo's lookup order.

This let me add

``` html
<iframe width="100%" height="390" frameborder="no" scrolling="no" seamless src="{{.Params.player}}"></iframe>
```
and then put the src for the player in the episode's Front Matter.

## About

I've got a simple about page live now. I copied the html layout from my ```/_default/single.html``` for now and removed:

``` css
<a href="/{{.Section}}" class="">back to {{.Section}}</a>
```

I also added 
``` yaml
layout: "about"
```
in the front matter to point it to the correct layout.

## Future Updates

There are still things needed as I improve the site's functionality and my own knowledge of Hugo. Noteable next additions:

1. Form submissions
1. Tags for posts
