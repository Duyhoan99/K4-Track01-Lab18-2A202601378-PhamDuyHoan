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
| **Situation** | Đang học qua slide/PDF và gặp một điểm quan trọng hoặc chưa hiểu; sau đó cần ôn lại. |
| **Task** | Tạo một tài nguyên ôn tập cá nhân từ những điểm quan trọng hoặc chưa hiểu, có thể quay lại đúng ngữ cảnh gốc. |
| **Desired outcome** | Người học có thể xem lại đúng điểm cần ôn mà không phải dò toàn bộ slide/PDF hoặc chỉ dựa vào ghi chú rời rạc. |
| **Content/data fixture** | Cùng một lesson RAG, cùng slide/PDF và cùng ba điểm: RAG, embeddings và semantic similarity. |

---

## 2. Chi tiết 3 Solution Options

| Thành phần | **Option A — AI Q&A có lưu nguồn** *(Duy Hoàn thực hiện)* | **Option B — Mục lục note–slide** | **Option C — AI tạo quiz từ điểm “chưa hiểu”** |
| :--- | :--- | :--- | :--- |
| **Người phụ trách** | **Phạm Duy Hoàn (2A202601378)** | *[Chưa phân công / Chưa cập nhật]* | *[Chưa phân công / Chưa cập nhật]* |
| **Solution mechanism** | User hỏi trợ lý tại điểm chưa hiểu; AI trả lời dựa trên slide và user chọn lưu câu hỏi–trả lời kèm trang nguồn. | *[Thành viên tự điền]* | *[Thành viên tự điền]* |
| **User làm gì?** | Chủ động hỏi, đọc câu trả lời, chọn lưu hoặc không lưu. | *[Thành viên tự điền]* | *[Thành viên tự điền]* |
| **AI làm gì?** | Trả lời từ nội dung slide, hiển thị evidence/trang nguồn; không tự lưu. | *[Thành viên tự điền]* | *[Thành viên tự điền]* |
| **Trigger** | User bấm “Hỏi AI” tại đoạn đang vướng. | *[Thành viên tự điền]* | *[Thành viên tự điền]* |
| **Quyền quyết định** | User quyết định câu hỏi nào được lưu vào tài nguyên ôn tập. | *[Thành viên tự điền]* | *[Thành viên tự điền]* |
| **Trade-off chính** | Hiểu nhanh và có ngữ cảnh, nhưng có thể làm gián đoạn việc học; AI có thể trả lời thiếu hoặc chưa chính xác. | *[Thành viên tự điền]* | *[Thành viên tự điền]* |

---

## 3. Distance Check & Design Guardrails (Phần Option A)

- **Distance Check (Định vị Option A):**
  - Option A tập trung vào giải quyết sự vướng mắc **ngay trong lúc học** bằng cơ chế hỏi–đáp ngữ nghĩa có dẫn nguồn trực tiếp từ slide, với nguyên tắc quyền kiểm soát hoàn toàn thuộc về người học (User-driven Save).
- **Design Guardrails cho Option A:**
  - Bắt buộc phải có nút **Save to review notes**; AI tuyệt đối không tự động lưu câu hỏi hoặc câu trả lời vào sổ tay của user.
  - Phải hiển thị trích dẫn nguồn số trang (`Slide X`) có thể click để mở đúng trang tài liệu gốc.
