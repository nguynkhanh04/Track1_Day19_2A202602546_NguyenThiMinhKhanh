# AI SUPPORT LOG (NHẬT KÝ SỬ DỤNG AI CÁ NHÂN)

> **Học viên:** Nguyễn Thị Minh Khánh (2A202602546)  
> **Nhóm:** Tung Tung Tung Sahur  
> **Cam kết liêm chính học thuật**: Tôi cam đoan không dùng AI để tạo giả tạo bất kỳ trích dẫn (quote), quan sát (observation) hay phản hồi (feedback) nào của người dùng. Mọi tương tác phỏng vấn (Note 2 - Lan) và thử nghiệm người dùng (Tester 3) đều được tiến hành với con người thật. Phần dưới đây khai báo trung thực các khía cạnh tôi đã sử dụng AI hỗ trợ trong quá trình thực hiện bài Lab.

---

## 1. CÁC CÔNG CỤ AI ĐÃ SỬ DỤNG
- [x] Antigravity AI / Claude Agent
- [x] ChatGPT (OpenAI)
- [x] Google Gemini

---

## 2. PHẠM VI ỨNG DỤNG AI TRONG BÀI LAB

### A. Gợi ý cơ chế tương tác và kịch bản (Mechanism Ideation)
- **Prompt đã hỏi AI:** `Phân tích cơ chế Human-AI tương tác cho tính năng Proactive Nudge (Option C): làm thế nào để AI tự động phát hiện người học kẹt mà không gây khó chịu hoặc cảm giác bị theo dõi?`
- **AI đã gợi ý gì hữu ích:** Đề xuất mô hình tín hiệu đa kênh (thời gian dừng >12s, tần suất lật slide, làm sai Checkpoint) kết hợp với **thẻ giải trình minh bạch ("Vì sao AI nghĩ vậy")** và nút tắt tức thì 1 chạm để trao quyền kiểm soát (User Agency) cho người học.
- **Phần tôi tự sàng lọc / thay đổi:** Tôi điều chỉnh lại nội dung giải trình ngắn gọn hơn, thêm các chip số liệu trực quan (*"4 phút ở slide này", "6/10 học viên bí ở đây"*) để người học cảm thấy tin cậy thay vì những câu giải thích chung chung.

### B. Sinh dữ liệu mẫu & Phản hồi mẫu (Synthetic Data & Canned Responses)
- **AI hỗ trợ tạo phần dữ liệu nào:** Hỗ trợ tạo các câu hỏi và giải thích ngắn cho 3 chủ đề kiến thức kỹ thuật (*Context Window, ReAct Loop, Gradient Descent*) trong prototype để đảm bảo dữ liệu chạy thử nghiệm chân thực.
- **Mức độ can thiệp thực tế của tôi:** Trực tiếp biên tập, kiểm tra tính chính xác của công thức và câu hỏi kiểm tra nhanh phù hợp với bài giảng trên lớp.

### C. Hỗ trợ kỹ thuật / Code giao diện (Prototype Coding / Design boilerplate)
- **AI đã hỗ trợ code hoặc dàn layout phần nào:** Hỗ trợ viết cấu trúc mã nguồn HTML/CSS/JS thuần cho hệ thống prototype 4 options, bộ đếm thời gian và hệ thống Logger xuất file CSV.
- **Cách tôi chỉnh sửa để phù hợp với ngữ cảnh:** Kiểm tra và tinh chỉnh giao diện tiếng Việt, tối ưu màu sắc viền vàng/đỏ cho các khối tương tác, và bổ sung các phím tắt điều khiển để thuận tiện cho người facilitate khi test.

### D. Rà soát kịch bản phỏng vấn (Bias & Leading Question Check)
- **AI đã phát hiện những câu hỏi dẫn dắt nào trong kịch bản ban đầu:** Phát hiện câu hỏi ban đầu *"Bạn có thấy tính năng tự nhắc này rất tiện lợi không?"* mang tính định hướng người dùng khen ngợi sản phẩm.
- **Cách viết lại trung tính sau khi chỉnh sửa:** Viết lại thành câu hỏi mở, khách quan: *"Khi thẻ gợi ý này tự động xuất hiện, bạn cảm thấy thế nào và suy nghĩ đầu tiên của bạn là gì?"*.

---

## 3. ĐÁNH GIÁ PHẢN BIỆN (CRITICAL REFLECTION VỀ AI)

- **Điểm yếu / Lỗ hổng lớn nhất trong các phản hồi của AI:**  
  AI có xu hướng đề xuất các câu trả lời rất lý thuyết và hoàn hảo, đôi khi đánh giá quá cao sự kiên nhẫn của người học. Trong thực tế phỏng vấn, học viên thật hành động rất nhanh, không đọc các văn bản dài quá 3 dòng và sẵn sàng rời bỏ hệ thống chỉ sau vài chục giây nếu cảm thấy bị gián đoạn.

- **Bài học kinh nghiệm về việc kiểm soát AI trong quy trình Human–AI Design:**  
  AI là một công cụ hỗ trợ tuyệt vời để brainstorm ý tưởng, tạo khung sườn và tự động hóa các tác vụ lặp lại (boilerplate). Tuy nhiên, **tâm lý, nỗi đau thực sự (Pain Points) và phản xạ thao tác của người dùng chỉ có thể được khám phá thông qua việc quan sát và lắng nghe con người thật**. Cần luôn giữ thái độ hoài nghi lành mạnh với các giải pháp AI đưa ra và liên tục kiểm chứng bằng User Testing thực tế.
