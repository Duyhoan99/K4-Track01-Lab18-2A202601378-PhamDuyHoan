# AI Support Log — Day 18

- **Người thực hiện:** Phạm Duy Hoàn (MHV: 2A202601378)
- **Nhóm:** 2T1H
- **Phần việc đảm nhiệm:** Thiết kế & Kiểm thử Option A — User-Led Smart Bookmark *(Người học kiểm soát capture; bấm Mark moment để lưu timestamp, slide hiện tại và note ngắn)*

---

## 1. AI đã giúp tôi những gì (Where AI Added Value)

1. **Khung cấu trúc Human–AI Design cho Option A:** AI hỗ trợ tôi phác thảo 4 quyết định thiết kế (Expectation, Role & Agency, Evidence & Uncertainty, Control & Recovery) và bảng so sánh 3 Option theo phổ mức độ tự chủ Human–AI.
2. **Xây dựng Interactive Micro-Prototype:** Hỗ trợ sinh mã HTML/CSS/JS cho prototype tương tác [prototype-option-a.html](prototype-option-a.html) với thiết kế đồng bộ từ file chung `day-18-abc-notes-prototype.html`.
3. **Chuẩn bị kịch bản kiểm thử (Test Script):** Hỗ trợ xây dựng kịch bản tester tương tác trực tiếp với slide bài giảng, thao tác bấm Mark moment, gõ note ngắn và đối chiếu liên kết slide.

---

## 2. Điểm AI làm sai, hời hợt hoặc thiên kiến mà tôi phát hiện (AI Limitations & Flaws)

1. **Thiên kiến biến thành AI Tutor hoặc Tự động hóa quá mức:**
   - *Vấn đề:* Ban đầu AI luôn có xu hướng biến giải pháp thành chatbot gia sư hỏi đáp phức tạp hoặc tự động tóm tắt toàn bộ bài học (Full Act) mà không để người học tự kiểm soát.
   - *Hệ quả:* Đề xuất này vi phạm bản chất của Case B (AI Notes) và làm mất tính chủ động của người học trong việc ghi chép.
2. **Thiết kế dàn trải, thiếu tập trung vào tương tác cốt lõi:**
   - *Vấn đề:* AI ban đầu đề xuất thêm nhiều chức năng rườm rà (quizzing, thi thử, flashcard phức tạp) thay vì tập trung vào tương tác 1-chạm: *Người học bấm Mark moment $\rightarrow$ Hệ thống lưu timestamp, slide và note ngắn $\rightarrow$ Đối chiếu lại ngữ cảnh slide gốc*.
3. **Mô tả chung chung, thiếu gắn với Evidence của case:**
   - *Vấn đề:* Các phản hồi ban đầu của AI không bám sát tình huống người học bị quá tải và mất *"45 phút tra cứu tài liệu PDF 60 trang cho bài test 15 phút"*.

---

## 3. Các điểm tôi đã tự mình điều chỉnh & hoàn thiện (Manual Corrections)

1. **Định hình lại chuẩn xác Option A là User-Led Smart Bookmark:**
   - Tôi kiên quyết thiết lập cơ chế **User-Led (Low AI Agency)**: Người học kiểm soát 100% việc đánh dấu khoảnh khắc và nội dung ghi chú; hệ thống chỉ đóng vai trò thư ký lưu chính xác tọa độ timestamp và số trang slide.
2. **Thiết kế tính năng 1-chạm và phím tắt nhanh `[M]`:**
   - Tôi tự bổ sung phím tắt bàn phím toàn cục **`[M]`** vào prototype để người học có thể đánh dấu tức thì mà không cần rê chuột làm gián đoạn việc nhìn slide bài giảng.
3. **Tích hợp tính năng chỉnh sửa trực tiếp (Inline Edit) và xuất đề cương:**
   - Bổ sung nút **`✏️ Edit note`** ngay trên thẻ bookmark và nút **`📋 Export structured summary`** giúp người học dễ dàng quản lý và sử dụng ghi chú sau buổi học.
