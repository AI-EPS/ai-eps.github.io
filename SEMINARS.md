# Adding Seminar Pages

This guide explains how to add new seminar pages and individual seminars to the AIEPS website.

## Overview

The AIEPS Seminar Series consists of:
- An entry in `_data/seminars.yml` for each year
- A markdown file in `seminars/` directory for each year (e.g., `seminars/2027.md`)
- Individual seminar entries within each year's page
- Uses the `seminar` layout template

## Steps to Add a New Seminar Year

### 1. Update `_data/seminars.yml`

Add an entry for the new year at the **top** of the file:

```yaml
- year: 2027
  title: "AIEPS Seminars 2027"
  url: "/seminars/2027"
  is_current: true
  status: "upcoming"
```

**Important:** Update the previous year's `is_current` field to `false`.

### 2. Create the Seminar Year Page

Create a new file `seminars/2027.md`:

```yaml
---
layout: seminar
title: "AIEPS Seminars 2027"
year: 2027
status: upcoming
hero_title: "AIEPS Seminars 2027"
hero_subtitle: "AI in Earth & Planetary Sciences Seminar Series"
description: "AIEPS Seminars 2027 - A series of talks on AI applications in Earth and Planetary Sciences"
contact: |
  For inquiries, please contact: **pankaj[dot]mishra[AT]gtk.fi**
  
  For more information about the AI-EPS seminar series, visit our [GitHub organization](https://github.com/AI-EPS).
---

## About AIEPS Seminars

The **AIEPS Seminar Series** provides a platform for researchers and practitioners to share their work on artificial intelligence applications in Earth and Planetary Sciences. These seminars feature presentations on cutting-edge research, methodologies, and practical implementations.

---

## 2027 Seminars

### AIEPS Seminar #1: [Title]

**Date:** [Date and Time]  
**Format:** Online (Zoom)  
**Speaker:** [Speaker Name], [Affiliation]

#### Title

[Full title of the talk]

#### Abstract

[Abstract text - describe the topic, key points, and what attendees will learn]

#### Speaker Bio

[Brief biography of the speaker, including their research interests and affiliations]

#### Registration

[Link or instructions for registration]

---

### AIEPS Seminar #2: [Title]

[Repeat structure for additional seminars]

---

## How to Attend

Details on how to register and attend the seminars will be posted here. Seminars are typically held online via Zoom to enable global participation.

---

## Past Seminars

Check the dropdown menu for seminars from previous years.
```

## Adding Individual Seminars

To add a new seminar to an existing year page:

### 1. Choose a Seminar Number

Seminars are numbered sequentially within each year:
- AIEPS Seminar #1
- AIEPS Seminar #2
- AIEPS Seminar #3
- etc.

### 2. Add Seminar Entry

Add the seminar details in the year's markdown file following this template:

```markdown
### AIEPS Seminar #3: Machine Learning for Climate Prediction

**Date:** 15 March 2027, 14:00 UTC  
**Format:** Online (Zoom)  
**Speaker:** Dr. Jane Smith, University of Example

#### Title

Advanced Neural Networks for Long-term Climate Forecasting

#### Abstract

This seminar explores recent advances in applying deep learning to climate prediction. We discuss how transformer architectures and physics-informed neural networks can improve long-term climate forecasts. The talk includes case studies on temperature prediction, extreme weather events, and uncertainty quantification.

**Topics covered:**
- Transformer models for climate time series
- Physics-informed constraints in climate models
- Handling uncertainty in predictions
- Real-world validation and deployment

#### Speaker Bio

Dr. Jane Smith is a climate scientist at the University of Example, specializing in machine learning applications for Earth system modeling. Her research focuses on integrating physical knowledge into deep learning models for improved climate predictions.

#### Registration

Please register at: [registration link]

Meeting link will be sent to registered participants.
```

### 3. Update Status After Completion

After a seminar is complete, you can:

1. Add a **Recording** section with link to the recording:

```markdown
#### Recording

The recording of this seminar is available at: [link]
```

2. Add **Resources** if materials were shared:

```markdown
#### Resources

- [Presentation Slides](link)
- [Code Repository](link)
- [Additional Materials](link)
```

## Front Matter Reference

| Field | Required | Description | Example |
|-------|----------|-------------|---------|
| `layout` | Yes | Page layout | `seminar` |
| `title` | Yes | Page title | `"AIEPS Seminars 2027"` |
| `year` | Yes | Year | `2027` |
| `status` | Yes | Status | `upcoming`, `completed`, or `planning` |
| `hero_title` | Yes | Main heading | `"AIEPS Seminars 2027"` |
| `hero_subtitle` | Yes | Subtitle | `"AI in Earth & Planetary Sciences Seminar Series"` |
| `description` | No | SEO description | Text for meta description |
| `contact` | No | Contact info | Markdown text |

## Seminar Entry Guidelines

### Required Information

Each seminar entry should include:
- **Number**: Sequential number (e.g., #1, #2, #3)
- **Title**: Descriptive title of the talk
- **Date**: Date and time (include timezone)
- **Format**: Typically "Online (Zoom)"
- **Speaker**: Name and affiliation
- **Abstract**: Clear description of the topic and key points
- **Speaker Bio**: Brief background of the speaker

### Optional Information

- Registration link
- Meeting link (can be sent separately to registrants)
- Prerequisites or recommended background
- Recording link (after the event)
- Slides or materials (after the event)

### Formatting Tips

- Use `###` for seminar titles to maintain hierarchy
- Use `####` for subsections (Title, Abstract, Speaker Bio, etc.)
- Use `**bold**` for field labels (Date:, Format:, Speaker:)
- Separate seminars with `---` horizontal rules
- Use bullet points for "Topics covered" lists

## Example: Complete Seminar Year Page

```markdown
---
layout: seminar
title: "AIEPS Seminars 2027"
year: 2027
status: upcoming
hero_title: "AIEPS Seminars 2027"
hero_subtitle: "AI in Earth & Planetary Sciences Seminar Series"
---

## About AIEPS Seminars

[Introduction text]

---

## 2027 Seminars

### AIEPS Seminar #1: Physics-Informed Neural Networks for Seismic Inversion

**Date:** 15 January 2027, 15:00 UTC  
**Format:** Online (Zoom)  
**Speaker:** Dr. John Doe, Geophysical Institute

#### Abstract

This talk explores...

#### Speaker Bio

Dr. John Doe is a geophysicist...

---

### AIEPS Seminar #2: Deep Learning for Satellite Imagery Analysis

[Next seminar details]

---

## How to Attend

[Registration instructions]
```

## Testing

After adding seminar content:

1. Run the local server: `bundle exec jekyll serve`
2. Visit `http://localhost:4000`
3. Check the AIEPS Seminar dropdown includes your year
4. Verify the page displays correctly
5. Check all links work
6. Test on mobile devices

## Tips

- Schedule seminars well in advance
- Send calendar invites to registrants
- Record seminars for those who can't attend live
- Archive recordings and materials for future reference
- Keep the format consistent across all seminars
- Include timezone information for global audience
- Consider different time zones when scheduling
