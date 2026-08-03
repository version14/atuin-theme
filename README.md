# Version 14 Theme for Atuin

An [Atuin](https://atuin.sh) shell-history theme built around the **Version 14** brand palette — the same palette used across the [Zed](https://github.com/version14/zed-theme), [VS Code](https://github.com/version14/vscode-theme), [Neovim/Vim](https://github.com/version14/nvim-theme), [Ghostty](https://github.com/version14/ghostty-theme), and [Starship](https://github.com/version14/starship-theme) ports.

## Variants

| Variant | File | Theme name |
|---|---|---|
| **Version 14** | `version14.toml` | `version14` |
| **Version 14 Black** | `version14-black.toml` | `version14-black` |
| **Version 14 Light** | `version14-light.toml` | `version14-light` |

> **Note:** Atuin's theme schema has no background/elevation color role — it only styles text, alerts, and syntax highlighting inside its search UI, which otherwise inherits your terminal's background. Because of that, `version14` and `version14-black` are identical here (the Dark/Black distinction only matters for background colors elsewhere in the suite).
>
> The violet accent (`Title`, `Important`, `SyntaxVariable`) is currently a **placeholder** hue, standing in for a retired lime-green accent while a permanent replacement is chosen.

## Installation

1. Copy the variant file you want into `~/.config/atuin/themes/`:
   ```sh
   mkdir -p ~/.config/atuin/themes
   curl -o ~/.config/atuin/themes/version14.toml \
     https://raw.githubusercontent.com/version14/atuin-theme/main/version14.toml
   ```
   or clone the repo (`git clone https://github.com/version14/atuin-theme`) to grab all three at once.
2. In `~/.config/atuin/config.toml`, set:
   ```toml
   [theme]
   name = "version14"
   ```
3. Restart your shell (or re-source it) to apply.

### Verifying the install

```sh
atuin config get theme.name
```

Should print `version14` (or whichever variant you set) — note this only confirms `config.toml` was edited correctly, not that the theme *file* was found. `atuin config get` doesn't validate the file exists, so if colors don't look right in the actual search UI, also double-check the file is really at `~/.config/atuin/themes/version14.toml` (or your `$ATUIN_THEME_DIR`).

Repeat with `version14-black` or `version14-light` for the other variants.

## Color Roles

Atuin themes map semantic **Meanings** to colors (see [Atuin's theming docs](https://docs.atuin.sh/cli/guide/theming/)):

| Meaning | Version 14 / Black | Version 14 Light |
|---|---|---|
| `Base` (main text) | `#F2F4F6` | `#0D0F11` |
| `Muted` / `Annotation` / `Guidance` / `SyntaxComment` | `#6E737A` | `#636870` |
| `Title` / `Important` / `SyntaxVariable` (placeholder accent) | `#B7A2FF` | `#5F3BBB` |
| `AlertInfo` / `SyntaxCommand` | `#78AFFF` | `#0054CB` |
| `AlertWarn` | `#FFA85E` | `#8F4400` |
| `AlertError` | `#FF5C59` | `#B91A25` |
| `SyntaxString` | `#4BDE7F` | `#166534` |
| `SyntaxFlag` | `#ED8EF3` | `#8C2293` |
| `SyntaxOperator` | `#F2F4F6` | `#0D0F11` |

## Also available for Zed, VS Code, Neovim/Vim, Ghostty, and Starship

- [Zed extension](https://github.com/version14/zed-theme)
- [VS Code extension](https://github.com/version14/vscode-theme)
- [Neovim/Vim plugin](https://github.com/version14/nvim-theme)
- [Ghostty theme](https://github.com/version14/ghostty-theme)
- [Starship palette](https://github.com/version14/starship-theme)

## License

[MIT](./LICENSE) © [Mathieu Souflis](https://mathieusouflis.fr)
