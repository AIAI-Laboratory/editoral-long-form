---
name: editorial-longform-bilingual
description: "Transform long source material into a memorable editorial/e-magazine HTML experience with 4–6 visual memory anchors while preserving source accuracy. / Biến tài liệu dài thành longform/e-magazine HTML với 4–6 điểm nhớ thị giác, đồng thời giữ trung thành với nội dung nguồn."
---

# Editorial Longform — Bilingual / Song ngữ

## Purpose / Mục tiêu

Transform a long article, research essay, speech, or source document into a responsive editorial longform where visual hierarchy makes the core ideas easier to remember without overstating, simplifying away, or rewriting the source's meaning.

Biến bài viết dài, bài nghiên cứu, bài phát biểu hoặc tài liệu nguồn thành một longform responsive, trong đó thứ bậc thị giác giúp người đọc ghi nhớ các luận điểm chính mà không làm mạnh tay hơn, đơn giản hóa sai hoặc viết lại ý nghĩa của nguồn.

Use `references/reference-longform.html` as the visual reference when available. Treat it as a design system and pacing reference only; never copy its topic-specific content into a new article.

Nếu có `references/reference-longform.html`, dùng làm tham chiếu cho hệ thống thị giác và nhịp trang. Chỉ học cách dàn, không sao chép nội dung chủ đề của bài mẫu sang bài mới.

## Core rule / Quy tắc cốt lõi

**The source is the factual authority. / Nguồn là chuẩn sự thật.**

Do not silently add facts, correct conclusions, remove material uncertainty, or turn a qualified claim into a stronger one. Preserve citations and references. Exact quotations may be styled as quotes; paraphrases must not be presented as verbatim quotes.

Không tự bổ sung dữ kiện, sửa kết luận, xóa mức độ bất định hay biến một claim có điều kiện thành kết luận mạnh hơn. Giữ citations/references. Chỉ câu nguyên văn mới được trình bày như quote; câu biên tập lại không được đặt như thể là trích dẫn nguyên văn.

## Memory-anchor model / Mô hình “điểm nhớ”

Select **4–6 anchors**, maximum 8 for unusually long pieces. / Chọn **4–6 điểm nhớ**, tối đa 8 với bài đặc biệt dài.

An anchor should normally be one of: / Mỗi điểm nhớ thường thuộc một trong các loại:

- Core question / Câu hỏi trung tâm
- Big claim / Luận điểm lớn
- Counterintuitive insight / Ý phản trực giác
- Conceptual distinction / Phân biệt khái niệm
- Data moment / Khoảnh khắc số liệu
- Case pattern / Pattern rút ra từ nhiều ví dụ
- Closing synthesis / Kết luận tổng hợp

If everything is highlighted, nothing is highlighted. / Nếu mọi thứ đều được nhấn, thực chất không còn gì nổi bật.

## Workflow / Quy trình

1. **Read everything first / Đọc toàn bộ trước.** Identify the central tension, thesis, supporting claims, cases, distinctions, meaningful numbers, caveats, and final synthesis.
2. **Choose 4–6 memory anchors / Chọn 4–6 điểm nhớ.** Prefer ideas a reader can understand in 5–10 seconds.
3. **Storyboard before HTML / Lập storyboard trước khi code.** Use only components justified by the content.
4. **Preserve depth / Giữ chiều sâu.** Re-hierarchize and regroup before cutting source material.
5. **Build self-contained responsive HTML / Dựng HTML responsive tự chứa.** Use semantic markup, internal CSS, minimal JS, and no external dependency unless necessary.
6. **QA for fidelity and recall / Kiểm tra độ trung thành và khả năng ghi nhớ.** A 20–30 second skim should reveal the article's 4–6 central ideas without creating a conclusion stronger than the source.

## Recommended story rhythm / Nhịp bài gợi ý

```text
HERO
Title + central tension
Tiêu đề + tension trung tâm

INTRO
Context / Bối cảnh

MEMORY ANCHOR 01
Big claim / Luận điểm lớn
→ supporting cases / các case hỗ trợ

MEMORY ANCHOR 02
Distinction or levels / Phân biệt hoặc mô hình tầng

MEMORY ANCHOR 03
Data moment / Số liệu trọng tâm
→ immediate counterpoint / ngay sau là phần giải nghĩa-phản biện

MEMORY ANCHOR 04
Conceptual triad or framework / Bộ ba khái niệm hoặc framework

SYNTHESIS
What changes when the ideas are combined?
Điều gì thay đổi khi đặt các ý cạnh nhau?

CLOSING
One idea to carry away / Một ý để người đọc mang theo

REFERENCES
Preserve the source trail / Giữ đầy đủ nguồn
```

## Component rules / Quy tắc component

### Hero
One viewport should communicate topic + tension. / Một màn hình phải truyền được chủ đề + vấn đề trung tâm.

### Question band
Use for the central question or major transition; usually 1–2 per article. / Dùng cho câu hỏi trung tâm hoặc chuyển ý lớn; thường 1–2 lần mỗi bài.

### Pull quote / Big claim
Use only for ideas that genuinely stand alone. / Chỉ dùng cho câu thực sự có thể đứng độc lập.

### Cards
Use for 3–4 peer cases. Keep each card concise; keep full reasoning in body copy nearby. / Dùng cho 3–4 case ngang hàng. Card ngắn; lập luận đầy đủ để ở phần body gần đó.

### Stack / Numbered levels
Use for ordered capabilities, process stages, or distinctions. / Dùng cho các tầng năng lực, quy trình hoặc distinction có thứ tự.

### Data stage
Use only when a number is central to the argument. Always pair it with context and qualifications. / Chỉ dùng khi số liệu là tâm điểm thật sự; luôn đi kèm context và điều kiện.

### Counter-stage
Use immediately after a dramatic claim or number that could be misread. / Đặt ngay sau claim hoặc con số dễ gây hiểu sai để trả lời “nó thực sự đo điều gì?”

### Triad
Use when three peer concepts must be separated. / Dùng khi ba khái niệm ngang hàng cần phân biệt rõ.

### Full-width statement
Use sparingly, roughly 1–2 times per article. / Dùng tiết chế, khoảng 1–2 lần mỗi bài.

### Closing
Synthesize; do not merely repeat the introduction. / Tổng hợp lại cách hiểu mới; không chỉ lặp phần mở đầu.

## Fidelity guardrails / Hàng rào trung thành nguồn

When compressing source prose: / Khi rút gọn nội dung nguồn:

- Preserve uncertainty and scope. / Giữ mức độ bất định và phạm vi.
- Do not change “may” to “will.” / Không đổi “có thể” thành “sẽ”.
- Do not change “candidate” to “proven.” / Không đổi “ứng viên” thành “đã được chứng minh”.
- Do not change association into causation. / Không biến liên hệ thành quan hệ nhân quả.
- Keep caveats required for correct interpretation. / Giữ các caveat cần thiết để hiểu đúng.
- Keep technical terms when they carry specialized meaning. / Giữ thuật ngữ kỹ thuật có ý nghĩa chuyên môn.
- Never fabricate numbers for visual drama. / Không bịa hoặc nội suy số liệu để làm visual mạnh hơn.

## Default visual system / Hệ thống thị giác mặc định

Unless the user specifies another art direction: / Nếu người dùng không yêu cầu style khác:

- light paper-like background / nền giấy sáng;
- dark text + one accent color / chữ đậm + một màu accent;
- large whitespace / khoảng trắng lớn;
- thin rules and borders / line/border mảnh;
- lightly differentiated cards / card nền nhẹ;
- one or two dark sections for data or closing / 1–2 section nền tối cho data hoặc closing;
- sans-serif display/headings + serif body / sans-serif cho display-heading + serif cho body;
- avoid heavy gradients, shadows, and decorative animation / tránh gradient, shadow nặng và animation trang trí.

The result should feel editorial and contemporary, not like a dashboard or sales landing page.

Kết quả nên mang cảm giác editorial hiện đại, không giống dashboard hay landing page bán hàng.

## HTML output contract / Chuẩn đầu ra HTML

By default, produce one self-contained HTML file with: / Mặc định xuất một file HTML tự chứa gồm:

- `<!doctype html>`;
- correct `lang` attribute / `lang` đúng ngôn ngữ bài;
- UTF-8 + responsive viewport;
- CSS inside `<style>`;
- minimal JavaScript only when useful / JavaScript tối thiểu;
- semantic HTML;
- sufficient contrast;
- `prefers-reduced-motion` when motion exists;
- no horizontal overflow at 320px;
- mobile body text around 16px or larger;
- basic print CSS where appropriate.

## QA checklist / Checklist QA

Before delivery, verify: / Trước khi giao, kiểm tra:

- Are only 4–6 ideas visually dominant? / Có đúng 4–6 ý thật sự nổi bật?
- Is any highlight visually strong but intellectually minor? / Có highlight nào đẹp nhưng không quan trọng?
- Has any claim become stronger than the source? / Có claim nào bị làm mạnh hơn nguồn?
- Is any paraphrase accidentally styled as a quote? / Có paraphrase nào bị trình bày như quote nguyên văn?
- Do large numbers retain context? / Số liệu lớn có đủ context?
- Can a 20–30 second skim reconstruct the article? / Lướt 20–30 giây có kể lại được bài?
- Is mobile free from horizontal overflow? / Mobile có tràn ngang không?
- Are cards concise and readable? / Card có gọn và dễ đọc không?
- Are references preserved? / References có được giữ nguyên?
- Does the closing synthesize instead of recap? / Closing có tổng hợp thay vì chỉ recap?

## Editorial decision rule / Quy tắc quyết định

> If the reader remembers only one thing from this section, what should it be?
>
> Nếu người đọc chỉ nhớ một điều từ section này, điều đó phải là gì?

Choose the component only after answering that question. / Chỉ chọn component sau khi trả lời được câu hỏi đó.
