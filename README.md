# Autumn Hollow Campaign Hub

A Jekyll-based static site for the Autumn Hollow TTRPG campaign, featuring a spooky, cozy, autumnal aesthetic with cosmic horror elements.

## Overview

This repository hosts the campaign hub for **Autumn Hollow**, a Kids On Bikes campaign set in a small Indiana town trapped in an eternal October 31st, 1986 time loop. When cosmic forces threaten their town, a group of kids must solve the mystery and break the cycle.

## Features

- **Public Player Content:**
  - Rules & Info: Kids On Bikes mechanics and cheat sheets
  - World: Setting, revealed NPCs, locations, and mysteries
  - Sessions: Chronological session summaries tracking loop progress
  
- **Private GM Content:**
  - Accessible via obscured URL (`/gm-hollow-8a4f2d/`)
  - Campaign planning and time loop mechanics
  - Hidden NPC secrets and motivations
  - World secrets and cosmic horror revelations
  - Not indexed by search engines (via robots.txt)

- **Theme:**
  - Warm autumn colors (oranges, browns, golds)
  - Spooky but cozy 1980s small-town atmosphere
  - Stranger Things + cosmic horror aesthetic
  - Coming-of-age story vibes
  - Mobile-responsive design

## Local Development

### Prerequisites

- Ruby 3.1 or higher
- Bundler gem

### Setup

```bash
# Install dependencies
bundle install

# Serve locally
bundle exec jekyll serve

# Build for production
bundle exec jekyll build
```

The site will be available at `http://localhost:4000`

## Project Structure

```
.
├── _config.yml           # Jekyll configuration
├── _info/                # Rules and mechanics (public)
│   ├── mechanics/        # Kids On Bikes gameplay explanations
│   └── cheat-sheets/     # Quick reference sheets
├── _world/               # Campaign world content (public)
│   ├── npcs/             # Non-player characters
│   ├── locations/        # Places in town
│   └── factions/         # Groups and organizations
├── _sessions/            # Session summaries (public)
├── _gm/                  # GM-only content (private URL)
│   ├── planning/         # Campaign and session planning
│   ├── npcs/             # Secret NPC information
│   └── secrets/          # Hidden world lore
├── _templates/           # Templates for new content
├── assets/css/           # Custom autumn/horror styling
├── index.md              # Home page
├── info.md               # Rules landing page
├── world.md              # World landing page
├── sessions.md           # Sessions landing page
└── gm-notes.md           # GM vault landing page
```

## Adding Content

### Public Content

Create new markdown files in the appropriate collection folder:

**NPC Example:**
```markdown
---
layout: page
title: Character Name
topic: NPCs
summary: Brief description
---

# Character Name

Full content here...
```

**Session Example:**
```markdown
---
layout: page
title: Session Title
index: 1
summary: Brief summary
---

# Session 1: Title

Full session summary...
```

### GM Content

Same structure, but place files in `_gm/` directory. These will be published at the obscured URL but won't appear in navigation or search engine indexes.

## Deployment

The site automatically deploys to GitHub Pages via GitHub Actions when changes are pushed to the `main` branch.

### GitHub Pages Setup

1. Go to repository Settings → Pages
2. Set Source to "GitHub Actions"
3. The workflow in `.github/workflows/pages.yml` handles the rest

## Theme Customization

The site uses Jekyll's Minima theme with extensive customization in `assets/css/style.scss`. The autumn/horror color scheme and styling can be adjusted there.

### Color Palette
- **Background:** Deep dark browns and blacks
- **Accents:** Burnt orange, golden autumn, deep purple
- **Text:** Warm off-white and muted beige
- **Atmosphere:** Cozy autumn meets cosmic horror

## Contributing

This is a private campaign repository. If you're a player, please don't peek at the `_gm/` folder—spoilers ahead!

## License

Campaign content is private. The Jekyll structure and theme are based on open-source components.

## Credits

- Built with [Jekyll](https://jekyllrb.com/)
- Theme based on [Minima](https://github.com/jekyll/minima)
- Powered by [Kids On Bikes](https://www.huntersentertainment.com/kids-on-bikes) by Hunters Entertainment
- Inspired by Stranger Things, Gravity Falls, and cosmic horror
- Structure inspired by [Vaultlight](https://github.com/JakeAO/Vaultlight)
