# Adding Workshop Pages

This guide explains how to add new workshop pages to the AIEPS website.

## Overview

Each workshop year has:
- An entry in `_data/workshops.yml` for navigation
- A dedicated markdown file (e.g., `2027.md`) with workshop details
- Uses the `workshop` layout template

## Steps to Add a New Workshop Year

### 1. Update `_data/workshops.yml`

Add an entry for the new year at the **top** of the file:

```yaml
- year: 2027
  title: "AIEPS Day 2027 – Workshop on AI in Earth & Planetary Sciences"
  date: "TBA"
  location: "TBA"
  url: "/2027"
  is_current: true
  status: "upcoming"
```

**Important:** Update the previous year's `is_current` field to `false`.

### 2. Create the Workshop Page

Create a new file `2027.md` in the root directory. You can copy from `YYYY-template.md` or use this template:

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
description: "Join us for the 2027 Workshop on Artificial Intelligence in Earth & Planetary Sciences."
sections:
  - id: overview
    title: Overview
  - id: topics
    title: Topics
  - id: dates
    title: Key Dates
  - id: venue
    title: Venue
  - id: registration
    title: Registration
  - id: schedule
    title: Schedule
  - id: speakers
    title: Speakers
  - id: organisers
    title: Organisers
  - id: conduct
    title: Code of Conduct
cta_buttons:
  - text: "Submit Abstract"
    url: "#"
    primary: true
    disabled: true
  - text: "Register Now"
    url: "#"
    primary: false
    disabled: true
sponsors:
  - name: "TBA"
contact: |
  For inquiries, please contact: **pankaj[dot]mishra[AT]gtk.fi**
  
  For more information about the AI-EPS workshop series, visit our [GitHub organization](https://github.com/AI-EPS).
---

## Overview
{: #overview}

The **2027 Workshop on Artificial Intelligence in Earth & Planetary Sciences (AIEPS Day 2027)** will bring together researchers, practitioners, and students working at the intersection of artificial intelligence and Earth & Planetary Sciences.

[Add your content here...]

---

## Topics of Interest
{: #topics}

We welcome contributions on topics including:

- Scientific Machine Learning
- Geophysical Modeling and Inversion
- Remote Sensing and Satellite Imagery
- Climate Science
- Planetary Science
- Natural Hazard Prediction

[Continue with other sections...]
```

### 3. Update Previous Year's Page

When a workshop is complete, update its page:

```yaml
status: completed  # Change from "upcoming" to "completed"
```

Update the content to reflect actual event details (speakers, schedule, etc.)

### 4. Update Navigation Data

In `_data/workshops.yml`, update the previous year's status:

```yaml
- year: 2026
  # ... other fields ...
  is_current: false      # Changed from true
  status: "completed"    # Changed from "upcoming"
```

## Front Matter Reference

| Field | Required | Description | Example |
|-------|----------|-------------|---------|
| `layout` | Yes | Page layout | `workshop` |
| `title` | Yes | Page title | `"AIEPS Day 2027"` |
| `year` | Yes | Workshop year | `2027` |
| `status` | Yes | Event status | `upcoming`, `completed`, or `planning` |
| `hero_title` | Yes | Main heading | `"AIEPS Day 2027"` |
| `hero_subtitle` | Yes | Subtitle | `"Workshop on AI in Earth & Planetary Sciences"` |
| `date` | No | Event date | `"15 June 2027"` or `"TBA"` |
| `location` | No | Venue | `"Helsinki, Finland"` |
| `format` | No | Event format | `"Hybrid (In-person + Online)"` |
| `description` | No | SEO description | Text for meta description |
| `sections` | No | Navigation sections | Array of `{id, title}` objects |
| `cta_buttons` | No | Call-to-action buttons | Array of button objects |
| `sponsors` | No | Sponsor list | Array of sponsor objects |
| `contact` | No | Contact info | Markdown text |

## Section IDs

Each major section should have an ID for navigation:

```markdown
## Overview
{: #overview}

Content here...

---

## Topics of Interest
{: #topics}

Content here...
```

## Call-to-Action Buttons

```yaml
cta_buttons:
  - text: "Submit Abstract"
    url: "https://example.com/submit"
    primary: true
    disabled: false
  - text: "Register Now"
    url: "https://example.com/register"
    primary: false
    disabled: false
```

Set `disabled: true` to gray out buttons that aren't active yet.

## Testing

After creating a new workshop page:

1. Run the local server: `bundle exec jekyll serve`
2. Visit `http://localhost:4000`
3. Check the Workshop Year dropdown includes your new year
4. Verify the page displays correctly
5. Test navigation between sections
6. Test on mobile devices

## Tips

- Use `TBA` for information not yet available
- Keep section structure consistent across years
- Add actual content as it becomes available
- Include all relevant dates in a table format
- Use the `highlight-box` class for important announcements
- Always include contact information
