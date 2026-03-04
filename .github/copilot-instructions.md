# Copilot instructions for microsoft-365-community

Purpose: help an AI coding agent be immediately productive in this repository (authoring content, validating builds, and following repo conventions).

## Big picture
- This is a documentation/content repo for Microsoft 365 Community; the site content lives in `Community/` (markdown + YAML TOCs).
- Site is built with DocFX (v3) configured in `Community/docfx.json`. Output folder: `microsoft-365-community` (see `.openpublishing.publish.config.json`).
- Presentation templates come from `_themes` (sourced from `https://github.com/Microsoft/templates.docs.msft` via the open publishing pipeline).

## Key files & locations (quick reference)
- `Community/` — all articles, `media/`, `includes/`, and TOC files (`TOC.yml`, `index.yml`, `index-mm4m365.yml`).
- `Community/docfx.json` — DocFX build config (markdig markdown engine; excludes README/LICENSE by default).
- `.openpublishing.publish.config.json` — publishing pipeline integration; PRs can produce preview builds.
- `Community/article-template.md` — canonical frontmatter and article structure (use as a starting point).
- `frontmatter.json` & `.vscode/settings.json` — frontmatter helpers and markdownlint rules (MD028 disabled; MD025 front_matter_title configured).

## Conventions you must follow (concrete rules)
- Frontmatter: every article should include the `ms.*` metadata keys. Common fields: `title`, `ms.date`, `author` (GitHub handle), `ms.topic` (e.g., `concept-article`, `overview`), `ms.localizationpriority`, `description`, `ms.collection: M365Community`.
  - Example (from `Community/article-template.md`):
    ```yaml
    ---
    title: My article
    ms.date: 1/6/2026
    author: your-github
    ms.topic: concept-article
    ms.localizationpriority: Low
    description: One-line description
    ms.collection: M365Community
    ---
    ```
- Use `includes/` for shared fragments via the `[!INCLUDE [name](includes/file.md)]` pattern (e.g., `content-disclaimer.md`).
- Navigation: update `Community/TOC.yml` (and `index.yml` or `index-mm4m365.yml` where appropriate) when adding or moving pages.
- Media: put images under `Community/media/` and reference them with relative paths.
- Filenames: prefer lower-case, hyphen-separated names that match TOC `href` entries.
- Do not change `_themes` in this repo — that comes from the templates repo and is managed by the publishing pipeline.

## Developer workflows (what works locally and in CI)
- Local preview: build the site with DocFX v3 (install docfx v3 tool). Typical commands run inside `Community/`:
  - `docfx build` (build)
  - `docfx serve _site` or `docfx serve` (serve locally; check docfx v3 docs)
- Validation: rely on the repo's markdownlint editor settings; there are no repository-level unit tests. PRs run the open publishing preview pipeline (see `.openpublishing.publish.config.json`).
- PR process: open a PR, ensure CLA-bot passes (contributors may need to sign a CLA), and confirm preview build renders as expected.

## Patterns to call out for automation or fixes
- When adding pages, remember to: add frontmatter, place content in `Community/`, add the page to the appropriate TOC, and include images in `Community/media/`.
- When modifying site templates or the look-and-feel, open an issue first — `_themes` is external and template changes are coordinated upstream.

## What I could not discover automatically / ask the maintainers
- Exact DocFX v3 install command preferred by the team and any recommended flags for local builds.
- Any additional CI checks (beyond the open publishing preview) that run in your upstream pipeline.

If anything above is incomplete or there are preferred local commands/flags you want me to add, tell me which area to clarify and I will update this file.