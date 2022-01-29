# Synthwave x Fluoromachine 🝰 Avant Noir

This is a fork of @webrenders's [Synthwave x Fluoromachine theme](https://github.com/webrender/synthwave-vscode-x-fluoromachine), which in turn is a fork of @robbowen's [Synthwave '84 theme](https://marketplace.visualstudio.com/items?itemName=RobbOwen.synthwave-vscode), merged with @fullerenedream's [Fluoromachine](https://colorsublime.github.io/themes/FluoroMachine/) theme for VSCode. 

This Avant Noir variation darkens the UI, and boosts the general color tone - making the important things pop more.

![Theme screenshot](https://repository-images.githubusercontent.com/184457193/69dcff00-14d2-11ea-90e1-4bdf6fef80ca)
<p>&nbsp;</p>

## Installation 
---
• Install this theme  

• Install the [Custom CSS and JS Loader](https://marketplace.visualstudio.com/items?itemName=be5invis.vscode-custom-css) extension for vscode

• Link the CSS file from this extension in your vscode `settings.json`:


>  **On Macs, the path to your vscode extensions might look something like the snippet below:**

```json
  "vscode_custom_css.imports": [
    "file:///Users/{your username}/.vscode/extensions/webrender.synthwave-x-fluoromachine-0.0.12/synthwave-x-fluoromachine.css"
  ]
```

> **On Windows, the path may resemble:**

```json
  "vscode_custom_css.imports": [
    "file:///C:/Users/{your username}/.vscode/extensions/webrender.synthwave-x-fluoromachine-0.0.12/synthwave-x-fluoromachine.css"
  ]
```
• Finally, open the vscode command panel ( **mac**:&nbsp;&nbsp; <kbd>cmd</kbd> + <kbd>shift</kbd> + <kbd>p</kbd>&nbsp;&nbsp; / &nbsp;&nbsp;**win**:&nbsp;&nbsp; <kbd>ctrl</kbd> + <kbd>shift</kbd> + <kbd>p</kbd> ), and select `Reload Custom CSS and JS`.

_**Note:** You'll need to run the `Reload Custom CSS and JS` command again, every time vscode updates._
<p>&nbsp;</p>

## Editor Font
---
The font being used in the screenshot above is [Victor Mono](https://rubjo.github.io/victor-mono/) which includes **Ligatures** and *_optional semi-connected cursive italics_.*


### Enabling Ligatures

To enable ligatures within your editor pane, add the following snippet to your vscode `settings.json`:

```json
  "editor.fontLigatures": true,
```

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
The terminal theme being used in the screenshot is [powerlevel10k](https://github.com/romkatv/powerlevel10k) for [ohmyzsh](https://ohmyz.sh/), and is using the [Meslo Nerd Font patched for Powerlevel10k](https://github.com/romkatv/powerlevel10k#meslo-nerd-font-patched-for-powerlevel10k)