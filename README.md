# CS241 Syntax Highlighting

This is a VS Code extension that adds syntax highlighting for the CS241 ASL (written in .asm) files.

After downloading, do the following steps:

1. Open `settings.json`
2. Add the following piece of text to the end of the json file:
```json
{
    "editor.tokenColorCustomizations": {
        "textMateRules": [
            {
                "scope": "asm.comment",
                "settings": {
                    "foreground": "#666666",
                    "fontStyle": "italic"
                }
            },
            {
                // registers
                "scope": "asm.register",
                "settings": {
                    "foreground": "#d4975e",
                }
            },
            {
                "scope": "asm.operation",
                "settings": {
                    "foreground": "#67e6df",
                }
            },
            {
                "scope": "asm.literal",
                "settings": {
                    "foreground": "#67a2e6",
                }
            },
            {
                "scope": "asm.loadstore",
                "settings": {
                    "foreground": "#a5e791",
                }
            },
            {
                "scope": "asm.setless",
                "settings": {
                    "foreground": "#67e6df",
                }
            },
            {
                "scope": "asm.branch",
                "settings": {
                    "foreground": "#67e6df",
                }
            },
            {
                "scope": "asm.jump",
                "settings": {
                    "foreground": "#67e6df",
                }
            },
            {
                "scope": "asm.constant",
                "settings": {
                    "foreground": "#dd6bd4",
                }
            },
            {
                // labels
                "scope": "asm.label",
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
