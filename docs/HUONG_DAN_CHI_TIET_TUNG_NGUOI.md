# HƯỚNG DẪN CHI TIẾT TỪNG NGƯỜI (NHÓM TUNG TUNG TUNG SAHUR)
*(Giai đoạn Thực thi User Testing & Hoàn tất Nộp bài Lab Day 18)*

> 🎉 **TÌNH TRẠNG HIỆN TẠI**: Nhóm đã hoàn thành trọn vẹn **Chặng 1, 2, 3 và Chặng 4 (Xây dựng Micro-Prototype hoàn chỉnh tại [`prototype/index.html`](file:///c:/Users/Vxtor/Documents/workspace/ai20k/Track1_Day18_02495_LaiBaQuan/prototype/index.html))**.  
> Prototype hỗ trợ đầy đủ 4 Options (A, B, C, D) trên 3 chủ đề thực tế (*Context Window*, *ReAct Agent*, *Gradient Descent*), có sẵn hệ thống **Logger đo lường thời gian thực** và nút **Copy CSV**.  
> 
> **PHÂN CÔNG PHỤ TRÁCH 4 OPTIONS (4 người – mỗi người 1 option):**
> 1. **Lại Bá Quân (2A202602495)**: Phụ trách **Option A (Chỉ vào chỗ kẹt - Inline Inspector & Contextual Help)** & Facilitator Tester 1
> 2. **Đỗ Lê Việt Anh (2A202602491)**: Phụ trách **Option B (Chẩn đoán 3 câu - 3-Question Diagnostic Micro-Quiz)** & Facilitator Tester 2
> 3. **Nguyễn Thị Minh Khánh (2A202602546)**: Phụ trách **Option C (AI gợi ý chủ động - Proactive Nudge Card & Confidence Reasoning)** & Facilitator Tester 3
> 4. **Nguyễn Quang Huy (2A202602421)**: Phụ trách **Option D (Hỏi người thật kèm bối cảnh - Human Escalation & Auto Context Docket)** & Facilitator Tester 4

---

## 📌 BẢNG PHÂN CÔNG THỬ NGHIỆM (CHẶNG 6 · 20–30 PHÚT)

Mỗi thành viên độc lập facilitate **1 Tester ngoài nhóm** (ưu tiên học viên khóa 3 hoặc bạn cùng lớp).  
Mỗi Tester phải được trải nghiệm **ĐỦ CẢ 4 OPTIONS (A, B, C, D)** trên cùng một chủ đề (khuyên dùng chủ đề **Context Window - Slide 12** để các phiên test có cùng hệ quy chiếu so sánh):

| Thành viên | Option phụ trách chính | Đối tượng Tester | Đường link mở test cho Tester | Nhiệm vụ chính trong phiên |
| :--- | :---: | :--- | :--- | :--- |
| **1. Lại Bá Quân** | **Option A** | **Tester 1** *(Học viên ngoài nhóm 1)* | `prototype/index.html#context/theory/A` | Cho thử A ➔ B ➔ C ➔ D; quan sát kỹ Option A; bấm Log lấy CSV; điền [prototype-feedback-note.md](file:///c:/Users/Vxtor/Documents/workspace/ai20k/Track1_Day18_02495_LaiBaQuan/prototype-feedback-note.md) |
| **2. Việt Anh** | **Option B** | **Tester 2** *(Học viên ngoài nhóm 2)* | `prototype/index.html#context/theory/B` | Cho thử B ➔ A ➔ C ➔ D; quan sát kỹ Option B; bấm Log lấy CSV; điền Feedback Note cá nhân của Anh |
| **3. Minh Khánh** | **Option C** | **Tester 3** *(Học viên ngoài nhóm 3)* | `prototype/index.html#context/theory/C` | Cho thử C ➔ A ➔ B ➔ D; quan sát kỹ Option C; bấm Log lấy CSV; điền Feedback Note cá nhân của Khánh |
| **4. Quang Huy** | **Option D** | **Tester 4** *(Học viên ngoài nhóm 4)* | `prototype/index.html#context/theory/D` | Cho thử D ➔ A ➔ B ➔ C; quan sát kỹ Option D; bấm Log lấy CSV; điền Feedback Note cá nhân của Huy |

---

## 🎯 CÁC TÍNH NĂNG VÀ VÍ DỤ CỤ THỂ TRONG PROTOTYPE KHI ĐEM ĐI TEST

### Dữ liệu bài học mẫu được dùng trong bài test:
- **Chủ đề**: Context Window (Khái niệm LLM & Chatbot) ➔ Tab **Slide 12 (Lý thuyết)**.
- **Nội dung slide**:
  - `context window ≥ token input + token output`
  - Input = system prompt + lịch sử chat + tài liệu + câu hỏi.
  - Vượt giới hạn ➔ Phần cũ bị cắt bỏ, hoặc câu trả lời bị cắt ngang.
- **Câu hỏi kiểm tra nhanh ở cuối slide**:  
  *"Model có context window 8.000 token. Prompt + tài liệu dài 7.500 token, yêu cầu tóm tắt khoảng 1.000 token. Điều gì dễ xảy ra nhất?"*  
  *(Đáp án đúng: "Bản tóm tắt bị cắt giữa chừng" - vì 7.500 + 1.000 = 8.500 > 8.000).*

---

### Cách tester tương tác với 4 Options trong Prototype:

#### 1. Option A (Chỉ vào chỗ kẹt - In-line Inspector · Quân lead):
- Mở link: `prototype/index.html#context/theory/A`
- **Thao tác**: Người học bấm nút **`Tôi vẫn chưa hiểu`** ➔ Màn hình hiện Pickbar ở dưới, các đoạn nội dung/code sáng viền vàng ➔ Người học bấm chạm vào khối công thức hoặc đoạn văn bản khó hiểu ➔ Chọn loại trợ giúp (*"Giải thích dễ hơn"*, *"Cho ví dụ"*, *"Ôn kiến thức nền"*) hoặc tự gõ câu hỏi ➔ Bấm **`Gửi`** ➔ Thẻ AI `icard` xuất hiện ngay bên dưới đoạn văn bản đó để giải thích kèm link `Nguồn: Slide 12`.
- Bấm nút `Làm lại` ở thanh trên cùng (Prototype bar) để reset trước khi chuyển option.

#### 2. Option B (Chẩn đoán 3 câu - Diagnostic Micro-Check · Việt Anh lead):
- Mở link: `prototype/index.html#context/theory/B`
- **Thao tác**: Người học bấm nút **`Tôi vẫn chưa hiểu`** ➔ Mở side panel bên phải với tiêu đề *"Trợ giảng AI: Mình hỏi nhanh 3 câu (~1 phút) để tìm đúng phần kiến thức nền bạn đang thiếu nhé. Không chấm điểm, không lưu kết quả."* ➔ Người học trả lời lần lượt 3 câu trắc nghiệm 1 chạm:
  - *Câu 1*: Token là gì? (*"Xin chào các bạn" chiếm bao nhiêu token?*)
  - *Câu 2*: Input và Output dùng chung context window (*Context window 8.000, prompt 7.900 thì câu trả lời còn dài khoảng bao nhiêu?*)
  - *Câu 3*: Bộ nhớ (*Chat rất dài, AI bắt đầu bỏ qua lời dặn ở đầu vì sao?*)
  ➔ AI đưa ra thẻ kết quả chẩn đoán `dcard` chỉ rõ lỗ hổng tri thức, thang đo độ chắc chắn (*Cao/Trung bình/Thấp*), bài ôn có đồ thị SVG minh hoạ trực quan. Có nút *"Không đúng chỗ"* để người học tự chọn lại chủ đề nếu AI chẩn đoán sai.
- Bấm nút `Làm lại` trước khi chuyển option.

#### 3. Option C (AI gợi ý chủ động - Proactive Nudge Card · Minh Khánh lead):
- Mở link: `prototype/index.html#context/theory/C`
- **Thao tác**: Người học đọc bài bình thường. Hệ thống có bộ đếm thời gian: nếu người học dừng lại quá **12 giây** trên slide hoặc vừa trả lời sai câu hỏi kiểm tra, thẻ gợi ý AI `icard nudge` sẽ **tự động trượt ra** ghim vào đúng khối nội dung nghi ngờ kẹt.
- **Điểm nổi bật**: Thẻ có các chip tín hiệu hành vi thực tế (*"4 phút ở slide này"*, *"Lật qua lại slide 11 ↔ 12 hai lần"*, *"6/10 học viên bí ở đây"*), mục mở rộng **`Vì sao AI nghĩ vậy?`** kèm thang đo độ tin cậy.
- Người học có nút *"Đúng chỗ, đã rõ hơn"*, nút *"Không phải chỗ này"* (mở danh sách đoạn để chọn lại), và link *"Tắt tự nhắc trong buổi này"*.
- Bấm nút `Làm lại` trước khi chuyển option.

#### 4. Option D (Hỏi người thật kèm bối cảnh - Human Escalation · Quang Huy lead):
- Mở link: `prototype/index.html#context/theory/D`
- **Thao tác**: Người học bấm nút **`Tôi vẫn chưa hiểu`** ➔ Một modal hiện lên mang tên *"Nhờ người hỗ trợ"*, AI **tự động điền sẵn các dòng bối cảnh** (Context Chips: Slide 12 đang học, đã dừng 4 phút, câu hỏi nhanh chưa làm/làm sai).
- Người học có thể chạm để bỏ dòng thông tin không muốn chia sẻ (bảo vệ quyền riêng tư).
- Người học chọn người nhận: **`TA Hà (Mentor lớp)`** hoặc **`Tuấn (Nhóm Lab)`** ➔ Bấm **`Gửi yêu cầu`** ➔ Mở thanh chat bên phải theo dõi tiến trình gửi (*Đã gửi ➔ Đã xem ➔ Đang trả lời ➔ Đã trả lời* sau 15 giây mô phỏng, có nút *"Vẫn chưa hiểu"* để hỏi sâu hơn).

---

## 🛠️ HƯỚNG DẪN DÙNG TÍNH NĂNG LOGGING TỰ ĐỘNG (LẤY DỮ LIỆU ĐIỀN NOTE)

1. Trong suốt quá trình tester thao tác, hệ thống tự động ghi lại từng hành vi và tính thời gian chính xác (`at`, `opt`, `t`, `evt`, `detail`).
2. Khi kết thúc phiên test với 1 option hoặc kết thúc cả buổi:
   - Click vào liên kết **`Facilitator log`** ở thanh đen trên cùng bên phải (hoặc mở `#log`).
   - Một bảng nhật ký hiện ra hiển thị đầy đủ:
     - *Mốc thời gian (t)* tính bằng giây từ lúc bắt đầu phương án.
     - *Tên sự kiện*: `open-help`, `a-select`, `a-send`, `b-answer`, `b-diag`, `c-nudge`, `d-send`, `quick-question`, v.v.
     - *Chi tiết lựa chọn và số lượt thử*.
   - Click nút **`Copy dạng CSV`** ➔ Mở file [prototype-feedback-note.md](file:///c:/Users/Vxtor/Documents/workspace/ai20k/Track1_Day18_02495_LaiBaQuan/prototype-feedback-note.md) và dán trực tiếp vào mục **OBSERVED**!

---

## 👤 HƯỚNG DẪN HÀNH ĐỘNG CỤ THỂ CHO TỪNG BẠN

### 1. Lại Bá Quân (Lead Option A):
- Hẹn **Tester 1**, mở `prototype/index.html#context/theory/A`.
- Đọc Outcome Task: *"Giả sử bạn đang tự học slide Context Window này và cảm thấy bối rối không hiểu vì sao khi chat dài model lại quên. Mục tiêu của bạn là tìm hiểu để trả lời đúng câu hỏi trắc nghiệm ở cuối trang."*
- Cho Tester 1 thử qua A ➔ B ➔ C ➔ D. Quan sát kỹ phản ứng của tester khi chạm vào khối viền vàng và chọn 3 kiểu giúp của Option A.
- Bấm `Facilitator log`, click `Copy dạng CSV`.
- Điền đầy đủ 4 lớp (*Observed, Interpreted, Decided, Still Unproven*) vào [prototype-feedback-note.md](file:///c:/Users/Vxtor/Documents/workspace/ai20k/Track1_Day18_02495_LaiBaQuan/prototype-feedback-note.md).
- Chủ trì cuộc họp nhóm Chặng 7 để điền [group-feedback-synthesis.md](file:///c:/Users/Vxtor/Documents/workspace/ai20k/Track1_Day18_02495_LaiBaQuan/group-feedback-synthesis.md).

### 2. Đỗ Lê Việt Anh (Lead Option B):
- Hẹn **Tester 2**, mở `prototype/index.html#context/theory/B`.
- Cho Tester 2 thử qua B ➔ A ➔ C ➔ D. Quan sát kỹ: Tester mất bao nhiêu giây trả lời 3 câu hỏi của Option B? Khi chẩn đoán xong, họ có đọc bài ôn và xem đồ thị SVG không? Có bấm nút *"Không đúng chỗ"* không?
- Lấy CSV log và điền Feedback Note cá nhân của Việt Anh.

### 3. Nguyễn Thị Minh Khánh (Lead Option C):
- Hẹn **Tester 3**, mở `prototype/index.html#context/theory/C`.
- Cho Tester 3 thử qua C ➔ A ➔ B ➔ D. Quan sát kỹ: Khi thẻ tự nhắc trượt ra sau 12 giây, tester giật mình hay cảm thấy được hỗ trợ kịp thời? Tester có bấm mở *"Vì sao AI nghĩ vậy"* không? Họ bấm *"Đúng chỗ"*, *"Không phải chỗ này"* hay bấm *"Tắt tự nhắc"*?
- Lấy CSV log và điền Feedback Note cá nhân của Khánh.

### 4. Nguyễn Quang Huy (Lead Option D):
- Hẹn **Tester 4**, mở `prototype/index.html#context/theory/D`.
- Cho Tester 4 thử qua D ➔ A ➔ B ➔ C. Quan sát kỹ: Khi mở modal hỗ trợ, tester có đọc các dòng bối cảnh AI điền sẵn không? Họ chọn gửi cho TA Hà hay Tuấn nhóm Lab? Độ trễ 15s chờ phản hồi có khiến họ muốn chuyển sang ChatGPT không?
- Lấy CSV log và điền Feedback Note cá nhân của Huy.

---

## ⚡ HỌP NHÓM TỔNG HỢP (CHẶNG 7) & NỘP BÀI (CHẶNG 8)
- Sau khi cả 4 bạn hoàn thành 4 phiên test, nhóm họp nhanh 15 phút:
  - Quân mở file [group-feedback-synthesis.md](file:///c:/Users/Vxtor/Documents/workspace/ai20k/Track1_Day18_02495_LaiBaQuan/group-feedback-synthesis.md).
  - Điền 4 cột tương ứng với 4 Tester của Quân, Việt Anh, Minh Khánh, Quang Huy.
  - So sánh: Option nào được tester đánh giá cao nhất? Trade-off nào khiến họ phân vân?
  - Chốt **1 Group Next Change duy nhất** cho vòng lặp tiếp theo.
  - Chốt các điểm **Still Unproven** (những điều 4 phiên test ngắn chưa thể khẳng định).
- Cập nhật mục 5 trong `README.md`, tự điền nhật ký cá nhân vào `ai-support-log.md` và push code lên GitHub!
