# 🌹 Rose Hugo

<div align="center">

A modern, responsive Hugo theme for content creators

[![Hugo](https://img.shields.io/badge/Hugo-0.80+-blue.svg)](https://gohugo.io)
[![License](https://img.shields.io/badge/License-GPL%20v2-blue.svg)](LICENSE.md)
[![GitHub stars](https://img.shields.io/github/stars/chensoul/rose-hugo.svg)](https://github.com/chensoul/rose-hugo/stargazers)

[Demo](https://rose-hugo-demo.netlify.app) • [Documentation](https://github.com/chensoul/rose-hugo/wiki) • [Issues](https://github.com/chensoul/rose-hugo/issues)

</div>

## ✨ Overview

Rose Hugo is a clean, responsive Hugo theme inspired by MH Magazine lite. Perfect for personal blogs, tech sites, and content-driven websites that prioritize readability and user experience.

### 🎯 Core Features

| Feature | Description |
|---------|-------------|
| 📱 **Responsive Design** | Optimized for all devices and screen sizes |
| 🌍 **Multilingual** | 15+ languages built-in, easily extensible |
| 🎨 **Customizable** | Flexible layouts, colors, and typography |
| ⚡ **Performance** | Fast loading with modern web standards |
| 🔍 **SEO Ready** | Built-in Open Graph, Schema, Twitter Cards |

### 🛠️ Advanced Features

<details>
<summary>Click to expand full feature list</summary>

#### Layout & Navigation
- Flexible main and secondary menus
- Configurable sidebar with widget support
- Multiple layout options (left/right/no sidebar)
- Responsive navigation with mobile menu

#### Content Features
- MathJax support for mathematical expressions
- Mermaid diagrams for flowcharts and visualizations
- Table of contents generation
- Related posts with i18n support
- Thumbnail support for posts and lists

#### Widgets & Integrations
- Search functionality
- Recent posts, categories, tags widgets
- Social media integration
- Language switcher
- Custom widget support

#### SEO & Analytics
- Open Graph meta tags
- Twitter Cards
- Schema.org structured data
- Google Analytics integration
- Disqus comments support

#### Customization
- Custom Google Fonts
- Configurable color schemes
- Post meta customization
- Author box and social sharing
- Back to top button

</details>

## 🚀 Quick Start

### Prerequisites

- [Hugo](https://gohugo.io/getting-started/installing/) v0.80.0 or higher
- Git

### Installation

1. **Create a new Hugo site** (skip if you already have one):
   ```bash
   hugo new site my-blog
   cd my-blog
   ```

2. **Install the theme**:

   **Option A: Git Clone** (for customization)
   ```bash
   git clone https://github.com/chensoul/rose-hugo.git themes/rose-hugo
   ```

   **Option B: Git Submodule** (recommended for updates)
   ```bash
   git submodule add https://github.com/chensoul/rose-hugo.git themes/rose-hugo
   ```

3. **Configure your site**:
   ```bash
   echo 'theme = "rose-hugo"' >> config.toml
   ```

4. **Start the development server**:
   ```bash
   hugo server -D
   ```

Your site will be available at `http://localhost:1313`

## ⚙️ Configuration

### Basic Configuration

Create or update your `config.toml` with these essential settings:

```toml
baseURL = "https://yoursite.com"
title = "Your Site Title"
theme = "rose-hugo"
defaultContentLanguage = "en"

[params]
  author = "Your Name"
  description = "Your site description"
  avatar = "/images/avatar.jpg"

  # Enable features
  opengraph = true
  schema = true
  twitter_cards = true

[params.sidebar]
  home = "right"
  widgets = ["search", "recent", "categories", "taglist"]
```

### Menu Configuration

```toml
[menu]
  [[menu.main]]
    name = "Home"
    url = "/"
    weight = 1
  [[menu.main]]
    name = "About"
    url = "/about/"
    weight = 2
  [[menu.main]]
    name = "Posts"
    url = "/posts/"
    weight = 3
```

<details>
<summary>📋 Complete Configuration Example</summary>

```toml
baseURL = "https://yoursite.com"
title = "Your Site Title"
defaultContentLanguage = "en"
theme = "rose-hugo"

summaryLength = 6
ignoreLogs = ['warning-goldmark-raw-html']

[pagination]
  pagerSize = 10

[permalinks]
  posts = "/posts/:year/:month/:day/:slug/"
  categories = "/categories/:slug/"
  tags = "/tags/:slug/"

[params]
  author = "Your Name"
  avatar = "/images/avatar.jpg"
  subtitle = "Your site subtitle"
  description = "Your site description"

  # SEO & Social
  opengraph = true
  schema = true
  twitter_cards = true

  # Content
  authorbox = true
  toc = true
  post_meta = ["date", "categories", "tags"]
  mainSections = ["posts"]
  dateformat = "2006-01-02"

  # Math & Diagrams
  mathjax = true
  mathjaxPath = "https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"

[params.style]
  highlightColor = "#e22d30"
  fontFamilyPrimary = '"Open Sans", sans-serif'
  fontFamilySecondary = '"Fira Code", monospace'

[params.sidebar]
  home = "right"
  list = "right"
  single = "right"
  widgets = ["search", "recent", "categories", "taglist", "social"]

[params.widgets.social]
  github = "yourusername"
  twitter = "yourusername"
  email = "your@email.com"
```

</details>

> 💡 **Tip**: Start with the basic configuration and gradually add features as needed. See the [full documentation](https://github.com/chensoul/rose-hugo/wiki) for all available options.

## 📝 Content Creation

### Front Matter

Add this to the top of your content files:

```yaml
---
title: "Your Post Title"
date: 2024-01-15
description: "Brief description of your post"
categories: ["Technology"]
tags: ["Hugo", "Web Development"]
thumbnail: "/images/post-thumbnail.jpg"
toc: true
---
```

### Available Front Matter Options

| Option | Type | Description |
|--------|------|-------------|
| `thumbnail` | string | Post thumbnail image path |
| `lead` | string | Highlighted text below title |
| `toc` | boolean | Enable table of contents |
| `mathjax` | boolean | Enable math expressions |
| `authorbox` | boolean | Show author information |
| `comments` | boolean | Enable comments |
| `sidebar` | string | Sidebar position (`left`, `right`, `none`) |

## 🎨 Customization

### Color Scheme

Customize your theme colors in `config.toml`:

```toml
[params.style]
  highlightColor = "#your-color"  # Primary accent color
```

### Typography

```toml
[params.style]
  fontFamilyPrimary = '"Your Font", sans-serif'
  fontFamilySecondary = '"Your Mono Font", monospace'
```

### Widgets

Enable and configure sidebar widgets:

```toml
[params.sidebar]
  widgets = ["search", "recent", "categories", "taglist", "social", "languages"]
```

## 🤝 Contributing

We welcome contributions! Here's how you can help:

1. **Report Issues**: Found a bug? [Open an issue](https://github.com/chensoul/rose-hugo/issues)
2. **Feature Requests**: Have an idea? [Start a discussion](https://github.com/chensoul/rose-hugo/discussions)
3. **Pull Requests**: Ready to contribute code? [Submit a PR](https://github.com/chensoul/rose-hugo/pulls)

### Development Setup

```bash
git clone https://github.com/chensoul/rose-hugo.git
cd rose-hugo
hugo server --source=exampleSite --themesDir=../..
```

## 📄 License

This theme is released under the [GPL v2 License](LICENSE.md).

---

<div align="center">

**[⭐ Star this repo](https://github.com/chensoul/rose-hugo)** • **[🐛 Report Bug](https://github.com/chensoul/rose-hugo/issues)** • **[💡 Request Feature](https://github.com/chensoul/rose-hugo/discussions)**

Made with ❤️ by [chensoul](https://github.com/chensoul)

</div>
