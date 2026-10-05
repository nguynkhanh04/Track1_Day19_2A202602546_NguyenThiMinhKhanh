# PROTOTYPE LINKS & TEST CONTEXT (NHÓM TUNG TUNG TUNG SAHUR)

> **Tài liệu truy cập Web Prototype chính thức của nhóm**: Phiên bản hoàn chỉnh tích hợp 4 cơ chế Human–AI, hỗ trợ đầy đủ chế độ Lý thuyết (Slide) và Thực hành (Lab) trên 3 chủ đề kiến thức thực tế, kèm hệ thống Logger tự động đo lường thời gian thực.

---

## 1. HƯỚNG DẪN TRUY CẬP VÀ MỞ PROTOTYPE

- **Công cụ xây dựng:** **Web Micro-Prototype (HTML5 / Vanilla CSS / Vanilla JavaScript thuần)**
- **Đường dẫn mở trực tiếp (Offline / Local):**
  - Mở file [`prototype/index.html`](file:///d:/New%20folder/LAB_D19/Track1_Day19_2A202602546_NguyenThiMinhKhanh/prototype/index.html) bằng bất kỳ trình duyệt nào (Chrome, Edge, Firefox, Safari).
- **Mã nguồn nguyên mẫu:**
  - Nằm trực tiếp tại file [`prototype/index.html`](file:///d:/New%20folder/LAB_D19/Track1_Day19_2A202602546_NguyenThiMinhKhanh/prototype/index.html) trong repository này.
- **Trang chủ Facilitator:** Mở file không có hash hoặc truy cập URL `#` để vào màn hình chính chọn chủ đề.

### Danh mục URL Hash trực tiếp cho phiên User Testing:

| Option | Tên cơ chế | URL chế độ Lý thuyết (Slide) | URL chế độ Thực hành (Lab) |
| :---: | :--- | :--- | :--- |
| **A** | **Chỉ vào chỗ kẹt** *(In-line Term/Block Inspector - Quân lead)* | `prototype/index.html#context/theory/A` | `prototype/index.html#context/lab/A` |
| **B** | **Chẩn đoán 3 câu** *(Diagnostic Micro-Check - Việt Anh lead)* | `prototype/index.html#context/theory/B` | `prototype/index.html#context/lab/B` |
| **C** | **AI gợi ý chủ động** *(Proactive Action Card - Minh Khánh lead)* | `prototype/index.html#context/theory/C` | `prototype/index.html#context/lab/C` |
| **D** | **Hỏi người thật** *(Context-Attached Support - Quang Huy lead)* | `prototype/index.html#context/theory/D` | `prototype/index.html#context/lab/D` |

*(Khuyên dùng: Khi test với người ngoài nhóm, nên bắt đầu bằng chủ đề **Context Window - Slide 12** để tester làm quen với khái niệm)*.

---

## 2. BỐI CẢNH DỮ LIỆU & VÍ DỤ TRONG PROTOTYPE (DATA FIXTURES)

Prototype tích hợp sẵn **3 chủ đề bài học thực tế** của chương trình đào tạo:

### 1. Chủ đề Context Window (`context`)
- **Tab Slide 12 (Lý thuyết)**:
  - *Nội dung*: Công thức `context window ≥ token input + token output`. Vì sao chat dài thì model quên lời dặn ở đầu (phần cũ bị cắt bỏ).
  - *Câu hỏi kiểm tra nhanh*: *"Model có context window 8.000 token. Prompt + tài liệu dài 7.500 token, yêu cầu tóm tắt khoảng 1.000 token. Điều gì dễ xảy ra nhất?"*  
    ➔ **Đáp án đúng:** Bản tóm tắt bị cắt giữa chừng (7.500 + 1.000 = 8.500 > 8.000).
- **Tab Task 2 (Lab Chatbot nhớ hội thoại)**:
  - *Nội dung*: Hoàn thiện hàm `trim_history(messages, max_tokens=8000, reserve=1000)` trong file `chat.py`. Ngân sách input = `max_tokens - reserve`.
  - *Checkpoint*: Lịch sử chat đang 7.600 token, hàm `trim_history` nên làm gì để không lỗi `context length exceeded`?

### 2. Chủ đề ReAct Agent (`react`)
- **Tab Slide 9 (Lý thuyết)**:
  - *Nội dung*: Vòng lặp `Thought → Action → Observation → Answer`. Model trả về `tool_calls`, ứng dụng chạy hàm (Action), kết quả gửi lại qua `role: "tool"` (Observation).
  - *Câu hỏi kiểm tra nhanh*: *"Trong vòng ReAct, Observation là gì?"*  
    ➔ **Đáp án đúng:** Kết quả tool được gửi lại cho model (message role "tool").
- **Tab Task 2.2 (Lab Lập trình ReAct Loop)**:
  - *Nội dung*: Hoàn thiện vòng `while step < MAX_STEPS` trong `agent.py`. Bắt `tool_calls` và thực thi tool.

### 3. Chủ đề Gradient Descent (`gd`)
- **Tab Slide 7 (Lý thuyết)**:
  - *Nội dung*: Công thức cập nhật trọng số $w \leftarrow w - \eta \cdot \frac{\partial L}{\partial w}$. Gradient chỉ hướng dốc lên, dấu trừ để đi xuống dốc, $\eta$ là learning rate.
  - *Câu hỏi kiểm tra nhanh*: *"Cho $L(w) = w^2$, đang ở $w = 3, \eta = 0.1$. Sau một bước gradient descent, $w$ mới bằng bao nhiêu?"*  
    ➔ **Đáp án đúng:** $2.4$ ($\frac{\partial L}{\partial w} = 2 \times 3 = 6 \rightarrow w = 3 - 0.1 \times 6 = 2.4$).
- **Tab Task 2 (Lab Chọn Learning Rate)**:
  - *Nội dung*: Thử 3 giá trị `lr` và phát hiện hiện tượng loss tăng vọt qua các epoch khi đặt `lr = 1.0`.

---

## 3. 4 CƠ CHẾ TƯƠNG TÁC HUMAN–AI ĐÃ CÀI ĐẶT
*(Phân công 4 thành viên: Quân - Opt A, Việt Anh - Opt B, Minh Khánh - Opt C, Quang Huy - Opt D)*

1. **Option A (Chỉ vào chỗ kẹt - Quân lead)**:
   - Bấm nút `Tôi vẫn chưa hiểu` ➔ Màn hình hiện Pickbar ở dưới, các đoạn sáng viền vàng ➔ Chạm vào khối văn bản/code bị kẹt ➔ Chọn kiểu giúp (*"Giải thích dễ hơn"*, *"Cho ví dụ"*, *"Ôn kiến thức nền"*) hoặc tự gõ câu hỏi ➔ Bấm `Gửi` ➔ Thẻ AI `icard` xuất hiện ngay bên dưới đoạn văn bản đó kèm trích dẫn lý thuyết liên quan.
2. **Option B (Chẩn đoán 3 câu - Việt Anh lead)**:
   - Bấm nút `Tôi vẫn chưa hiểu` ➔ Mở side panel "Trợ giảng AI" bên phải ➔ AI hỏi lần lượt 3 câu trắc nghiệm nhanh 1 chạm (~1 phút) ➔ Thẻ kết quả chẩn đoán `dcard` hiện ra kèm thước đo độ chắc chắn (*Cao, Trung bình, Thấp*), chỉ rõ học viên đang hổng ở kiến thức nào ➔ Trả lời đúng chỗ ngứa kèm đồ thị SVG minh hoạ. Có nút *"Không đúng chỗ"* để học viên tự chọn lại chủ đề muốn ôn.
3. **Option C (AI gợi ý chủ động - Minh Khánh lead)**:
   - AI tự động theo dõi tín hiệu (học viên dừng quá 12s, lật qua lại slide nhiều lần, hoặc vừa trả lời sai câu hỏi kiểm tra) ➔ Tự động trượt thẻ `icard.nudge` ra màn hình ghim vào đoạn nghi ngờ kẹt. Có các chip dữ liệu hành vi thực tế, mục giải trình minh bạch *"Vì sao AI nghĩ vậy"* kèm thang đo độ tin cậy. Có nút *"Đúng chỗ, đã rõ hơn"*, *"Không phải chỗ này"* (để chạm đoạn kẹt thực tế), và nút *"Tắt tự nhắc trong buổi này"*.
4. **Option D (Hỏi người thật kèm bối cảnh - Quang Huy lead)**:
   - Bấm nút `Tôi vẫn chưa hiểu` ➔ Mở modal "Nhờ người hỗ trợ" tự động gom các thẻ bối cảnh (Context Chips: Slide đang học, thời gian dừng, số lần trả lời sai). Học viên tick/untick từng dòng để bảo mật thông tin, chọn người gửi (`TA Hà - Mentor lớp` hoặc `Tuấn - Nhóm Lab`) ➔ Bấm `Gửi yêu cầu` ➔ Side panel theo dõi tiến trình gửi (*Đã gửi ➔ Đã xem ➔ Đang trả lời ➔ Đã trả lời* sau 15 giây mô phỏng, có nút *"Vẫn chưa hiểu"* để hỏi thêm).

---

## 4. KỊCH BẢN THỬ NGHIỆM ĐÃ CHUẨN HÓA (DÀNH CHO CHẶNG 6)

### Câu hỏi Relevant Context (2 phút đầu):
> *"Gần đây khi học bài hoặc làm Lab trên VLearn mà gặp phải một đoạn lý thuyết khó hiểu hoặc chạy code báo lỗi, bạn thường làm gì đầu tiên để giải quyết?"*

### Outcome Task (Giao cho tester khi mở prototype):
> *"Giả sử bạn đang tự học slide Context Window này và cảm thấy bối rối không hiểu vì sao khi chat dài thì model lại quên lời dặn ở đầu. Mục tiêu của bạn là tìm hiểu để trả lời đúng câu hỏi trắc nghiệm ở cuối trang. Bạn hãy thao tác tự nhiên với màn hình."*  
*(⚠️ Lưu ý người facilitate: Tuyệt đối không chỉ tester bấm vào đâu! Hãy để họ tự nhìn và thao tác).*

### 5 Tiêu điểm quan sát (Observation Focus):
1. **First action:** Tester bấm vào đâu đầu tiên (đọc bài, bấm nút `Tôi vẫn chưa hiểu`, hay làm câu hỏi nhanh)?
2. **Hesitation:** Chỗ nào tester dừng lại lâu, đọc đi đọc lại hoặc thể hiện sự ngập ngừng?
3. **Evidence:** Tester có đọc phần giải thích "Vì sao AI nghĩ vậy" / trích dẫn nguồn bài học không?
4. **Control & Recovery:** Tester có biết cách đóng/hủy/chọn lại khi gợi ý không đúng ý không?
5. **Trade-off:** Sau khi thử qua các options, tester chọn phương án nào và chấp nhận đánh đổi điều gì?

### Tính năng Logging tự động dành cho Facilitator:
- Trong quá trình test, hệ thống tự động ghi lại từng mili-giây hành vi của tester.
- Ở thanh Prototype Bar (góc trên) hoặc khi kết thúc phiên: Click vào nút **`Log`** ➔ Xem bảng phân tích thời gian ➔ Click **`Copy CSV`** để dán dữ liệu khách quan vào file `prototype-feedback-note.md`!
