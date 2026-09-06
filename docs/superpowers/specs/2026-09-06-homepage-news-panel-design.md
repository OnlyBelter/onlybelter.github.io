# Homepage News Panel Design

Date: 2026-09-06
Status: Design approved in conversation, awaiting user review of written spec

## Goal

Add a lightweight "News" panel to the homepage so short updates can be published in a tweet-like style without cluttering the stable self-introduction content.

The News panel should:

- keep the homepage introduction focused on long-lived research identity,
- make short updates easy to publish and maintain,
- support chronological ordering automatically,
- and allow a news item to link out to an external project or resource.

## Audience

Primary audience:

- academic peers,
- potential collaborators,
- repeat visitors checking for recent activity.

Secondary audience:

- broader visitors who want to see current work at a glance.

## Design Direction

Use Jekyll posts as mini-updates and render recent news items on the homepage.

This approach is preferred over embedding updates directly in `about.md` because it keeps the homepage narrative stable while allowing short, dated updates to accumulate separately.

## In Scope

- Add a "News" section to the homepage
- Use Jekyll posts in `_posts/` as the source of news items
- Filter the homepage to show only posts intended as news
- Add the QClaw literature-tracking update as the first news item
- Remove the QClaw paragraph from the main research narrative if it is better represented as news

## Out of Scope

- Full blog redesign
- Rich social-media-style interactions
- External CMS integration
- Automated ingestion of news from another platform
- Building a separate full news archive page unless needed later

## Content Model

Each news item will be stored as a small Markdown post in `_posts/`.

Recommended front matter:

- `title`
- `date`
- `tags` or `categories` including `news`
- optional `excerpt`
- optional `link`

Each item should contain:

- one concise paragraph,
- optional outbound link,
- no heavy formatting requirements.

## Homepage Placement

The homepage order should become:

1. Hero
2. Research Focus
3. News
4. Selected Work
5. Brief Background

Reasoning:

- `Research Focus` describes stable interests,
- `News` captures current movement,
- `Selected Work` remains a curated record of representative contributions.

## Rendering Behavior

The homepage should display only the most recent few news items.

Recommended initial behavior:

- show the latest 3 items,
- include date and title,
- render a short excerpt or compact body text,
- optionally show a "Read more" or direct link when relevant.

Filtering rule:

- only posts marked with `news` should appear in the homepage panel.

This avoids mixing any future long-form blog posts with short news updates.

## QClaw News Item

The selected paragraph from `about.md` should be converted into the first News item rather than kept inside the main research description.

Recommended wording:

> I am building an automated literature-tracking system based on QClaw, a variant of OpenClaw, to monitor recent advances from journals and arXiv across bioinformatics, cancer biology, and AI for science. The system updates daily through public APIs and email alert parsing. I welcome collaborators interested in improving this [tracking system](https://github.com/OnlyPandaX/bioinformatics-frontier).

This wording fits the "current update" character better than the "stable self-introduction" character.

## Implementation Notes

Likely files to edit:

- `_pages/about.md`
- a layout or include used by the homepage, depending on the cleanest insertion point
- one or more files in `_posts/`

Possible implementation approaches:

1. Add Liquid directly inside `_pages/about.md` to render filtered news posts
2. Create a reusable include for homepage news rendering if the markup becomes non-trivial

Recommendation:

- start with the smallest clean solution,
- use direct Liquid in `about.md` unless the template gets too noisy.

## Verification

Success criteria:

- the homepage shows a clear News section,
- only news-tagged posts appear there,
- the QClaw update appears as the first item,
- the main self-introduction remains concise and research-first,
- adding a future news item only requires creating a new `_posts/*.md` file.

Manual checks after implementation:

- verify post ordering by date,
- verify the news filter works,
- verify the homepage still reads cleanly,
- verify links render correctly,
- preview locally or via GitHub Pages deployment if available.

## Notes

- This feature is intended to support lightweight, frequent updates with minimal maintenance.
- No git commit is created at this stage unless explicitly requested by the user.
