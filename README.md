# Housing Crisis Campaign Hub

A Jekyll-based static site for the Housing Crisis TTRPG campaign, featuring a gritty cyberpunk dystopian aesthetic with satirical corporate horror elements.

## Overview

This repository hosts the campaign hub for **Housing Crisis**, a Ray Winninger's Underground RPG campaign set in a crumbling, gang-infested housing project in Neo-L.A. Veteran super-soldiers ("Slushies") fight to transform their war zone into a self-sustaining utopia over 20 sessions of corporate warfare and community building.

## Campaign Structure

**Housing Crisis** spans 20 sessions across three major arcs:

1. **Sessions 1–7:** Street-Level Threats — Dealing with corporate-sponsored gangs and corrupt "Rent-A-Cops"
2. **Sessions 8–14:** Infrastructure Building — Securing clean water, food (Tastee-Goo alternatives), and medical supplies through "liberation" missions
3. **Sessions 15–20:** Corporate Pushback — The neighborhood's success attracts corporate attention, culminating in a massive high-power siege

**Key Themes:** Satirical cyberpunk dystopia, corporate greed, housing crisis, social change mechanics, genetically engineered super-soldiers, urban decay, consumer dystopia

**Cultural Touchstones:** Robocop, Judge Dredd, Escape from New York, The Warriors, Brazil, Blade Runner (with crass product placement), 1990s urban decay

## Features

- **Public Player Content:**
  - Rules & Info: Underground RPG mechanics, Social Change system, and power references
  - World: Neo-L.A. setting, Slushies background, corporations, and factions
  - Sessions: Chronological session summaries tracking neighborhood transformation
  
- **Private GM Content:**
  - Accessible via `/gm/` URL
  - Campaign arc breakdowns and session planning (20 sessions)
  - NPCs, corporate antagonists, and gang factions
  - Plot hooks, worldbuilding secrets, and adventure seeds
  - Not indexed by search engines (via robots.txt)

- **Theme:**
  - Gritty urban decay color scheme (concrete grays, neon accents, rust colors)
  - Industrial/dystopian typography
  - Corporate dystopia and urban warfare aesthetic
  - 1990s cyberpunk with brutalist design elements
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
│   ├── character-creation/   # Slushie creation and powers
│   ├── social-change/        # Neighborhood stat tracking system
│   ├── combat-powers/        # Combat and power usage
│   ├── cheat-sheets/         # Quick reference sheets
│   └── setting-rules/        # Technology and economics
├── _world/               # Campaign world content (public)
│   ├── setting/          # Underground dystopia overview
│   ├── neo-la/           # City and housing project
│   ├── slushies/         # Super-soldier background
│   ├── factions/         # Corporations and gangs
│   └── technology/       # Cybernetics and daily life
├── _sessions/            # Session summaries (public)
├── _gm/                  # GM-only content (private URL)
│   ├── campaign-arcs/    # 20-session breakdown
│   ├── npcs/             # NPCs, corporates, gangs
│   ├── secrets/          # Hidden worldbuilding
│   └── adventures/       # Mission seeds and hooks
├── _templates/           # Templates for new content
├── assets/css/           # Custom cyberpunk/dystopian styling
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
- **Background:** Concrete grays and deep blacks
- **Accents:** Neon cyan, warning orange, toxic green
- **Text:** Off-white and cold gray
- **Atmosphere:** Urban decay meets corporate dystopia

## Contributing

This is a private campaign repository. If you're a player, please don't peek at the `_gm/` folder—spoilers ahead!

## License

Campaign content is private. The Jekyll structure and theme are based on open-source components.

## Credits

- Built with [Jekyll](https://jekyllrb.com/)
- Theme based on [Minima](https://github.com/jekyll/minima)
- Powered by **Underground** by Ray Winninger (Mayfair Games, 1993)
- Inspired by Robocop, Judge Dredd, Escape from New York, The Warriors, Brazil, Blade Runner
- Structure inspired by [Autumn-Hollow](https://github.com/JakeAO/Autumn-Hollow)
