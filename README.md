# rebugo

reb + hugo = rebugo

## Installation

Clone to `themes/` directory:

```
git clone https://github.com/robherley/rebugo.git themes/rebugo
```

Set the theme in your hugo `config` file:

```diff
+theme = "rebugo"
```

## Features

- GitHub readme integration (see configuration below)
- Automatic JSON feed homepage: `https://<your-site>/index.json`
- Custom shortcodes
  - `mermaid`: renders [mermaid diagrams](https://mermaid.js.org/)
  - `terminal`: renders terminal style prompt
- Easily integrate custom CSS, JS and extend `<head>`.

## Configuration

```toml
[params]
  # set a custom favicon
  favicon = "images/logo.png"
  # inject a GitHub readme into the home page
  readmeRepo = "robherley/robherley"
  # set a custom emoji logo
  emoji = "💾"
  # set a custom primary css color
  primaryColor = "#0071F3"

# add social links to footer
# 'name' refers to a simple icon: https://simpleicons.org/
[[params.social]]
  name = "github"
  link = "https://github.com/robherley"

[[params.social]]
  name = "x"
  link = "https://x.com/robherley"

# customize rendered code blocks
# https://gohugo.io/getting-started/configuration-markup/
[markup]
  [markup.highlight]
    style = 'catppuccin-frappe'
    tabWidth = 4
```

For custom CSS or JS, just include them in your `assets/(css|js)` directory within your project's root (files added in alphabetical order):

```
assets/
  js/
    my-script.js
  css/
    my-styles.css
```

Otherwise, to add additional content to `<head>`, simple create a file at `layouts/partials/head_includes.html` with any content (analytics, external stylesheets/scripts, etc).

## Inspiration

- https://github.com/monkeyWzr/hugo-theme-cactus
- https://github.com/athul/archie
