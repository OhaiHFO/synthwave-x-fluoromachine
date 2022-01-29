# Synthwave x Fluoromachine 🝰 Avant Noir

This is a fork of @webrenders's [Synthwave x Fluoromachine theme](https://github.com/webrender/synthwave-vscode-x-fluoromachine), which in turn is a fork of @robbowen's [Synthwave '84 theme](https://marketplace.visualstudio.com/items?itemName=RobbOwen.synthwave-vscode), merged with @fullerenedream's [Fluoromachine](https://colorsublime.github.io/themes/FluoroMachine/) theme for VSCode. 
<p>&nbsp;</p>

**This Avant Noir variation darkens the UI, and boosts the general color tone - making the important things pop more.**
<p>&nbsp;</p>

![Theme screenshot](https://raw.githubusercontent.com/OhaiHFO/synthwave-x-fluoromachine-avant-noir/master/images/ext_multi_file.png)
<p>&nbsp;</p>

## Table of Contents
---

- [Synthwave x Fluoromachine 🝰 Avant Noir](#synthwave-x-fluoromachine--avant-noir)
  - [## Table of Contents](#-table-of-contents)
  - [## Editions](#-editions)
  - [Comparison of Additions (Screenshots)](#comparison-of-additions-screenshots)
  - [## Installation](#-installation)
    - [Option 1: Base Edition](#option-1-base-edition)
    - [Option 2: Extended Edition](#option-2-extended-edition)
  - [## Editor Font](#-editor-font)
    - [Enabling Ligatures](#enabling-ligatures)
    - [Enabling Italics](#enabling-italics)
  - [## Terminal](#-terminal)
<p>&nbsp;</p>

## Editions
---
<p>&nbsp;</p>

**This theme is available in 2 editions:**

- Base Edition
- Extended Edition
<p>&nbsp;</p>

> ## Base Edition
> ---
> The base edition is the easiest to install, but lacks some of the features of the extended edition.
> 
> This theme has been designed with progressive enhancement in mind, and as such the base theme should be perfectly functional without the additions of the extended version.
<p>&nbsp;</p>

> ## Extended Edition ☀️😎
> ---
> The extended edition utilises a custom stylesheet in order to expand on the capabilities of the vscode themeing engine.
> 
> There's a couple of steps involved in getting it installed, but nothing too crazy, it shouldn't take much more than a few minutes.
<p>&nbsp;</p>

## Comparison of Additions (Screenshots)

| 🚥&nbsp;&nbsp; Base Edition | 🌈&nbsp;&nbsp; Extended Edition |
| ----------- | ----------- |
| ![Theme screenshot](https://raw.githubusercontent.com/OhaiHFO/synthwave-x-fluoromachine-avant-noir/master/images/base_new_session.png) | ![Theme screenshot](https://raw.githubusercontent.com/OhaiHFO/synthwave-x-fluoromachine-avant-noir/master/images/ext_new_session.png) |
| ![Theme screenshot](https://raw.githubusercontent.com/OhaiHFO/synthwave-x-fluoromachine-avant-noir/master/images/base_multi_file.png) | ![Theme screenshot](https://raw.githubusercontent.com/OhaiHFO/synthwave-x-fluoromachine-avant-noir/master/images/ext_multi_file.png) |
| ![Theme screenshot](https://raw.githubusercontent.com/OhaiHFO/synthwave-x-fluoromachine-avant-noir/master/images/base_panels_ligatures_cusrsive.png) | ![Theme screenshot](https://raw.githubusercontent.com/OhaiHFO/synthwave-x-fluoromachine-avant-noir/master/images/ext_panels_ligatures_cusrsive.png) |

<p>&nbsp;</p>

## Installation 
---
<p>&nbsp;</p>

### Option 1: Base Edition
<p>&nbsp;</p>

1. Install this theme from within vscode or on the vscode themes website
<p>&nbsp;</p>

### Option 2: Extended Edition
<p>&nbsp;</p>

1. Install this theme  

2. Install the [Custom CSS and JS Loader](https://marketplace.visualstudio.com/items?itemName=be5invis.vscode-custom-css) extension for vscode

3. Link the CSS file from this extension in your vscode `settings.json`:
<p>&nbsp;</p>

>  **On Macs, the path to your vscode extensions might look something like the snippet below:**

```json
  "vscode_custom_css.imports": [
    "file:///Users/{your username}/.vscode/extensions/ohaihfo.synthwave-x-fluoromachine-avant-noir-0.1.0/synthwave-x-fluoromachine-avant-noir.css"
  ]
```
<p>&nbsp;</p>

> **On Windows, the path may resemble:**

```json
  "vscode_custom_css.imports": [
    "file:///C:/Users/{your username}/.vscode/extensions/ohaihfo.synthwave-x-fluoromachine-avant-noir-0.1.0/synthwave-x-fluoromachine-avant-noir.css"
  ]
```
<p>&nbsp;</p>

4. Finally, open the vscode command panel ( **Mac:**&nbsp;&nbsp; <kbd>cmd</kbd> + <kbd>shift</kbd> + <kbd>p</kbd>&nbsp;&nbsp; / &nbsp;&nbsp; **Windows:**&nbsp;&nbsp; <kbd>ctrl</kbd> + <kbd>shift</kbd> + <kbd>p</kbd> ), and select `Reload Custom CSS and JS`.

<p>&nbsp;</p>

_**Note:**_ You'll need to run the `Reload Custom CSS and JS` command again, every time vscode updates.
<p>&nbsp;</p>

## Editor Font
---
The font being used in the screenshot above is [Victor Mono](https://rubjo.github.io/victor-mono/) which includes **Ligatures** and *_optional semi-connected cursive italics_.*
<p>&nbsp;</p>

### Enabling Ligatures

To enable ligatures within your editor pane, add the following snippet to your vscode `settings.json`:

```json
  "editor.fontLigatures": true,
```
<p>&nbsp;</p>

### Enabling Italics

To enable italics within your editor pane, add the following snippet to your vscode `settings.json`:

```json
  "editor.tokenColorCustomizations": {
    "textMateRules": [
        {
            "scope": [
                //following will be in italic (=FlottFlott)
                "comment",
                "entity.name.type.class", //class names
                "keyword", //import, export, return…
                "constant", //String, Number, Boolean…, this, super
                "storage.modifier", //static keyword
                "storage.type.class.js", //class keyword
            ],
            "settings": {
                "fontStyle": "italic"
            }
        },
        {
            "scope": [
                //following will be excluded from italics (VSCode has some defaults for italics)
                "invalid",
                "keyword.operator",
                "constant.numeric.css",
                "keyword.other.unit.px.css",
                "constant.numeric.decimal.js",
                "constant.numeric.json"
            ],
            "settings": {
                "fontStyle": ""
            }
        }
    ]
  },
```
<p>&nbsp;</p>

## Terminal
---
<p>&nbsp;</p>

The terminal theme being used in the screenshot is [powerlevel10k](https://github.com/romkatv/powerlevel10k) for [ohmyzsh](https://ohmyz.sh/), and is using the [Meslo Nerd Font patched for Powerlevel10k](https://github.com/romkatv/powerlevel10k#meslo-nerd-font-patched-for-powerlevel10k)