# VS Code 2026 — Theme for Zed

A faithful port of the VS Code 2026 light and dark themes to [Zed](https://zed.dev).

## Preview

### Dark

![VS Code 2026 Dark in Zed](screenshots/dark.png)

### Light

![VS Code 2026 Light in Zed](screenshots/light.png)

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
└── themes/
    └── vs-code-2026.json                # Both Dark and Light variants
```

## Credits

- Theme design and palette: based on the VS Code 2026 light and dark themes by Mustafa Yurdakul.
- Zed port: Mustafa Yurdakul.

## License

MIT
