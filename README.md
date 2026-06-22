# Luke T Barrett – Research Website

A personal academic website built with [Quarto](https://quarto.org). All content lives in `index.qmd`.

## Prerequisites

Install [Quarto](https://quarto.org/docs/get-started/) before running any commands below.

---

## Rendering the site

```powershell
quarto render
```

Output goes to `_site/`. Open `_site/index.html` in a browser to preview locally.

To preview with live reload on save:

```powershell
quarto preview
```

---

## Updating content

All editable content is in [index.qmd](index.qmd). The sections map to the navbar links:

| Section | Heading in `index.qmd` |
|---|---|
| About | `## About` |
| Publications | `## Publications` |
| Grants | `## Grants` |
| Media | `## In the media` |
| Education | `## Education` |

### Adding a publication

Copy an existing entry and paste it at the top of the numbered list under `## Publications`. Each entry follows this pattern:

```markdown
1. Author A, **Barrett LT**, Author B (YEAR) Title of paper. [*Journal Name*](https://doi.org/...). Open access.
```

For papers without open access, link to a local PDF instead:

```markdown
[[pdf]](pdfs/filename.pdf)
```

Or link to request a copy by email:

```markdown
[[email for pdf]](mailto:l.barrett@deakin.edu.au)
```

### Adding a grant

Add a new block under `## Grants`, keeping reverse chronological order:

```markdown
**YEAR**
*Title*: Full grant title
*Funder*: Funding body and project number
*Role*: Your role
```

### Adding a media item

Under `## In the media`, add a new heading and bullet list:

```markdown
**Short description of the story**

- [Outlet name](https://url-to-article)
```

### Updating profile details

The bio text, title, and affiliation are in the `## About` section. The profile photo is `images/forestprofile.jpg` — replace that file to update the photo (keep the same filename, or update the path in the image tag near the top of `index.qmd`).

---

## Adding a PDF

Place the PDF in the `pdfs/` folder, then reference it in the publication entry:

```markdown
[[pdf]](pdfs/your-filename.pdf)
```

---

## Deploying

After rendering, commit and push all changes including the `_site/` folder:

```powershell
git add .
git commit -m "your message"
git push
```

The site is hosted via GitHub Pages. The `CNAME` file sets the custom domain — do not delete it.
