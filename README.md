# Mood

A lightweight, JavaScript-free [Hugo](https://gohugo.io/) theme for moodboarding.

![Mood](preview.png)

## Live demo

- https://mood.harrycresswell.com/

## Features

- Clean and simple design
- Page specific meta titles
- Responsive layout
- Minimal CSS
- [Cloudinary](https://cloudinary.com/) image hosting
- Page specific keywords
- Low quality Image placeholders (LQIP)
- Next-gen image formats (WebP & AVIF)
- Immutable image caching
- Image proxying with Netlify Redirects
- 100/100 score on Lighthouse
- SEO optimized (Twitter cards, Facebook Open Graph)
- Superlite (Only ~3kb of CSS)

## Installation

[Install Hugo](https://gohugo.io/getting-started/installing/), then create a new site.

```
hugo new your-site-name
```

Install this repository in the themes/ directory of your Hugo project:

```
cd themes/
git clone https://github.com/harrycresswell/mood.git
```

## Configuration

First, move the `config.toml` and `netlify.toml` files from `themes/mood/exampleSite` to the root of your new project.

Then, at the top of your _config.toml_ file, set `mood` as your default theme:

```
theme = "mood"
```

Next, head to [Cloudinary.com](https://cloudinary.com/) and set up a free account.

When you have a Cloudinary account set up, open `netlify.toml` and update the `to` value under redirects to your Cloudinary cloud name. 

```
[[redirects]]
from = "/images/:format/:quality/:width/*"
# Replace “your-cloud-name” in URL below to your actual cloud name
to = "https://res.cloudinary.com/your-cloud-name/image/upload/:format/:quality/:width/:splat"
status = 200
```

You can find your cloud name on your Cloudinary dashboard.

Inside `config.toml`, under the `[params]` section update `cloudinary_url` to include your cloud name.

Finally, move the _assets_ folder including it’s contents from the _themes/mood_ folder to the root of your project.


## Adding content

Use the `hugo` command to create new posts.

```
hugo new post/your-post-title.md
```

You will find comments in the front matter that explain how to format data correctly.

Add pages in the same manner.

```
hugo new some-page-name.md
```

If you want to kick things off with some demo content, then replace your /content folder with `themes/mood/exampleSite/content`.

## Managing menu items

Configure your menu items in the _config.toml_ file.

```toml
[menu]
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

## Building site

Run `hugo server` to start Hugo’s built-in web server.

```
hugo server
```

Then head to http://localhost:1313/ to view your site in the browser.

## Author

Harry Cresswell

- https://github.com/harrycresswell
- https://twitter.com/harrycresswell

## Problems?

Email me [studio@harrycresswell.com](mailto:studio@harrycresswell.com).

## Licence

Copyright 2022 [Harry Cresswell](https://harrycresswell.com/)

This theme has been released under the MIT License. Check the original license for additional licensing information.
