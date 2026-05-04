# Gooner Red — Omarchy Theme

A red noir gooner theme for [Omarchy](https://omarchy.org/). Deep crimson base, pure red accents and muted rose borders.

![Preview 1](screenshots/preview-1.png)
![Preview 2](screenshots/preview-2.png)
![Preview 3](screenshots/preview-3.png)

## Requirements

- [`ttf-nerd-fonts-symbols-mono`](https://archlinux.org/packages/extra/any/ttf-nerd-fonts-symbols-mono/) — required for correct icon rendering in Waybar

```bash
fc-list | grep -q "Symbols Nerd Font Mono" || yay -S --noconfirm ttf-nerd-fonts-symbols-mono
```

## Install

```bash
omarchy-theme-install https://github.com/throb-goblin/omarchy-gooner-red-theme
omarchy-theme-set "gooner-red"
```

## Palette

| Role | Hex |
|------|-----|
| Background | `#1b1112` |
| Surface | `#2B2826` |
| Text | `#ffffff` |
| Primary red | `#ff3a3a` |
| Muted red | `#b33a3a` |
| Active border | `#bf7b75` |
| Inactive border | `#642425` |
| Active shadow | `rgba(ff3a3a, 0.4)` |
| Selection | `#372223` |

## Terminal ANSI Palette

| # | Normal | Bright |
|---|--------|--------|
| 0 black | `#1A0E0E` | `#2B1818` |
| 1 red | `#b33a3a` | `#ff3a3a` |
| 2 green | `#C05A5A` | `#D97171` |
| 3 yellow | `#D66B6B` | `#E87F7F` |
| 4 blue | `#1e90ff` | `#60b8ff` |
| 5 magenta | `#bf7b75` | `#d99189` |
| 6 cyan | `#d97a7a` | `#e89494` |
| 7 white | `#F2E8E8` | `#FFF1F1` |

## Components

- **Hyprland** — border colors, shadow, blur, rounded corners, spring animations
- **Walker** — launcher with full layout and red noir colors
- **Waybar** — complete pill layout with dark red base
- **Mako** — notifications with red border and dark base
- **SwayOSD** — red gradient progress bar
- **Hyprlock** — minimal lock screen with red glow
- **Alacritty / Ghostty / Kitty** — full ANSI palette
- **btop** — grey → muted red → primary red gradients
- **Neovim** — Matte Black colorscheme
- **VSCode** — Matte Black theme

## Walker Config

Copy `walker-config.toml` to `~/.config/walker/config.toml` to apply the full walker behaviour settings.

## License

MIT
