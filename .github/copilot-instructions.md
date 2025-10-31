# Copilot Instructions for Point-of-Care-AI-Lab.github.io

This repository is a Jekyll-based academic/lab website using the al-folio theme. Follow these guidelines to be productive as an AI coding agent:

## Architecture & Structure

- **Jekyll site**: Content is organized in collections (`_posts`, `_news`, `_projects`), data files (`_data/`), layouts (`_layouts/`), and includes (`_includes/`).
- **Theme**: Uses the [al-folio](https://github.com/alshedivat/al-folio) theme, with customizations in `_config.yml`, `_sass/`, and various `.liquid` templates.
- **CV Generation**: CV page sources data from either `assets/json/resume.json` (JSON Resume standard) or `_data/cv.yml` (YAML fallback).
- **Publications**: Bibliography managed in `_bibliography/papers.bib`, rendered via Jekyll Scholar and customized in `_pages/publications.md`.
- **Collections**: Custom collections (e.g., news, projects) are defined in `_config.yml` and have corresponding folders and landing pages in `_pages/`.

## Developer Workflows

- **Build & Serve**: Use Jekyll commands (`bundle exec jekyll serve`) or Docker (`docker-compose up`) for local development. See `INSTALL.md` for details.
- **Quality Checks**: Formatting is enforced with Prettier; broken links checked with Lychee; accessibility tested manually with Axe. See GitHub Actions config for automation.
- **Customization**: Theme colors and styles are set in `_sass/_themes.scss` and `_sass/_variables.scss`. Social media previews require `serve_og_meta: true` and `og_image` in `_config.yml`.

## Project-Specific Patterns

- **Liquid Templates**: Reusable components in `_includes/` (e.g., `figure.liquid`, `citation.liquid`).
- **Data-Driven Pages**: Pages like CV, repositories, and people use YAML/JSON data from `_data/`.
- **Publication Extras**: Add fields like `pdf`, `code`, `video`, etc., to BibTeX entries for richer publication pages.
- **Related Posts**: Controlled via `related_blog_posts` in `_config.yml` and per-post front matter.
- **Social Previews**: Configure Open Graph images per page or site-wide using `og_image`.

## Integration Points

- **GitHub Stats**: Edit `_data/repositories.yml` to display user/repo info on `/repositories/`.
- **External Libraries**: MathJax, Chart.js, Mermaid, and TikZJax are supported for math/code/diagram rendering.
- **Bootstrap**: Used for grid layouts in posts and project pages.

## Key Files & Directories

- `_config.yml`: Main site configuration, collections, theme options.
- `_data/`: YAML files for coauthors, CV, repositories, socials, venues.
- `_bibliography/papers.bib`: BibTeX bibliography for publications.
- `_includes/`, `_layouts/`: Liquid templates for reusable components and page layouts.
- `_sass/`: Theme and style variables.
- `assets/`: Static files (images, PDFs, JSON resume).
- `docker-compose.yml`, `Gemfile`: Build and dependency management.

## Example: Adding a Publication

1. Add BibTeX entry to `_bibliography/papers.bib`.
2. Optionally add PDF to `assets/pdf/` and reference in BibTeX `pdf` field.
3. Customize display in `_pages/publications.md` or via Jekyll Scholar config in `_config.yml`.

## Example: Customizing Theme Color

- Edit `--global-theme-color` in `_sass/_themes.scss`.
- Add new colors in `_sass/_variables.scss`.

---

For more details, see `README.md`, `INSTALL.md`, and `CUSTOMIZE.md`.

---

**Feedback:** If any section is unclear or missing, please specify which workflows, conventions, or integration points need more detail.
