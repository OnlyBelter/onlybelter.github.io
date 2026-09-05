# Self-Introduction Page Redesign

Date: 2026-09-05
Status: Draft approved in conversation, awaiting user review of written spec

## Goal

Redesign the self-introduction homepage (`_pages/about.md`) so it reads as an academic profile page for peers and potential collaborators, rather than a chronological biography or CV-like narrative.

The redesigned page should help a visitor understand, within a few seconds:

- who Xin Xiong is,
- what research problems he works on,
- what computational approaches he uses,
- and which representative works best reflect his research profile.

## Audience

Primary audience:

- academic peers,
- potential collaborators,
- researchers visiting from publications, GitHub, or Google Scholar.

Secondary audience:

- broader visitors who want a concise overview without reading a full CV.

## Design Direction

The page will follow an "academic profile + selected work" structure.

Key characteristics:

- research-first, not biography-first,
- concise and professional,
- direct opening language,
- moderate information density,
- limited background detail,
- selective highlighting of representative work rather than exhaustive listing.

## In Scope

- Rewrite the homepage body content in [`_pages/about.md`](file:///Users/belter/github/onlybelter.github.io/_pages/about.md)
- Reorganize content into clearer sections
- Update wording to sound more focused, mature, and collaborator-friendly
- Add a compact "Selected Work" section with 2-3 representative items
- Optionally refine the short author bio in [`_config.yml`](file:///Users/belter/github/onlybelter.github.io/_config.yml) so it matches the new homepage positioning

## Out of Scope

- Full-site visual redesign
- Changes to Jekyll layouts, sidebar templates, or theme structure
- Building custom cards or a new component system
- Replacing the publications page
- Turning the homepage into a full CV or long-form autobiographical page

## Page Structure

The homepage should be organized into four sections in this order.

### 1. Hero

Purpose:

- establish academic identity immediately,
- communicate current role and research area,
- create a strong first impression for academic readers.

Content:

- name and current position,
- one short opening paragraph in a direct, focused tone,
- 2-3 compact research keywords or themes embedded naturally in the prose or listed lightly.

Writing style:

- direct and confident,
- method-aware,
- domain-specific,
- no long backstory.

### 2. Research Focus

Purpose:

- explain the scientific questions, computational lens, and systems-level perspective.

Content:

- one compact paragraph explaining:
  - what biological problems matter most,
  - what kinds of computational methods are used,
  - what kind of insight the work aims to produce.

Expected emphasis:

- multi-omics data analysis,
- machine learning and statistical modeling,
- tumor microenvironment,
- cancer systems biology,
- immunology,
- systems-level understanding.

### 3. Selected Work

Purpose:

- give visitors concrete anchors for Xin Xiong's research contributions.

Content:

- 2-3 representative papers, tools, or projects,
- each with:
  - a title or short label,
  - a one-sentence description of the problem and contribution,
  - a link to the relevant paper, project, or page.

Selection principle:

- prioritize representativeness over completeness,
- choose items that best reflect research identity,
- avoid repeating the full publications list already available elsewhere.

### 4. Brief Background

Purpose:

- provide enough academic trajectory to contextualize the current research position,
- avoid returning to a CV-like structure.

Content:

- current postdoctoral appointment,
- PhD training,
- brief mention of earlier research roles relevant to present work.

Constraints:

- keep this section short,
- avoid detailed year-by-year narration,
- use it as context, not as the page centerpiece.

## Writing Guidance

The rewritten page should:

- lead with present research identity rather than past chronology,
- avoid vague phrases such as "I have broad interests" unless made more specific,
- reduce repetition across paragraphs,
- use shorter and cleaner academic English,
- preserve systems-level thinking as a distinctive theme,
- sound professional but not overly formal or inflated.

The opening should follow the approved "direct and focused" style:

- clearly state current role,
- state methodological focus,
- state research domains without overexplaining.

## Implementation Notes

Likely files to edit:

- [`_pages/about.md`](file:///Users/belter/github/onlybelter.github.io/_pages/about.md)
- [`_config.yml`](file:///Users/belter/github/onlybelter.github.io/_config.yml) (only if the author bio should be aligned with the rewritten homepage)

Implementation should be surgical:

- preserve existing routing and front matter,
- keep the page compatible with the current Jekyll theme,
- avoid unnecessary formatting or structural changes outside this page.

## Verification

Success criteria:

- the homepage reads like an academic profile, not a chronological autobiography,
- the first screen makes the research identity obvious,
- the page is shorter and easier to scan than the current version,
- representative work is visible without duplicating the publications page,
- background information remains present but clearly secondary.

Manual review checklist after implementation:

- read the page top-to-bottom for flow and tone,
- confirm section order matches this spec,
- check that all selected links render correctly,
- confirm no broken Markdown formatting,
- preview locally if needed to ensure readability in the existing theme.

## Notes

- This document is written as the approved design basis for later implementation.
- Per repository safety rules, no git commit is created at this stage unless explicitly requested by the user.
