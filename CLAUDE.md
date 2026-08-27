# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A Jekyll site (GitHub Pages) hosting a non-technical course, "Data Lakehouse Fundamentals for Finance SMEs" — aimed at a finance subject-matter expert (not an engineer) leading a data lakehouse build at an investment firm. It is a curated reading list with commentary, not original explainer prose: each module page is "what you'll learn / why it matters for this project / curated external links," and the value is in that framing plus vetted links, not in re-explaining concepts from scratch.

## Commands

```bash
bundle install          # install gems (first time / after Gemfile changes)
bundle exec jekyll build          # build the static site into _site/
bundle exec jekyll serve          # build + serve locally at http://127.0.0.1:4000, watches for changes
bundle exec jekyll serve --port 4321   # serve on a specific port
```

There are no tests or linters in this repo.

## Architecture

- Every top-level `module-*.md` and `capstone.md` file is a standalone Jekyll page (front matter: `title`, `nav_order`), rendered into the sidebar nav by the `just-the-docs` theme (`_config.yml`) purely from `nav_order` — there is no `_config.yml` nav list to hand-maintain. `index.md` (`layout: home`) is the landing page and links to each module.
- Content per module is intentionally minimal and link-heavy (What you'll learn / Why it matters / Resources). When adding or editing a module, preserve that structure and tone — do not expand it into original explainer prose, and keep the audience non-technical (Module 8, SQL, is deliberately the one exception that goes more hands-on).
- Theme: `just-the-docs` is installed as a real gem (`Gemfile`) via `theme: just-the-docs` in `_config.yml`, not `remote_theme`. This is a deliberate choice, not the default GitHub Pages setup — `just-the-docs` is not in GitHub's native-Pages theme allowlist, so the site cannot rely on GitHub's built-in branch-based Jekyll build. Deployment instead goes through `.github/workflows/pages.yml`, which builds with `ruby/setup-ruby` + `bundle exec jekyll build` and deploys via `actions/deploy-pages`. On push to `main`, this is what actually publishes the site — the GitHub repo's Settings → Pages → Source must be set to "GitHub Actions" (not "Deploy from a branch") for it to take effect.
- The current branch is `master`, not `main` — the workflow trigger (`branches: ["main"]`) won't fire until either the workflow is updated or the default branch is renamed. This is an open item, not an oversight to silently fix.
- Versioning strategy for releases/deploys has not been decided yet — check with the user before assuming a scheme (e.g. tags, changelog) when touching CI.
