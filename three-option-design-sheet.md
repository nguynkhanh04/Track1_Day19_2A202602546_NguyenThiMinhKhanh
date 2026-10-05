# THREE-OPTION DESIGN SHEET (BẢN CHUẨN THEO PROTOTYPE THỰC TẾ)

> **Nhóm:** Tung Tung Tung Sahur  
> **Thành viên:** Nguyễn Thị Minh Khánh (2A202602546), Lại Bá Quân (2A202602495), Đỗ Lê Việt Anh (2A202602491), Nguyễn Quang Huy (2A202602421)  
> **Case Study:** Case A - AI Tutor: Diagnostic Refresher (Hỗ trợ người học vượt qua điểm nghẽn kiến thức trên nền tảng VLearn)

---

## PHẦN 1: TỔNG HỢP EVIDENCE & CHỐT HYPOTHESIS PROBLEM (CHẶNG 1)

### 1. Bảng đối chiếu Evidence (Fact vs. Interpretation)
| Practice Note | Người dùng thực sự làm/nói gì? (Raw Fact / Quote từ Người học) | Điều nhóm diễn giải / suy đoán (Interpretation) |
| :--- | :--- | :--- |
| **Note 1**<br>• *Interviewer*: Đỗ Lê Việt Anh<br>• *Interviewee*: **Học viên khóa 3 (Lab Coach)** | *"Nghe giảng các thầy cô thì hiểu nhưng mà có một số các lý thuyết thì nhìn slide đương nhiên nhìn lại mà nó viết tắt thì chắc chắn không hiểu"*. Người học mất 30p–1h tra AI/YouTube để học lại; cảm thấy nản. | Người học hiểu đại ý khi nghe giảng nhưng bị đứt mạch khi tự ôn vì **thuật ngữ viết tắt / khái niệm cô đọng** trên slide bài giảng. |
| **Note 2**<br>• *Interviewer*: Nguyễn Thị Minh Khánh<br>• *Interviewee*: **Lan (Học viên VLearn)** | Nhận ra mình chưa hiểu khi **làm Quiz/Checkpoint và bị sai đáp án**. Người học khẳng định nếu công cụ hỗ trợ bắt chờ 3–5 phút thì sẽ **chuyển tab sang ChatGPT** vì quá lâu; mong muốn câu hỏi chẩn đoán bấm chọn nhanh dưới 1 phút. | **Thời điểm vàng kích hoạt (Trigger) là khi làm sai Checkpoint**. Người học yêu cầu độ trễ cực thấp (< 1 phút) và cơ chế chọn nhanh (1 chạm), không muốn gõ chữ dài. |
| **Note 3**<br>• *Interviewer*: Lại Bá Quân<br>• *Interviewee*: **Học viên tự học Cloud/Dev** | Người học bỏ qua video lý thuyết lướt, nhảy thẳng sang làm lab vì *"quay lại làm lab dễ hiểu hơn"*. Vừa gõ lab vừa mở ChatGPT hỏi *"cái này dùng để làm gì, có tác dụng gì"*. Thường xuyên không làm xong bài trong ca lab 4 tiếng trên lớp và phải mang về nhà. | Người học chuộng **Hands-on (học qua thực hành)**. Lý thuyết phải gắn liền với **tác dụng thực tế trong bài lab**, không chấp nhận lý thuyết hàn lâm suông. |
| **Note 4**<br>• *Interviewer*: Nguyễn Quang Huy<br>• *Interviewee*: **Học viên Khóa 3 (Nam)** | Người học chụp cả ảnh slide hoặc copy nguyên văn text ném vào ChatGPT. Nhận thức rằng AI trả lời sai ý là *"do con chat lan man và prompt của mình chưa clear"*. Chịu áp lực thời gian lớn vì phải học 2 buổi/ngày. | Người học **chưa biết cách đặt prompt chuẩn**, dẫn đến việc copy/paste máy móc vào AI ngoài và nhận lại câu trả lời lan man, làm trầm trọng thêm áp lực thời gian. |

### 2. Phát biểu Hypothesis Problem chuẩn của nhóm
- **Hypothesis Problem nhóm tiếp tục:**  
  *Khi **bắt đầu ôn tập kiến thức bị hổng trước kỳ thi hoặc làm bài Lab trên VLearn**, **học viên CNTT** gặp khó khăn trong việc **xác định chính xác và ôn luyện đúng phần kiến thức mình còn yếu** vì **các khái niệm trừu tượng (như Token, Context Window, Tool Calling, Gradient Descent) trên slide bài giảng quá cô đọng, bài kiểm tra chẩn đoán thông thường quá dài và giải thích của AI ngoài chưa trúng ngữ cảnh**, dẫn đến **người học bị đứt mạch học, mất 30–60 phút phải chuyển tab sang ChatGPT ngoài với prompt chưa chuẩn nhận về câu trả lời lan man, và thường xuyên không hoàn thành được bài học trong 4 tiếng trên lớp**.*
- **Evidence ban đầu hỗ trợ giả thuyết:**  
  - 100% người học được phỏng vấn (4/4) đều sử dụng ChatGPT bên ngoài như một phương án chữa cháy bắt buộc khi không hiểu bài.
  - Hậu quả thực tế được ghi nhận: Mất 30–60 phút tự mày mò (Note 1); không kịp nộp bài trong ca lab 4 tiếng (Note 3); chịu áp lực học cả ngày, prompt chưa chuẩn nên AI trả lời lan man (Note 4); và sẵn sàng bỏ công cụ nếu bắt chờ quá 3 phút (Note 2).
- **Điều quan trọng vẫn chưa được chứng minh:**  
  - Liệu việc đưa sự trợ giúp trực tiếp ngay tại ngữ cảnh bài học (In-context) có thực sự giúp người học hiểu bản chất và làm lab nhanh hơn, hay họ vẫn giữ phản xạ copy/paste sang ChatGPT ngoài?

---

## PHẦN 2: CHỌN CÁC SOLUTION OPTIONS (CHẶNG 2)
*(Được hiện thực hóa trọn vẹn trong `prototype/index.html`)*

### 1. Phân công phụ trách 4 Options trong nhóm (4 người – mỗi người 1 Option)
| Option | Tên phương án & Cơ chế Human–AI | Thành viên phụ trách chính (Owner) | Nhiệm vụ chính |
| :---: | :--- | :--- | :--- |
| **A** | **Chỉ vào chỗ kẹt** *(Inline Term/Block Inspector - Don't Act)* | **Lại Bá Quân** (2A202602495) | Thiết kế tương tác chạm khối văn bản/code, Pickbar 3 chế độ trợ giúp, thẻ `icard` in-line và trích dẫn slide. |
| **B** | **Chẩn đoán 3 câu** *(3-Question Diagnostic Micro-Quiz - Ask)* | **Đỗ Lê Việt Anh** (2A202602491) | Thiết kế bộ 3 câu hỏi trắc nghiệm 1 chạm, logic chẩn đoán lỗ hổng tri thức, thẻ `dcard`, đồ thị SVG minh hoạ và nút ghi đè. |
| **C** | **AI gợi ý chủ động** *(Proactive Context Nudge Card - Act)* | **Nguyễn Thị Minh Khánh** (2A202602546) | Thiết kế bộ đếm thời gian 12s/bắt lỗi Checkpoint, thẻ `icard.nudge`, chip tín hiệu hành vi, mục giải trình *"Vì sao AI nghĩ vậy"* và nút tắt tự nhắc. |
| **D** | **Hỏi người thật** *(Human Escalation & Auto Context Docket - Suggest)* | **Nguyễn Quang Huy** (2A202602421) | Thiết kế modal gom bối cảnh tự động, cơ chế chọn người nhận (TA Hà / Tuấn nhóm Lab), bảo vệ quyền riêng tư và panel theo dõi tiến trình phản hồi. |

---

### 2. Những thứ BẮT BUỘC GIỮ NGUYÊN (70% Shared Core)
- **Target User:** Học viên CNTT đang học trên nền tảng VLearn.
- **Situation:** Đang trong buổi học, đối mặt với bài học Slide lý thuyết hoặc bài thực hành Lab.
- **3 Chủ đề kiến thức mẫu (Content Fixtures):**
  1. **Chủ đề 1: Context Window** (`context`):
     - *Slide 12 (Lý thuyết)*: Công thức `context window ≥ token input + token output`. Vì sao chat dài thì model quên lời dặn ở đầu.
     - *Lab 4 Task 2 (Chatbot nhớ hội thoại)*: Hoàn thiện hàm `trim_history(messages, max_tokens=8000, reserve=1000)` trong `chat.py`. Ngân sách input = `max_tokens - reserve`.
     - *Checkpoint*: Context window 8.000 token, prompt 7.500 token, tóm tắt 1.000 token ➔ Câu trả lời bị cắt giữa chừng.
  2. **Chủ đề 2: ReAct Agent** (`react`):
     - *Slide 9 (Lý thuyết)*: Vòng lặp `Thought → Action → Observation → Answer`. Model trả về `tool_calls`, code ứng dụng chạy tool (Action), trả về qua role `"tool"` (Observation).
     - *Lab 3 Task 2.2 (Lập trình ReAct Loop)*: Hoàn thiện vòng `while step < MAX_STEPS` trong `agent.py`.
     - *Checkpoint*: Observation là gì / Model trả về tool_calls thì code cần làm gì tiếp theo.
  3. **Chủ đề 3: Gradient Descent** (`gd`):
     - *Slide 7 (Lý thuyết)*: Công thức cập nhật trọng số $w \leftarrow w - \eta \cdot \frac{\partial L}{\partial w}$. Gradient chỉ hướng dốc lên, dấu trừ để đi xuống dốc, $\eta$ là learning rate.
     - *Lab 9 Task 2 (Train MLP đầu tiên)*: Thử 3 giá trị `lr = 1.0, 0.1, 0.001` trong `train.py` và phát hiện hiện tượng loss tăng vọt.
     - *Checkpoint*: Tính $w$ mới khi biết $w=3, \eta=0.1$ hoặc xử lý khi loss tăng vọt.
- **Task chung:** Đọc hiểu nội dung và trả lời đúng Câu hỏi nhanh (Slide) hoặc Checkpoint (Lab).
- **Desired Outcome:** Nắm bắt được bản chất kiến thức trong vòng < 60 giây, trả lời đúng câu hỏi kiểm tra và tiếp tục bài học mà không cần mở tab khác.

---

### 3. Bảng so sánh 4 Options (Comparison Contract trong Prototype)
| Tiêu chí | Option A: Chạm vào đoạn chưa hiểu *(Quân lead)* | Option B: Chẩn đoán 3 câu *(Việt Anh lead)* | Option C: AI tự nhắc *(Minh Khánh lead)* | Option D: Hỏi người thật *(Quang Huy lead)* |
| :--- | :--- | :--- | :--- | :--- |
| **Solution Mechanism** | Bấm nút **`Tôi vẫn chưa hiểu`** ➔ Màn hình hiện Pickbar ở dưới, chạm vào khối văn bản/code khó hiểu (sáng viền vàng) ➔ Chọn kiểu giúp (*"Giải thích dễ hơn"*, *"Cho ví dụ"*, *"Ôn kiến thức nền"*) hoặc tự gõ câu hỏi ➔ Thẻ AI in-line `icard` giải thích ngay bên dưới kèm trích dẫn nguồn bài giảng. | Bấm nút **`Tôi vẫn chưa hiểu`** ➔ Mở side panel "Trợ giảng AI", trả lời 3 câu trắc nghiệm 1 chạm (~1 phút) ➔ Thẻ `dcard` phân loại lỗ hổng kiến thức kèm mức độ chắc chắn (*Cao, Trung bình, Thấp*), bài ôn có đồ thị SVG minh hoạ trực quan. | Hệ thống theo dõi tín hiệu (dừng >12s hoặc làm sai câu hỏi kiểm tra) ➔ Tự động trượt thẻ gợi ý `icard.nudge` kèm ghim đỏ *"AI nghĩ bạn bí ở đây"*, chip tín hiệu hành vi và mục giải trình *"Vì sao AI nghĩ vậy"*. | Bấm nút **`Tôi vẫn chưa hiểu`** ➔ Mở modal "Nhờ người hỗ trợ" tự động gom bối cảnh (slide, thời gian, số lần thử sai) ➔ Chọn gửi tới TA Hà (Mentor) hoặc Tuấn (Đồng đội) ➔ Side panel chat mô phỏng theo dõi trạng thái phản hồi. |
| **User làm gì?** | Bấm nút trợ giúp ➔ Chạm đoạn kẹt ➔ Chọn kiểu giúp (*"Giải thích dễ hơn / Cho ví dụ / Ôn kiến thức nền"*) ➔ Bấm Gửi ➔ Đọc thẻ in-line và bấm *"Đã rõ hơn → câu hỏi nhanh"*. | Bấm nút trợ giúp ➔ Bấm chọn 3 câu trắc nghiệm nhanh ➔ Đọc kết quả chẩn đoán và lời giải thích ➔ Nếu AI đoán sai bấm *"Không đúng chỗ"* để chọn lại chủ đề khác. | Đang học ➔ Thấy khối viền đỏ và thẻ gợi ý trượt ra ➔ Bấm *"Đúng chỗ, đã rõ hơn"*, *"Không phải chỗ này"* (chọn lại đoạn thật sự bí), xem *"Vì sao AI nghĩ vậy"*, hoặc *"Tắt tự nhắc"*. | Bấm nút trợ giúp ➔ Duyệt người nhận (Coach/Bạn) ➔ Bật/tắt các thẻ bối cảnh muốn chia sẻ ➔ Nhập ghi chú (tùy chọn) ➔ Bấm Gửi yêu cầu ➔ Chờ và đọc phản hồi. |
| **AI làm gì?** | Đóng vai trò tra cứu ngữ cảnh vi mô tại đúng vị trí đoạn văn bản được chọn. Không suy diễn ngoài đoạn học viên chọn. | Đóng vai trò bác sĩ chẩn đoán tri thức, phân loại học viên đang hổng ở kiến thức nền nào qua 3 câu trắc nghiệm. | Tự động phân tích tín hiệu hành vi và chủ động đề xuất kiến thức liên quan kèm mức độ tin cậy. | Đóng vai trò thư ký tự động gom bối cảnh học tập, số lần thử lỗi và chuyển tiếp cho người thật trả lời. |
| **Trigger kích hoạt** | **User-initiated** (Người học chủ động bấm nút trợ giúp và chạm đoạn nội dung). | **User-initiated** (Người học bấm nút trợ giúp khi cảm thấy kẹt). | **Proactive / System-initiated** (Hệ thống tự động kích hoạt sau 12s idle hoặc khi trả lời sai). | **User-initiated** (Người học chủ động nhờ người hỗ trợ khi AI không giải quyết được). |
| **Trade-off chính** | Cực nhanh (<5s), không đứt mạch; **Đánh đổi:** Chỉ giải quyết đoạn nhỏ được chọn, không bóc tách được lỗ hổng tư duy tổng thể. | Đánh trúng gốc rễ hiểu sai; **Đánh đổi:** Tốn thêm ~1 phút thao tác trả lời 3 câu trắc nghiệm chẩn đoán. | Tiết kiệm công tìm kiếm; **Đánh đổi:** Dễ gây phân tâm nếu AI tự động nhảy ra sai thời điểm hoặc đoán sai ý. | Đảm bảo tính chính xác và an tâm tuyệt đối; **Đánh đổi:** Phụ thuộc vào độ trễ phản hồi của con người (~10 phút). |

---

### 4. Distance Check (Kiểm tra khoảng cách khác biệt)
- **A khác B vì:** Option A hoàn toàn thụ động chờ người dùng chỉ định điểm nghẽn (Lookup tại chỗ), trong khi Option B là quy trình chẩn đoán đối thoại 2 chiều qua 3 câu hỏi để bóc tách nhận thức (Co-creation).
- **B khác C vì:** Option B người dùng chủ động kích hoạt và trả lời câu hỏi phân loại (AI Ask - User Decides), trong khi Option C là AI tự động can thiệp dựa trên tín hiệu hành vi (AI Proactive Act - User Reviews).
- **C khác D vì:** Option C do máy tính (AI) hoàn toàn tự động sinh nội dung hỗ trợ, trong khi Option D là cơ chế leo thang (Human Escalation) chuyển giao cho con người thật (Lab Coach / Đồng đội).

---

## PHẦN 3: HUMAN–AI DESIGN PASS (CHẶNG 3)

### Human–AI Decision Table
| Tiêu chí thiết kế | Option A: Chạm vào đoạn chưa hiểu | Option B: Chẩn đoán 3 câu | Option C: AI tự nhắc *(Minh Khánh lead)* | Option D: Hỏi người thật |
| :--- | :--- | :--- | :--- | :--- |
| **1. Role & Agency** | - User: Chạm chọn đoạn kẹt.<br>- AI: Trả lời ngắn tại chỗ.<br>➔ **Don't Act** *(User-initiated)*. | - User: Trả lời 3 câu hỏi.<br>- AI: Đưa ra chẩn đoán.<br>➔ **Ask** *(Co-creation)*. | - User: Duyệt/bỏ qua gợi ý.<br>- AI: Tự phát hiện và đề xuất.<br>➔ **Act** *(Proactive)*. | - User: Duyệt bối cảnh & gửi.<br>- AI: Thư ký gom dữ liệu.<br>➔ **Suggest** *(Escalation)*. |
| **2. Expectation** | Thanh Pickbar ghi rõ: *"AI chỉ trả lời đúng phần bạn chọn, dựa trên slide này. AI không tự đoán bạn đang thiếu gì"*. | AI chào rõ ràng: *"Mình hỏi nhanh 3 câu (~1 phút) để tìm đúng phần kiến thức nền bạn đang thiếu nhé. Không chấm điểm, không lưu kết quả"*. | Thẻ ghi rõ mức độ tin cậy và nêu rõ: *"AI suy ra từ hành vi của bạn và học viên khác, chưa hỏi bạn câu nào, nên có thể đoán sai"*. | Modal ghi rõ: *"Trợ giảng AI đã soạn sẵn yêu cầu từ những gì bạn đang học. Người thật sẽ trả lời; AI không tự giải thích"* kèm thời gian dự kiến (*"Thường trả lời trong ~10 phút"*). |
| **3. Evidence & Uncertainty** | Trích xuất nguồn chính xác: Nút `cite` (*"Xem lại lý thuyết: Slide X · Đoạn"*), câu nối liên kết (`bridge`) và ví dụ minh họa. | Hiển thị ma trận căn cứ: Thước đo **Độ chắc chắn (Cao / Trung bình / Thấp)**, dải huy hiệu mini `[✓]`, `[✗]`, `[?]` và mục mở rộng *"Xem chi tiết từng câu"*. | Thẻ tín hiệu thực tế: *"4 phút ở slide này"*, *"Lật slide 2 lần"*, *"6/10 học viên bí ở đây"*, kèm mục *"Vì sao AI nghĩ vậy?"*. | Hiển thị đầy đủ danh sách các thẻ bối cảnh (Context Chips: slide đang học, thời gian dừng, số lần thử sai câu hỏi) được gửi đi. |
| **4. Control & Recovery** | Bấm nút `Huỷ`, bấm `×`, bấm Esc hoặc click ra ngoài để đóng tức thì (<1s). Có nút *"Sửa câu hỏi"* sau khi đã nhận giải thích. | Có nút *"Không đúng chỗ"* để tự chọn chủ đề muốn ôn ghi đè chẩn đoán; nút *"Làm lại 3 câu"*; nút `×` đóng panel bất cứ lúc nào. | Có nút *"Không phải chỗ này"* (chuyển sang chọn đoạn thật sự bí hoặc chọn topic thay thế); nút *"Tắt tự nhắc trong buổi này"* (có nút bật lại ở helpbar). | Người học có quyền tick/untick từng thẻ bối cảnh trước khi gửi để bảo vệ quyền riêng tư; nút *"Huỷ yêu cầu"*; nút *"Vẫn chưa hiểu"* để yêu cầu giải thích sâu hơn. |
