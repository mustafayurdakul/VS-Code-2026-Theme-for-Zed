# VS Code 2026 — Theme for Zed

A faithful port of the VS Code 2026 light and dark themes to [Zed](https://zed.dev), built directly from the original theme sources in [microsoft/vscode](https://github.com/microsoft/vscode/tree/main/extensions/theme-defaults/themes).

## Preview

### Dark

![VS Code 2026 Dark in Zed](screenshots/dark.png)

### Light

![VS Code 2026 Light in Zed](screenshots/light.png)

## Faithful to the source

This is not an approximation or a look-alike. Every color in this theme is taken **verbatim from the upstream VS Code 2026 theme definitions** — the same JSON files VS Code itself ships in `extensions/theme-defaults/themes`:

- Hex values are copied 1:1 from the upstream `2026 Dark` and `2026 Light` definitions, including their exact alpha channels (e.g. the dark focus border `#3994BCB3`).
- Where the upstream themes inherit from `dark_modern` / `light_modern` via `include`, the resolved values from those bases are used.
- Each Zed theme property is mapped to its closest VS Code counterpart (workbench chrome, editor surfaces, terminal ANSI palette, git/diagnostic states, and the full syntax token scope mapping). No colors were invented.

The unmodified upstream theme files are kept in [`reference/`](reference/) so every value in [`themes/vs-code-2026.json`](themes/vs-code-2026.json) can be audited against its source.

## Variants

- **VS Code - 2026 Dark** — the dark variant, neutral chrome (`#191a1b`) with a near-black editor surface (`#121314`) and a teal-blue accent (`#3994bc`).
- **VS Code - 2026 Light** — the light variant, soft off-white chrome (`#fafafd`) with a pure white editor surface and a saturated blue accent (`#0069cc`).

Both variants share GitHub-style syntax highlighting: red keywords, purple functions, blue constants and properties, orange types, green tags, and muted grey comments.

## Install

### From the Zed extension registry

1. Open the command palette (`cmd-shift-p` / `ctrl-shift-p`).
2. Run `zed: extensions`.
3. Search for **VS Code 2026** and install.
4. Run `theme selector: toggle` and pick **VS Code - 2026 Dark** or **VS Code - 2026 Light**.

### As a dev extension (from source)

1. Clone this repository.
2. In Zed, run `zed: install dev extension` and point it at the cloned directory.
3. Pick the theme via `theme selector: toggle`.

## Structure

```
.
├── extension.toml                       # Zed extension manifest
├── themes/
│   └── vs-code-2026.json                # Both Dark and Light variants
└── reference/
    ├── 2026-dark.json                   # Upstream VS Code 2026 Dark theme (unmodified)
    └── 2026-light.json                  # Upstream VS Code 2026 Light theme (unmodified)
```

The `reference/` folder holds the original VS Code theme definitions from [microsoft/vscode](https://github.com/microsoft/vscode/tree/main/extensions/theme-defaults/themes) that this port is built from. They are kept out of `themes/` because Zed loads every JSON file in that folder as a Zed theme.

## Credits

- Original VS Code 2026 theme design and palette: the [VS Code](https://github.com/microsoft/vscode) team at Microsoft.
- Zed port: Mustafa Yurdakul.

## License

MIT
