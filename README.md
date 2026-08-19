## Thông tin bài làm và Phân công vai trò nhóm (Team Role Matrix)

- **Lớp / Khóa:** K4 - Track 01 (AI Product Development)
- **Tên nhóm:** 2T1H
- **Case đã chọn:** **Case B — AI Notes: Personal Learning Notes**
- **Repo cá nhân nộp bài:** Thư mục: `K4-Track01-Lab18-2A202601378-PhamDuyHoan`

**Thành viên nhóm & Phân công giải pháp:**

1. **Phạm Duy Hoàn (MHV: 2A202601378):** Phụ trách **Option A — User-Led Smart Bookmark**
2. **Nguyễn Khánh Toàn (MHV: 2A202601843):** Phụ trách **Option B — Co-create AI Draft Notes**
3. **Phan Văn Tình (MHV: 2A202601430):** Phụ trách **Option C — Proactive AI Notes**

---

**2. Hypothesis Problem:**

Hypothesis Problem nhóm tiếp tục:

> Khi tham gia các buổi học hoặc đào tạo có mật độ thông tin cao, người học có thói quen ghi chép hoặc highlight gặp khó khăn trong việc lưu lại đầy đủ các điểm quan trọng và phần chưa hiểu vì tốc độ tiếp nhận thông tin nhanh hơn khả năng ghi chép, đồng thời ghi chú thường bị tách rời khỏi tài liệu gốc, dẫn đến việc phải mất nhiều thời gian tra cứu lại sau buổi học.

**Evidence ban đầu hỗ trợ giả thuyết:**

> Trong Practice Note Day 17, tester P-01 kể rằng khi tham gia buổi đào tạo trực tuyến về quản lý rủi ro, diễn giả trình bày nhanh khiến tester chỉ kịp ghi một phần nội dung và phải đánh dấu các chỗ chưa rõ bằng dấu “?”. Sau buổi học, tester mất khoảng 45 phút đối chiếu lại file PDF 60 trang để chuẩn bị cho bài test 15 phút. Điều này cho thấy việc ghi chú không kịp và mất liên kết với tài liệu gốc có thể tạo ra chi phí tra cứu đáng kể.

**Điều vẫn chưa được chứng minh:**

* Vấn đề này có xảy ra thường xuyên với phần lớn người học, hay chỉ xảy ra trong một số buổi học đặc biệt nhiều thông tin.
* Việc tra cứu lại ghi chú rời rạc có luôn gây tốn thời gian đáng kể với các người học khác hay không.
* Người học có thực sự quay lại sử dụng ghi chú sau buổi học thường xuyên không.
* Cách nào hỗ trợ tốt hơn: User tự kiểm soát capture (User-Led), AI gợi ý draft từng mẩu để user duyệt (Co-create), hay AI tự tổng hợp toàn bộ bài học (Proactive).
* Người học sẵn sàng trao cho AI bao nhiêu quyền tự chủ (Agency) trong việc chọn lọc nội dung ghi chú bài học.

---

## Chặng 2 — Chọn ba Solution Options

### 1. Comparison Contract

Để phép so sánh A/B/C có ý nghĩa, cả ba option giữ nguyên cùng user, situation, task, desired outcome và content fixture.

| Thành phần | Quyết định chung cho A/B/C |
| :--- | :--- |
| **Target user** | Người học có thói quen ghi chép hoặc highlight khi tham gia các buổi học có mật độ thông tin cao. |
| **Situation** | Đang học qua slide/PDF và gặp một điểm quan trọng hoặc chưa hiểu; sau đó cần lưu lại để ôn tập. |
| **Task** | Tạo một tài nguyên ghi chú bài học cá nhân từ những điểm quan trọng hoặc chưa hiểu, có thể quay lại đúng ngữ cảnh gốc. |
| **Desired outcome** | Người học có thể xem lại đúng điểm cần ôn mà không phải dò toàn bộ slide/PDF hoặc chỉ dựa vào ghi chú rời rạc. |
| **Content/data fixture** | Cùng một lesson *AI Fundamentals & Model Risk (10 phút)*, cùng slide bài học (Slide 5: Model Risk, Slide 6: Mitigation, Slide 8: Governance) và live transcript. |

### 2. Ba Solution Options

| Thành phần | **Option A — User-Led Smart Bookmark** *(Duy Hoàn)* | **Option B — Co-create AI Draft Notes** *(Khánh Toàn)* | **Option C — Proactive AI Notes** *(Văn Tình)* |
| :--- | :--- | :--- | :--- |
| **Solution mechanism** | Người học vẫn là người kiểm soát nội dung cần capture. Khi họ thấy một thông tin quan trọng hoặc không kịp ghi, họ bấm **Mark current moment**. Hệ thống lưu timestamp, slide hiện tại, và một note ngắn nếu user nhập vào. | AI tạo **draft notes** từ transcript bài học và context slide. Người học review từng draft, sau đó chọn keep, edit, remove, hoặc mở source để kiểm tra. | AI **tự động capture và tổ chức** nội dung bài học thành một structured note hoàn chỉnh. Người học chủ yếu review output cuối, kiểm tra coverage nếu cần, rồi quyết định accept, edit, hoặc reject notes. |
| **User làm gì?** | Chủ động bấm "Mark current moment" khi nghe điểm quan trọng/chưa rõ; gõ thêm note ngắn nếu muốn. | Đọc lướt từng draft card do AI sinh ra $\rightarrow$ chọn Keep, Edit, Remove hoặc mở Source để kiểm tra. | Tập trung 100% nghe giảng; khi kết thúc bài, đọc toàn bộ bản structured note, kiểm tra coverage, chọn Accept/Edit/Reject. |
| **AI làm gì?** | Ghi nhận timestamp, liên kết đúng số trang slide và note ngắn của user; không tự ý suy diễn nội dung khi chưa có lệnh. | Lắng nghe transcript và context slide, tự động tạo các draft notes ngắn dạng thẻ gợi ý theo thời gian thực. | Tự động phân tích, trích xuất, cấu trúc hóa và biên soạn toàn bộ nội dung bài học thành một bản ghi chú hoàn chỉnh. |
| **Trigger** | Người học bấm "Mark current moment" (hoặc phím tắt nhanh `[M]`). | Xuất hiện tự động theo từng ý mới trong transcript hoặc khi chuyển slide. | Kết thúc bài học (End-of-lesson trigger). |
| **Quyền quyết định** | Người học toàn quyền quyết định thời điểm và nội dung được capture. | Người học kiểm duyệt từng draft trước khi đưa vào sổ tay chính thức. | Người học kiểm soát ở đầu ra cuối cùng (Batch Review: Accept / Edit / Reject). |
| **Trade-off chính** | Kiểm soát tối đa, 0% rủi ro AI ảo giác, nhưng người học vẫn phải phân tâm bấm nút trong lúc nghe giảng. | Giảm đáng kể công gõ chữ, nhưng người học cần phân tâm nhẹ để liên tục review các draft card xuất hiện. | Người học hoàn toàn rảnh tay khi học, nhưng mất công kiểm tra lại toàn bộ bản note dài ở cuối bài và có nguy cơ AI bỏ sót ý quan trọng. |

### 3. Distance Check (Phổ mức độ tự chủ Human–AI)

**A khác B vì:** Option A hoàn toàn do người học chủ động kích hoạt (User-Led Capture) và chỉ lưu vị trí/note ngắn của user; Option B do AI chủ động tạo trước các đoạn tóm tắt (Draft Notes) theo thời gian thực để user duyệt từng cái.

**B khác C vì:** Option B cho user tương tác và duyệt theo từng mẩu nhỏ (Micro Review: Keep/Edit/Remove từng draft trong khi học); Option C dồn toàn bộ việc xử lý cho AI và user chỉ review một lần ở cuối bài học (Macro Review: Accept/Edit/Reject bản Structured Note hoàn chỉnh).

**A khác C vì:** Option A là mức tự chủ AI thấp nhất (User kiểm soát 100%); Option C là mức tự chủ AI cao nhất (AI tự động làm tất cả từ đầu đến cuối).

```text
       MỨC TỰ CHỦ THẤP (USER-LED)                MỨC TỰ CHỦ TRUNG BÌNH (CO-CREATE)                MỨC TỰ CHỦ CAO (PROACTIVE)
┌──────────────────────────────────────┐     ┌──────────────────────────────────────┐     ┌──────────────────────────────────────┐
│  OPTION A: USER-LED SMART BOOKMARK   │     │  OPTION B: CO-CREATE AI DRAFT NOTES  │     │     OPTION C: PROACTIVE AI NOTES     │
│  • User bấm "Mark current moment"    │ ──> │  • AI sinh draft notes thời gian thực │ ──> │  • AI tự capture & tổ chức toàn bộ    │
│  • Lưu timestamp, slide, note ngắn   │     │  • User review: Keep/Edit/Remove     │     │  • User review cuối: Accept/Edit/Rej │
│  👉 Phụ trách: Phạm Duy Hoàn         │     │  👉 Phụ trách: Nguyễn Khánh Toàn     │     │  👉 Phụ trách: Phan Văn Tình         │
└──────────────────────────────────────┘     └──────────────────────────────────────┘     └──────────────────────────────────────┘
```

### 4. Design Guardrails

- **Option A (User-Led):** Phải có nút **Mark current moment** bấm 1-chạm hoặc phím tắt `[M]`; tự động bắt đúng số slide và timestamp; hỗ trợ gõ note ngắn tùy chọn.
- **Option B (Co-create):** Mỗi draft note do AI tạo ra phải có đủ 4 hành động rõ ràng: **Keep**, **Edit**, **Remove**, và **View Source (Slide/Transcript)**.
- **Option C (Proactive):** Phải cung cấp màn hình **Coverage Check** và bộ 3 hành động quyết định ở cuối bài: **Accept all**, **Edit section**, **Reject**.

---

## Phần thực hiện của cá nhân: Phạm Duy Hoàn (MHV: 2A202601378)

- **Solution tôi chọn thực hiện:** **Option A — User-Led Smart Bookmark** *(Người học kiểm soát capture; bấm Mark moment để lưu timestamp, slide hiện tại và note ngắn)*.

### 1. Đóng góp của tôi trong bài làm Day 18
1. **Thiết kế chi tiết Human–AI Interaction cho Option A:** Định nghĩa 4 quyết định thiết kế cho cơ chế User-Led Smart Bookmark, xây dựng bảng tương tác, chốt mức độ agency và cơ chế recovery khi bấm nhầm hoặc muốn sửa note.
2. **Xây dựng Interactive Micro-Prototype cho Option A (Chặng 4):** Xây dựng giao diện web tương tác [prototype-option-a.html](prototype%20_canhan/prototype-option-a.html) với nút 1-chạm *"Mark Current Moment"*, tự động bắt timestamp & slide, ô nhập note ngắn tùy chọn, và danh sách bookmark feed với đầy đủ Edit/Delete/Open slide context.
3. **Trực tiếp Facilitate phiên kiểm thử Option A:** Điều phối phiên test thực tế với Tester T-02 (35 phút), ghi nhận quan sát trực tiếp, trích dẫn, ma sát và phản hồi của người học.
4. **Cập nhật dữ liệu cá nhân vào các tài liệu nhóm:** Điền kết quả Option A vào [three-option-design-sheet.md](three-option-design-sheet.md), [prototype-link.md](prototype-link.md) và [group-feedback-synthesis.md](group-feedback-synthesis.md).
5. **Viết AI Support Log cá nhân:** Tự đánh giá quá trình tương tác với AI và ghi lại các điểm bản thân đã tự điều chỉnh.

---

### 2. Chặng 3 — Human–AI Design pass (Chi tiết Option A)

#### Bốn quyết định thiết kế
1. **Expectation (Kỳ vọng & Giới hạn):**
   - *Trước khi hoạt động:* Giao diện hiển thị rõ ràng nút bấm *"🔖 Mark current moment"* kèm phím tắt `[M]`. User hiểu rõ hệ thống sẽ đánh dấu đúng mốc thời gian và trang slide đang mở, kèm ghi chú ngắn nếu user muốn nhập.
   - *Capability:* Bắt chính xác timestamp (`07:18`), số trang slide hiện tại (`Slide 5, 6, 8`), và lưu kèm note cá nhân của user.
   - *Limit:* Hệ thống không tự ý tóm tắt dài dòng hay tự ý thêm bớt nội dung khi user chưa bấm Mark.
2. **Role and Agency (Phân vai & Mức độ chủ động):**
   - *Phân vai:* User toàn quyền quyết định khi nào cần đánh dấu khoảnh khắc quan trọng. Hệ thống đóng vai trò thư ký ghi nhớ tọa độ chính xác.
   - *Agency tại Critical Moment:* **User-Led (Don't Act without trigger)** — Hệ thống chỉ ghi nhận khi có thao tác bấm từ người học, đảm bảo sổ tay hoàn toàn sạch sẽ và chỉ chứa những gì người học thực sự quan tâm.
   - *Hậu quả khi sai:* User chỉ mất 1 click xóa hoặc sửa; rủi ro bằng 0 vì nội dung do chính user kiểm soát.
3. **Evidence and Uncertainty (Căn cứ & Xử lý bất định):**
   - *Evidence:* Thẻ bookmark luôn hiển thị rõ `07:18 ➔ Slide 5: Model Risk`. Khi click vào thẻ, slide bài giảng lập tức nhảy về đúng trang đó và phát sáng viền xanh đối chiếu.
   - *Uncertainty:* Nếu user bấm Mark mà không nhập chữ, hệ thống tự động gán nhãn *"Đánh dấu khoảnh khắc tại Slide X"* để user không bị rỗng nội dung.
4. **Control and Recovery (Kiểm soát & Phục hồi):**
   - *Kiểm soát:* Nút 1-chạm Mark moment, Inline Edit trực tiếp trên thẻ bookmark, Phím tắt bàn phím `[M]`, Nút Xóa (Remove).
   - *Phục hồi:* Hỗ trợ nút Edit sửa lại note bất cứ lúc nào; nút Reset State khôi phục trạng thái ban đầu.

#### Human–AI Decision Table cho Option A

| Tiêu chí / Quyết định | **Option A — User-Led Smart Bookmark** *(Duy Hoàn thực hiện)* |
| :--- | :--- |
| **User làm gì? AI/Hệ thống làm gì?** | **User:** Bấm nút "Mark current moment" (hoặc phím `M`) khi nghe điểm quan trọng; gõ thêm note ngắn nếu muốn. <br>**Hệ thống:** Lưu chính xác timestamp, liên kết đúng số trang slide và note cá nhân vào sổ tay. |
| **AI Act / Ask / Don't Act? Vì sao?** | **Don't Act without trigger (User-Led)**: Chỉ kích hoạt khi user bấm nút. Giúp người học kiểm soát 100% nội dung sổ tay. |
| **User hiểu capability/limit bằng gì?** | Nút bấm có gắn phím tắt rõ ràng, nhãn hiển thị slide đang theo dõi, hướng dẫn *"Hệ thống sẽ lưu vị trí slide & timestamp hiện tại"*. |
| **Evidence & Uncertainty được thể hiện thế nào?** | Thẻ bookmark gắn nhãn `Timestamp ➔ Slide X`. Click vào thẻ sẽ mở đúng slide và highlight viền xanh đối chiếu. |
| **User kiểm soát và recovery thế nào?** | Sửa trực tiếp (Inline Edit), Xóa thẻ bookmark (Remove), xuất tóm tắt (Export), mở lại slide gốc bằng 1-click. |

#### Feedback and data check
- Phản hồi của user (thêm note, sửa, xóa bookmark) được lưu cục bộ trong phiên học, không làm thay đổi bài giảng gốc.
- Dữ liệu hoàn toàn riêng tư thuộc quyền sở hữu của người học.

#### Tự kiểm·GATE 3 — Human Control
- [x] **Rõ ràng vai trò Human & AI:** User là người kiểm soát hoàn toàn việc capture nội dung; hệ thống đảm bảo liên kết chính xác với ngữ cảnh slide.
- [x] **Agency phù hợp rủi ro:** Vận hành ở mức **User-Led**, triệt tiêu nguy cơ AI tự động tạo rác hoặc hiểu sai ý định của người học.
- [x] **Cơ chế kiểm soát & Phục hồi hoàn chỉnh:** Cung cấp đầy đủ Inline Edit, Delete, Undo và 1-click quay lại trang slide gốc.

---

### 3. Chặng 4 — Build Micro-Prototype (Phần việc của tôi: Option A)

#### 1. Scope chuẩn của Micro-Prototype Option A
- **Trạng thái 1: COMMON CONTEXT (Màn hình bài học chung):**
  - Màn hình bài giảng slide PDF (Slide 5: Model Risk, Slide 6: Mitigation, Slide 8: Governance) với thanh timeline 10 phút và live transcript.
  - Khung Smart Bookmark bên phải với nút bấm 1-chạm **"🔖 Mark current moment"** (Phím tắt `[M]`) và ô nhập note ngắn.
- **Trạng thái 2: CRITICAL INTERACTION (Đánh dấu khoảnh khắc & Ghi chú nhanh):**
  - Người học bấm *"Mark current moment"*: Thẻ bookmark được tạo ngay lập tức trong 0.1 giây, tự động đính kèm `Slide 5` và `Timestamp 07:18`.
  - Hỗ trợ gõ nhanh 1 dòng note cá nhân: *"Chưa kịp ghi 3 exception cases, cần xem lại slide này"*.
- **Trạng thái 3: RESULT / USER DECISION & RECOVERY (Quản lý & Đối chiếu Bookmark):**
  - Danh sách Smart Bookmarks hiển thị trong mục *My review points*.
  - Khi click vào bất kỳ bookmark nào, slide bên trái lập tức chuyển đến đúng trang slide tương ứng và highlight viền xanh.
  - Hỗ trợ đầy đủ các nút kiểm soát: **✏️ Edit note**, **🗑️ Remove bookmark**, **📋 Export structured summary**, **⟲ Reset prototype**.

#### 2. Prototype Annotation (Dành cho Facilitator kiểm thử Option A)

```text
OPTION A PROTOTYPE (User-Led Smart Bookmark with Timestamp, Slide Linking & Quick Note)
We expect the tester to: Thử bấm nút "Mark current moment" khi đang xem slide bài giảng (hoặc nhấn phím M), thử gõ một dòng ghi chú ngắn cá nhân, sau đó chuyển sang slide khác và bấm vào thẻ bookmark đã lưu để kiểm tra xem slide có tự động nhảy về đúng trang hay không.
Watch for: Tester có thao tác bấm Mark nhanh chóng không; tester có gặp khó khăn khi vừa nghe giảng vừa gõ note không; tester có sử dụng tính năng click vào bookmark để đối chiếu lại slide gốc không.
Do not explain: Không hướng dẫn tester phải bấm nút nào; để tester tự bấm nút "Mark current moment", tự sửa nội dung note và tự trải nghiệm cơ chế đồng bộ slide.
```

#### 3. Tự kiểm·GATE 4 — Test-ready
- [x] **Tự vận hành:** Một tester chưa từng thấy prototype có thể tự mở file [prototype-option-a.html](prototype%20_canhan/prototype-option-a.html) và hoàn thành task đánh dấu–ghi chú–đối chiếu slide mà không cần hướng dẫn.
- [x] **Dữ liệu thật:** Slide bài học AI Fundamentals & Model Risk thực tế với 3 mốc kiến thức rõ ràng.
- [x] **Có cơ chế lấy lại quyền kiểm soát:** Đầy đủ Inline Edit, Delete bookmark, Export và nút Reset prototype.

---

### 4. Prototype Feedback của phiên tôi Facilitate

- **Phiên kiểm thử:** Do chính **Phạm Duy Hoàn facilitate** (Tester T-02, 35 phút).
- **Quan sát chính:**
  - *Tốc độ & Tính kiểm soát:* Tester đánh giá nút "Mark current moment" rất tiện lợi vì chỉ mất 1 click để ghi nhớ mốc slide mà không phải dừng lại gõ chữ dài dòng.
  - *Đối chiếu tài liệu:* Tester rất thích tính năng bấm vào thẻ bookmark để slide tự nhảy về đúng trang bài giảng.
  - *Ma sát:* Tester đề xuất hỗ trợ phím tắt bàn phím (nhấn phím `M` để đánh dấu nhanh) để không phải rê chuột trong lúc đang tập trung nhìn slide.
- **Next Changes cho Option A:** Thêm phím tắt `[M]` để đánh dấu tức thì và cho phép chỉnh sửa nội dung ghi chú trực tiếp ngay trên thẻ bookmark (Inline Edit).

📄 *Xem toàn văn biên bản test:* [prototype-feedback-note.md](prototype-feedback-note.md).

---

### 5. AI Support Log của riêng tôi

- **AI đã giúp gì:** Hỗ trợ cấu trúc tài liệu theo đúng chuẩn so sánh A/B/C, sinh code HTML/CSS/JS cho prototype tương tác Option A và gợi ý kịch bản test.
- **AI sai / thiên kiến ở đâu:** Ban đầu AI luôn có xu hướng biến giải pháp thành chatbot hỏi đáp phức tạp (AI Tutor) thay vì tập trung vào trải nghiệm ghi chép sổ tay (AI Notes).
- **Tôi tự sửa:** Chỉnh lại toàn bộ định hướng về **User-Led Smart Bookmark**, nhấn mạnh quyền kiểm soát của người học, thiết kế tính năng 1-chạm capture và liên kết slide trực tiếp.

📄 *Xem toàn văn nhật ký:* [ai-support-log.md](ai-support-log.md).
