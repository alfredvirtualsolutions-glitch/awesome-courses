# CLAUDE.md — AI Assistant Guide for awesome-courses

## Repository Overview

This is **awesome-courses** — a curated list of high-quality university CS courses that make their materials (lectures, assignments, notes, exams) freely available online. The entire content lives in a single `README.md` file structured as a GitHub-flavored Markdown document. There is no application code, build system, or package manager.

## File Structure

```
awesome-courses/
├── README.md        # The entire curated course list (~70k tokens)
├── CONTRIBUTING.md  # Contribution guidelines for new entries
├── .gitignore       # Only ignores .DS_Store
└── CLAUDE.md        # This file
```

## Course Entry Format

Each course entry follows this exact structure:

```markdown
- [COURSE_CODE](URL) **Course Title** *University Name* <icons...>
  - Brief description of the course.
  - [Lecture Videos](URL)
  - [Lecture Notes](URL)
  - [Assignments](URL)
  - [Readings](URL)
```

### Icon Legend

Icons are inline `<img>` tags from GitHub's CDN. Use copy-paste from existing entries:

| Icon Unicode | Meaning |
|---|---|
| `1f4f9` | Lecture Videos |
| `1f4dd` | Lecture Notes |
| `1f4bb` | Assignments / Labs |
| `1f4da` | Readings |

Standard icon HTML (copy as-is):
```html
<img src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4f9.png" width="20" height="20" alt="Lecture Videos" title="Lecture Videos" />
<img src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4dd.png" width="20" height="20" alt="Lecture Notes" title="Lecture Notes" />
<img src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4bb.png" width="20" height="20" alt="Assignments" title="Assignments" />
<img src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4da.png" width="20" height="20" alt="Readings" title="Readings" />
```

## Course Categories (Sections in README.md)

- **Algorithms**
- **Artificial Intelligence**
- **Computer Graphics**
- **CS Theory**
- **Introduction to CS**
- **Machine Learning**
- **Misc**
- **Programming Languages / Compilers**
- **Security**
- **Systems**
- **Statistics / Regression**

## Key Conventions

### 1. Alphabetical Ordering Within Sections
Courses within each section must be sorted alphabetically by course code. For numbered codes, numeric order applies (e.g., `CS 48` comes before `CS 240`). Always verify sort position before inserting a new entry.

### 2. Course Eligibility
Only include courses that:
- Are relatively **unknown** (not MOOCs like Coursera/edX, not MIT OCW mega-courses)
- Make materials **freely available online** (lectures, assignments, notes, or exams)
- Have course-specific pages with actual content (not just a syllabus)

### 3. Icon Placement
Icons appear immediately after the university name on the same line, with no trailing newline between the university name and the icons.

### 4. Sub-bullet Indentation
Sub-bullets (description, resource links) use a single tab character for indentation, not spaces.

## Development Workflow

### Making Changes
This is a pure Markdown project. All edits are directly to `README.md`.

1. **Adding a course**: Find the correct section, find the alphabetically correct position, insert the entry using the standard format above.
2. **Fixing a link**: Edit the URL in the relevant `- [Label](URL)` line.
3. **Removing a dead course**: Delete the entire entry block (list item + all sub-bullets).

### Git Workflow
- Main branch: `master`
- Feature branches follow the pattern: `claude/<description>-<id>`
- Commit messages are short imperative phrases describing what changed (e.g., `Added course on X (#325)`, `Fix dead link for Y`)
- No CI/CD, no tests, no linting — changes go directly to markdown

### Pushing Changes
```bash
git add README.md
git commit -m "Description of change"
git push -u origin <branch-name>
```

## What NOT to Do

- Do not add popular MOOCs or aggregated courses (Coursera, edX, Khan Academy, MIT OCW flagship courses) — ClassCentral already covers those
- Do not change the icon image CDN URL or dimensions
- Do not reorder sections or change section headings
- Do not add new sections without strong justification
- Do not introduce code, scripts, or non-Markdown files
- Do not use spaces instead of tabs for sub-bullet indentation
