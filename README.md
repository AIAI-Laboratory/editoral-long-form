# Editorial Longform

A portable agent skill for turning long articles, research essays, speeches, and source documents into memorable editorial longform experiences.

Instead of treating a long document as one continuous wall of text, Editorial Longform identifies the few ideas readers should remember, builds a visual hierarchy around them, and produces a responsive standalone HTML page while preserving the source's meaning, uncertainty, citations, and technical depth.

**English:** `editorial-longform-en/skill.md`  
**Tiếng Việt:** `editorial-longform-vi/skill.md`  
**Bilingual:** `skill.md`

---

## What it does

Editorial Longform restructures source material around **4–6 memory anchors**: the questions, claims, distinctions, cases, or numbers that carry the argument.

It can:

- turn Word, Markdown, plain text, or article content into editorial/e-magazine HTML;
- surface a central question or tension in the hero;
- convert parallel examples into concise case cards;
- turn ordered concepts into numbered levels or stacks;
- make an important number a visual focal point without stripping away context;
- place counterpoints immediately after claims that could otherwise be misread;
- separate closely related concepts into clear comparison frameworks;
- preserve full body reasoning for readers who want depth;
- retain citations, references, caveats, and technical terminology;
- produce one self-contained responsive HTML file with no unnecessary dependencies.

The goal is not decoration. The goal is **recall**.

A reader who skims for 20–30 seconds should be able to reconstruct the article's main argument in a handful of ideas.

---

## Installation

This package is plain Markdown plus an HTML reference file, so it can be used by any agent harness that supports skill-style instructions.

### Manual

Copy the skill directory into the location your agent uses for skills.

For the English version:

```text
editorial-longform-en/
├── skill.md
└── references/
    └── reference-longform.html
```

For the Vietnamese version:

```text
editorial-longform-vi/
├── skill.md
└── references/
    └── reference-longform.html
```

Or use the bilingual root skill:

```text
editorial-longform-skill/
├── skill.md
└── references/
    └── reference-longform.html
```

Some agent harnesses require the runtime file to be named `SKILL.md`. If yours does, rename the relevant `skill.md` to `SKILL.md` after copying it into the skill directory.

If you later publish this package to a Git repository, it can also be installed through whatever skill/package mechanism your agent harness supports.

---

## Usage

Invoke the skill with a source document and a clear request to reformat it as editorial longform.

### English

```text
Use Editorial Longform on this document.
Keep the full argument, but make the 4–6 most important ideas much easier to remember.
Output a self-contained responsive HTML file.
```

Or point it at a file:

```text
Reformat article.docx with Editorial Longform.
Preserve citations and technical caveats.
```

### Tiếng Việt

```text
Dùng Editorial Longform để dàn lại tài liệu này.
Giữ đầy đủ lập luận, nhưng làm nổi bật 4–6 ý quan trọng nhất để người đọc dễ nhớ.
Xuất thành một file HTML responsive tự chứa.
```

Hoặc:

```text
Dàn lại bai-viet.docx theo Editorial Longform.
Giữ nguyên citations, thuật ngữ kỹ thuật và các caveat quan trọng.
```

You can also give an art direction:

```text
Use the same editorial logic, but make the visual language more restrained,
academic, and suitable for a research institute.
```

The source still controls the facts. The art direction controls presentation.

---

## How it works

Editorial Longform uses a simple editorial pipeline.

### 1. Read the whole source

Before designing anything, the skill identifies:

- the central question or tension;
- the main thesis;
- supporting claims;
- case studies and examples;
- conceptual distinctions;
- meaningful numbers;
- qualifications and uncertainty;
- the final synthesis.

It does not begin by decorating paragraphs one by one.

### 2. Select 4–6 memory anchors

A memory anchor is an idea worth giving disproportionate visual weight.

Typical anchors include:

| Anchor type | What it captures |
| --- | --- |
| Core question | The tension that makes the article worth reading |
| Big claim | A central argument that can stand on its own |
| Counterintuitive insight | A point that corrects a common intuition |
| Distinction | Concepts that are often confused but should be separated |
| Data moment | A number central enough to deserve visual emphasis |
| Case pattern | A shared lesson emerging from several examples |
| Closing synthesis | The idea the reader should carry away |

The skill normally chooses **4–6**, and rarely more than 8 even for very long pieces.

If everything is highlighted, nothing is highlighted.

### 3. Storyboard before coding

The skill maps each anchor to the smallest component that communicates it clearly.

A typical rhythm might look like:

```text
HERO
Title + central tension

INTRO
Context and setup

MEMORY ANCHOR 01
Big claim
→ supporting cases

MEMORY ANCHOR 02
Distinction / levels / framework

MEMORY ANCHOR 03
Data moment
→ immediate context or counterpoint

MEMORY ANCHOR 04
Conceptual comparison

SYNTHESIS
What changes when the ideas are combined?

CLOSING
One idea to carry away

REFERENCES
Preserve the source trail
```

This is a rhythm, not a rigid template. Components are used only when the content justifies them.

### 4. Build the page

By default the output is one standalone HTML file with:

- semantic HTML;
- CSS inside `<style>`;
- minimal JavaScript only when useful;
- responsive typography and layout;
- no unnecessary CDN or framework dependency;
- accessible contrast and heading structure;
- `prefers-reduced-motion` support when motion is used;
- no horizontal overflow at narrow mobile widths;
- basic print behavior for document-oriented pieces.

The included `references/reference-longform.html` acts as a visual and pacing reference. It is not a content template.

---

## Built-in editorial guardrails

Visual emphasis can accidentally distort meaning. The skill treats that as a factual error, not merely a design issue.

It therefore follows these rules:

- **The source is the factual authority.** No invented facts, dates, names, numbers, or citations.
- **Qualified claims stay qualified.** “May” does not silently become “will.”
- **Candidates stay candidates.** An unverified or provisional result is not presented as established fact.
- **Association does not become causation.**
- **Caveats stay attached to the claims that need them.**
- **Technical terms are preserved when they carry specialized meaning.**
- **Paraphrases are not styled as verbatim quotations.**
- **Large numbers keep their denominator, timeframe, scope, or other necessary context.**
- **A visually dramatic section must also be intellectually important.**

The skill prefers **re-hierarchizing and regrouping before cutting**. Longform should remain deep enough for a careful reader.

---

## Components

The skill has a small editorial vocabulary rather than a large library of decorative blocks.

### Hero

Topic + tension in one viewport.

### Question band

A central question or major transition. Usually no more than one or two per article.

### Pull quote / big claim

For a sentence that genuinely deserves to stand alone. Exact quotes and editorial summaries are treated differently.

### Case cards

For 3–4 parallel examples. Cards stay concise; the full reasoning remains nearby in body copy.

### Numbered stack

For ordered levels, stages, capabilities, or conceptual progression.

### Data stage

For a number that is part of the argument, not merely an interesting statistic.

### Counter-stage

Placed immediately after a dramatic number or claim when readers need to know what it does **not** mean.

### Triad / comparison framework

For three peer concepts that need to remain distinct.

### Full-width statement

A high-emphasis transition or synthesis. Used sparingly.

### Closing

A synthesis of what the reader now understands differently, not a generic recap.

---

## Example transformation

A conventional long article may contain this sequence:

```text
Introduction
Historical example A
Historical example B
Historical example C
Technical framework
Large experiment
Methodological caveat
Verification discussion
Conclusion
```

Editorial Longform might reveal a more memorable structure:

```text
HERO
The question the whole article is really asking

01 — ONE BIG CLAIM
What the historical examples collectively show

02 — A THREE-LEVEL MODEL
The framework hidden inside the technical section

03 — THE NUMBER EVERYONE WILL REMEMBER
The large experiment

COUNTERPOINT
What that number actually measures

04 — THREE DIFFERENT KINDS OF “RIGHT”
The verification concepts readers might otherwise conflate

CLOSING
The consequence of putting all four ideas together
```

The underlying evidence remains available. What changes is the hierarchy.

---

## Visual reference

`references/reference-longform.html` is included to give the agent a concrete reference for:

- editorial pacing;
- whitespace;
- typography hierarchy;
- case cards;
- large data moments;
- dark/light section contrast;
- pull quotes;
- closing statements;
- responsive behavior.

Treat it as a **design system and pacing reference only**. Do not copy topic-specific text, claims, numbers, or examples from the reference into a new article.

---

## Package structure

```text
editorial-longform-skill/
├── README.md
├── skill.md                         # Bilingual skill
├── references/
│   └── reference-longform.html
│
├── editorial-longform-en/
│   ├── skill.md                     # English skill
│   └── references/
│       └── reference-longform.html
│
└── editorial-longform-vi/
    ├── skill.md                     # Vietnamese skill
    └── references/
        └── reference-longform.html
```

The three variants implement the same editorial method. Use the version that best matches your agent workflow and working language.

---

## Tiếng Việt

**Editorial Longform** là một agent skill dùng để biến bài viết dài, bài nghiên cứu, bài phát biểu hoặc tài liệu nguồn thành một trải nghiệm đọc kiểu longform/e-magazine dễ nhớ hơn.

Thay vì coi toàn bộ tài liệu như một khối chữ liên tục, skill tìm ra **4–6 “điểm nhớ”** quan trọng nhất và xây dựng thứ bậc thị giác quanh chúng. Người đọc lướt nhanh vẫn nắm được cấu trúc tư tưởng của bài, trong khi người đọc kỹ vẫn có đầy đủ lập luận, ví dụ, caveat và tài liệu tham khảo.

### Skill này làm gì?

- tìm câu hỏi hoặc tension trung tâm của bài;
- chọn 4–6 luận điểm đáng được nhấn mạnh nhất;
- gom nhiều ví dụ cùng cấp thành case cards;
- chuyển progression thành numbered stack;
- biến số liệu thực sự quan trọng thành data moment;
- đặt context/counterpoint ngay sau con số hoặc claim dễ bị hiểu quá mức;
- tách các khái niệm dễ bị đánh đồng thành framework rõ ràng;
- giữ phần body đầy đủ để không làm mất chiều sâu;
- giữ citations, references, mức độ bất định và thuật ngữ kỹ thuật;
- xuất một file HTML responsive tự chứa.

### Nguyên tắc quan trọng nhất

> Nếu người đọc chỉ nhớ một điều từ section này, điều đó phải là gì?

Chỉ sau khi trả lời được câu hỏi đó, skill mới quyết định section nên là đoạn văn, quote, card, stack, data stage hay một statement lớn.

### Cách dùng nhanh

```text
Dùng Editorial Longform để dàn lại tài liệu này.
Đừng tóm tắt mất chiều sâu. Hãy xác định 4–6 ý đáng nhớ nhất,
xây hierarchy quanh chúng và xuất thành một file HTML responsive tự chứa.
```

Hoặc:

```text
Dàn lại file này thành một bài e-magazine.
Giữ nguyên citations và caveat, nhưng làm cho người đọc lướt 20–30 giây
vẫn kể lại được các luận điểm chính.
```

### Hàng rào biên tập

Skill không được làm cho bài “hay hơn” bằng cách làm sai nguồn:

- không tự bịa fact, số liệu, citation;
- không biến “có thể” thành “sẽ”;
- không biến kết quả ứng viên thành kết luận đã được xác nhận;
- không biến tương quan thành nhân quả;
- không bỏ caveat chỉ vì nó làm visual kém gọn;
- không trình bày paraphrase như trích dẫn nguyên văn;
- không làm một chi tiết phụ nổi hơn luận điểm chính chỉ vì nó dễ thiết kế.

Mục tiêu là **làm lộ rõ cấu trúc tư tưởng đã có trong nguồn**, không áp một câu chuyện mới lên tài liệu.

---

## Design principle

Editorial Longform is built around one rule:

> **Design should change what the reader notices, not what the source means.**

**Thiết kế có thể thay đổi điều người đọc chú ý, nhưng không được thay đổi điều nguồn thực sự nói.**
