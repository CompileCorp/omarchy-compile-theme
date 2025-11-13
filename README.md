# Felix - Omarchy Theme (Oxide Edition)

An Omarchy Theme for your Arch Linux / Hyprland setup

A refined theme for the digital minimalist, featuring the Oxide Computer design system color palette. Dark backgrounds with vibrant Oxide green accents, complemented by carefully selected secondary colors. Going edge-to-edge on your monitor without wasting valuable screen real estate.

Single curated wallpaper. No clown-color text. No workspace animations. No nonsense.

## Color Palette

Based on the Oxide Computer design system:
- **Oxide Green** (#48d597) - Primary accent
- **Yellow** (#F5B944), **Red** (#FB6E88), **Blue** (#8BA1FF) - Secondary colors
- **Dark Neutrals** (#080F11, #1C2225) - Backgrounds
- **Near White** (#FEFFFF) - Text

## Installation

### 1. Clone the Repository and Checkout the Branch

```bash
# Clone the repository
git clone https://github.com/CompileCorp/omarchy-compile-theme.git
cd omarchy-compile-theme

# Checkout the Oxide edition branch
git checkout claude/update-theme-primary-colors-011CV5rUv1nLbf5kHq5YxWwK
```

### 2. Download the Wallpaper

```bash
# See backgrounds/README.md for wallpaper download instructions
# Download from: https://wallhaven.cc/w/8g5qr2
# Save as: backgrounds/wallpaper.png
```

### 3. Apply Theme Components

The theme includes configuration for multiple components. Copy the relevant files to your config directories:

#### Hyprland (Window Manager)
```bash
# Append or merge with your existing hyprland.conf
cat hyprland.conf >> ~/.config/hypr/hyprland.conf
# OR manually copy the general, decoration, and group sections
```

#### Hyprlock (Lock Screen)
```bash
cp hyprlock.conf ~/.config/hypr/hyprlock.conf
```

#### Alacritty (Terminal)
```bash
# Backup your existing config first
cp ~/.config/alacritty/alacritty.toml ~/.config/alacritty/alacritty.toml.backup
# Copy the theme colors
cp alacritty.toml ~/.config/alacritty/alacritty.toml
```

#### Waybar (Status Bar)
```bash
cp waybar.css ~/.config/waybar/style.css
```

#### Walker (Application Launcher)
```bash
cp walker.css ~/.config/walker/style.css
```

#### Mako (Notifications)
```bash
cp mako.ini ~/.config/mako/config
```

#### SwayOSD (Volume/Brightness OSD)
```bash
cp swayosd.css ~/.config/swayosd/style.css
```

#### Btop (System Monitor)
```bash
mkdir -p ~/.config/btop/themes
cp btop.theme ~/.config/btop/themes/oxide.theme
# Then in btop, press ESC -> Options -> Color theme -> oxide
```

### 4. Reload/Restart Components

```bash
# Reload Hyprland config (Super + Shift + C or:)
hyprctl reload

# Restart Waybar
killall waybar && waybar &

# Restart Mako
killall mako && mako &

# Lock screen test
hyprlock

# Terminal - just open a new Alacritty window
```

## Wallpaper

See `backgrounds/README.md` for wallpaper installation instructions.

## Components Themed

- **Hyprland** - Window manager borders, groups, opacity
- **Hyprlock** - Lock screen
- **Alacritty** - Terminal colors
- **Waybar** - Status bar
- **Walker** - Application launcher
- **Mako** - Notifications
- **SwayOSD** - Volume/brightness indicators
- **Btop** - System monitor

![Felix Omarchy Theme Screenshot](theme.png)
