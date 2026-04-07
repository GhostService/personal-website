# CLAUDE.md — Ghost's Personal Website

## Project overview

Personal website for Liam (GhostYT7582) to showcase projects, share links, and document changes. Hosted on Vercel via automatic deploys from the `main` branch on GitHub.

## Tech stack

- Pure HTML + CSS — no frameworks, no build tools, no package manager
- `style.css` is the single shared stylesheet for all pages
- No JavaScript (keep it that way unless there's a specific reason to add it)

## File structure

```
index.html      — Home / landing page
about.html      — About me
projects.html   — Projects showcase
socials.html    — Contact / socials links
changes.html    — Changelog
style.css       — Global styles (shared by all pages)
```

## Conventions

- Every page must include the same `<nav class="navbar">` block with links to all five pages
- Every page links to `style.css` via `<link rel="stylesheet" href="style.css" />`
- Use `<main class="hero">` as the page content wrapper
- Page titles follow the pattern `Page Name | Ghost's World` (or just `Ghost's World` for the home page)

## Design

- Dark theme: background `#0f0f0f`, primary text `#f5f5f5`
- Navbar background: `#111`
- Accent/hover color: `#4da3ff` (nav links on hover)
- Link color: `#f43535`
- Font: Arial, sans-serif
- Keep the aesthetic minimal and dark

## Deployment

Push to `main` on GitHub — Vercel auto-deploys. No build step required since this is static HTML/CSS.

## Adding a new project to projects.html

Add an `<a>` tag wrapping a `<p>` for the project name, followed by a description `<p>`:

```html
<a href="PROJECT_URL" target="_blank" rel="noopener noreferrer">
    <p>Project Name</p>
</a>
<p>Short description of the project.</p>
```

## Updating the changelog (changes.html)

Add a new entry at the top of the `<main class="hero">` section with the current date and bullet points for what changed.
