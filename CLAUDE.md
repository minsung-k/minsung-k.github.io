# CLAUDE.md — Minsung Kang's academic homepage

Jekyll site on GitHub Pages (https://minsung-k.github.io), based on the MIT-licensed
[luost26/academic-homepage](https://github.com/luost26/academic-homepage) template.
Pages: Home and Publications only (no Blog or Showcase).

## Publishing (important)
- GitHub Pages builds from **`main`**. Pushing only the feature branch does NOT update the live site.
- Develop on the branch named in the session instructions, then also push the same commits to `main`
  (`git push origin HEAD:main`). Before editing, `git fetch` and fast-forward: the owner often edits
  files directly on GitHub (uploads, news items) and those commits must not be overwritten.
- Don't open a new PR unless asked; an existing PR for the branch updates automatically on push.
- Build check: `bundle exec jekyll build` (gems may need `bundle config set --local path <scratchpad>`;
  don't commit `_site/`, `.bundle/`, `Gemfile.lock`). Cloud sandbox has no CDN access, so a local render is unstyled —
  verify content in `_site/*.html`, and say the live styling is unverified.

## Where things live
- `_data/profile.yml` — name, positions, email, links (`gscholar`, `github`, `cv_link`), `short_bio`
  (welcome text), `job_market` (highlighted full-width line), `portrait_url`, `education`, `experience`, `awards`.
  Education/experience entries take `logo:` (image in `assets/images/badges/`; a generic building icon shows if absent).
  `logo_wide: true` swaps the name for a wordmark logo.
- `_news/*.md` — one file per item. Fields: `date` (sort), `date_text` (shown, e.g. "Aug. 2026"), `emoji`, `text`.
  Style follows yewon-kim.com: bold date, emoji, ONE short line. Newest first.
- `_publications/*.md` — `status`: `published` | `review` | `preparation` | `talk` (sections on the Publications page).
  Other fields: `title`, `authors` (own name is `Minsung Kang`, bolded via `_data/authors.yml`; co-authors as initials),
  `pub`, `pub_pre`, `pub_post`, `pub_date`, `links`, `rank` (order inside non-published sections),
  `selected: true` (shows on Home), `cover:` (image in `assets/images/pubs/`), `type`/`badge` (small tags),
  `award:` (gold trophy line, e.g. best paper / finalist).
- `assets/cv/Minsung_Kang_CV.pdf` — linked from the profile card. Replace the file to update the CV.
- `_includes/widgets/` — `profile_card.html`, `experience_card.html` (Education | Experience + Honors & Awards),
  `news_card.html`, `publication_item.html`, `publication_card.html`.

## Owner preferences
- A paper and its conference-presentation entry share the same cover image.
- Welcome text should be easy to read: short intro, the two research areas as a bulleted list,
  and the highlighted job-market line on its own row (seeking faculty and postdoctoral positions; graduation July 2027).
- Education/Experience cards: date on the same line as the institution, role/degree on the next line; keep default font sizes.
- Use the CV as the source of truth for facts. If unsure, leave a `TODO` comment instead of guessing.
- Replacing an image: use a NEW file name (browser caching), and update every file that references the old one.

## Privacy and cautions
- Never publish the owner's phone number (it is in some CV versions; the current CV PDF has none).
  The earlier CV with the number remains in git history.
- The sandbox cannot reach external sites (e.g. school/company/lab sites): ask the owner to upload logos and figures.
- Don't rewrite git history or force-push without explicit approval.
