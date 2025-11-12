<!--
Guidance for AI coding agents working on this repository.
This file is intentionally short and pragmatic — follow only discoverable patterns.
-->

# Copilot instructions for this repository

Repository snapshot: this project is a student assignment template for an Exploratory Data Analysis (EDA) and pitch. It mainly contains Markdown files and image assets (no build, no CI, no code runtime).

Key files and patterns
- `EN-template-for-analysis.md` — canonical English template demonstrating heading levels, image inclusion, and code-block examples (see `![](import-screen-capture.png)` and fenced code with language hint like ``` r).
- `README.md` — short project description and links to the instructor's template repo.
- image files in the repository root (e.g. `import-screen-capture.png`, `pivot-table-screen-capture.png`, `chart-screen-capture.png`, `image-*.png`) — images are referenced inline from Markdown and should not be moved without updating references.
- `jou4500-a25-groupe-6` — a Markdown-formatted student submission file (appears as a file, not a folder). Treat it as user content: preserve author metadata and student answers.

What you (the agent) should do
- Make small, explicit edits only: fix typos, clarify wording, improve Markdown structure, add alt text to images, fix broken links, and normalize headings to the template (#, ##, ###).
- Do not invent or alter dataset values, analysis results, or screenshots. If additional data is required, add an explicit TODO comment and open an issue instead of fabricating content.
- Keep images in-place. If you must add a new image, store it next to the Markdown file that references it and use a descriptive filename (e.g. `chart-income-by-neighbourhood.png`).
- Preserve bilingual content: files may contain English and French sections. Avoid translating student-written passages without explicit instruction from the repo owner.

Formatting and examples to follow
- Use fenced code blocks and a language tag when showing code or spreadsheet formulas. Example taken from `EN-template-for-analysis.md`:

``` r
=IMPORTHTML("https://en.wikipedia.org/wiki/China"; "table", 5)
```

- Use the same image pattern shown in the template: `![](pivot-table-screen-capture.png)` and supply an explanatory caption after the image on the next line.
- For headings: level 1 (`#`) for the assignment title, level 2 (`##`) for main sections (Introduction, Getting Data, etc.), level 3 (`###`) for subsections.

> Quick commit/PR rules for the agent
- Create a topic branch named `fix/<short-desc>` or `edit/<short-desc>` for non-trivial edits.
- Keep PRs small and atomic (one conceptual change per PR). Provide a short description referencing the affected file(s), e.g. "Fix typos and add alt text in `jou4500-a25-groupe-6`".
- Use conservative commit messages: `docs: ` or `fix(docs): ` prefixes are acceptable.

When you can't proceed
- If the task requires external datasets, credentials, or confirmation about changing student answers, open an issue and add a clear question rather than guessing.
- If unsure whether a file is student-submitted content vs. repo template, prefer non-destructive edits and add a short note in the PR explaining intent.

Contact and verification
- After making structural edits (headings, image paths, captions), verify locally by previewing the Markdown in VS Code or GitHub preview.
- Leave a brief summary comment in the PR describing the verification steps you ran (previewed file X, confirmed images render).

This file aims to make the agent productive quickly. If you need more rules (lint, CI, tests), request the project owner to add them — currently none are present.
