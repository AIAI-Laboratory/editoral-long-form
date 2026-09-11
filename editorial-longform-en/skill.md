---
name: editorial-longform-en
description: "Transform long-form articles, research essays, speeches, or source documents into editorial/e-magazine HTML with clear visual hierarchy, 4–6 memorable ideas, pull quotes, data moments, and conceptual distinctions while preserving source accuracy. Use when the user wants content reformatted for readability, recall, and responsive standalone HTML output."
---

# Editorial Longform — English

Transform a long source document into an editorial reading experience with pacing, visual hierarchy, and memorable anchors while remaining faithful to the source. The goal is not to decorate the text. The goal is to reveal the article’s intellectual structure so a skimming reader can retain the core arguments, while a careful reader still has access to the full reasoning and evidence.

If `references/reference-longform.html` exists, use it as the visual and structural reference for pacing, components, typography hierarchy, and responsive behavior. Do not copy topic-specific content from the reference into a new article.

## When to use this skill

Use this skill when the user wants to:

- reformat a long article as a longform/e-magazine experience;
- emphasize distinctive core ideas so readers remember them;
- turn Word, Markdown, plain text, or a web article into editorial HTML;
- create visual pauses using quotes, numbers, cards, distinctions, or statements;
- preserve technical depth while reducing the feeling of a continuous wall of text;
- produce a self-contained, responsive HTML file that can open directly in a browser.

Do not use this skill for a short summary, a full substantive rewrite, or a marketing landing page that is not grounded in source material.

## Core principles

1. **The source is the factual authority.** Do not add facts, silently correct conclusions, reconcile inconsistencies, or replace source claims with outside knowledge unless the user explicitly asks.
2. **Re-hierarchize before cutting.** Preserve depth by default. Change hierarchy, grouping, pacing, and visual emphasis before removing material.
3. **Every article gets only a few memory anchors.** Select 4–6, with an absolute maximum of 8 for unusually long pieces. If everything is highlighted, nothing is highlighted.
4. **Highlights must clarify the argument.** Favor counterintuitive claims, important distinctions, memorable numbers, the central question, and the final synthesis.
5. **Do not turn paraphrases into quotations.** Exact source language may be styled as a quote. Edited or compressed wording must be presented as an editorial claim/summary, not placed in quotation marks as if verbatim.
6. **Only visualize numbers supported by the source.** Do not infer, extrapolate, or round numbers merely to make a visual more dramatic.
7. **Preserve citations and references.** If the source contains citations, footnotes, or references, retain them or reorganize them into a clearly accessible reference section.
8. **Design for recall.** Every component should answer: “What should the reader remember here?”

## Workflow

### 1. Read and map the argument

Read the entire source before designing. Identify:

- the central question or tension;
- the primary thesis;
- 3–5 supporting claims;
- case studies or examples that function as evidence;
- important conceptual distinctions;
- numbers with genuine visual value;
- a possible closing synthesis;
- sections that should remain intact for academic, legal, ceremonial, or evidentiary reasons.

Do not start coding the page until you know what the reader should remember.

### 2. Select memory anchors

Choose 4–6 anchors. Each should fit at least one of these categories:

- **Core question:** the tension that earns continued attention;
- **Big claim:** a central idea that can stand on its own;
- **Counterintuitive insight:** an idea that corrects a common intuition;
- **Distinction:** concepts that are easy to conflate but must be separated;
- **Data moment:** one number or cluster of numbers worth remembering;
- **Case pattern:** several examples that collectively establish a pattern;
- **Closing synthesis:** a compact statement of what the whole article changes.

Prefer anchors that can be understood in 5–10 seconds without requiring the reader to reread the preceding paragraph.

### 3. Build a storyboard before coding

A useful default rhythm is:

**Hero → Intro → Question/Thesis band → Section 1 → Pull quote → Case cards → Section 2 → Distinction/stack → Data stage → Counterpoint → Concept triad → Synthesis → Closing → References**

Use only the components the content actually needs. Do not force every article into the entire sequence.

### 4. Component selection rules

#### Hero

Use for the main title, subtitle/deck, and one strong hook. The hero should communicate both topic and tension within one viewport.

#### Question band

Use for the central question or a major transition. Limit to roughly one or two per article.

#### Pull quote / big claim

Use for a sentence that genuinely stands alone. Avoid dense repetition. Roughly one pull quote per two or three major content blocks is usually enough.

#### Cards

Use for three or four peer case studies or examples. Each card should contain:

- a short label;
- the case name;
- 1–3 sentences of explanation;
- no attempt to squeeze the full source paragraph into the card.

Keep the complete reasoning in nearby body copy when needed.

#### Stack / numbered levels

Use for progression, levels of capability, process stages, or ordered distinctions.

#### Data stage

Use when a number is genuinely central to the argument. A large number must be paired with context, qualification, or a counterpoint so the design does not create a misleading impression.

#### Counter-stage

Place immediately after a claim or number that could be oversimplified. Its purpose is to answer “What does this number actually measure?” or “What does this claim not imply?”

#### Triad

Use when three peer concepts need clean separation. Each item should have a short definition or question that is easy to retain.

#### Full-width statement

Use for an especially strong transition or insight. Limit to one or two per article.

#### Closing

End with synthesis rather than recap. The closing should explain what changes in the reader’s understanding after the preceding sections are considered together.

### 5. Edit for visual presentation without changing meaning

When turning prose into a card, quote, or statement:

- preserve the original meaning;
- retain important conditions, limitations, and uncertainty;
- never change “may” into “will,” “candidate” into “proven,” or “associated with” into “caused by”;
- do not remove caveats that are necessary to interpret a claim correctly;
- preserve technical terms when they carry specialized meaning;
- if wording is substantially compressed, make it clear that it is editorial wording rather than a verbatim quotation.

### 6. Typography hierarchy

Use no more than four primary levels:

- **Display:** hero, large data, closing statement;
- **Section heading:** chapter or major claim;
- **Subhead/card title:** distinction, case, concept;
- **Body:** long-form reading text.

A useful editorial default is sans-serif for display/headings and serif for body copy. For self-contained output, prefer system fonts rather than external web-font dependencies.

### 7. Default visual system

Unless the user asks for a different art direction, follow the spirit of `references/reference-longform.html`:

- light paper-like background;
- strong dark text;
- one accent color;
- generous whitespace;
- thin borders/rules;
- lightly differentiated cards;
- one or two dark sections for a data moment or closing;
- avoid heavy gradients, shadows, and decorative animation;
- do not use many colors merely to classify content.

The result should feel editorial, serious, and contemporary rather than like a dashboard or sales landing page.

### 8. HTML output contract

By default, produce **one self-contained HTML file** with:

- `<!doctype html>`;
- `lang="en"`;
- UTF-8;
- responsive viewport metadata;
- CSS inside `<style>`;
- minimal JavaScript only when it adds clear value, such as reading progress;
- no CDN dependency unless necessary;
- semantic HTML such as `header`, `main`, `section`, `blockquote`, `footer`, and `details` where appropriate;
- sufficient color contrast;
- `prefers-reduced-motion` support when motion exists;
- no horizontal overflow at 320px viewport width;
- mobile-readable typography;
- basic print CSS for archival or academic material when appropriate.

### 9. Accessibility

- Maintain a logical heading order.
- Do not use color as the only information signal.
- Keep quotations as selectable text rather than images.
- Add meaningful `alt` text for user-provided images.
- Controls need labels and keyboard focus states.
- Keep mobile body text at roughly 16px or larger.

### 10. QA before delivery

Check at minimum:

- Are the 4–6 key ideas visibly more important than everything else?
- Is any highlight visually dramatic but intellectually minor?
- Has any claim become stronger than the source supports?
- Is any paraphrase accidentally presented as a quote?
- Do large numbers retain the context needed to interpret them?
- Can a reader skim for 20–30 seconds and retell the article in 4–6 ideas?
- Is there any horizontal overflow on desktop or mobile?
- Do cards break badly or contain too much copy?
- Are references/citations preserved?
- Does the closing synthesize rather than merely repeat the introduction?

## Editorial decision rule

Do not ask, “How should this paragraph be decorated?” Ask:

> If the reader remembers only one thing from this section, what should it be?

Then choose the component based on that answer.

## Short storyboard template

```text
HERO
Title + core tension / big question

INTRO
2–4 paragraphs of context

MEMORY ANCHOR 01
One big claim
→ supporting case studies

MEMORY ANCHOR 02
One distinction / three-level model

MEMORY ANCHOR 03
One data moment
→ immediately followed by a counterpoint explaining the number

MEMORY ANCHOR 04
One conceptual distinction

SYNTHESIS
What changes when the preceding ideas are considered together?

CLOSING
One idea the reader should carry away after closing the article

REFERENCES
Preserve the source trail and necessary notes
```

## Success criterion

A strong longform is not the one with the most visual effects. It is the one where, after reading, a reader can accurately recall 4–6 central ideas, understand how they connect, and has not been visually pushed toward a conclusion stronger than the source warrants.
