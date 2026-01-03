# ai-eps.github.io

Website for the AI in Earth & Planetary Sciences (AI-EPS) workshop series.

## About

This repository hosts the official website for the annual AI in Earth & Planetary Sciences workshop. The website is built using Jekyll and GitHub Pages with a custom responsive design.

## Website Structure

```
├── _config.yml           # Jekyll configuration
├── _data/
│   └── workshops.yml     # Workshop years data (for navigation dropdown)
├── _includes/
│   └── header.html       # Site header with navigation
├── _layouts/
│   └── workshop.html     # Workshop page layout template
├── assets/
│   └── css/
│       └── style.css     # Site styles
├── index.md              # Landing page (shows current year workshop)
├── 2026.md               # 2026 workshop details
├── 2025.md               # 2025 workshop details
└── YYYY-template.md      # Template for new workshop years
```

## Adding a New Year

To add a new workshop year:

### 1. Update `_data/workshops.yml`

Add an entry for the new year at the top of the file:

```yaml
- year: 2027
  title: "AIEPS Day 2027 – Workshop on AI in Earth & Planetary Sciences"
  date: "TBA"
  location: "TBA"
  url: "/2027"
  is_current: true
  status: "upcoming"
```

Update the previous current year's `is_current` to `false`.

### 2. Create the Workshop Page

Create a new file `2027.md` (or copy from `YYYY-template.md`):

```yaml
---
layout: workshop
title: "AIEPS Day 2027"
year: 2027
status: upcoming
hero_title: "AIEPS Day 2027"
hero_subtitle: "Workshop on AI in Earth & Planetary Sciences"
date: "TBA"
location: "TBA"
format: "Hybrid (In-person + Online)"
# ... additional front matter
---

## Overview
{: #overview}

Your content here...
```

### 3. Update the Landing Page

If this is the new current workshop, update `index.md` to show the new year's content (copy the front matter and content from the new workshop file).

### 4. Update Previous Year

Update the previous year's page (e.g., `2026.md`):
- Change `status: upcoming` to `status: completed`
- Update content as needed

## Front Matter Options

Each workshop page supports the following front matter:

| Field | Description |
|-------|-------------|
| `layout` | Should be `workshop` |
| `title` | Page title |
| `year` | Workshop year (number) |
| `status` | `upcoming`, `completed`, or `planning` |
| `hero_title` | Main heading in hero section |
| `hero_subtitle` | Subtitle in hero section |
| `date` | Workshop date |
| `location` | Venue location |
| `format` | e.g., "Hybrid (In-person + Online)" |
| `description` | Meta description for SEO |
| `sections` | Array of section objects for navigation |
| `cta_buttons` | Array of call-to-action buttons |
| `sponsors` | Array of sponsor objects |
| `contact` | Contact information (markdown) |

## Local Development

To test the website locally:

```bash
# Install dependencies
bundle install

# Run local server
bundle exec jekyll serve
```

Then visit `http://localhost:4000` in your browser.

## Design Features

- **Responsive Design**: Works on mobile, tablet, and desktop
- **Year Dropdown**: Navigate between workshop years
- **Section Navigation**: Jump to specific sections within a page
- **Modern Styling**: Clean typography, card components, and subtle gradients
- **Accessibility**: Semantic HTML, ARIA attributes, and keyboard navigation

## License

MIT License - see [LICENSE](LICENSE) file for details.
