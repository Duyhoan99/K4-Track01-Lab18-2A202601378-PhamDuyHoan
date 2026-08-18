
## Thông tin bài làm và Phân công vai trò nhóm (Team Role Matrix)

- **Lớp / Khóa:** K4 - Track 01 (AI Product Development)
- **Tên nhóm:** 2T1H
- **Case đã chọn:** **Case B — AI Notes: Personal Learning Notes**
- **Repo cá nhân nộp bài:** Thư mục: `K4-Track01-Lab18-2A202601378-PhamDuyHoan`

**Thành viên nhóm:**

1. Phan Văn Tình(MHV: 2A202601430)

2. Phạm Duy Hoàn(MHV: 2A202601378)

3. Nguyễn Khánh Toàn(MHV: 2A202601843)

**2. Hypothesis Problem:**

Hypothesis Problem nhóm tiếp tục:

> Khi tham gia các buổi học hoặc đào tạo có mật độ thông tin cao, người học có thói quen ghi chép hoặc highlight gặp khó khăn trong việc lưu lại đầy đủ các điểm quan trọng và phần chưa hiểu vì tốc độ tiếp nhận thông tin nhanh hơn khả năng ghi chép, đồng thời ghi chú thường bị tách rời khỏi tài liệu gốc, dẫn đến việc phải mất nhiều thời gian tra cứu lại sau buổi học.
>



**Evidence ban đầu hỗ trợ giả thuyết:**



> Trong Practice Note Day 17, tester P-01 kể rằng khi tham gia buổi đào tạo trực tuyến về quản lý rủi ro, diễn giả trình bày nhanh khiến tester chỉ kịp ghi một phần nội dung và phải đánh dấu các chỗ chưa rõ bằng dấu “?”. Sau buổi học, tester mất khoảng 45 phút đối chiếu lại file PDF 60 trang để chuẩn bị cho bài test 15 phút. Điều này cho thấy việc ghi chú không kịp và mất liên kết với tài liệu gốc có thể tạo ra chi phí tra cứu đáng kể.

**Điều vẫn chưa được chứng minh:**

* Vấn đề này có xảy ra thường xuyên với phần lớn người học, hay chỉ xảy ra trong một số buổi học đặc biệt nhiều thông tin.
* Việc tra cứu lại ghi chú rời rạc có luôn gây tốn thời gian đáng kể với các người học khác hay không.
* Người học có thực sự quay lại sử dụng ghi chú sau buổi học thường xuyên không.
* Cách nào hỗ trợ tốt hơn: user tự chọn nội dung, AI đề xuất draft, hay AI tự tạo draft để user review.
* AI-generated notes có giúp người học ôn tập hiệu quả hơn so với ghi chú hiện tại hay không.
* Người học sẵn sàng trao cho AI bao nhiêu quyền quyết định trong việc chọn nội dung quan trọng hoặc “chưa hiểu”.



## Chặng 2 — Chọn ba Solution Options

### 1. Comparison Contract

Để phép so sánh A/B/C có ý nghĩa, cả ba option giữ nguyên cùng user, situation, task, desired outcome và content fixture.

| Thành phần                   | Quyết định chung cho A/B/C                                                                                                           |
| ------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------- |
| **Target user**          | Người học có thói quen ghi chép hoặc highlight khi tham gia các buổi học có mật độ thông tin cao.                        |
| **Situation**            | Đang học qua slide/PDF và gặp một điểm quan trọng hoặc chưa hiểu; sau đó cần ôn lại.                                    |
| **Task**                 | Tạo một tài nguyên ôn tập cá nhân từ những điểm quan trọng hoặc chưa hiểu, có thể quay lại đúng ngữ cảnh gốc.   |
| **Desired outcome**      | Người học có thể xem lại đúng điểm cần ôn mà không phải dò toàn bộ slide/PDF hoặc chỉ dựa vào ghi chú rời rạc. |
| **Content/data fixture** | Cùng một lesson RAG, cùng slide/PDF và cùng ba điểm: RAG, embeddings và semantic similarity.                                    |

### 2. Ba Solution Options

| Thành phần                   | **Option A — AI Q&A có lưu nguồn**                                                                                          | **Option B — Mục lục note–slide**                                                                               | **Option C — AI tạo quiz từ điểm “chưa hiểu”**                                                                          |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| **Solution mechanism**   | User hỏi trợ lý tại điểm chưa hiểu; AI trả lời dựa trên slide và user chọn lưu câu hỏi–trả lời kèm trang nguồn. | Hệ thống liên kết từng ghi chú hoặc đánh dấu của user với đúng trang slide PDF; không suy luận nội dung. | User đánh dấu đoạn “chưa hiểu”; AI tạo câu hỏi ôn tập ngắn từ đúng các đoạn đó và đính kèm trang nguồn.    |
| **User làm gì?**       | Chủ động hỏi, đọc câu trả lời, chọn lưu hoặc không lưu.                                                                 | Tự viết note/highlight; mở mục lục để xem lại.                                                                    | Đánh dấu phần chưa hiểu, làm quiz, xem lại slide khi cần.                                                                     |
| **AI làm gì?**         | Trả lời từ nội dung slide, hiển thị evidence/trang nguồn; không tự lưu.                                                     | Không có AI; hệ thống lưu liên kết page/slide theo thao tác của user.                                            | Tạo câu hỏi ôn tập từ phần user đã đánh dấu; chỉ là draft để user review.                                              |
| **Trigger**              | User bấm “Hỏi AI” tại đoạn đang vướng.                                                                                      | User tạo note/highlight hoặc mở lại note.                                                                             | User đánh dấu “Chưa hiểu”, sau đó bấm “Tạo quiz ôn tập”.                                                                |
| **Quyền quyết định** | User quyết định câu hỏi nào được lưu vào tài nguyên ôn tập.                                                            | User hoàn toàn quyết định nội dung note.                                                                            | User quyết định dùng, sửa, bỏ câu hỏi quiz hoặc tạo lại.                                                                    |
| **Trade-off chính**     | Hiểu nhanh và có ngữ cảnh, nhưng có thể làm gián đoạn việc học; AI có thể trả lời thiếu hoặc chưa chính xác.   | Kiểm soát cao, ít rủi ro sai, nhưng user vẫn phải tự ghi và tự tổng hợp.                                      | Giảm công sức chuyển điểm chưa hiểu thành hoạt động ôn tập, nhưng AI có thể tạo câu hỏi không đúng trọng tâm. |

### 3. Distance Check

**A khác B vì** A cho AI tham gia giải thích nội dung khi user đang vướng và user lưu kết quả; B không dùng AI để suy luận hay giải thích, chỉ liên kết note do user tạo với trang PDF gốc.

**B khác C vì** B giữ nguyên nội dung do user tự ghi và hỗ trợ tìm lại ngữ cảnh; C dùng AI biến các điểm user đánh dấu thành câu hỏi ôn tập để hỗ trợ recall.

**A khác C vì** A giải quyết sự vướng mắc ngay trong lúc học bằng hỏi–đáp có nguồn; C hỗ trợ ôn lại sau đó bằng quiz được tạo từ các điểm chưa hiểu.

```text
OPTION B
USER CREATES NOTES / SYSTEM LINKS CONTEXT

        ↓

OPTION A
USER ASKS / AI ANSWERS / USER SAVES

        ↓

OPTION C
USER MARKS UNCERTAINTY / AI CREATES REVIEW QUIZ / USER REVIEWS
```

### 4. Design Guardrails

- Option A phải có nút **Save to review notes**; AI không tự lưu câu hỏi hoặc câu trả lời.
- Option C phải cho user sửa, bỏ hoặc tạo lại quiz; mỗi câu hỏi cần có liên kết **View source: slide/page X**.
- Cả ba option cùng dùng lesson RAG và cùng hướng đến việc tạo tài nguyên ôn tập có liên kết ngữ cảnh.

---

## Phần thực hiện của cá nhân: Phạm Duy Hoàn (MHV: 2A202601378)

- **Solution tôi chọn thực hiện:** **Option A — [AI] Trợ lý ảo giải đáp nhanh các câu hỏi vướng mắc / điều khoản luật ngay trong lúc học dựa trên nội dung slide.**

### 1. Đóng góp của tôi trong bài làm Day 18
1. **Thiết kế chi tiết Human–AI Interaction cho Option A:** Định nghĩa 4 quyết định thiết kế, xây dựng bảng tương tác, chốt mức độ agency và cơ chế recovery khi AI trả lời sai/không tìm thấy thông tin.
2. **Xây dựng Interactive Micro-Prototype cho Option A (Chặng 4):** Xây dựng giao diện web tương tác [prototype-option-a.html](file:///d:/VIN_BaiLab/Track%201%20chuyen%20sau/K4-Track01-Lab18-2A202601378-PhamDuyHoan/prototype-option-a.html) với 3 trạng thái rõ ràng, hỗ trợ đầy đủ trigger hỏi đáp, trích nguồn 1-click, inline-edit, dismiss, undo và nút reset state.
3. **Trực tiếp Facilitate phiên kiểm thử Option A:** Điều phối phiên test thực tế với Tester T-02 (35 phút), ghi nhận quan sát trực tiếp, trích dẫn, ma sát và phản hồi của người học.
4. **Cập nhật dữ liệu cá nhân vào các tài liệu nhóm:** Điền kết quả Option A vào [three-option-design-sheet.md](file:///d:/VIN_BaiLab/Track%201%20chuyen%20sau/K4-Track01-Lab18-2A202601378-PhamDuyHoan/three-option-design-sheet.md), [prototype-link.md](file:///d:/VIN_BaiLab/Track%201%20chuyen%20sau/K4-Track01-Lab18-2A202601378-PhamDuyHoan/prototype-link.md) và [group-feedback-synthesis.md](file:///d:/VIN_BaiLab/Track%201%20chuyen%20sau/K4-Track01-Lab18-2A202601378-PhamDuyHoan/group-feedback-synthesis.md).
5. **Viết AI Support Log cá nhân:** Tự đánh giá quá trình tương tác với AI và ghi lại các điểm bản thân đã tự điều chỉnh.

---

### 2. Chặng 3 — Human–AI Design pass (Chi tiết Option A)

#### Bốn quyết định thiết kế
1. **Expectation (Kỳ vọng & Giới hạn):**
   - *Trước khi AI hoạt động:* Giao diện hiển thị placeholder định hướng rõ ràng: *"Hỏi nhanh điều khoản, định nghĩa hoặc nội dung từ tài liệu [Tên tài liệu.pdf]"*. User hiểu rõ AI là công cụ tra cứu nội bộ slide, không phải chatbot tự do.
   - *Capability:* Trích xuất định nghĩa, giải thích thuật ngữ, đối chiếu nội dung trong slide và gắn nhãn số trang/đoạn cụ thể (`Slide X, Đoạn Y`).
   - *Limit:* AI chỉ tra cứu nội dung trong slide bài học, không tự ý suy diễn hoặc tìm ngoài luồng; không thay thế văn bản quy phạm pháp luật chính thức.
2. **Role and Agency (Phân vai & Mức độ chủ động):**
   - *Phân vai:* User chủ động hỏi khi bị nghẽn, đọc câu trả lời và quyết định bấm *"Lưu vào Note"* hoặc bỏ qua. AI trả lời ngắn gọn và trích dẫn số trang nguồn; không tự ý lưu vào note.
   - *Agency tại Critical Moment:* **Ask / Suggest (không tự ý Act)** — AI chỉ hiển thị draft câu trả lời ở sidebar và chờ user bấm *"Lưu vào Note"*, tránh làm loãng ghi chú cá nhân của người học.
   - *Hậu quả khi sai:* User chỉ mất 3–5 giây đọc lướt; rất dễ phát hiện vì AI luôn dẫn kèm số trang slide gốc.
3. **Evidence and Uncertainty (Căn cứ & Xử lý bất định):**
   - *Evidence:* Thẻ trích dẫn trực quan (`Citation Badge`: *Slide 14 - Mục 2.3*) và đoạn trích dẫn nguyên văn ngắn.
   - *Uncertainty:* Khi câu hỏi ngoài phạm vi hoặc độ tin cậy thấp, AI thông báo rõ: *"Nội dung này không được đề cập rõ trong slide buổi học. Dưới đây là các phần gần nhất có liên quan: [...]"*.
4. **Control and Recovery (Kiểm soát & Phục hồi):**
   - *Kiểm soát:* Preview câu trả lời, Edit nội dung trước khi lưu, Dismiss nhanh bằng phím `Esc`/nút `X`, Undo/Delete ghi chú đã lưu.
   - *Phục hồi:* Khi AI trả lời sai/không tìm thấy: User bấm nút *"Mở slide liên quan"* để tự xem tài liệu hoặc bấm icon `?` để tra cứu lại sau mà không gián đoạn bài giảng.

#### Human–AI Decision Table cho Option A

| Tiêu chí / Quyết định | **Option A — Trợ lý AI Q&A giải đáp nhanh có lưu nguồn** *(Duy Hoàn thực hiện)* |
| :--- | :--- |
| **User làm gì? AI làm gì?** | **User:** Gõ/nói câu hỏi vướng mắc; đọc câu trả lời; chọn lưu vào note kèm nguồn hoặc đóng chat. <br>**AI:** Tra cứu semantic trên slide bài học, sinh câu trả lời ngắn gọn + đính kèm số trang nguồn. |
| **AI Act / Ask / Don't Act? Vì sao?** | **Ask / Suggest**: AI sinh câu trả lời nhưng **chờ User bấm Lưu**. Giúp user kiểm soát trọn vẹn chất lượng note cá nhân. |
| **User hiểu capability/limit bằng gì?** | Placeholder hướng dẫn, badge hiển thị tài liệu nguồn đang tra cứu, disclaimer *"Chỉ trả lời từ nội dung slide bài học"*. |
| **Evidence & Uncertainty được thể hiện thế nào?** | Trích dẫn trực tiếp `Slide X, đoạn Y`. Nếu độ tin cậy thấp, báo rõ *"Không tìm thấy trong tài liệu"*. |
| **User kiểm soát và recovery thế nào?** | Preview câu trả lời, edit nội dung trước khi lưu, dismiss bằng phím `Esc`/nút `X`, mở slide gốc bằng 1 click. |

#### Feedback and data check
- Phản hồi của user (Like/Dislike, Edit draft) chỉ phục vụ tối ưu phiên học hiện tại, không làm biến đổi nội dung gốc của bài giảng.
- Dữ liệu sử dụng giới hạn trong phạm vi slide bài học và câu hỏi tra cứu. Hỗ trợ xóa lịch sử hoặc dùng chế độ *"Phiên riêng tư (Incognito Session)"*.

#### Tự kiểm·GATE 3 — Human Control
- [x] **Rõ ràng vai trò Human & AI:** User toàn quyền quyết định nội dung nạp vào sổ tay; AI đóng vai trò tra cứu và dẫn nguồn.
- [x] **Agency phù hợp rủi ro:** Vận hành ở mức **Suggest/Ask**, triệt tiêu nguy cơ AI tự động ghi đè hoặc tạo rác dữ liệu.
- [x] **Cơ chế kiểm soát & Phục hồi hoàn chỉnh:** Cung cấp đầy đủ Preview, Edit, Dismiss (`Esc`/`X`), Undo và liên kết 1-click quay lại tài liệu gốc.

---

### 3. Chặng 4 — Build Micro-Prototype (Phần việc của tôi: Option A)

#### 1. Scope chuẩn của Micro-Prototype Option A
- **Trạng thái 1: COMMON CONTEXT (Màn hình bài học chung):**
  - Màn hình bài giảng slide PDF (Slide 14/60: *Đo lường sự tương đồng ngữ nghĩa: Cosine Similarity*).
  - Khung Trợ lý AI tích hợp bên phải với huy hiệu tài liệu nguồn `RAG_Lesson.pdf` và các nút gợi ý câu hỏi nhanh (Quick Prompts).
- **Trạng thái 2: CRITICAL INTERACTION (Tương tác hỏi–đáp và trích nguồn):**
  - Tester gửi câu hỏi (tự gõ hoặc 1-click); AI phản hồi nhanh trong 1 giây với 2 gạch đầu dòng tóm tắt.
  - Thẻ trích dẫn `🔗 Trích nguồn: Slide 14` có thể click để nhảy/highlight trực tiếp slide gốc.
  - Xử lý câu hỏi không có trong tài liệu (Uncertainty): AI cảnh báo rõ và chỉ gợi ý các slide gần nhất.
- **Trạng thái 3: RESULT / USER DECISION & RECOVERY (Quyết định của người học):**
  - Người học có 4 lựa chọn kiểm soát rõ ràng:
    1. Bấm **"📌 Lưu vào Note"**: Lưu vào danh sách sổ tay bên dưới + Toast thông báo kèm nút **"Hoàn tác (Undo)"**.
    2. Bấm **"✏️ Sửa trước khi lưu"**: Mở modal Inline Edit cho phép chỉnh sửa lại câu chữ theo ý mình.
    3. Bấm **"Bỏ qua (Esc)"**: Làm mờ và ẩn câu trả lời không ưng ý.
    4. Bấm nút **"⟲ Reset State"**: Khôi phục toàn bộ prototype về trạng thái Common Context ban đầu.

#### 2. Prototype Annotation (Dành cho Facilitator kiểm thử Option)

```text
OPTION B PROTOTYPE (AI In-session Q&A Assistant with Citation, Failure Recovery & User-driven Save)
We expect the tester to: Thử bấm câu hỏi nhanh hoặc gõ câu hỏi khi gặp đoạn kiến thức ở Slide 5, 12, 14, đọc câu trả lời và số trang nguồn của AI, sau đó thử nghiệm bấm "Lưu vào Note", "Sửa trước khi lưu" hoặc "⚠️ Báo sai / Hỏi Giảng viên".
Watch for: Tester có chú ý và click vào thẻ trích dẫn [Slide X] để đối chiếu không; tester phản ứng thế nào khi AI trả lời sai/không đúng ý; tester có sử dụng nút gửi câu hỏi cho giảng viên không.
Do not explain: Không chỉ tay bảo tester phải bấm nút nào; không giải thích thay cho câu trả lời của AI; để tester tự khám phá nút Mở slide nguồn, nút Inline Edit và nút Hoàn tác (Undo).
```

#### 3. Tự kiểm·GATE 4 — Test-ready
- [x] **Tự vận hành:** Một tester chưa từng thấy prototype có thể tự mở file [prototype-option-a.html](file:///d:/VIN_BaiLab/Track%201%20chuyen%20sau/K4-Track01-Lab18-2A202601378-PhamDuyHoan/prototype-option-a.html) và hoàn thành task hỏi–đối chiếu–lưu mà không cần người bên cạnh thuyết minh.
- [x] **Dữ liệu thật:** Nội dung bài học và câu trả lời AI đều lấy từ kịch bản chuẩn RAG & Vector Embeddings 60 trang.
- [x] **Có cơ chế lấy lại quyền kiểm soát:** Đầy đủ Inline Edit, Dismiss, Undo và nút Reset quay về điểm xuất phát.

---

### 4. Prototype Feedback của phiên tôi Facilitate

- **Phiên kiểm thử:** Do chính **Phạm Duy Hoàn facilitate** (Tester T-02, 35 phút).
- **Quan sát chính:**
  - *Tốc độ phản hồi & Bằng chứng:* AI trả lời sau 1.5 giây, thẻ `[Slide 14]` mở đúng vị trí slide giúp đối chiếu ngay mà không cần dừng bài giảng.
  - *Sự kiểm soát:* Tester đánh giá rất cao việc AI không tự động lưu mà trao quyền cho người học bấm *"Lưu vào Note"*.
  - *Điểm nghẽn:* Người học ngại gõ câu hỏi dài trong lúc nghe giảng; mong muốn có nút gợi ý câu hỏi 1-click và tính năng inline-edit trước khi lưu.
- **Next Changes cho Option A:** Bổ sung Quick Prompts (*"Tóm tắt slide này"*) để giảm thao tác gõ phím và thêm tính năng Inline Edit trước khi lưu.

📄 *Xem toàn văn biên bản test:* [prototype-feedback-note.md](file:///d:/VIN_BaiLab/Track%201%20chuyen%20sau/K4-Track01-Lab18-2A202601378-PhamDuyHoan/prototype-feedback-note.md).

---

### 5. AI Support Log của riêng tôi

- **AI đã giúp gì:** Gợi ý khung cấu trúc 4 quyết định thiết kế, hỗ trợ code HTML/CSS/JS cho prototype tương tác và soạn câu hỏi debriefing cho buổi test Option A.
- **AI sai / thiên kiến ở đâu:** Ban đầu AI luôn đề xuất cơ chế "Full Act" (tự động tóm tắt và tự chèn note), đồng thời vẽ thêm nhiều màn hình rườm rà ngoài phạm vi.
- **Tôi tự sửa:** Chuyển đổi Agency về **Ask / Suggest** với nút Save chủ động; tự thiết kế tính năng Inline Edit, phím tắt Dismiss `Esc` và thẻ trích dẫn 1-click.

📄 *Xem toàn văn nhật ký:* [ai-support-log.md](file:///d:/VIN_BaiLab/Track%201%20chuyen%20sau/K4-Track01-Lab18-2A202601378-PhamDuyHoan/ai-support-log.md).
