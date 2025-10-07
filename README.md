# ai-eps.github.io

Website for the AI in Earth & Planetary Sciences (AI-EPS) workshop series.

## About

This repository hosts the official website for the annual AI in Earth & Planetary Sciences workshop. The website is built using Jekyll and GitHub Pages.

## Website Structure

- `index.md` - Main landing page (shows current year workshop)
- `2025.md` - 2025 workshop details
- `_config.yml` - Jekyll configuration

## Adding a New Year

To add a new workshop year:

1. Create a new markdown file named `YYYY.md` (e.g., `2026.md`)
2. Copy the structure from `2025.md` and update the content
3. Update `index.md` to point to the new year as the current workshop
4. Add the previous year to the "Past Workshops" section

## Local Development

To test the website locally:

```bash
gem install jekyll bundler
jekyll serve
```

Then visit `http://localhost:4000` in your browser.

## License

MIT License - see [LICENSE](LICENSE) file for details.
