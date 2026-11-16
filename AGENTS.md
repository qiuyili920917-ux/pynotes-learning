# PyNotes — AI development guide

## Purpose and audience
PyNotes is a Traditional Chinese, beginner-friendly Python learning site. Each lesson explains one specific Python concept or common error with reproducible examples. Prioritize correctness and clarity over flashy effects. The site is a static website deployed with GitHub Pages; do not introduce a backend, paid APIs, build steps, or dependencies without approval.

## Source of truth and structure
- `index.html`: landing page, lesson cards, and navigation.
- `lessons/<slug>.html`: individual lessons. Slugs use lowercase ASCII and hyphens.
- `css/style.css`: the ONLY shared stylesheet; use existing classes and design tokens.
- `js/main.js`: shared interactions, including filtering and the mobile menu.
- `README.md`: setup, deployment, and extension instructions.
- `AGENTS.md`: these rules. Do not delete or override them.

## Visual and accessibility rules
- Use Traditional Chinese (`lang="zh-Hant"`) for instructional copy; preserve Python terms and code in English.
- Use the existing navy/teal palette and CSS custom properties. Reuse the header, breadcrumb, article layout, cards, and footer.
- Mobile-first, readable on 360px wide screens, visible keyboard focus, semantic HTML, descriptive link text, sufficient contrast.
- Do not add external CSS frameworks or remote fonts. Avoid inline styles and scripts.

## Mandatory lesson format
Each new lesson must follow this order and include matching anchor IDs:
1. `#overview` — what the error/concept means and when it occurs.
2. `#broken` — an **actually reproducible** incorrect code sample and expected error/output; do not fabricate traceback details.
3. `#why` — explanation in simple language.
4. `#fixed` — a correct, executable Python example.
5. `#practice` — one small exercise and a solution in `<details>`.
6. `#related` — links to related existing lessons and home.
Use `<pre><code>` for Python code and escape `<`, `>` and `&` in HTML. Examples should run in Python 3 without external libraries unless clearly stated. Distinguish syntax/runtime errors from conceptual misunderstandings.

## Adding a lesson: required workflow
1. Read this file and inspect `lessons/typeerror.html` and `css/style.css` first.
2. Pick an unused lowercase hyphenated slug (e.g. `zero-division-error`). Create `lessons/<slug>.html` using the same page shell, navigation, section IDs, and footer.
3. Write accurate beginner-friendly Traditional Chinese text. Include a broken example, the expected error/output, a corrected example, and a practice answer.
4. Add exactly one lesson card to `index.html` with a meaningful `data-keywords` attribute, and add the lesson to relevant related links.
5. Do not edit unrelated lesson content. Keep all internal links relative so GitHub Pages works under `/pynotes-learning/`.
6. Verify every internal link, keyboard navigation, 360px layout, and Python examples. Update README's lesson list if needed.
7. In your completion summary, list changed files, the new lesson URL, and the checks performed. Never claim checks you did not perform.

## Editing safeguards
- Preserve existing URLs and anchors unless explicitly asked to migrate them.
- Do not silently change the meaning of code examples.
- No credentials, secrets, tracking scripts, or copied proprietary course materials.
- When uncertain about technical accuracy, flag the uncertainty and request clarification.

## Acceptance checklist
- [ ] All required lesson sections and IDs exist.
- [ ] Broken and fixed Python snippets behave as described.
- [ ] Homepage card and related links work with relative paths.
- [ ] Header, footer, typography, and CSS classes match existing pages.
- [ ] Search/filter still works and keyboard focus is visible.
- [ ] New page reads correctly on mobile and desktop.
- [ ] README and GitHub Pages deployment remain usable.

## Example future AI task
"Read AGENTS.md and the existing TypeError lesson. Add a ZeroDivisionError lesson using the required sections, add a searchable card to the homepage, link it from related lessons, and report what you tested. Do not change existing layouts or unrelated content."
