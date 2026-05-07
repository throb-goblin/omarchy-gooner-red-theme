# Gooner Red — Omarchy Theme

A red noir gooner theme for [Omarchy](https://omarchy.org/). Deep crimson base, pure red accents and muted rose borders.

![Preview 1](screenshots/preview-1.png)
![Preview 2](screenshots/preview-2.png)

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

> **Waybar:** copy `waybar-config.jsonc` to `~/.config/waybar/config.jsonc` to apply the full module layout. The CSS alone won't render correctly without it. Then update the `hwmon-path` in the temperature module to match your hardware — find the right path with `find /sys/devices -name "temp1_input" 2>/dev/null`.

> **Walker:** copy `walker-config.toml` to `~/.config/walker/config.toml` to apply the full launcher layout and behaviour settings.

> **About:** copy `about.txt` to `~/.config/omarchy/branding/about.txt` to apply the custom branding shown in the Omarchy menu.

## Plymouth Boot Splash

The `plymouth/` directory contains a custom boot splash. This requires a manual install as it needs sudo and an initramfs rebuild.

```bash
sudo mkdir -p /usr/share/plymouth/themes/omarchy-red
sudo cp plymouth/* /usr/share/plymouth/themes/omarchy-red/
sudo plymouth-set-default-theme omarchy-red

# Rebuild initramfs (use the second line if you're on Limine)
sudo mkinitcpio -P
# sudo limine-mkinitcpio
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
| Active shadow | `#ff3a3a66` |
| Selection | `#372223` |

## Terminal ANSI Palette

Monochromatic red-noir approach — colors 2–4 are shades of red rather than green/yellow/blue, with cool greys for magenta and cyan.

| # | Normal | Bright |
|---|--------|--------|
| 0 black | `#1A0E0E` | `#4b515b` |
| 1 red | `#b33a3a` | `#ff3a3a` |
| 2 red (mid) | `#d13a3a` | `#d13a3a` |
| 3 red (dark) | `#9e3a3a` | `#9e3a3a` |
| 4 red (muted) | `#ad3a3a` | `#ad3a3a` |
| 5 magenta | `#c3c8d0` | `#c3c8d0` |
| 6 cyan | `#8f949c` | `#8f949c` |
| 7 white | `#b9bec6` | `#eceff2` |

## Components

- **Hyprland** — border colors, shadow, blur, rounded corners, spring animations
- **Walker** — launcher with full layout and red noir colors
- **Waybar** — complete pill layout with dark red base
- **Mako** — notifications with red border and dark base
- **SwayOSD** — red gradient progress bar
- **Hyprlock** — minimal lock screen
- **Plymouth** — red boot splash with animated progress bar
- **Alacritty / Ghostty / Kitty** — full ANSI palette
- **btop** — grey → muted red → primary red gradients
- **Neovim** — Matte Black colorscheme
- **VSCode** — Matte Black theme

## License

MIT