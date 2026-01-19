# AIEPS - AI in Earth & Planetary Sciences

**AIEPS (AI in Earth & Planetary Sciences)** is a special interest group dedicated to advancing the application of artificial intelligence, machine learning, and scientific computing in Earth and Planetary Sciences.

We bring together researchers, practitioners, and students to explore how AI is transforming geoscience research, from climate modeling and geophysical inversion to planetary exploration and natural hazard prediction.

## Website

This repository hosts the official website for AIEPS, built using Jekyll and GitHub Pages with a custom responsive design.

Visit us at: [https://ai-eps.github.io](https://ai-eps.github.io)

## Activities

- **Annual Workshop (AIEPS Day)**: Our flagship event featuring invited talks and contributed presentations
- **Seminar Series**: Regular online seminars on AI applications in geoscience

## Adding New Year Pages

### Adding a New Workshop Year

1. Copy `/workshops/_year-template.md` to `/workshops/2027.md` (replace 2027 with the actual year)
2. Update the frontmatter (title, year, permalink, dates, etc.)
3. Add an entry to `_data/workshops.yml`:
   ```yaml
   - year: 2027
     title: "AIEPS Day 2027 – Workshop on AI in Earth & Planetary Sciences"
     date: "TBA"
     location: "TBA"
     url: "/workshops/2027"
     is_current: true
     status: "upcoming"
   ```
4. Set previous year's `is_current` to `false`

### Adding a New Seminar Year

1. Copy `/seminars/_year-template.md` to `/seminars/2027.md` (replace 2027 with the actual year)
2. Update the frontmatter (title, year, permalink, etc.)
3. Add an entry to `_data/seminars.yml`:
   ```yaml
   - year: 2027
     title: "AIEPS Seminars 2027"
     url: "/seminars/2027"
     is_current: true
     status: "upcoming"
   ```
4. Set previous year's `is_current` to `false`

## Local Development

To test the website locally:

```bash
# Install dependencies
bundle install

# Run local server
bundle exec jekyll serve
```

Then visit `http://localhost:4000` in your browser.

## Contact

For inquiries: **pankaj[dot]mishra[AT]gtk.fi**

## License

MIT License - see [LICENSE](LICENSE) file for details.
