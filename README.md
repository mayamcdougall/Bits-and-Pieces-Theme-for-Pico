# Bits and Pieces theme for Pico

Bits and Pieces is a minimalistic note-taking theme for PicoCMS.

![Preview of theme](preview.png)

## Background

I had long searched for a way to store useful "bits and pieces" of information for personal reference; snippets of Javascript, odd CSS selectors, how to exit vim, etc. General purpose bins like Evernote, where you're supposed to just throw everything into it, had never really worked for me. It always ended up looking like my desk – messy and disorganized. 

For the last couple of years I have stored my reference files as markdown files, using different front-ends to render them. Using [Pico CMS](http://picocms.org) as my front-end, I created this minimalistic theme to give them an elegant presentation.

The theme is really simple and barebones, and can easily be customized and extended to suit your needs.

## Getting Started

### Installation

Download the repository and put the `bitsandpieces` folder in Pico's `themes` folder. Then, update Pico's `config.yml` theme setting:

```yml
theme: bitsandpieces
```

## Theme Specific Guidelines

### Navigation

The theme has currently no subfolder navigation. Regardless of the folder structure in your `content` directory all pages will be rendered as a flat list.

### Keyboard Shortcuts

You can assign keyboard shortcuts to quickly switch between pages. Just add `Shortcut: <key>` to the YAML metadata of your page to assign it a shortcut key. Use `+` to make key combos. [Look at mousetrap documentation to see what you can do](https://craig.is/killing/mice)

```yaml
---
Title: Bits and Pieces theme for Pico
Shortcut: alt+1
---
```

The above example will open the "Bits and Pieces" page when the keys `alt` and `1` keys are pressed simultaneously.

### Titles & Headings

**Be sure to include a level 1 header** in your content (`# This is an H1`)!

In this theme, the title you specify in your YAML is used only for the navigation and is not displayed above the content.

"Bits and Pieces" also only provides styles for the first three levels of heading (h1, h2, h3). The remaining headers will simply be styled as bold text. If you need more than three levels of hierarchy you'd probably be better splitting the content into separate files anyway.

### Code Snippets

Code highlight are rendered using [highlight.js](https://highlightjs.org). Put the language right after the three backticks to get proper language highlighting. To see what language prefix to use see [highlight.js documentation](http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html#language-names-and-aliases).

```markdown
​```html
<h1>Hello world!</h1>
​```
```

### Loading External CSS Files

Uncomment the following setting in `pico-theme.yml` to load external css files.

```yml
external_css:
  - "%assets_url%/styles.css" # Path to CSS File.
```

### Browser Compatibility

This theme uses a few modern CSS features.  While these should work fine on any modern browser (Safari, Chrome, Edge), they haven't been tested in legacy browsers like IE (and very likely won't work there).

![scroll-preview](scroll-preview.gif)

_Sticky headers on safari_
