# Hugo Discaptive

A simple light theme that supports full responsive.

Inspired by [tailwind-nextjs-starter-blog](https://github.com/timlrx/tailwind-nextjs-starter-blog)

## Overview

~~In real usage: [discaptive.com](https://discaptive.com)~~

![screenshot](https://raw.githubusercontent.com/discaptive/hugo-discaptive/main/images/screenshot.png)

## Installation

Install Hugo and create a new site. See the Hugo documentation for details.

### Git Submodule

Before adding `hugo-discaptive` theme, initialize a Git repository.

    $ git init

Add `hugo-discaptive` as git submodule:

    $ git submodule add https://github.com/discaptive/hugo-discaptive.git themes/hugo-discaptive

### Hugo module

Initialize your site as hugo module:

    $ hugo mod init github.com/USERNAME/SITENAME

Add `hugo-discaptive` module as a dependency of your site:

    $ hugo mod get github.com/discaptive/hugo-discaptive

To update module

    $ hugo mod get -u

### Site preview

Copy the content of `exampleSite` at the root of your project:

    cp -r themes/hugo-discaptive/exampleSite/* .

If you installed `hugo-discaptive` as hugo module, set your theme in your config file (hugo.toml):

    [[module.imports]]
      path = "github.com/discaptive/hugo-discaptive"

Start Hugo:

    hugo serve

### Site preview (another option)

    $ cd themes/hugo-discaptive/exampleSite
    $ hugo server --theme ../..

## Content structure

```
content/
  ├── first-slug/
  │       ├── index.md
  │       ├── image1.jpg
  │       └── image1.png
  └── second-slug/
          ├── index.md
          ├── image1.jpg
          └── image1.png
```

## Example of the `hugo.toml`

```toml
baseURL = 'https://example.org'  # Your domain name.
languageCode = 'en-US'
title = '<TITLE>'  # Title of your website

[[module.imports]]
  path = "github.com/discaptive/hugo-discaptive"

[params]
  github = 'https://github.com/<YOUR_GITHUB_USERNAME>'
  username = '<USERNAME>'

  # To enable giscus, the GitHub-discussions-based comment section,
  # input the repository for the discussions below. For more details, see
  # https://giscus.app
  [params.giscus]
    repo = '[ENTER REPO HERE]'
    repoId = '[ENTER REPO ID HERE]'
    category = '[ENTER CATEGORY NAME HERE]'
    categoryId = '[ENTER CATEGORY ID HERE]'
    mapping = 'pathname'
    reactionsEnabled = '1'
    inputPosition = 'bottom'
    theme = 'light'
    lang = 'en'

[pagination]
  pagerSize = 5  # Specify the max number of rows to be returned in list

# Menu items displayed in the header.
[[menus.main]]
  name = 'Contact'
  url = 'mailto:youremail@email.com'
  weight = 1
[[menus.main]]
  name = 'Tags'
  url = '/tags'
  weight = 2
[[menus.main]]
  name = 'About'
  url = '/about'
  weight = 3
```

## License

MIT Licensed, see [LICENSE](https://github.com/discaptive/hugo-discaptive/blob/main/LICENSE).
