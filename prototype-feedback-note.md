# Prototype Feedback Note — Day 18

- **Người thực hiện facilitate:** Phạm Duy Hoàn (MHV: 2A202601378)
- **Giải pháp kiểm thử chính:** **Option A — User-Led Smart Bookmark** *(Người học kiểm soát capture; bấm Mark moment để lưu timestamp, slide hiện tại và note ngắn)*
- **Người tham gia test (Tester):** Tester T-02 (Sinh viên kỹ thuật, thường xuyên học qua slide bài giảng có mật độ thông tin cao)
- **Thời lượng phiên test:** 35 phút (10 phút làm quen kịch bản, 15 phút tương tác trực tiếp với prototype trong bài học, 10 phút debrief phỏng vấn sâu)

---

## 1. Bối cảnh & Nhiệm vụ kiểm thử (Setup & Task)

- **Kịch bản:** Tester theo dõi bài giảng kỹ thuật *AI Fundamentals & Model Risk* (Slide 5/8: *Model Risk & Exception Cases*). Giảng viên nói nhanh qua 3 trường hợp ngoại lệ quan trọng (dữ liệu nhạy cảm, quyết định ảnh hưởng lớn, AI không đủ confidence).
- **Nhiệm vụ của Tester:**
  1. Khi giảng viên giảng nhanh qua đoạn khó không kịp chép, bấm nút **"Mark current moment"** (hoặc nhấn phím tắt **[M]**) để lưu lại mốc kiến thức.
  2. Nhập một dòng ghi chú ngắn cá nhân: *"Chưa kịp ghi 3 exception cases, cần xem lại slide này"*.
  3. Chuyển sang slide khác (Slide 6 hoặc Slide 8), sau đó bấm vào thẻ bookmark đã lưu trong mục *My review points* để kiểm tra xem slide có tự động nhảy về đúng Slide 5 hay không.
  4. Thử nghiệm chỉnh sửa ghi chú (**Edit note**), xóa bookmark (**Remove**), và lưu quyết định ôn tập.

---

## 2. Quan sát thực tế (Direct Observations)

### Hành vi tích cực & Điểm mượt mà:
1. **Thao tác 1-chạm tức thì:** Khi giảng viên nói lướt qua 3 trường hợp exception, tester chỉ mất chưa đầy 1 giây để bấm nút *"Mark current moment"* (hoặc nhấn phím `M`). Hệ thống bắt ngay mốc thời gian `07:18` và liên kết với `Slide 5`.
2. **Không làm gián đoạn bài giảng:** Tester không phải dừng lại gõ một đoạn văn dài, giúp tester duy trì sự tập trung 100% vào lời giảng tiếp theo của giảng viên.
3. **Đồng bộ ngữ cảnh ngược 1-click:** Sau khi chuyển sang Slide 8, tester bấm vào thẻ bookmark `07:18 ➔ Slide 5: Model Risk`, màn hình slide bên trái lập tức chuyển về đúng Slide 5 và viền slide phát sáng màu xanh thương hiệu (`var(--brand)`), giúp tester đối chiếu ngay hình vẽ minh họa và trích dẫn bài giảng.
4. **Quyền kiểm soát trọn vẹn:** Tester thử nghiệm nút `✏️ Edit note` để diễn đạt lại câu chữ theo ý mình và đánh giá cao việc hệ thống chỉ lưu những gì do chính tay tester bấm đánh dấu.

### Ma sát & Điểm bối rối (Friction & Hesitations):
1. **Phân tâm khi rê chuột:** Trong lần đánh dấu đầu tiên, tester phải rời mắt khỏi slide để rê chuột sang khung bên phải tìm nút bấm. Tester gợi ý: *"Nếu có phím tắt bàn phím kiểu bấm phím M là hệ thống tự đánh dấu thì tiện hơn rất nhiều"*.
2. **Nhu cầu xuất đề cương tổng hợp:** Sau khi kết thúc bài học với nhiều mốc bookmark, tester muốn có nút xuất nhanh toàn bộ danh sách bookmark thành một bản tóm tắt có cấu trúc để in ra hoặc lưu vào Notion ôn thi.

---

## 3. Trích dẫn đáng chú ý (User Quotes)

> *"Lúc giảng viên nói lướt qua phần khó, mình chỉ cần gõ nhẹ một nút là hệ thống tự ghim lại phút 07:18 ở Slide 5. Mình không phải cuống cuồng cắm đầu gõ chữ dài dòng làm lỡ mất đoạn giảng tiếp theo."*

> *"Thích nhất là cái nút bấm mở slide ngữ cảnh. Sau buổi học bấm vào cái bookmark là màn hình tự nhảy về đúng Slide 5 có viền xanh phát sáng, không phải mất 45 phút lật từng trang PDF 60 trang tìm lại."*

> *"Với Option A, mình là người kiểm soát 100% sổ tay của mình. Mình đánh dấu chỗ nào thì lưu chỗ đó, không sợ AI tự tiện tóm tắt sai hoặc nhét rác vào sổ tay cá nhân."*

---

## 4. Đánh giá theo 4 Tiêu chí Human–AI Design

1. **Expectation (Kỳ vọng):** Đạt xuất sắc. Tester hiểu ngay cơ chế lưu tọa độ slide & timestamp mà không bị nhầm lẫn sang chatbot hỏi đáp.
2. **Role & Agency (Phân vai & Quyền tự chủ):** Rất tốt. Mức độ **User-Led (Don't Act without trigger)** giúp người học giữ trọn quyền kiểm soát nội dung nạp vào sổ tay cá nhân.
3. **Evidence & Uncertainty (Căn cứ & Bất định):** Đạt. Thẻ bookmark hiển thị rõ `07:18 ➔ Slide 5`, click là nhảy đúng slide gốc với hiệu ứng phát sáng viền.
4. **Control & Recovery (Kiểm soát & Phục hồi):** Rất tốt. Cung cấp đầy đủ tính năng sửa ghi chú (Inline Edit), xóa (Remove), hoàn tác (Undo) và nút Reset Prototype.

---

## 5. Kết luận & Đề xuất điều chỉnh (Takeaways & Iterations)

- **Giữ lại:**
  - Nút bấm 1-chạm **"Mark current moment"** tự động bắt timestamp và slide hiện tại.
  - Cơ chế đồng bộ 1-click từ thẻ bookmark nhảy ngược về đúng slide bài giảng kèm hiệu ứng viền xanh.
  - Quyền kiểm soát 100% thuộc về người học (User-Led Capture).
- **Cải tiến đã thực hiện ngay vào prototype cá nhân [prototype-option-a.html](prototype-option-a.html):**
  - Tích hợp phím tắt bàn phím toàn cục **`[M]`** để người học bấm đánh dấu tức thì mà không cần rê chuột.
  - Thêm chức năng **`✏️ Edit note`** trực tiếp trên từng thẻ bookmark.
  - Bổ sung nút **`📋 Export structured summary`** để xuất nhanh danh sách mốc ôn tập có cấu trúc.
