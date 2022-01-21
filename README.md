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
                // comments (ie ; ...)
                "scope": "asm.comment",
                "settings": {
                    "foreground": "#666666",
                    "fontStyle": "italic"
                }
            },
            {
                // registers (ie $X)
                "scope": "asm.register",
                "settings": {
                    "foreground": "#d4975e",
                }
            },
            {
                // the four operations (ie add, sub, mult[u], div[u], mflo, mfhi)
                "scope": "asm.operation",
                "settings": {
                    "foreground": "#67e6df",
                }
            },
            {
                // literals (lis, .word)
                "scope": "asm.literal",
                "settings": {
                    "foreground": "#67a2e6",
                }
            },
            {
                // load and store (lw, sw)
                "scope": "asm.loadstore",
                "settings": {
                    "foreground": "#a5e791",
                }
            },
            {
                // set less than (slt, sltu)
                "scope": "asm.setless",
                "settings": {
                    "foreground": "#67e6df",
                }
            },
            {
                // branching (beq, bne)
                "scope": "asm.branch",
                "settings": {
                    "foreground": "#67e6df",
                }
            },
            {
                // jumping (jr, jalr)
                "scope": "asm.jump",
                "settings": {
                    "foreground": "#67e6df",
                }
            },
            {
                // constants (ie numbers)
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

## Version History

### 1.0.0
Initial release

### 1.0.1
Edited `package.json` and `README.md` to increase clarity

