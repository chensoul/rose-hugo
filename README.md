# Hugo Rose

**hugo-rose** is a responsive, simple, clean and content-focused [Hugo](https://gohugo.io/) theme based on the
[MH Magazine lite](https://wordpress.org/themes/mh-magazine-lite/) theme.

**[Demo](https://blog.chensoul.cc/)**

![screenshot](https://raw.githubusercontent.com/chensoul/hugo-rose/master/images/screenshot.png)

**Features:**

+ Responsive design
+ Main & secondary menus
+ Widgetized sidebar
+ Translations. Over 15 languages and counting
+ Configurable theme settings (sidebar position, author box, post navigation, highlight color) via `config.toml`
+ Hugo internal templates (Open Graph, Schema, Twitter Cards, Disqus, Google Analytics)
+ Wide cross-browser compatibility
  + *Desktop: IE11+, Chrome, Firefox, Safari*
  + *Mobile: Android browser (on Android 4.4+), Safari (on iOS 7+), Google Chrome, Opera mini*
+ Custom Google Fonts support, MathJax, Table of Contents, SVG icons and much more…

## Installation

*Before starting, please be sure that you have
[installed Hugo](https://gohugo.io/getting-started/quick-start/#step-1-install-hugo) and
[created a new site](https://gohugo.io/getting-started/quick-start/#step-2-create-a-new-site). After that, you are ready
to install **hugo-rose**.*

From your project's root directory, run:

```
git clone https://github.com/chensoul/hugo-rose.git themes/hugo-rose
```

Or, if you don't plan to make any significant changes but want to track and update the theme, you can add it as a git
submodule via the following command:

```
git submodule add https://github.com/chensoul/hugo-rose.git themes/hugo-rose
```

Next, open `config.toml` in the base of the Hugo site and ensure the theme option is set to `hugo-rose`:

```
theme = "hugo-rose"
```

## Configuration

### Config.toml example

```toml
baseurl = "/"
title = "hugo-rose"
languageCode = "en-us"
theme = "hugo-rose"

summaryLength = 6
ignoreLogs = ['warning-goldmark-raw-html']

[services.disqus]
  shortname = "" # Enable Disqus by entering your Disqus shortname

[pagination]
  pagerSize = 10

[permalinks]
  posts="/posts/:year/:month/:day/:slug/"
  categories="/categories/:slug/"
  tags="/tags/:slug/"
  pages="/:slug/"

[Params]
  author = "hugo-rose"
  avatar = "/image/favicon.webp"
  subtitle = "Just another blog" # Logo subtitle
  description = "Hugo Rose's Personal blog about everything" # Description of your site
  opengraph = true # Enable OpenGraph if true
  schema = true # Enable Schema
  twitter_cards = true # Enable Twitter Cards if true
  readmore = true # Show "Read more" button in list if true
  authorbox = true # Show authorbox at bottom of pages if true
  toc = false # Enable Table of Contents
  pagination = true # Show pagination navigation (prev/next links) at the bottom of pages if true
  post_meta = [ "date", "categories"] # Order of post meta information
  mainSections = ["posts"] # Specify section pages to show on home page and the "Recent articles" widget
  dateformat = "2006-01-02" # Change the format of dates
  mathjax = true # Enable MathJax
  mathjaxPath = "https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.6/MathJax.js" # Specify MathJax path
  mathjaxConfig = "TeX-AMS-MML_HTMLorMML" # Specify MathJax config
  # customHeader = ""
  # customFooter = ""
  # customSidebar = ""

[Params.style.vars]
  highlightColor = "#e22d30" # Override highlight color

  # Override font-family sets
  # googleFontsLink = "https://fonts.loli.net/css?family=Open+Sans:400,400i,700" # Load Google Fonts
  # Take care of different quotes OR escaping symbols in these params if necessary
  fontFamilyPrimary = '"Open Sans", "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei", "WenQuanYi Micro Hei", Helvetica, Arial, sans-serif'
  # Secondary font-family set responsible for pre, code, kbd, and samp tags font
  fontFamilySecondary = "SFMono-Regular, Menlo, Monaco, Consolas, 'Liberation Mono', 'Courier New', monospace"

[Params.sidebar]
  home = "right"   # Configure layout for home page
  list = "right"   # Configure layout for list pages
  single = "right" # Configure layout for single pages
  # Enable widgets in given order：["search", "recent", "categories", "taglist", "social", "languages"]
  widgets = [ "search", "recent", "categories", "taglist"]

[Params.widgets]
  recent_num = 10 # Set the number of articles in the "Recent articles" widget
  categories_counter = true # Enable counter for each category in "Categories" widget
  tags_counter = true # Enable counter for each tag in "Tags" widget (disabled by default)

[Params.thumbnail]
  # Control thumbnail visibility, eg: list、post
  visibility = ["list"]

# Custom social links
[[Params.widgets.social.custom]]
  title = "Youtube"
  url = "https://youtube.com/user/username"
  icon = "youtube.svg" # Optional. Path relative to "layouts/partials"
  rel = "noopener noreferrer" # Set to false to remove the rel attribute

[[Params.widgets.social.custom]]
  title = "My Home Page"
  url = "https://example.com"

[Params.widgets.search]
  cached = false # activate cache if true
  url = "https://google.com/search"
  [Params.widgets.search.input]
    name = "sitesearch"
    pre = ""
```

**Do not copy example config as-is**. Use only those parameters that you need.

For more information about all available standard configuration settings, please read
[All Hugo Configuration Settings](https://gohugo.io/getting-started/configuration/#all-configuration-settings).

### Front Matter example

```yaml
---
# Common-Defined params
title: "Example article title"
date: "2017-08-21"
description: "Example article description"
categories:
  - "Category 1"
  - "Category 2"
tags:
  - "Test"
  - "Another test"

# Theme-Defined params
thumbnail: "image/placeholder.png" # Thumbnail image
lead: "Example lead - highlighted near the title" # Lead text
comments: false # Enable Disqus comments for specific page
authorbox: true # Enable authorbox for specific page
pagination: true # Enable pagination navigation (prev/next) for specific page
toc: true # Enable Table of Contents for specific page
mathjax: true # Enable MathJax for specific page
sidebar: "right" # Enable sidebar (on the right side) per page
widgets: # Enable sidebar widgets in given order per page
  - "search"
  - "recent"
  - "taglist"
---
```

For more information about all available standard front matter variables, please read
[Hugo Front Matter](https://gohugo.io/content-management/front-matter).

## Contributing

Have you found a bug or got an idea for a new feature? Feel free to use the
[issue tracker](https://github.com/chensoul/hugo-rose/issues) to let me know. Or make directly a
[pull request](https://github.com/chensoul/hugo-rose/pulls), but please respect the following

## License

This theme is released under the [GPLv2 license](https://github.com/chensoul/hugo-rose/blob/master/LICENSE.md).
