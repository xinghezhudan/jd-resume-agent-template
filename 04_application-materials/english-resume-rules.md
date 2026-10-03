# English Resume Generation Rules

This file is the execution standard for an Agent that writes or checks an English resume. The default output is a one-page, single-column A4 HTML resume with selectable text. Start from `templates/resume-en.html`; do not overwrite the template. Placeholder text and fictional examples are not applicant facts.

## 1 Source of truth

1. Use only facts confirmed by the applicant in non-`.example.md` files under `01_profile/`.
2. Use a real job description saved or supplied by the applicant. Record the company, role, source, access date, and original text. Do not infer duties from the job title alone.
3. Mark missing education, dates, responsibilities, tools, certificates, project status, and results as `NEEDS USER INPUT`. Do not fill a gap with a plausible statement.
4. You may reorder entries, shorten weak material, improve verbs, and emphasize supported contributions. Do not turn assistance into ownership, a concept into a launched product, or a team result into an individual result.
5. Use `about` or `approximately` only when the applicant can explain the source and measurement. If a number lacks evidence, describe the actual deliverable instead.
6. Never copy facts from the Chinese DOCX example or from any `.example.md` file.

## 2 Required analysis before writing

Create a role evidence matrix before editing the resume:

| Field | Requirement |
|---|---|
| JD requirement | Quote or accurately summarize the requirement and assign priority |
| Applicant evidence | Cite the exact `01_profile/` file and confirmed fact |
| Match | Strong, moderate, weak, or no evidence |
| Resume action | Emphasize, retain, shorten, remove, or request information |

Select the entries that best prove the three to five most important requirements. Use a JD keyword only when a confirmed fact supports it. Do not repeat keywords for ATS scoring.

## 3 Section order and content budget

Default order for an undergraduate or recent graduate:

1. Contact
2. Education
3. Experience
4. Projects
5. Skills

Experience and Projects may switch order when project evidence is more relevant. Optional sections such as Awards, Leadership, or Research should appear only when they add role-relevant evidence.

Use two to four bullets for a highly relevant entry and one to two for a weakly relevant entry. When space is limited, remove unrelated coursework, generic summaries, repeated tools, and weak entries before changing typography.

## 4 Contact education and dates

- Use the applicant's confirmed preferred English name. Do not invent an English name or reverse name order without confirmation.
- Include a verified phone number, professional email address, and confirmed portfolio or LinkedIn URL when relevant.
- Do not include a photo, age, gender, marital status, identity number, full street address, or other protected personal details unless the applicant explicitly requests an appropriate local format.
- Use one date style throughout, preferably `Sep 2025 – Dec 2025` and `Sep 2025 – Present`. Use an en dash with spaces; do not mix numeric and written-month formats.
- Recommended entry heading: `Organization | Role` or `Project Name | Project Type`. Use the actual role and project status.
- Put dates at the far right of the entry heading and prevent wrapping. Shorten secondary wording before narrowing the date column.
- GPA, ranking, awards, and coursework are optional. Include them only when confirmed and helpful for the role. Keep the original grading scale, such as `3.6/4.0`.

## 5 Bullet writing standard

Prefer this structure:

> action + task or method + verifiable deliverable, change, or result

Structural examples only; do not reuse them as applicant facts:

- `Interviewed 8 target users and synthesized recurring pain points into prioritized design requirements.`
- `Developed three Rhino concepts and delivered renderings, an exploded view, and dimension specifications.`

Rules:

1. Start with a specific verb such as `analyzed`, `designed`, `modeled`, `tested`, `coordinated`, `built`, or `delivered`.
2. Use past tense for completed work and present tense only for ongoing responsibilities.
3. Do not use first-person pronouns. Omit the subject and begin with the action verb.
4. Keep one main contribution per bullet. Split a sentence that combines unrelated research, design, marketing, coordination, and results.
5. Prefer evidence and deliverables over adjectives. Replace `excellent design skills` with the actual design work produced.
6. Attach every metric to its unit, time period, population, and comparison when relevant. Do not write `increased by 30%` without defining the metric and baseline.
7. For team work, identify the applicant's module and use accurate ownership language such as `contributed`, `supported`, or `co-developed` when appropriate.
8. State whether work was a course project, concept, prototype, competition entry, pilot, or launched product.
9. Aim for 16–30 English words per bullet and normally no more than two lines in the template. Rewrite lines with one- or two-word tails.
10. Write natural English instead of translating Chinese syntax word for word. Avoid empty phrases such as `responsible for`, `participated in`, `hard-working`, and `good communication skills` unless followed by concrete evidence.
11. End all bullets consistently: either use periods for every complete sentence or omit periods for every fragment. The template recommends complete sentences with periods.

## 6 Language and capitalization

- Use US or UK English consistently. The default is US English unless the JD uses another convention.
- Preserve official product, company, software, certificate, and degree names.
- Use title case consistently for section headings and entry titles; do not capitalize ordinary nouns for emphasis.
- Expand an uncommon abbreviation on first use. Familiar design tools such as CAD may remain abbreviated when the intended audience will understand them.
- Use numerals for measurements and counts. Keep units consistent, such as `mm`, `hours`, or `users`.
- Check articles, singular and plural forms, prepositions, verb tense, and parallel structure. Do not rely on a literal translation checker alone.

## 7 HTML layout contract

Copy `templates/resume-en.html` to a new pending-review file. Preserve these defaults unless relevant content has already been shortened and the page still needs a small layout adjustment.

| Element | Default | Allowed range or requirement |
|---|---:|---|
| Page | A4 portrait `210mm × 297mm` | One page by default; do not switch to Letter |
| Print margin | `@page { margin: 0; }` | Disable browser headers and footers |
| Content safe area | `.page { padding: 5mm; }` | Do not go below `5mm` on any side |
| Body font | `11pt` | Minimum `10pt`; do not shrink further to force one page |
| Body line height | `1.25` | Adjust only within `1.20–1.32` |
| Name | `17pt`, line height `1.1` | Recommended `16–20pt` |
| Contact line | `10pt` | Keep to one or two lines; no overlap with other content |
| Header bottom spacing | `16pt` | May adjust within `12–17pt` |
| Section bottom spacing | `15pt` | Minimum `9pt` when space is tight |
| Section heading | `13pt`, line height `1.1` | Bottom margin `6pt`, bottom padding `4pt`, rule `.6pt` |
| Entry bottom spacing | `11pt` | May adjust within `7–12pt` |
| Heading-date gap | `10pt` | Date uses `white-space: nowrap` |
| Entry heading | `11pt` bold | Must not be smaller than body text |
| Date | `10pt` | Use one format and keep on one line |
| List top spacing | `3pt` | Left indent `1.2em` |
| Bullet spacing | `2pt` | May adjust within `1–3pt` |

Keep the template font stack: `"MiSans", Arial, sans-serif`. Use dark, high-contrast text and the existing restrained accent color. Do not use skill bars, rating dots, charts, decorative timelines, text embedded in images, or multi-column layouts that harm ATS parsing.

## 8 Overflow resolution order

If print preview creates a second page or the first page becomes crowded, apply fixes in this order:

1. Remove weakly relevant entries, coursework, generic summaries, and repeated skills.
2. Rewrite background-heavy bullets around actions and deliverables; remove repeated context and short tail lines.
3. Reduce weak entries from three or four bullets to one or two.
4. Reduce section, entry, and bullet spacing within the allowed ranges.
5. Reduce line height within the allowed range.
6. Reduce body text from `11pt` to no smaller than `10pt` only as the final adjustment.

Do not use negative margins, page scaling, hidden overflow, overlapping elements, or margins under `5mm`. If relevant content still does not fit, ask the applicant to choose what to remove or explicitly approve a two-page resume.

## 9 ATS and export rules

- Keep all primary content as real HTML text. Do not convert the resume into a screenshot.
- Use standard headings such as `Education`, `Experience`, `Projects`, and `Skills` unless the JD requires a clear alternative.
- Avoid critical information in headers, footers, floating images, icons without text labels, or decorative sidebars.
- Use valid links with visible, understandable labels. Verify portfolio and LinkedIn links before delivery.
- Print settings: A4, portrait, 100% scale, no browser margins, headers and footers off, background graphics on.
- The PDF must contain exactly one page by default, selectable text, no clipping, and no blank second page.
- Keep at least `5–8mm` of safe white space below the final line.

## 10 Final quality checklist

- [ ] Every applicant fact traces to `01_profile/`; every role claim traces to the real JD.
- [ ] All placeholders, fictional examples, sample contact details, and sample metrics are removed.
- [ ] Each important JD keyword is supported by evidence and used naturally.
- [ ] Bullets identify the applicant's action and do not exaggerate ownership, status, or results.
- [ ] Tense, date style, capitalization, punctuation, and English convention are consistent.
- [ ] Spelling, grammar, articles, and singular/plural forms are checked.
- [ ] No orphan heading, one-word tail, overlap, clipping, or unintended second page appears in print preview.
- [ ] PDF text is selectable and all portfolio or profile links work.
- [ ] The draft is saved under `04_application-materials/pending-review/Company-Role/` without overwriting the template.
- [ ] The applicant has reviewed the final wording. Do not submit the application without confirmation.
