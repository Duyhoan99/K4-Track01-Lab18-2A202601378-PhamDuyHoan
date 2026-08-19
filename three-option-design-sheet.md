# Three-Option Design Sheet — Day 18

- **Khóa / Lớp:** K4 - Track 01 (AI Product Development)
- **Nhóm:** 2T1H
- **Case:** Case B — AI Notes: Personal Learning Notes
- **Thành viên cập nhật:** **Phạm Duy Hoàn (MHV: 2A202601378)** — *Phụ trách Option A*

---

## 1. Comparison Contract (Khung đối chiếu chung)

| Thành phần | Quyết định chung cho A/B/C |
| :--- | :--- |
| **Target user** | Người học có thói quen ghi chép hoặc highlight khi tham gia các buổi học có mật độ thông tin cao. |
| **Situation** | Đang học qua slide/PDF và gặp một điểm quan trọng hoặc chưa hiểu; sau đó cần lưu lại để ôn tập. |
| **Task** | Tạo một tài nguyên ghi chú bài học cá nhân từ những điểm quan trọng hoặc chưa hiểu, có thể quay lại đúng ngữ cảnh gốc. |
| **Desired outcome** | Người học có thể xem lại đúng điểm cần ôn mà không phải dò toàn bộ slide/PDF hoặc chỉ dựa vào ghi chú rời rạc. |
| **Content/data fixture** | Cùng một lesson *AI Fundamentals & Model Risk (10 phút)*, cùng slide bài học (Slide 5: Model Risk, Slide 6: Mitigation, Slide 8: Governance) và live transcript. |

---

## 2. Chi tiết 3 Solution Options

| Thành phần | **Option A — User-Led Smart Bookmark** *(Duy Hoàn thực hiện)* | **Option B — Co-create AI Draft Notes** *(Khánh Toàn thực hiện)* | **Option C — Proactive AI Notes** *(Văn Tình thực hiện)* |
| :--- | :--- | :--- | :--- |
| **Người phụ trách** | **Phạm Duy Hoàn (2A202601378)** | **Nguyễn Khánh Toàn (2A202601843)** | **Phan Văn Tình (2A202601430)** |
| **Solution mechanism** | Người học vẫn là người kiểm soát nội dung cần capture. Khi họ thấy một thông tin quan trọng hoặc không kịp ghi, họ bấm **Mark current moment**. Hệ thống lưu timestamp, slide hiện tại, và một note ngắn nếu user nhập vào. | AI tạo **draft notes** từ transcript bài học và context slide. Người học review từng draft, sau đó chọn keep, edit, remove, hoặc mở source để kiểm tra. | AI **tự động capture và tổ chức** nội dung bài học thành một structured note hoàn chỉnh. Người học chủ yếu review output cuối, kiểm tra coverage nếu cần, rồi quyết định accept, edit, hoặc reject notes. |
| **User làm gì?** | Chủ động bấm "Mark current moment" khi nghe điểm quan trọng/chưa rõ; gõ thêm note ngắn nếu muốn. | Đọc lướt từng draft card do AI sinh ra $\rightarrow$ chọn Keep, Edit, Remove hoặc mở Source để kiểm tra. | Tập trung 100% nghe giảng; khi kết thúc bài, đọc toàn bộ bản structured note, kiểm tra coverage, chọn Accept/Edit/Reject. |
| **AI làm gì?** | Ghi nhận timestamp, liên kết đúng số trang slide và note ngắn của user; không tự ý suy diễn nội dung khi chưa có lệnh. | Lắng nghe transcript và context slide, tự động tạo các draft notes ngắn dạng thẻ gợi ý theo thời gian thực. | Tự động phân tích, trích xuất, cấu trúc hóa và biên soạn toàn bộ nội dung bài học thành một bản ghi chú hoàn chỉnh. |
| **Trigger** | Người học bấm "Mark current moment" (hoặc phím tắt nhanh `[M]`). | Xuất hiện tự động theo từng ý mới trong transcript hoặc khi chuyển slide. | Kết thúc bài học (End-of-lesson trigger). |
| **Quyền quyết định** | Người học toàn quyền quyết định thời điểm và nội dung được capture. | Người học kiểm duyệt từng draft trước khi đưa vào sổ tay chính thức. | Người học kiểm soát ở đầu ra cuối cùng (Batch Review: Accept / Edit / Reject). |
| **Trade-off chính** | Kiểm soát tối đa, 0% rủi ro AI ảo giác, nhưng người học vẫn phải phân tâm bấm nút trong lúc nghe giảng. | Giảm đáng kể công gõ chữ, nhưng người học cần phân tâm nhẹ để liên tục review các draft card xuất hiện. | Người học hoàn toàn rảnh tay khi học, nhưng mất công kiểm tra lại toàn bộ bản note dài ở cuối bài và có nguy cơ AI bỏ sót ý quan trọng. |

---

## 3. Distance Check & Design Guardrails (Phần Option A)

- **Distance Check (Định vị Option A):**
  - Option A đại diện cho mức **Tự chủ AI Thấp nhất (User-Led / Low AI Agency)** trong phổ giải pháp. Người học giữ trọn 100% quyền kiểm soát việc đánh dấu khoảnh khắc (Capture Moment) và nội dung ghi chú, AI/Hệ thống chỉ đóng vai trò thư ký ghi nhận tọa độ chính xác (Timestamp + Slide Number).
- **Design Guardrails cho Option A:**
  - Nút **Mark current moment** phải hỗ trợ thao tác 1-chạm hoặc phím tắt nhanh `[M]`.
  - Thẻ bookmark bắt buộc phải lưu kèm số trang `Slide X` và `Timestamp` để người học click là quay lại đúng vị trí slide gốc.
  - Cung cấp đầy đủ tính năng Inline Edit, Delete bookmark, Export và nút Reset prototype.
