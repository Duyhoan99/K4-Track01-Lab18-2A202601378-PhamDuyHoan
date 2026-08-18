# AI Support Log — Day 18

- **Người thực hiện:** Phạm Duy Hoàn (MHV: 2A202601378)
- **Nhóm:** 2T1H
- **Phần việc đảm nhiệm:** Thiết kế & Kiểm thử Option A — Trợ lý AI Q&A giải đáp nhanh có lưu nguồn

---

## 1. AI đã giúp tôi những gì (Where AI Added Value)

1. **Khung cấu trúc Human–AI Design cho Option A:** AI hỗ trợ tôi phác thảo 4 quyết định thiết kế (Expectation, Role & Agency, Evidence & Uncertainty, Control & Recovery) và bảng quyết định tương tác chi tiết.
2. **Xây dựng kịch bản kiểm thử (Test Script):** Hỗ trợ chuẩn bị các câu hỏi debriefing và tiêu chí quan sát hành vi người dùng trong phiên thử nghiệm Option A (tốc độ đọc lướt, phản xạ kiểm tra nguồn slide).
3. **Format và cấu trúc tài liệu:** Hỗ trợ định dạng bảng Markdown và chuẩn hóa cách trình bày các trích dẫn và kết quả quan sát.

---

## 2. Điểm AI làm sai, hời hợt hoặc thiên kiến mà tôi phát hiện (AI Limitations & Flaws)

1. **Thiên kiến tự động hóa quá mức (Over-automation Bias):**
   - *Vấn đề:* Ban đầu AI luôn đề xuất cơ chế "Full Act" (AI tự động tóm tắt bài giảng và tự chèn các đoạn note vào sổ tay của user mà không cần hỏi).
   - *Hệ quả:* Đề xuất này vi phạm quyền tự chủ của người học. Nếu AI tự chèn ghi chú, sổ tay cá nhân sẽ bị loãng và user không có động lực đọc lại để hiểu.
2. **Thiết kế dàn trải, vi phạm nguyên tắc "chỉ review critical interaction":**
   - *Vấn đề:* AI gợi ý thêm nhiều màn hình phụ (cài đặt model, dashboard thống kê, xuất file PDF...) thay vì tập trung vào tương tác cốt lõi: *User hỏi vướng mắc trong lúc học → AI trả lời kèm nguồn → User bấm lưu*.
3. **Mô tả chung chung, thiếu gắn với Evidence của case:**
   - *Vấn đề:* Các phản hồi ban đầu của AI không bám sát tình huống người học bị quá tải và mất "45 phút tra cứu tài liệu 60 trang cho bài test 15 phút".

---

## 3. Các điểm tôi đã tự mình điều chỉnh & hoàn thiện (Manual Corrections)

1. **Chuyển đổi Agency về mức Ask / Suggest:**
   - Tôi kiên quyết thiết lập cơ chế **User-driven Save**: AI chỉ hiển thị draft câu trả lời và số trang nguồn ở sidebar; quyền bấm nút *"Lưu vào Note"* hoàn toàn thuộc về người học.
2. **Thiết kế các chốt chặn kiểm soát (Human Control & Recovery):**
   - Tôi tự bổ sung tính năng **Inline Edit** (cho phép người học sửa nhanh vài từ trong draft trước khi lưu), phím tắt đóng nhanh (`Esc`/`X`) để không che slide bài giảng, và thẻ trích dẫn **Citation Badge 1-click** quay về trang PDF gốc.
3. **Tập trung hóa kịch bản test:**
   - Tôi lược bỏ các bước kiểm thử rườm rà, tập trung 100% vào tình huống người học gặp đoạn kiến thức khó/lướt nhanh trên slide 14 để kiểm tra tốc độ phản hồi và sự an tâm của người học.
