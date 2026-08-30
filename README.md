# Department of Computer Engineering — Ahmadu Bello University, Zaria

A modern, professional, fully responsive static website redesign for the
Department of Computer Engineering, Ahmadu Bello University (ABU), Zaria,
built for the **COEN 554 (Web Programming)** examination.

This is the **corrected revision** of the project, updated against a
supplied corrections document and a supplied staff directory (extracted
from the departmental Student Handbook).

## Project Purpose

This project redesigns the departmental website into a professional,
accessible, mobile-friendly experience while preserving verified
departmental information, correcting mismatched content inherited from
other departments, and presenting the department's real uploaded
photographs (building, current and former Heads of Department,
laboratories, and a smart classroom).

## Technologies Used

- **HTML5** — semantic markup across 16 pages
- **CSS3** — a single external stylesheet (`assets/css/style.css`) using
  CSS variables, Flexbox, CSS Grid, media queries, transitions and
  CSS-only interactivity (`:hover`, `:focus-within`, `:checked`,
  `<details>`/`<summary>`)
- **JSON** — structured departmental data (`data.json`)
- **JSON-LD** — structured data (`schema.org`) embedded on key pages
  (Home, B.Eng., Leadership, Contact)

**No JavaScript, no CMS, no static site generator, and no CSS framework
were used anywhere in this project.**

## How to Open This Project in VS Code

1. Open Visual Studio Code.
2. Choose **File → Open Folder…** and select the `abu-computer-engineering`
   folder.
3. Install the **Live Server** extension if you don't already have it.
4. Right-click `index.html` and choose **Open with Live Server**
   (or simply double-click `index.html` to open it directly in a browser).
5. Use the navigation bar to move between pages. On mobile-width screens,
   use the menu icon (a CSS-only toggle — no JavaScript) to open navigation.

## Folder Structure

```
abu-computer-engineering/
├── index.html
├── about.html
├── programme-outcomes.html      (merged Programme Outcomes & Educational Objectives)
├── academic-programmes.html
├── beng.html
├── pgd.html
├── msc.html
├── phd.html
├── research.html
├── staffs.html                  (renamed from "people")
├── leadership.html
├── students.html
├── news-events.html
├── admissions.html
├── facilities.html
├── contact.html
├── data.json
├── README.md
└── assets/
    ├── css/
    │   └── style.css            (the ONLY stylesheet — all CSS lives here)
    ├── images/
    │   ├── department/          (building photograph)
    │   ├── leadership/          (current + former HOD photographs)
    │   ├── facilities/          (Smart Classroom lecture hall)
    │   ├── laboratories/        (Concept-to-Product Lab, C2P Tech Hub, Digital Electronics Lab)
    │   ├── branding/            (department logo)
    │   └── events/
    └── documents/
```

## Summary of Corrections Applied in This Revision

- **Navigation simplified**: Contact Us moved out of the main nav into a
  prominent footer call-to-action; Community & Consultancy page removed
  entirely; About, Staffs, Students and Facilities dropdown submenus
  simplified or removed; About's History/Philosophy/Mission & Vision/
  Objectives remain as content on the About page but are no longer
  separate nav items.
- **Programme Outcomes and Programme Educational Objectives** merged into
  a single page (`programme-outcomes.html`) using the exact required
  PO1–PO12 and PEO1–PEO5 wording, verbatim.
- **"People" renamed to "Staffs"** (`staffs.html`), and "Heads of
  Department" removed from its dropdown (still reachable via the
  Leadership page link).
- **Staff Directory populated with real data** extracted from the
  supplied Student Handbook staff directory: 23 academic staff members
  with rank and area of specialization, 4 technical staff, and 3
  administrative staff. No staff photographs are shown in the general
  directory, per departmental policy.
- **Staff offices** are noted as being located on the **second floor**,
  alongside the departmental library.
- **Facilities page rebuilt** as a single consolidated page (no
  dropdown/sub-pages) organised by floor:
  - **Ground Floor** — Laboratories (Concept-to-Product Laboratory, C2P
    Tech Hub, Digital Electronics and Microprocessor Laboratory), each
    shown with real photographs.
  - **1st Floor** — 300, 400 and 500 Level Lecture Halls, including a
    real photograph of the Smart Classroom.
  - **2nd Floor** — Departmental Library and Staff Offices.
  - **3rd Floor** — Postgraduate Lecture Hall.
  - The Mechanical Workshop section has been removed from this page per
    the corrections.
- **HOD titles corrected**: the current Head of Department is now shown
  as *Engr. Dr. Basira Yahaya*; former Heads of Department are shown as
  *Engr. Prof. E. A. Adedokun* and *Engr. Prof. M. B. Muazu*.
- **Department logo** now used in the header and footer brand mark,
  replacing the earlier text placeholder.
- **Header height slightly reduced** and the old top utility bar removed.
- **Student Directory section removed** from the Students page (sample
  data no longer shown); all other student resources (Academic Advisers,
  SWEP, SIWES, Final Year Projects, Examination Guidelines, Timetable,
  Student Handbook) remain on a single Students page.
- **Home page Quick Links section removed.**
- **Footer** no longer states "This website is a COEN 554 academic
  redesign project."

## Image Organization

Real, uploaded departmental photographs are used throughout:

- **`assets/images/department/department-building.jpg`** — the front of
  the Department of Computer Engineering building.
- **`assets/images/leadership/hod-current-basira-yahaya.jpg`** — the
  current Head of Department, Engr. Dr. Basira Yahaya.
- **`assets/images/leadership/former-hod-e-a-adedokun.jpg`** and
  **`former-hod-m-b-muazu.jpg`** — former Heads of Department, Engr.
  Prof. E. A. Adedokun and Engr. Prof. M. B. Muazu.
- **`assets/images/laboratories/concept-to-product-lab.jpg`**,
  **`c2p-tech-hub.jpg`** and
  **`digital-electronics-microprocessor-lab.jpg`** — real laboratory
  photographs supplied for this revision.
- **`assets/images/facilities/smart-classroom-lecture-hall.jpg`** — a
  real photograph of the department's Smart Classroom lecture hall.
- **`assets/images/branding/department-logo.png`** — the official
  department logo, used in the header and footer.

No stock, Unsplash, Pexels or AI-generated images were used. Staff
photographs are intentionally **not** shown in the general Staff
Directory (`staffs.html`) — only the Leadership page displays HOD
photographs, per the departmental photograph policy.

## JSON Data

`data.json` holds structured department data (programmes, Programme
Outcomes, Programme Educational Objectives, research groups, leadership,
academic/technical/administrative staff, news, events, building layout
and facilities). It is provided as valid structured data per the
examination requirement; visible page content is written directly into
the HTML rather than being loaded by script, since **no JavaScript is
used anywhere in this project.**

## JSON-LD

Valid `application/ld+json` structured data blocks (schema.org
`CollegeOrUniversity`, `Course`, `Person`, `EducationalOrganization`) are
embedded on `index.html`, `beng.html`, `leadership.html` and
`contact.html`. JSON-LD is structured data, not JavaScript, and is
explicitly permitted by the examination brief.

## Responsive Design

The layout is fully responsive using CSS Grid, Flexbox and media queries
at 980px, 860px, 760px and 640px breakpoints, covering desktop, laptop,
tablet and mobile phone viewports. Mobile navigation, dropdown submenus
and the FAQ-style accordions on `beng.html` all work without any
JavaScript, using the checkbox hack and native `<details>`/`<summary>`.

## CSS-Only Interactivity

- **Mobile navigation** — a hidden checkbox + label toggle
  (`.nav-toggle-checkbox` / `.nav-toggle-label`)
- **Dropdown menus** — `:hover` and `:focus-within` on `<li>` elements
- **Accordion (B.Eng. requirements)** — native `<details>`/`<summary>`
- **Tabs (News & Events)** — radio-input CSS tabs

## No JavaScript

There are **zero** `.js` files, zero `<script>` tags other than
`application/ld+json`, and zero inline event handlers
(`onclick`, `onload`, etc.) anywhere in this project.

## No CMS / No Static Site Generator / No CSS Framework

This project uses hand-authored HTML5 and CSS3 only. No WordPress,
Jekyll, Hugo, Next.js, Bootstrap, Tailwind or any comparable tool was
used to produce any file in this project.

## External CSS Only

Every page links to a single external stylesheet:

```html
<link rel="stylesheet" href="assets/css/style.css">
```

There are no `style=""` attributes and no `<style>` blocks anywhere in
the HTML.

## Content Accuracy

Where official departmental facts (exact course codes, HOD tenure dates,
current fees, event dates, etc.) were not present in the supplied source
material, this project does **not** invent them. Instead, pages state
that the information is *"to be updated"* or direct the reader to
*"contact the department for current information."* Content inherited
from unrelated departments (e.g. Veterinary Medicine, Metallurgical &
Materials Engineering, Production Engineering) has been removed
entirely.

---

## COEN 554 REQUIREMENT COMPLIANCE

- [x] HTML5
- [x] CSS3
- [x] External CSS only
- [x] NO inline CSS
- [x] NO `style=""` attributes
- [x] NO internal `<style>` blocks
- [x] Responsive design
- [x] Semantic HTML
- [x] CSS-only interactivity
- [x] JSON
- [x] JSON-LD
- [x] At least three linked pages (16 pages, fully linked)
- [x] Organized folder structure
- [x] NO JavaScript
- [x] NO `.js` files
- [x] NO inline JavaScript
- [x] NO external JavaScript
- [x] NO DOM manipulation
- [x] NO Bootstrap
- [x] NO Tailwind
- [x] NO React
- [x] NO Vue
- [x] NO Angular
- [x] NO CMS
- [x] NO static site generator
- [x] Professional UI/UX
- [x] Home
- [x] About
- [x] Academic Programmes
- [x] Staff Directory (Staffs)
- [x] News & Events
- [x] Admissions
- [x] Contact Us
- [x] Research & Innovation
- [x] Leadership
- [x] Facilities
- [x] Real departmental building image
- [x] Current HOD image (Engr. Dr. Basira Yahaya)
- [x] Former HOD images (Engr. Prof. E. A. Adedokun, Engr. Prof. M. B. Muazu)
- [x] Real laboratory and lecture hall images
- [x] Correct floor arrangement (Ground: Labs, 1st: 300/400/500L Halls, 2nd: Library & Staff Offices, 3rd: PG Hall)
- [x] Exact PO1–PO12 and PEO1–PEO5 wording
- [x] Real staff directory data from supplied Student Handbook
