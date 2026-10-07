# Website Review – Multiscale Mechanics Group

*October 2026. Review of https://noyco5.github.io (code and live site), compared with about 7 strong lab websites. This file is excluded from the built site (see `exclude` in `_config.yml`).*

The site works, and its content is a good start: research sub-pages, a facilities page, and a list of 71 publications. The weak points are search ranking, leftovers from the Academic Pages template, very large images, and a home page that says very little.

## 1. Problems to fix

| # | Problem | Where |
|---|---|---|
| 1 | **Google is told to index template demo pages**: `/markdown/`, `/non-menu-page/`, `/terms/`, `/markdown_generator/`, `/talkmap/map.html`. Someone who searches for the lab could land on a demo page. | `_pages/markdown.md`, `non-menu-page.md`, `terms.md`, plus leftover folders |
| 2 | **`terms.md` is wrong about this site.** It is a template page that mentions Disqus comments and Google Analytics, and none of that is used here. | `_pages/terms.md` |
| 3 | **The cookie banner says "This site uses cookies to analyze traffic".** There is no analytics on the site, so the message is untrue. | `_includes/footer.html` |
| 4 | **Placeholder text is visible to visitors**: "*Detailed list of papers or a link back to the Publications page.*" | `gels.md`, `composites.md`, `spider-silk.md` |
| 5 | **A broken publication link** points to `href="..."` (the "Hydrogel mechanics across application domains" paper). | `publications.md` |
| 6 | **Typos in publications**: "polymer chain elasticity**e**", and "Peréz" is probably "Pérez". The page range "59–48" (EJM-A, 2014) can't be right, since a range can't run backwards. | `publications.md` |
| 7 | **Huge images**: the 3D-printer photo is 8 MB, the spider-silk button is 7 MB, and the home image is 5 MB. The site will load slowly, especially on phones, and Google ranks slow pages lower. | `images/` |
| 8 | **The home page has two `<h1>` headings, and one of them is empty** (`title: ""`). | `_pages/about.md` |
| 9 | **The `repository` setting still points to `academicpages/academicpages.github.io`**, and the README is still the template's. | `_config.yml` |
| 10 | **The accessibility widget loads its `@latest` version from a CDN.** An update to that library can break the site without warning. Pin a fixed version. | footer scripts |

## 2. SEO: helping people find the group on Google

What the live site sends to Google now:
- **Every page has the same description**: "Associate Professor, Materials Science…". It never mentions hydrogels, spider silk, or "Multiscale Mechanics Group".
- **The home page title is only "Multiscale Mechanics Group".** "Technion" and "Noy Cohen" are missing.
- **The structured data has `"sameAs": null`.** No Google Scholar or ORCID links are listed, and they are also commented out in the sidebar.
- **There is no preview image or description** for links shared on WhatsApp, LinkedIn, etc.
- **The research topic names exist only inside the button images**, so Google can't read them.

What to do, most important first:
1. **Google Search Console**: verify the site and submit `sitemap.xml`.
2. **Links to and from the site.** This matters most for searches on the PI's name. Link to the site from the Technion faculty page, Google Scholar, ORCID, ResearchGate and LinkedIn. Then turn the Scholar and ORCID links back on in `_config.yml`.
3. **A unique title and description for each page**, e.g. "Mechanics of Gels | Multiscale Mechanics Group – Noy Cohen, Technion".
4. **Structured data**: describe the group as a `ResearchOrganization` (address, logo, profile links) and the PI as a person profile (`ProfilePage` + `Person`). These are types Google actually uses.
5. **A default preview image** (1200×630) for link previews.
6. **Optional, bigger job**: give each paper its own page with `citation_*` tags so Google Scholar can index it. Academic Pages already supports this. Only host PDFs the publisher's license allows.
7. **Skip `llms.txt`.** Google says it doesn't use it, and AI search uses normal SEO.

**Custom domain:** github.io ranks fine. A Technion subdomain looks more official and is more likely to get links from the university. If you want one, decide **before** the SEO work, because changing the address later resets some of it (old URLs must redirect).

## 3. UI

- **Home page:** add a short hero line, 3 research tiles, the latest news, and featured papers. Right now it is one paragraph and a large picture captioned "created using NotebookLM".
- **Research page:** put real text titles and one-line summaries under the image buttons. The titles are written in the code but hidden as comments.
- **People page:**
  - Names are underlined, so they look like links, but they aren't clickable.
  - Add a PI card, and a short line about each person's research.
  - In the alumni list, add where each person went.
- **Publications:**
  - Group the papers by year.
  - Add filter buttons by topic (gels / silk / composites / dielectric elastomers).
  - Add DOI and PDF links, and mark featured papers.
- **Code cleanup:** move the many inline `style="..."` blocks into one CSS file. Some hard-coded colors (`#eee`, `rgba(0,0,0,.03)`) look wrong in dark mode.
- **Phone check:** test all pages at phone width; the facility cards use `min-width: 300px`.

## 4. Content

- **"Teaching" page:** it actually holds outreach videos, so rename it "Outreach" or add the real courses (they are commented out at the bottom of the page).
- **Join Us:** split it by level (M.Sc. / Ph.D. / postdoc / undergraduate projects), and keep it on the site even when there are no openings.
- **Contact details:** add the building, room, a map, and the department link.
- **Funding:** acknowledge funders (ISF, ERC, etc.) in the footer. Grants often require this.

## 5. New features (from other lab websites)

1. **News feed** (papers, awards, graduations, conferences), shown on the home page.
2. **Publications from a data file**: publications stored in one YAML/BibTeX file instead of hand-written HTML, which makes adding a paper easy. It could later fetch citations automatically from ORCID.
3. **Media and videos page**: research videos and journal covers.
4. **Automatic broken-link check**, run by GitHub Actions on every push.
5. **Analytics without cookies** (GoatCounter or Plausible), so you can see visitors without needing a cookie banner.

### Example lab websites

- **Bertoldi Group, Harvard**: https://bertoldi.seas.harvard.edu/ (open-positions box on the home page; alumni list with where each person went)
- **Daraio Group, Caltech**: https://www.daraio.caltech.edu/ (research image tiles, dated news, Videos and Facilities pages)
- **Tal Cohen Group, MIT**: https://tal-cohen.mit.edu (closest field; research videos; alumni grouped by degree)
- **Bao Group, Stanford**: https://baogroup.stanford.edu/ (publications filtered by year; journal-cover gallery)
- **Mechanics & Materials Lab, ETH**: https://mm.ethz.ch/ (news feed featuring student awards)
- **Complex Materials, ETH**: https://www.complex.mat.ethz.ch/ ("How to find us" page)

## Suggested order

1. **Quick fixes**: section 1, plus SEO steps 1–5.
2. **New home page, research page and people/alumni page.**
3. **Publications from a data file**, plus the news feed.
4. **Optional**: paper pages for Scholar, the media page, and a custom domain.
