# CLAUDE.md — AI Assistant Guide for awesome-courses

## Repository Overview

**awesome-courses** is a community-curated list of high-quality Computer Science university courses that make their materials (assignments, lectures, notes, readings, exams) freely available online. It is a pure Markdown documentation repository with no code, no build system, and no dependencies.

- **Primary file:** `README.md` (~1,031 lines, 228 courses across 11 categories)
- **Contributing guide:** `CONTRIBUTING.md`
- **No build tooling**, package managers, CI/CD, or test suites

---

## Repository Structure

```
awesome-courses/
├── README.md         # The entire curated list
├── CONTRIBUTING.md   # Guidelines for contributors
├── CLAUDE.md         # This file
└── .gitignore        # Ignores .DS_Store only
```

---

## Course Entry Format

Every course entry follows this exact structure:

```markdown
- [COURSE_CODE](course_url) **Course Title** *University Name* <icon> <icon> ...
	- One-sentence description of course content and learning outcomes.
	- [Resource Name](resource_url)
	- [Resource Name](resource_url)
```

### Rules for entries:
- Course code is hyperlinked to the course homepage
- Course title is **bold**
- University name is *italic*
- Material icons immediately follow the university name (see Icon System below)
- Description and resource links are **tab-indented** (not spaces)
- Resource links are descriptive (e.g., "Lecture Videos", "Assignments", "Lecture Notes")

---

## Icon System

Icons indicate what materials are available for each course. Always copy these exact `<img>` tags — do not substitute emoji or other formats.

| Icon | Meaning | HTML Tag |
|------|---------|----------|
| ![video](https://assets-cdn.github.com/images/icons/emoji/unicode/1f4f9.png) | Lecture Videos | `<img src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4f9.png" width="20" height="20" alt="Lecture Videos" title="Lecture Videos" />` |
| ![notes](https://assets-cdn.github.com/images/icons/emoji/unicode/1f4dd.png) | Lecture Notes | `<img src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4dd.png" width="20" height="20" alt="Lecture Notes" title="Lecture Notes" />` |
| ![assignments](https://assets-cdn.github.com/images/icons/emoji/unicode/1f4bb.png) | Assignments / Labs | `<img src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4bb.png" width="20" height="20" alt="Assignments" title="Assignments" />` |
| ![readings](https://assets-cdn.github.com/images/icons/emoji/unicode/1f4da.png) | Readings | `<img src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4da.png" width="20" height="20" alt="Readings" title="Readings" />` |

---

## Course Categories (Sections in README.md)

Courses are grouped into 11 sections in this order:

1. Systems
2. Programming Languages / Compilers
3. Algorithms
4. CS Theory
5. Introduction to CS
6. Machine Learning
7. Security
8. Artificial Intelligence
9. Computer Graphics
10. Misc
11. Statistics / Regression

---

## Key Conventions

### Alphabetical Ordering
Within each category, courses **must be sorted alphabetically by course code**. Alphabetization follows string comparison of the course code (e.g., `CS 240` comes before `CSCE 48`).

### What Belongs Here
This list is for courses that are:
- Relatively **unknown** (not already in major MOOC aggregators)
- From **universities** (not MOOCs like Coursera, edX, MIT OCW)
- Providing **free, publicly accessible** materials

Do **not** add: popular MOOCs, courses behind paywalls, courses without publicly available materials.

### Indentation
Use **tab characters** (not spaces) for all indented lines under a course entry (description and resource links).

---

## Making Changes

Since this is a pure Markdown repository, all edits are made directly to `README.md`.

### Adding a new course
1. Identify the correct category section
2. Find the correct alphabetical position within that section
3. Add the entry using the exact format above
4. Include only icons for materials that are actually available
5. Verify all URLs are accessible

### Fixing a broken link
Find the course entry and update the URL. Do not remove the entry unless the course materials are entirely gone with no archival copy.

### Moving or renaming a section
The Table of Contents at the top of `README.md` uses anchor links — update both the TOC entry and the section heading together.

---

## Git Workflow

This repository uses a standard fork-and-PR workflow on GitHub.

```bash
# Stage and commit changes
git add README.md
git commit -m "Add [Course Name] to [Category]"

# Push to branch
git push -u origin <branch-name>
```

Commit messages should be descriptive, e.g.:
- `Add CS 189 Machine Learning to ML section`
- `Fix broken link for CMU 15-410`
- `Maintain alphabetical order in Algorithms section`

---

## No Build or Test Commands

There are no commands to run. There is no:
- `npm install` / `yarn`
- `make`
- Linter or formatter
- Test suite
- CI/CD pipeline

When contributing, manually verify:
- Markdown renders correctly
- All links are valid and publicly accessible
- Alphabetical order is maintained
- Icon tags are copied correctly (no truncation or modification)
