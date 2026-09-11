---
name: editorial-longform-vi
description: "Biến bài viết dài, bài nghiên cứu, bài phát biểu hoặc tài liệu nguồn thành longform/e-magazine HTML có thứ bậc thị giác rõ, nhấn mạnh 4–6 ý đáng nhớ, pull quote, số liệu và các phân biệt khái niệm mà không làm mất độ chính xác của nguồn. Dùng khi người dùng muốn dàn lại nội dung để dễ đọc, dễ nhớ và có thể xuất thành một trang HTML responsive."
---

# Editorial Longform — Tiếng Việt

Biến một tài liệu dài thành một trải nghiệm đọc longform có nhịp, có điểm nhớ và vẫn trung thành với nguồn. Mục tiêu không phải “trang trí” nội dung, mà là làm lộ rõ cấu trúc tư tưởng của bài để người đọc lướt nhanh vẫn nhớ được các luận điểm cốt lõi, còn người đọc kỹ vẫn có đầy đủ lập luận và bằng chứng.

Nếu có file `references/reference-longform.html`, dùng nó làm chuẩn tham chiếu cho hệ thống thị giác, nhịp trang, component và responsive behavior. Không sao chép máy móc nội dung cụ thể của file tham chiếu sang bài mới.

## Khi nào dùng skill này

Dùng khi người dùng muốn một hoặc nhiều việc sau:

- dàn lại bài dài thành longform/e-magazine;
- nhấn mạnh các ý chính đặc sắc để dễ nhớ;
- biến tài liệu Word/Markdown/text/web article thành HTML editorial;
- tạo các điểm dừng thị giác bằng quote, số liệu, card, distinction hoặc statement;
- giữ nội dung chuyên sâu nhưng giảm cảm giác “khối chữ dài”;
- tạo một file HTML tự chứa, responsive, có thể mở trực tiếp bằng trình duyệt.

Không dùng skill này chỉ để tóm tắt ngắn, viết lại toàn bộ nội dung, hoặc tạo một landing page marketing không dựa trên một tài liệu nguồn.

## Nguyên tắc cốt lõi

1. **Nguồn là chuẩn sự thật.** Không tự bổ sung dữ kiện, sửa kết luận, hòa giải mâu thuẫn hay “nâng cấp” nội dung bằng kiến thức bên ngoài nếu người dùng không yêu cầu.
2. **Phân cấp thay vì cắt bỏ.** Mặc định giữ lại chiều sâu của bài; thay đổi chủ yếu nằm ở hierarchy, grouping, nhịp trang và điểm nhấn.
3. **Mỗi bài chỉ có vài điểm nhớ.** Chọn 4–6 memory anchors; tối đa 8 trong bài rất dài. Nếu mọi câu đều được highlight thì không còn câu nào nổi bật.
4. **Highlight phải làm rõ luận điểm.** Ưu tiên câu phản trực giác, distinction quan trọng, con số đáng nhớ, câu hỏi trung tâm, hoặc kết luận cô đọng.
5. **Không biến diễn giải thành trích dẫn.** Nếu dùng nguyên văn từ nguồn, có thể trình bày như quote. Nếu biên tập lại cho ngắn/gọn, trình bày như editorial summary/claim, không đặt trong ngoặc kép như thể là lời nguyên văn.
6. **Số liệu chỉ được nhấn khi có trong nguồn.** Không suy ra, nội suy hoặc làm tròn tùy tiện để tạo visual đẹp hơn.
7. **Giữ tham chiếu và tài liệu tham khảo.** Nếu nguồn có citations/references/footnotes, giữ chúng hoặc tái tổ chức thành phần tham khảo cuối bài.
8. **Thiết kế phục vụ nhớ ý.** Mọi component phải trả lời câu hỏi: “Nó giúp người đọc nhớ điều gì?”

## Workflow

### 1. Đọc và lập bản đồ nội dung

Đọc toàn bộ tài liệu trước khi thiết kế. Xác định:

- câu hỏi trung tâm hoặc tension của bài;
- luận điểm chính;
- 3–5 luận điểm phụ;
- các case study/ví dụ làm bằng chứng;
- những distinction quan trọng;
- những con số có giá trị thị giác;
- câu kết có khả năng trở thành closing statement;
- phần nào bắt buộc phải giữ nguyên vì tính học thuật, pháp lý hoặc nghi thức.

Không bắt đầu dàn HTML trước khi biết bài muốn người đọc nhớ điều gì.

### 2. Chọn “memory anchors”

Chọn 4–6 điểm nhớ. Mỗi điểm phải thuộc ít nhất một loại:

- **Core question:** câu hỏi khiến người đọc muốn tiếp tục;
- **Big claim:** luận điểm trung tâm có thể đứng độc lập;
- **Counterintuitive insight:** ý phá một trực giác phổ biến;
- **Distinction:** hai hoặc ba khái niệm dễ bị đánh đồng nhưng cần tách rõ;
- **Data moment:** một con số hoặc cụm số liệu đáng nhớ;
- **Case pattern:** nhiều ví dụ khác nhau cùng chứng minh một pattern;
- **Closing synthesis:** kết luận cô đọng toàn bài.

Ưu tiên memory anchor có thể hiểu trong 5–10 giây mà không cần đọc cả đoạn trước.

### 3. Dựng storyboard trước khi code

Mặc định dùng nhịp sau, nhưng chỉ chọn component phù hợp với nội dung:

**Hero → Intro → Question/Thesis band → Section 1 → Pull quote → Case cards → Section 2 → Distinction/stack → Data stage → Counterpoint → Concept triad → Synthesis → Closing → References**

Không ép bài mới phải có đủ mọi component.

### 4. Quy tắc chọn component

#### Hero

Dùng cho tiêu đề chính + subtitle/deck + một câu dẫn mạnh. Hero phải truyền được chủ đề và tension của bài trong một màn hình.

#### Question band

Dùng cho câu hỏi trung tâm hoặc câu chuyển quan trọng. Chỉ nên dùng 1–2 lần trong toàn bài.

#### Pull quote / big claim

Dùng cho câu có khả năng đứng độc lập. Không dùng quá dày. Khoảng 1 pull quote sau mỗi 2–3 khối nội dung lớn là mức tối đa hợp lý.

#### Cards

Dùng khi có 3–4 case study song song hoặc ví dụ cùng cấp. Mỗi card nên chứa:

- nhãn ngắn;
- tên case;
- 1–3 câu giải thích;
- không nhồi toàn bộ chi tiết của đoạn gốc.

Phần giải thích đầy đủ có thể ở đoạn văn trước/sau card.

#### Stack / numbered levels

Dùng cho progression, tầng năng lực, quy trình hoặc distinction có thứ tự.

#### Data stage

Dùng khi một con số là tâm điểm thật sự của lập luận. Số lớn phải đi kèm context, counterpoint hoặc lời giải thích để tránh tạo ấn tượng sai.

#### Counter-stage

Dùng ngay sau một claim/con số có nguy cơ bị hiểu quá đơn giản. Mục tiêu là làm rõ “con số này thực sự đo điều gì?” hoặc “ý này không đồng nghĩa với điều gì?”.

#### Triad

Dùng khi bài có ba khái niệm ngang hàng cần phân biệt rõ. Mỗi mục phải có câu hỏi hoặc định nghĩa ngắn, dễ nhớ.

#### Full-width statement

Dùng cho một câu chuyển hoặc một insight đặc biệt mạnh. Tối đa 1–2 lần.

#### Closing

Kết thúc bằng một synthesis, không chỉ là “tóm tắt lại”. Closing nên nêu điều gì thay đổi trong cách ta nhìn vấn đề sau khi đọc bài.

### 5. Biên tập nội dung cho thị giác

Khi chuyển đoạn văn thành card, quote hoặc statement:

- giữ nguyên nghĩa;
- không làm mất điều kiện, giới hạn hay mức độ bất định quan trọng;
- không biến “có thể” thành “sẽ”, “ứng viên” thành “đã được chứng minh”, “liên quan” thành “gây ra”;
- không loại bỏ câu cảnh báo nếu nó là điều kiện để hiểu đúng claim;
- giữ nguyên các từ kỹ thuật quan trọng nếu chúng mang ý nghĩa chuyên môn;
- nếu rút gọn mạnh, dùng wording cho thấy đó là bản biên tập chứ không phải nguyên văn.

### 6. Thứ bậc typography

Dùng tối đa 4 cấp chính:

- **Display:** hero, con số lớn, closing statement;
- **Section heading:** tên chương hoặc luận điểm chính;
- **Subhead/card title:** distinction, case, khái niệm;
- **Body:** nội dung đọc dài.

Ưu tiên sans-serif cho display/heading và serif cho body để tạo tương phản editorial. Nếu cần file tự chứa, dùng system fonts thay vì phụ thuộc web font bên ngoài.

### 7. Hệ thống thị giác mặc định

Nếu người dùng không chỉ định style khác, dùng hệ thống gần với `references/reference-longform.html`:

- nền giấy sáng, chữ đậm, một màu accent;
- khoảng trắng lớn;
- line/border mảnh;
- card nền nhẹ;
- một hoặc hai section nền tối cho data/closing;
- tránh gradient, shadow nặng, animation gây xao nhãng;
- không dùng quá nhiều màu để phân loại nội dung.

Thiết kế phải tạo cảm giác editorial, nghiêm túc, hiện đại; không giống dashboard hoặc landing page bán hàng.

### 8. HTML output contract

Mặc định xuất **một file HTML tự chứa**:

- `<!doctype html>`;
- `lang="vi"`;
- UTF-8;
- responsive meta viewport;
- CSS nằm trong `<style>`;
- JavaScript tối thiểu, chỉ dùng khi có giá trị rõ ràng (ví dụ reading progress);
- không phụ thuộc CDN nếu không cần;
- semantic HTML: `header`, `main`, `section`, `blockquote`, `footer`, `details` khi phù hợp;
- đủ contrast;
- hỗ trợ `prefers-reduced-motion` nếu có motion;
- layout không tràn ngang ở 320px;
- typography đọc tốt ở mobile;
- print CSS cơ bản nếu tài liệu có tính lưu trữ/học thuật.

### 9. Accessibility

- Heading theo thứ tự hợp lý, không nhảy cấp vô lý.
- Không dùng màu là tín hiệu duy nhất.
- Quote phải là text thực, không phải ảnh.
- Nếu có hình ảnh do người dùng cung cấp, thêm `alt` mô tả phù hợp.
- Controls phải có label và keyboard focus.
- Đảm bảo font-size body mobile tối thiểu khoảng 16px.

### 10. QA trước khi giao

Kiểm tra ít nhất:

- 4–6 ý chính có thực sự nổi hơn phần còn lại không?
- Có highlight nào chỉ “đẹp” nhưng không quan trọng không?
- Có claim nào bị mạnh tay hơn nguồn không?
- Có quote nào thực ra là paraphrase không?
- Các con số có đủ context không?
- Người đọc lướt 20–30 giây có thể kể lại bài bằng 4–6 ý không?
- Desktop và mobile có tràn ngang không?
- Card có bị vỡ cột hoặc quá nhiều chữ không?
- References/citations có còn nguyên không?
- Closing có tổng hợp luận điểm thay vì chỉ lặp lại phần mở đầu không?

## Mẫu tư duy editorial

Đừng hỏi “đoạn này nên trang trí thế nào?”. Hãy hỏi:

> Nếu người đọc chỉ nhớ một điều sau section này, điều đó phải là gì?

Sau đó chọn component dựa trên câu trả lời.

## Mẫu storyboard ngắn

```text
HERO
Tiêu đề + tension / câu hỏi lớn

INTRO
2–4 đoạn đặt bối cảnh

MEMORY ANCHOR 01
Một big claim
→ các case study hỗ trợ

MEMORY ANCHOR 02
Một distinction / mô hình 3 tầng

MEMORY ANCHOR 03
Một data moment
→ ngay sau đó là counterpoint giải thích số liệu

MEMORY ANCHOR 04
Một distinction khái niệm

SYNTHESIS
Điều gì thay đổi khi các phần trên đặt cạnh nhau?

CLOSING
Một câu để người đọc mang theo sau khi đóng bài

REFERENCES
Giữ đầy đủ nguồn và ghi chú cần thiết
```

## Tiêu chí thành công

Một longform tốt không phải bài có nhiều hiệu ứng nhất. Nó là bài mà sau khi đọc, người đọc có thể nhắc lại đúng 4–6 luận điểm chính, hiểu quan hệ giữa chúng, và không bị thiết kế dẫn đến một kết luận mạnh hơn tài liệu nguồn.
