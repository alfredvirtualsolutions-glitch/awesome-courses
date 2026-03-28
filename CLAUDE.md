# CLAUDE.md

This file provides guidance for AI assistants working with the `awesome-courses` repository.

## Repository Overview

This is a curated list of high-quality university CS courses that make their materials (assignments, lectures, notes, readings, exams) freely available online. It is part of the [awesome](https://github.com/sindresorhus/awesome) ecosystem.

The repository is a **pure content/Markdown project** — there is no application code, build system, test suite, or package manager.

## File Structure

```
awesome-courses/
├── README.md        # The main curated list (the entire product)
├── CONTRIBUTING.md  # Contribution guidelines for submitters
├── CLAUDE.md        # This file
└── .gitignore       # Ignores .DS_Store
```

## README.md Structure

`README.md` is the core of the project. It is organized as follows:

1. **Header** — Title, badges, introduction paragraph
2. **Table of Contents** — Links to each category section
3. **Legend** — Icon key for the four material-type indicators
4. **Courses** — Organized into topic sections, each listing courses alphabetically

### Course Categories

- Algorithms
- Artificial Intelligence
- Computer Graphics
- CS Theory
- Introduction to CS
- Machine Learning
- Misc
- Programming Languages / Compilers
- Security
- Systems
- Statistics / Regression

### Course Entry Format

Each course follows this exact Markdown pattern:

```markdown
- [COURSE_CODE](URL) **Course Title** *University Name* <icon(s)>
  - Short description of the course.
  - [Material Type](URL)
  - [Material Type](URL)
```

**Icons** — inline `<img>` tags referencing GitHub emoji CDN assets:

| Emoji unicode | Meaning | Alt text |
|---|---|---|
| `1f4f9` | Lecture Videos | `Lecture Videos` |
| `1f4dd` | Lecture Notes | `Lecture Notes` |
| `1f4bb` | Assignments | `Assignments` |
| `1f4da` | Readings | `Readings` |

Icon template (copy-paste as needed):
```html
<img src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4f9.png" width="20" height="20" alt="Lecture Videos" title="Lecture Videos" />
<img src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4dd.png" width="20" height="20" alt="Lecture Notes" title="Lecture Notes" />
<img src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4bb.png" width="20" height="20" alt="Assignments" title="Assignments" />
<img src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4da.png" width="20" height="20" alt="Readings" title="Readings" />
```

## Contribution Conventions

These rules are documented in `CONTRIBUTING.md` and must be respected when adding or editing courses:

1. **Alphabetical order** — Within each category, entries must be sorted alphabetically by course code/title (e.g., `CSCE 48` comes after `CS 240`).
2. **Free materials only** — Only include courses where the listed materials are freely accessible online.
3. **No popular MOOCs** — Courses widely aggregated by services like ClassCentral (e.g., Coursera, MIT OpenCourseWare) are intentionally excluded. Focus on relatively unknown university courses.
4. **Use correct icons** — Only include icons for material types that are actually available at the linked URL.
5. **No trailing whitespace or spurious blank lines** — Keep the Markdown clean and consistent with surrounding entries.

## Development Workflow

This repository has no build or test commands. Workflow is purely git-based:

```bash
# Make changes to README.md
git add README.md
git commit -m "Add <Course Name> to <Category>"
git push origin <branch>
```

### Branch Conventions

- `master` — Production branch containing the live curated list
- Feature branches follow the pattern `claude/<description>` for AI-assisted changes

## Key Notes for AI Assistants

- **Do not reorder sections** — The category order in the Table of Contents and in the body must stay in sync.
- **Do not invent course URLs** — Only use URLs that are verifiably present in the existing file or provided by the user.
- **Preserve icon formatting exactly** — The `<img>` tags use specific CDN URLs and dimensions; do not alter them.
- **Alphabetization is critical** — Misplaced entries are the most common contribution error; always verify sort order before committing.
- **Indentation uses tabs** — Course sub-bullet lines (description, material links) use a single tab for indentation.
- **README.md is large** — The file is ~70,000 tokens. When editing, use targeted reads with `offset`/`limit` and surgical `Edit` operations rather than rewriting the whole file.
