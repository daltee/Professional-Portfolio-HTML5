# Professional Semantic Portfolio

A five-page personal portfolio website built with semantic HTML5 for the **SWE2106 Internet Technologies and Web Design** (Activity 3 submission, Group C IT & Web Design). The site introduces a second-year Software Engineering student at Mbarara University of Science and Technology and demonstrates correct use of semantic elements, accessibility practices, tables, forms, and embedded media.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Project Structure](#project-structure)
3. [Pages](#pages)
4. [Semantic HTML5 Elements Used](#semantic-html5-elements-used)
5. [Accessibility Features](#accessibility-features)
6. [Navigation and Site Map](#navigation-and-site-map)
7. [Getting Started](#getting-started)
8. [Browser Support](#browser-support)
9. [Known Issues and Recommendations](#known-issues-and-recommendations)
10. [Future Improvements](#future-improvements)
11. [Credits](#credits)

---

## Project Overview

| Item | Details |
|------|---------|
| **Project name** | My Personal Portfolio |
| **Course** | SWE2106 – Internet Technologies and Web Design |
| **Assignment** | Activity 3: The Professional Semantic Portfolio |
| **Technologies** | HTML5 only (no CSS, JavaScript, or frameworks) |
| **Pages** | 5 (Home, About, Gallery, Data, Contact) |
| **Language** | English (`lang="en"`) |

**Goals**

- Apply semantic HTML5 structure (`header`, `nav`, `main`, `section`, `article`, `footer`).
- Provide consistent relative navigation across all pages.
- Use lists, tables, forms, images, and video appropriately and accessibly.

---

## Project Structure

```
portfolio/
├── index.html          # Home page
├── about.html          # About Me page
├── gallery.html        # Portfolio Gallery page
├── data.html           # Academic Results page
├── contact.html        # Contact form page
├── images/
│   ├── WireFrame.jpg
│   ├── site map.png
│   └── sample code.png
└── videos/
    └── AWS_presentation.mp4
```

---

## Pages

### 1. Home – `index.html`

- **Title:** My Personal Portfolio
- **Purpose:** Landing page that introduces the author and the site.
- **Content:** An `<article>` with a welcome heading, the author's professional identity (second-year Software Engineering student at Mbarara University of Science and Technology), and a "Current Focus" statement on internet technologies and web design.
- **Extras:** The only page with a `<meta name="description">` and `<meta name="viewport">`. Navigation uses `aria-label="Main navigation"` and `aria-current="page"` on the active link. The footer links to the Contact page.

### 2. About Me – `about.html`

- **Title:** Professional Portfolio - About Me
- **Purpose:** Background and expertise.
- **Content:**
  - **Career Milestones** – an ordered list (`<ol>`) in chronological order, from enrolling in SWE2106 to planning a first full-stack deployment.
  - **Technical Terminology** – a description list (`<dl>`, `<dt>`, `<dd>`) defining *Semantic HTML*, *Version Control (Git)*, and *Accessibility (a11y)*.

### 3. Portfolio Gallery – `gallery.html`

- **Title:** Gallery Page
- **Purpose:** Showcases project visuals and a video demonstration.
- **Content:**
  - **Project Screenshots** – three `<figure>` elements, each with an `<img>` (descriptive `alt` text, `width="350"`) and a `<figcaption>`:
    1. Initial wireframe for the portfolio architecture
    2. Structured sitemap showing user flow
    3. Clean, semantic code implementation
  - **Project Demonstration** – a `<video controls width="500">` using `videos/AWS_presentation.mp4`, with fallback text and a `<figcaption>`.

### 4. Academic Results – `data.html`

- **Title:** Professional Portfolio - Academic Results
- **Purpose:** Presents assessment results in tabular form.
- **Content:** A table with a `<caption>`, `<thead>`, `<tbody>`, and `<tfoot>`, using `scope="col"` and `scope="row"` for screen-reader support.

| Assessment Type | Topic Focus | Score / Status |
|-----------------|-------------|----------------|
| Lab 1 & 2 | Basic HTML & File Structures | 95% |
| Lab 3 & 4 | Semantic HTML5 & Accessibility | 88% |
| Activity 3 | The Professional Semantic Portfolio | Pending Evaluation |
| **Overall Average Grade** | | **91.5%** |

### 5. Contact – `contact.html`

- **Title:** Professional Portfolio - Contact Form
- **Purpose:** Lets visitors send a message about collaborations or inquiries.
- **Form fields:**

| Field | Element / Type | `id` / `name` | Required |
|-------|----------------|---------------|----------|
| Full Name | `input type="text"` | `fullName` | Yes |
| Email Address | `input type="email"` | `emailAddress` | Yes |
| Phone Number | `input type="tel"` (placeholder `+256 700 000000`) | `phoneNumber` | No |
| Your Message | `textarea` (5 rows) | `userMessage` | Yes |

- Each field has an explicitly associated `<label for="...">`.
- The form uses `method="POST"` with `action="#"` (see [Known Issues](#known-issues-and-recommendations)).

---

## Semantic HTML5 Elements Used

| Element | Where | Purpose |
|---------|-------|---------|
| `<header>` | All pages | Page title and navigation |
| `<nav>` + `<ul>` | All pages | Primary site navigation |
| `<main>` | All pages | Unique page content |
| `<article>` | Home | Self-contained introduction |
| `<section>` | About, Gallery, Data, Contact | Thematic grouping of content |
| `<footer>` | All pages | Copyright / closing links |
| `<ol>` | About | Chronological milestones |
| `<dl>`, `<dt>`, `<dd>` | About | Glossary of technical terms |
| `<figure>`, `<figcaption>` | Gallery | Captioned images and video |
| `<video>`, `<source>` | Gallery | Embedded demonstration |
| `<table>`, `<caption>`, `<thead>`, `<tbody>`, `<tfoot>` | Data | Structured results |
| `<form>`, `<label>`, `<input>`, `<textarea>`, `<button>` | Contact | User input |

---

## Accessibility Features

- `lang="en"` declared on every page's `<html>` element.
- Unique, descriptive `<title>` on each page.
- Descriptive `alt` text on all images.
- `aria-label` and `aria-current="page"` on the Home page navigation.
- Table `scope` attributes and a `<caption>` for screen-reader context.
- Explicit `<label for>` / `id` pairing on every form control.
- Native HTML5 validation (`required`, `type="email"`, `type="tel"`).
- Logical heading hierarchy (`h1` → `h2`, with `h3`/`h4` on Home).
- Fallback text inside the `<video>` element.

---

## Navigation and Site Map

All pages are linked with relative URLs, so the site works from any folder or hosting location.

```
                  index.html (Home)
                        |
   ┌──────────┬─────────┼──────────┬──────────┐
about.html  gallery.html  data.html  contact.html
```


## Browser Support

The site uses only standard HTML5 and works in current versions of Chrome, Edge, Firefox, and Safari. The video is MP4 (H.264), which is supported by all major browsers.

---


## Future Improvements

- Add a shared external stylesheet for layout, typography, colours, and responsive design.
- Connect the contact form to a backend or a form service so messages are actually delivered.
- Add a `<link rel="icon">` favicon and a skip-to-content link.
- Add `<track>` captions or a transcript for the video.
- Deploy the site (e.g. GitHub Pages) and add the live URL to this README.
- Extend the Home page with featured projects and links to GitHub.

---

## Credits

- **Author / Team:** Group C IT & Web Design
- **Institution:** Mbarara University of Science and Technology
- **Course:** SWE2106 – Internet Technologies and Web Design
- **Year:** 2026

&copy; 2026 Group C IT & Web Design. SWE2106 Activity 3 Submission.
