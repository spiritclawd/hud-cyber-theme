# HUD Cyber Theme 🎨

> Cyberpunk command center theme for the Hermes Agent dashboard. Deep navy, electric cyan, amber accents, Orbitron typography, and a HUD-inspired cockpit layout.

![Preview](./preview.png)
*HUD Cyber theme paired with Hermes Pulse plugin.*

## ✨ Features

- **Palette:** Deep navy background (`#050915`), electric cyan primary (`#3fd3ff`), amber accents (`#ffce3a`)
- **Typography:** Orbitron for headers, Share Tech Mono for code — that classic sci-fi HUD feel
- **Layout:** `cockpit` variant — reserves sidebar slot for plugin telemetry panels
- **Visual chrome:** Corner brackets on cards, hairline borders, scanline overlay, tech-grid backdrop
- **Glowing elements:** Headers and live indicators have subtle text-shadow glow

## 📦 Installation

```bash
# Clone or download this theme
git clone https://github.com/spiritclawd/hud-cyber-theme.git
cd hud-cyber-theme

# Install to Hermes themes directory
cp hud-cyber.yaml ~/.hermes/dashboard-themes/

# Restart Hermes dashboard (or trigger theme rescan)
hermes dashboard --restart  # if using systemd
# Or just kill and restart the dashboard process

# Switch theme
# Open http://127.0.0.1:9119, click the theme swatch in header, select "HUD Cyber"
```

## 🎛️ Configuration

The theme is pure YAML — no extra dependencies. All styling is done via:

- `palette` — 3-layer color system (background, midground, foreground)
- `typography` — font families, sizes, Google Fonts URL
- `componentStyles` — per-component CSS var overrides (card, header, sidebar, tab, badge, backdrop)
- `colorOverrides` — shadcn/ui color system mapping
- `customCSS` — raw CSS for advanced effects (scanlines, corner brackets, grid)

Feel free to fork and tweak colors, fonts, or effects.

## 🧩 Companion Plugin

For the full experience, install [Hermes Pulse](https://github.com/spiritclawd/hermes-pulse) — it populates the sidebar slot with live telemetry and adds a `/pulse` tab with agent metrics.

```bash
# Install both
gh repo clone spiritclawd/hermes-pulse
# (follow plugin install instructions)
```

## 🎨 Color Reference

| Role | Hex | Usage |
|------|-----|-------|
| Primary | `#3fd3ff` | Buttons, links, active elements |
| Accent | `#ffce3a` | Warnings, highlights, badges |
| Success | `#4ade80` | Success states |
| Destructive | `#ff3a5e` | Errors, destructive actions |
| Background | `#050915` | Main canvas |
| Card | `rgba(10, 20, 40, 0.8)` | Card backgrounds |
| Border | `rgba(63, 211, 255, 0.25)` | Hairlines, dividers |

## 📸 Screenshots

![HUD Dashboard](./preview.png)
*Dashboard with Orbitron headers, cyan accents, and amber warning highlights.*

![Sidebar](./preview.png)
*Cockpit layout reserves a 260px left rail for plugin telemetry.*

## 🛠️ Building from Source

The theme YAML lives in this repo. No build step required — just copy the YAML file:

```bash
cp hud-cyber.yaml ~/.hermes/dashboard-themes/
hermes dashboard --restart  # or restart manually
```

## 📜 License

MIT © 2026 Zaia (spiritclawd)

## 🙏 Credits

- Inspired by *Gundam* cockpit HUDs, classic CRT terminals, and *strike-freedom* demo theme
- Fonts by Google Fonts (Orbitron, Share Tech Mono)
- Part of the Hermes Agent plugin ecosystem by Nous Research

---

*"Looking at your agent shouldn't feel like looking at a spreadsheet."* 📡
