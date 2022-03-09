# Mood

A JavaScript free moodboard [Hugo](https://gohugo.io/) theme for minimalists.

![Screenshot](screenshot.png)

## Live demo

- https://mood.harrycresswell.com/

## Features

- Clean and simple design
- Dynamic page meta titles
- Responsive layout
- Minimal CSS
- [Cloudinary](https://cloudinary.com/) image hosting
- Low quality Image placeholders (LQIP)
- Next-gen image formats (WebP & AVIF)
- Immutable image caching
- Image proxying with Netlify Redirects
- 100/100 score on Lighthouse
- SEO optimized (Twitter cards, Facebook Open Graph, Schema.org)
- Superlite (Only ~3kb of CSS)

## Installation

First, [install Hugo](https://gohugo.io/getting-started/installing/), then create a new site.

```
hugo new your-site-name
```

To install Mood as your default theme, install this repository in the themes/ directory at the root of your Hugo project:

```
cd themes/
git clone https://github.com/harrycresswell/mood.git
```

Then at the top of your _config.toml_ file, set `mood` as your default theme:

```
theme = "mood"
```

## Configuration

First, set up an account at [Cloudinary.com](https://cloudinary.com/).

Open `netlify.toml` and update the `to` value under redirects from my cloud name to your own. 

```
[[redirects]]
from = "/images/:format/:quality/:width/*"
# Change from this:
to = "https://res.cloudinary.com/harrycresswell/image/upload/:format/:quality/:width/:splat"
# to this
to = "https://res.cloudinary.com/your-cloud-name/image/upload/:format/:quality/:width/:splat"
status = 200
```

You can find your cloud name on your Cloudinary dashboard.

## Add content

Use hugo command to create new posts.

```
hugo new post/your-post-title.md
```

You will find comments in the front matter that explain how to format data correctly.

Add pages as usual.

```
hugo new some-page-name.md
```

## Updating menu items

Add menu items to _config.toml_:

```
[[menu.main]]
  name = "About"
  url = "/about"
  weight = 5
[[menu.main]]
  name = "Contact"
  url = "/contact"
  weight = 10
[[menu.main]]
  name = "Some other page"
  url = "/some-other-page"
  weight = 10 
```

## Build site

```
hugo server
```

Then head to http://localhost:1313/ in your browser.

## Author

Harry Cresswell

- https://github.com/harrycresswell
- https://twitter.com/harrycresswell


## Problems?

Email me [studio@harrycresswell.com](mailto:studio@harrycresswell.com).

## Licence

Copyright 2022 [Harry Cresswell](https://harrycresswell.com/)

This theme has been released under the MIT License. Check the original license for additional licensing information.