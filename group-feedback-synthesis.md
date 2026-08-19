# Group Feedback Synthesis — Day 18

- **Nhóm:** 2T1H
- **Case:** Case B — AI Notes: Personal Learning Notes
- **Người cập nhật phần việc:** **Phan Văn Tình (MHV: 2A202601430)**

---

## 1. Tổng hợp phản hồi các Option

| Tiêu chí | **Option A — User-Led Smart Bookmark** <br>*(Facilitator: Phạm Duy Hoàn)* | **Option B — Co-create AI Draft Notes** <br>*(Facilitator: Nguyễn Khánh Toàn)* | **Option C — Proactive AI Notes** <br>*(Facilitator: Phan Văn Tình)* |
| :--- | :--- | :--- | :--- |
| **Người phụ trách** | **Phạm Duy Hoàn (2A202601378)** | **Nguyễn Khánh Toàn (2A202601843)** | **Phan Văn Tình (2A202601430)** |
| **Phản hồi chính** | Ghi note thủ công chưa tiện lợi; thao tác đánh dấu mốc đơn lẻ chưa hỗ trợ tốt khi người học muốn giữ lại đúng từ khóa hoặc đoạn chưa hiểu. | Người dùng lo AI generate thiếu ý hoặc không chính xác; họ vẫn phải đọc lại để kiểm tra nên tốn thời gian. | Người dùng không tin tưởng AI tự tạo note; lo AI sinh nội dung rác và cho rằng giải pháp chưa giải quyết được vấn đề ghi chép/ôn tập. |
| **Điểm hữu ích còn giữ lại** | Liên kết lại ngữ cảnh bài học là có ích, nhưng cần capture trực tiếp trên nội dung thay vì chỉ tạo note thủ công. | Có quyền review trước khi lưu, tránh AI tự chèn note không mong muốn. | Quyền Reject ở cuối luồng là cần thiết để người dùng không bị ép dùng output AI. |
| **Ma sát (Friction)** | Phải tự thao tác tạo note; chưa có cách bôi đen nhanh từ/đoạn và gắn nhãn theo mục đích ôn tập. | Review từng draft làm tăng tải nhận thức; việc kiểm chứng lại có thể triệt tiêu lợi ích tiết kiệm thời gian. | Mức tự chủ AI quá cao nhưng thiếu niềm tin; rủi ro “rác” làm user mất thêm thời gian dọn dẹp hoặc bỏ toàn bộ note. |
| **Nhu cầu/đề xuất từ feedback** | Cho phép bôi đen từ khóa hoặc đoạn chưa hiểu ngay trên slide/transcript và gắn tag như **Quan trọng**, **Lưu ý**, **Cần xem lại**. | Chỉ gợi ý khi có evidence rõ ràng; hiển thị source và mức độ chắc chắn để giảm công đọc lại toàn bộ. | Không nên triển khai proactive note hoàn toàn ở dạng hiện tại; cần giảm autonomy, chỉ tạo draft có evidence hoặc chuyển sang cơ chế user-triggered. |
| **Kết luận về mức độ kiểm soát** | Nên tăng khả năng kiểm soát trực tiếp trên nội dung nguồn. | HITL có kiểm soát, nhưng cần giảm chi phí review. | User không chấp nhận trao quyền tự chủ cao cho AI khi chưa thấy bằng chứng đáng tin cậy. |

---

## 2. Insight tổng hợp & đề xuất cho nhóm

1. **Điểm đau cốt lõi không chỉ là lưu mốc thời gian, mà là giữ lại đúng ngữ cảnh chưa hiểu.** Option A nên chuyển trọng tâm từ tạo note thủ công sang highlight trực tiếp từ khóa/đoạn trên slide hoặc transcript và gắn tag phục vụ ôn tập.
2. **AI chỉ tạo giá trị khi giảm thời gian kiểm tra, không phải tạo thêm công việc review.** Với Option B, mọi draft cần đi kèm source và phải ngắn, có thể bỏ qua nhanh; nếu user phải đọc lại gần như toàn bộ thì HITL không còn giải quyết vấn đề.
3. **Không thể giả định người học tin proactive AI.** Feedback Option C cho thấy bản note tự động có thể bị xem là “rác” nếu user không hiểu AI đã lấy thông tin từ đâu và vì sao chọn nội dung đó.
4. **Hướng ưu tiên tiếp theo:** Kết hợp điểm mạnh của A và B: user chủ động highlight/tag trên source, AI chỉ hỗ trợ tạo draft ngắn từ phần đã được user chọn; tránh tự động tạo toàn bộ note ở cuối bài như Option C.

### Đề xuất iteration cụ thể

- **Option A:** Thêm thao tác bôi đen từ khóa/đoạn, tag `Quan trọng` / `Lưu ý` / `Cần xem lại`, và mở lại đúng đoạn nguồn khi review.
- **Option B:** Hiển thị source, confidence và cho phép Keep/Remove nhanh; không bắt user review các draft không có evidence rõ ràng.
- **Option C:** Tạm thời không ưu tiên giải pháp proactive toàn phần. Nếu tiếp tục thử nghiệm, AI chỉ được tạo note theo phần user đã highlight hoặc phải yêu cầu user xác nhận trước khi tạo bản tổng hợp.
