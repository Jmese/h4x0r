# Custom Retro Theme

This repository contains my personalized take on the original **h4x0r** WordPress block theme. I tweaked it to match my own retro aesthetic: a CRT-inspired layout, multiple terminal color schemes, and a soft backlight glow that makes the typography feel like it is painted on a monitor.

## Highlights
- Native WordPress block theme with header/footer template parts and pattern-friendly templates.
- CRT scanline effect, backlight glow, and monospace typography for that terminal vibe.
- Multiple style variations (`styles/*.json`) including Cyberpunk, Dracula, Solarized, and more.
- Custom font faces (Roboto Mono, Fira Code, JetBrains Mono, Source Code Pro, Noto Sans Mono) bundled inside `assets/fonts`.
- Minimal PHP (`functions.php`)—only enqueues styles—so most customization happens through CSS and block templates.

## Screenshots

- Cyberpunk: `screenshot-full.png`
- Default Light/Dark: `screenshot-default-light.png`, `screenshot-default-dark.png`
- Dracula: `screenshot-dracula.png`
- Solarized Light/Dark: `screenshot-solarized-light.png`, `screenshot-solarized-dark.png`

Feel free to replace these images once you capture your own variants; WordPress uses `screenshot.png` for the theme picker.

## Getting Started
1. Copy the theme folder into `wp-content/themes/` of your WordPress install.
2. From the admin dashboard, go to **Appearance → Themes** and activate “Custom Retro Theme”.
3. Open the Site Editor to adjust templates (`templates/*.html`) or global styles (`theme.json`, style variations).

## Personalization Guide

| Area | File(s) | Notes |
| --- | --- | --- |
| Theme metadata & CRT/backlight CSS | `style.css` | Update the header block for your site info. Two CSS variables control the glow: `--h4x0r-backlight-color` and `--h4x0r-backlight-size`. |
| Global design tokens | `theme.json` | Adjust color palette, spacing, typography, and registered fonts. |
| Alternate palettes | `styles/*.json` | Duplicate and tweak to add more colorways; each file overrides pieces of `theme.json`. |
| Header/Footer | `parts/header.html`, `parts/footer.html` | Swap social links, add navigation, or change copy. |
| Templates | `templates/*.html` | Control layout for front page, posts, archives, and specialized categories. |
| Fonts | `assets/fonts/` | Drop in additional fonts and register them in `theme.json`. |

### Adjusting the Text Backlight
The glow is defined at the top of `style.css`:

```css
:root {
  --h4x0r-backlight-color: rgba(0, 122, 204, 0.35);
  --h4x0r-backlight-size: 1.5ch;
}
```

Change the color or size to make the effect stronger, softer, or match a different palette. You can also override these variables via the Site Editor’s “Additional CSS” if you prefer not to edit the theme files.

## License

This theme inherits the [GNU General Public License v2](LICENSE). Feel free to remix it as long as derivatives stay GPL-compatible.
