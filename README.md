## Jasper2

[![Build Status](https://github.com/AntonyLeons/jasper2/actions/workflows/jekyll_build.yml/badge.svg)](https://github.com/AntonyLeons/jasper2/actions/workflows/jekyll_build.yml)
[![Netlify Status](https://api.netlify.com/api/v1/badges/606a2019-c4ba-4b5e-9989-199765b6590f/deploy-status)](https://app.netlify.com/projects/jasper2-reloaded/deploys)
[![Ruby](https://img.shields.io/badge/ruby-4.0.5-blue.svg?style=flat)](https://github.com/AntonyLeons/jasper2)
[![Jekyll](https://img.shields.io/badge/jekyll-4.4.1-blue.svg?style=flat)](https://github.com/AntonyLeons/jasper2)

This is a modern, full-featured port of Ghost's default theme [Casper](https://github.com/tryghost/casper) for [Jekyll](https://jekyllrb.com/) / [GitHub Pages](https://pages.github.com/).

## Live Demo

[Ghost's Casper](https://demo.ghost.io) // [Jasper2](https://antonyleons.github.io/jasper2)

![home page](https://raw.githubusercontent.com/AntonyLeons/jasper2/master/assets/screenshot-desktop.jpg)


## Key Features & Upgrades

* **Pure Ruby/Jekyll Stack**: Upgraded to Jekyll 4.4 and `jekyll-sass-converter`. **No Node.js, NPM, or Gulp required!** SCSS styles compile natively during Jekyll builds.
* **Dark Mode**: Beautiful, responsive dark mode support with a theme toggle switch (persisted in `localStorage`).
* **Netlify CMS Integration**: Out-of-the-box support for Netlify CMS admin dashboard (`/admin/`) using `git-gateway`.
* **Conditional Search**: Powerful search engine integration powered by [Algolia](https://www.algolia.com/). The search interface and icon hide automatically if no credentials are set in `_config.yml`, preventing JavaScript errors.
* **Multiple Authors**: Support for multiple authors out of the box (configured in `_data/authors.yml`) with full profile information (avatar, bio, links).
* **Tag Pages**: Custom covers and descriptions for tag pages (configured in `_data/tags.yml`).
* **Post Navigation**: Next/Previous post suggestions and related posts at the bottom of each post.
* **Disqus Comments**: Corrected, post-specific Disqus comment thread integration.
* **Google Analytics & Feeds**: Integrated Google Analytics (UA/GA4) and Atom feed generation.


## Getting Started

### Prerequisites

- [Ruby](https://www.ruby-lang.org/en/documentation/installation/) (Check with `ruby -v`)
- [Bundler](https://bundler.io/) (Install with `gem install bundler`)

### Installation & Local Run

1. **Clone the repository**:
   ```bash
   git clone https://github.com/AntonyLeons/jasper2.git
   cd jasper2
   ```

2. **Install Ruby gems**:
   ```bash
   bundle install
   ```

3. **Serve locally with live-reload**:
   ```bash
   bundle exec jekyll serve --livereload
   ```

Open `http://localhost:4000/jasper2/` (or your configured `baseurl`) in your browser. Any changes to markdown posts, HTML layouts, or SCSS files will compile and refresh automatically.


## Deployment

There are several ways to deploy your site:

1. **GitHub Pages (via GitHub Actions)**:
   Builds the site automatically on push using GitHub Actions and deploys the contents of `_site/` to your `gh-pages` branch. See `.github/workflows/jekyll_build.yml` for configuration.

2. **Netlify**:
   Highly recommended for static hosting. Netlify links directly to your repository and rebuilds on every push. A preconfigured `netlify.toml` is provided:
   - Build command: `bundle exec jekyll build`
   - Publish directory: `_site`

3. **Traditional Hosting**:
   Simply build the site locally with `bundle exec jekyll build` and upload the contents of the generated `_site/` folder to your server.


## Customization

### Author Pages

Rename the `author` field in the front matter of your posts to match the author's username defined in `_data/authors.yml`. Profiles support:
- `name` and `bio`
- `location` and `url_full`
- `picture` and `cover` images
- `x_username` / `twitter`, `facebook`, and `github` accounts

### Styling

Styles are written in SCSS and compile automatically. 
- Global variables, colors (including light/dark mode properties), and typography are located in `_sass/_global.scss`.
- Layout components are structured in `assets/css/screen.scss` and custom post/syntax highlighting styling in `assets/css/syntax.scss`.


## Issues and Contributing

If you run into any problems or have feature suggestions, please log them on the [issue tracker](https://github.com/AntonyLeons/jasper2/issues). Feel free to submit pull requests with bug fixes and features!


## Copyright & License

Same license as the one provided by Ghost's team. See Casper's theme [license](GHOST.txt).

Copyright (C) 2015-2026 - Released under the MIT License.
