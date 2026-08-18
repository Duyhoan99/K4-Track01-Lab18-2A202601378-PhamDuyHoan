# Prototype Feedback Note — Day 18

- **Người thực hiện facilitate:** Phạm Duy Hoàn (MHV: 2A202601378)
- **Giải pháp kiểm thử chính:** **Option A — [AI] Trợ lý ảo giải đáp nhanh các câu hỏi vướng mắc / điều khoản luật ngay trong lúc học có lưu nguồn**
- **Người tham gia test (Tester):** Tester T-02 (Sinh viên kỹ thuật, thường xuyên học qua slide/video kỹ thuật số lượng lớn)
- **Thời lượng phiên test:** 35 phút (10 phút làm quen kịch bản, 15 phút tương tác trực tiếp với prototype trong bài học, 10 phút debrief phỏng vấn sâu)

---

## 1. Bối cảnh & Nhiệm vụ kiểm thử (Setup & Task)

- **Kịch bản:** Tester theo dõi một video bài giảng kỹ thuật 15 phút về chủ đề RAG & Vector Database.
- **Nhiệm vụ của Tester:**
  1. Khi gặp khái niệm "Cosine Similarity vs Dot Product" lướt qua quá nhanh trên slide 14, sử dụng thanh trợ lý AI để hỏi làm rõ.
  2. Đọc phản hồi của AI, kiểm tra trích dẫn nguồn, và quyết định có lưu vào sổ tay ôn tập hay không.
  3. Sau bài học, mở mục ôn tập để chuẩn bị cho bài mini-test 5 câu hỏi.

---

## 2. Quan sát thực tế (Direct Observations)

### Hành vi tích cực & Điểm mượt mà:
1. **Tốc độ phản hồi và nắm bắt:** Khi gặp đoạn công thức khó, tester mở ngay sidebar AI và gõ *"Công thức Cosine Similarity ở slide này là gì?"*. AI phản hồi sau 1.5 giây với 2 gạch đầu dòng ngắn gọn và trích dẫn `[Slide 14 - Đoạn 2]`. Tester đọc lướt trong 4 giây và hiểu ngay mà không cần dừng video bài giảng.
2. **Tác vụ lưu note chủ động:** Tester chủ động bấm nút *"Lưu vào Note"*. Khi được hỏi, tester chia sẻ: *"Mình thích việc nó không tự động nhét vào sổ tay. Mình chỉ muốn lưu những câu mình thấy giải thích hay và đúng trọng tâm"*.
3. **Tra cứu ngược 1-click:** Tester bấm thử vào thẻ `[Slide 14]` trên câu trả lời, màn hình slide lập tức nhảy đúng vị trí để tester đối chiếu hình vẽ minh họa.

### Ma sát & Điểm bối rối (Friction & Hesitations):
1. **Phân vân khi gõ câu hỏi:** Ở lần hỏi thứ hai, tester mất 12 giây để suy nghĩ và gõ câu hỏi dài vì sợ AI không hiểu ngữ cảnh đang nói về phần nào. Tester nhận xét: *"Nếu có nút bấm nhanh kiểu 'Giải thích slide hiện tại' thì đỡ phải gõ tay trong lúc đang nghe giảng"*.
2. **Nhu cầu chỉnh sửa trước khi lưu:** Tester muốn sửa lại 1 từ trong câu trả lời của AI theo cách diễn giải cá nhân trước khi bấm lưu, nhưng giao diện prototype lúc đầu chỉ cho phép bấm "Lưu toàn bộ" mà chưa có ô edit trực tiếp.
3. **Lo ngại che khuất màn hình:** Khi mở thanh chat bên phải, khung hình video slide bị co lại khoảng 25%, khiến tester phải nheo mắt nhìn sơ đồ bên trái.

---

## 3. Trích dẫn đáng chú ý (User Quotes)

> *"Lúc đi học sợ nhất là giảng viên nói lướt qua một thuật ngữ mới rồi sang slide khác luôn, mình ghi không kịp là coi như mất dấu. Có con AI này tóm tắt tại chỗ và chỉ rõ nó nằm ở slide nào làm mình an tâm hơn hẳn."*

> *"Tôi không muốn AI tự động ghi chú hộ tôi toàn bộ. Nó chỉ nên đóng vai trò phụ tá tra cứu khi tôi hỏi. Việc tôi bấm nút 'Lưu' giống như một hành động xác nhận là tôi đã hiểu ý đó."*

> *"Cái hay nhất là cái link nhảy về đúng slide. Bình thường sau buổi học mở file PDF 60 trang tìm lại cái công thức mất cả chục phút, giờ bấm một phát là ra ngay."*

---

## 4. Đánh giá theo 4 Tiêu chí Human–AI Design

1. **Expectation:** Đạt. Tester hiểu ngay AI là trợ lý tra cứu nội bộ slide nhờ dòng placeholder *"Hỏi nhanh điều khoản/khái niệm trong slide..."*.
2. **Role & Agency:** Rất tốt. Mức độ **Suggest / Ask** (AI đề xuất câu trả lời, User bấm Lưu) được tester đánh giá cao vì giữ được quyền kiểm soát thông tin cá nhân.
3. **Evidence & Uncertainty:** Đạt. Badge dẫn nguồn `[Slide X]` tạo sự tin cậy cao; tester thực sự click vào nguồn để kiểm chứng.
4. **Control & Recovery:** Cần cải thiện thêm: Cần bổ sung tính năng inline-edit (sửa nhanh text trước khi lưu) và phím tắt đóng nhanh (`Esc`) để không ảnh hưởng tầm nhìn bài giảng.

---

## 5. Kết luận & Đề xuất điều chỉnh (Takeaways & Iterations)

- **Giữ lại:** Cơ chế hỏi–đáp kèm thẻ trích dẫn nguồn 1-click và nút lưu chủ động (User-driven Save).
- **Cải tiến trong sprint tới:**
  - Thêm gợi ý câu hỏi 1-click (Quick Prompts: *"Tóm tắt slide này"*, *"Giải thích thuật ngữ chính"*).
  - Cho phép inline edit nội dung tóm tắt trước khi bấm lưu vào note.
  - Tối ưu hóa UI: dạng popover nổi trong suốt hoặc tự động ẩn khi không tương tác để không che slide bài học.
