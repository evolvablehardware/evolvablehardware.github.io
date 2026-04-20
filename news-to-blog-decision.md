# Decision: Blog Plugin over News Pages

**Date:** 2026-02-23
**Decision:** Use the MkDocs Material Blog plugin instead of the manual News pages for announcements and updates.

## Rationale

Both the Blog plugin and the News section serve the same role (announcing papers, grants, events, etc.), so maintaining both is redundant. After comparing the two workflows side-by-side, the Blog plugin was chosen because:

1. **Less judgment required** — each post is a self-contained file dropped into `docs/blog/posts/`. No decisions about which year file to edit, which month section to insert under, or what position to place the entry in.
2. **Less manual maintenance** — ordering, archive pages, category pages, and the listing page are all auto-generated. News pages require manual organization by year/month and separate updates to the landing page.
3. **Simple "copy and edit" workflow** — a novice can copy an existing post, rename it, update the front matter and content, and push. The steps are mechanical.
4. **Lower long-term maintenance burden** — no `.nav.yml` updates needed for new years, no manual index page curation.

## Trade-offs Accepted

- **Front matter is required** — each post needs a `---` block with `date`, `categories`, and `authors`. A typo in the author name or an invalid date format will break the build.
- **Authors file must be maintained** — `docs/blog/.authors.yml` must contain an entry for each author with `name`, `description`, and `avatar` fields. New authors must be added there before they can be referenced in a post.
- **`<!-- more -->` marker** — must be preserved in each post to separate the excerpt from the full body.

## How to Create a Blog Post

1. Open `docs/blog/posts/` and find an existing post to use as a template.
2. Copy it and rename to `YYYY-MM-DD-short-title.md`.
3. Update `date:` in the front matter to the post date.
4. Update `categories:` as appropriate (e.g., `Publications`, `Grants`, `Student Research`).
5. Ensure `authors:` matches a key in `docs/blog/.authors.yml`.
6. Replace the `#` title, intro paragraph, and body content.
7. Keep `<!-- more -->` between the excerpt and the full body.
8. Commit and push.

## Migration Status

- **Blog plugin:** Active, configured in `mkdocs.yml`.
- **News section (`docs/news/`):** Still present. Existing news entries should be migrated to blog posts and the news section removed once migration is complete.
