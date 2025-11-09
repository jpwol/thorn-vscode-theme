# Contributing to Thorn

Thank you for your interest in contributing to Thorn!

There isn't a lot to be worked on here, but any input is welcome!

Namely, the extra variants are yet to be added, so contributions there are welcome. Additionally, if there are any bugs/issues with highlighting in certain programming languages, issues or pull-requests pertaining to that are also welcome!

## Todo

These are the items which need to be/have been completed. For working on any of these, please refer to [thorn.nvim](https://github.com/jpwol/thorn.nvim) for styling/highlights.

- [x] Thorn Dark Warm (base theme)
- [ ] Thorn Dark Cold
- [ ] Thorn Light Warm
- [ ] Thorn Light Cold

### How to start

For contributing to the themes, follow these steps:

1. Copy the main theme (Thorn-color-theme.json) to the variant you're working on.
   - The variant should be titled `dark/light`-`warm/cold`-color-theme.json.
   - The file name must end with `-color-theme.json` to utilize VSCode's built-in auto-completion and color previewer.
2. Referring to **thorn.nvim's** [colors](https://github.com/jpwol/thorn.nvim/tree/main/lua/thorn/colors.lua), do a mass **find and replace** on the hex values.
3. For any other values in the vscode theme that may not match, do your best to pick values that match the feel of the main theme.
   - These will be kept or changed at my discretion.
4. Add your variant to the `contributes` section of the `package.json` file, with the label "Thorn (dark/light warm/cold)", and the correct path.

#### Example of `package.json`

```json
"contributes": {
    "themes": [
        {
            "label": "Thorn (dark warm)",
            "uiTheme": "vs-dark",
            "path": "./themes/dark-warm-color-theme.json"
        },
        {
            "label": "Thorn (light cold)",
            "uiTheme": "vs",
            "path": "./themes/light-cold-color-theme.json"
        }
    ]
},
```

## Commit Guidelines

Please follow the general **Angular** commit style, i.e.

- feat (an added feature)
- fix (a bug fix/style fix)
- refactor (non-user facing code changes)
- style (non-user facing code style changes)
- docs (changes to documentation such as README or CONTRIBUTING)
- perf (in this context, making package size smaller)
- chore (non-user facing changes that don't fit into other categories)

Where a commit would look like

```
feat(theme): added light warm variant
```
