# CS241 Syntax Highlighting

This is a VS Code extension that adds syntax highlighting for the CS241 ASL (written in .hex) files.

After downloading, do the following steps:

1. Open `settings.json`
2. Add the following piece of text to the end of the json file:
```json
{
    "editor.tokenColorCustomizations": {
        "textMateRules": [
            {
                "scope": "hex.comment",
                "settings": {
                    "foreground": "#666666",
                    "fontStyle": "italic"
                }
            },
            {
                // registers
                "scope": "hex.register",
                "settings": {
                    "foreground": "#d4975e",
                }
            },
            {
                "scope": "hex.operation",
                "settings": {
                    "foreground": "#67e6df",
                }
            },
            {
                "scope": "hex.literal",
                "settings": {
                    "foreground": "#67a2e6",
                }
            },
            {
                "scope": "hex.loadstore",
                "settings": {
                    "foreground": "#a5e791",
                }
            },
            {
                "scope": "hex.setless",
                "settings": {
                    "foreground": "#67e6df",
                }
            },
            {
                "scope": "hex.branch",
                "settings": {
                    "foreground": "#67e6df",
                }
            },
            {
                "scope": "hex.jump",
                "settings": {
                    "foreground": "#67e6df",
                }
            },
            {
                "scope": "hex.constant",
                "settings": {
                    "foreground": "#dd6bd4",
                }
            },
            {
                // labels
                "scope": "hex.label",
                "settings": {
                    "foreground": "#d8d789",
                    "fontStyle": "bold"
                }
            }
        ]
    }
}
```
This activates the color scheme. You can also customize the colors if you want.
