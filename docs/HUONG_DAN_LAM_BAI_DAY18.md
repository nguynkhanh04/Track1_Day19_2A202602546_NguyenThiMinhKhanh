# HƯỚNG DẪN THỰC CHIẾN BÀI LAB DAY 18: TỪ PROTOTYPE ĐẾN USER TESTING
*(Dành riêng cho nhóm Tung Tung Tung Sahur: Bá Quân, Việt Anh, Minh Khánh, Quang Huy)*

> **TÌNH TRẠNG HIỆN TẠI CỦA NHÓM**:
> - ✅ **Chặng 1, 2, 3**: Đã hoàn thành 100% trong [three-option-design-sheet.md](file:///c:/Users/Vxtor/Documents/workspace/ai20k/Track1_Day18_02495_LaiBaQuan/three-option-design-sheet.md).
> - ✅ **Chặng 4 & 5 (Xây dựng Prototype & Kịch bản test)**: **ĐÃ HOÀN THÀNH 100%** tại file [`prototype/index.html`](file:///c:/Users/Vxtor/Documents/workspace/ai20k/Track1_Day18_02495_LaiBaQuan/prototype/index.html) với đầy đủ 4 Options (A, B, C, D), 3 chủ đề kiến thức thực tế (*Context Window*, *ReAct Agent*, *Gradient Descent*), 2 chế độ (*Lý thuyết Slide* & *Thực hành Lab*), kịch bản Outcome Task và hệ thống **Logger đo lường thời gian thực** kèm nút **Copy dạng CSV**.
> 
> **PHÂN CÔNG 4 THÀNH VIÊN PHỤ TRÁCH 4 OPTIONS**:
> 1. **Lại Bá Quân** (2A202602495): Phụ trách **Option A** (Chỉ vào chỗ kẹt - Inline Inspector) & Facilitator Tester 1
> 2. **Đỗ Lê Việt Anh** (2A202602491): Phụ trách **Option B** (Chẩn đoán 3 câu - Diagnostic Micro-Quiz) & Facilitator Tester 2
> 3. **Nguyễn Thị Minh Khánh** (2A202602546): Phụ trách **Option C** (AI gợi ý chủ động - Proactive Nudge Card) & Facilitator Tester 3
> 4. **Nguyễn Quang Huy** (2A202602421): Phụ trách **Option D** (Hỏi người thật kèm bối cảnh - Human Escalation) & Facilitator Tester 4
> 
> Tài liệu này hướng dẫn **CÁC BƯỚC THỰC THI TIẾP THEO**: Chạy User Testing (Chặng 6), Họp tổng hợp nhóm (Chặng 7) và Hoàn tất hồ sơ nộp bài (Chặng 8).

---

## 🧭 CÁC BƯỚC CẦN THỰC HIỆN TIẾP THEO

```
[ĐÃ XONG 100%]: Chặng 1, 2, 3 (Design Sheet) + Chặng 4 & 5 (Web Prototype index.html)
                                      ↓
[BƯỚC 1 - CHẶNG 6]: 4 Thành viên độc lập Test với 4 Tester ngoài nhóm (20–30 phút)
                    (Cho thử A ➔ B ➔ C ➔ D ➔ Bấm nút "Facilitator log" copy CSV ➔ Điền note cá nhân)
                                      ↓
[BƯỚC 2 - CHẶNG 7]: Họp nhóm 15 phút tổng hợp Ma trận 4 Testers & Chốt 1 Next Change
                    (Ghép dữ liệu vào group-feedback-synthesis.md)
                                      ↓
[BƯỚC 3 - CHẶNG 8]: Hoàn thiện 6 files trong Repo cá nhân & Nộp bài lên GitHub (15 phút)
```

---

## 🧪 BƯỚC 1: TIẾN HÀNH TEST VỚI 4 TESTER ĐỘC LẬP (CHẶNG 6 · 20–30 PHÚT)
* **Hình thức**: 👤 **CÁ NHÂN ĐỘC LẬP THỰC HIỆN**
* **Mục tiêu**: Mỗi người hẹn 1 bạn ngoài nhóm (ưu tiên học viên khóa 3 hoặc bạn cùng lớp), cho thử **ĐỦ CẢ 4 OPTIONS (A, B, C, D)** trên cùng một chủ đề (khuyên dùng **Context Window - Slide 12**) và tự ghi chép.

### 1. Phân công 4 phiên test:
- **Lại Bá Quân**: Test với **Tester 1** ➔ Quan sát kỹ phản ứng với Option A và các phương án so sánh ➔ Ghi chép vào [prototype-feedback-note.md](file:///c:/Users/Vxtor/Documents/workspace/ai20k/Track1_Day18_02495_LaiBaQuan/prototype-feedback-note.md).
- **Đỗ Lê Việt Anh**: Test với **Tester 2** ➔ Quan sát kỹ phản ứng với Option B ➔ Ghi chép vào Note cá nhân của Việt Anh.
- **Nguyễn Thị Minh Khánh**: Test với **Tester 3** ➔ Quan sát kỹ phản ứng với Option C ➔ Ghi chép vào Note cá nhân của Khánh.
- **Nguyễn Quang Huy**: Test với **Tester 4** ➔ Quan sát kỹ phản ứng với Option D ➔ Ghi chép vào Note cá nhân của Huy.

### 2. Trình tự 20 phút phỏng vấn mỗi tester:
- **Phút 0–2: Chào hỏi & Đặt câu hỏi Relevant Context**:
  > *"Chúng mình đang thử nghiệm vài cách tương tác hỗ trợ học tập, test hệ thống chứ không test bạn. Bạn cứ thao tác thoải mái và nói to suy nghĩ của mình nhé."*  
  > *"Gần đây khi học bài hoặc làm Lab trên VLearn mà gặp phải một đoạn lý thuyết khó hiểu hoặc chạy code báo lỗi, bạn thường làm gì đầu tiên để giải quyết?"*
- **Phút 2–14: Giao Outcome Task và cho trải nghiệm lần lượt 4 Options**:
  - Mở link: `prototype/index.html#context/theory/A` (hoặc B/C/D).
  - Đọc Outcome Task:  
    > *"Giả sử bạn đang tự học slide Context Window này và cảm thấy bối rối không hiểu vì sao khi chat dài model lại quên lời dặn ở đầu. Mục tiêu của bạn là tìm hiểu để trả lời đúng câu hỏi trắc nghiệm ở cuối trang."*  
    *(⚠️ Lưu ý: Tuyệt đối không chỉ tester bấm vào đâu! Hãy để họ tự nhìn và thao tác).*
  - **Trải nghiệm lần lượt**:
    1. Thử **Option A** (`#context/theory/A`): Bấm nút *"Tôi vẫn chưa hiểu"*, chạm khối viền vàng, chọn kiểu giúp hoặc gõ câu hỏi, đọc thẻ `icard`. Bấm nút `Làm lại` ở thanh Prototype bar trên cùng.
    2. Thử **Option B** (`#context/theory/B`): Bấm nút *"Tôi vẫn chưa hiểu"*, trả lời 3 câu trắc nghiệm 1 chạm trong side panel, đọc thẻ chẩn đoán `dcard` và xem đồ thị SVG. Bấm `Làm lại`.
    3. Thử **Option C** (`#context/theory/C`): Đọc bình thường, sau 12 giây thẻ tự nhắc `icard.nudge` trượt ra. Xem mục *"Vì sao AI nghĩ vậy"*, thử bấm *"Đúng chỗ"* hoặc *"Không phải chỗ này"*. Bấm `Làm lại`.
    4. Thử **Option D** (`#context/theory/D`): Bấm *"Tôi vẫn chưa hiểu"*, xem modal gom bối cảnh tự động, chọn người gửi (TA Hà / Tuấn nhóm Lab), gửi và quan sát trạng thái phản hồi.
- **Phút 14–18: Hỏi 3 câu so sánh trải nghiệm**:
  1. *"Trong 4 cách vừa rồi, cách nào giúp bạn hiểu bản chất vấn đề và đỡ tốn thời gian nhất? Vì sao?"*
  2. *"Bạn thích tự mình chỉ định chỗ kẹt (như Option A) hay muốn AI tự chẩn đoán (như Option B, C) hay nhờ người thật (như Option D)?"*
  3. *"Điều gì ở phương án bạn thích nhất khiến bạn vẫn cảm thấy chưa thực sự hài lòng (trade-off)?"*
- **Phút 18–20: Trích xuất Log và điền 4 lớp vào Feedback Note**:
  - Click vào link **`Facilitator log`** ở thanh góc trên bên phải màn hình (hoặc URL `#log`).
  - Click nút **`Copy dạng CSV`**.
  - Mở file [prototype-feedback-note.md](file:///c:/Users/Vxtor/Documents/workspace/ai20k/Track1_Day18_02495_LaiBaQuan/prototype-feedback-note.md) và dán log CSV vào mục **OBSERVED**.
  - Hoàn thiện 4 lớp: **OBSERVED**, **INTERPRETED**, **DECIDED**, **STILL UNPROVEN**.

> 🏁 **CHECKPOINT BƯỚC 1**:
> - [ ] Cả 4 thành viên hoàn thành 4 phiên test độc lập với 4 người ngoài nhóm.
> - [ ] Cả 4 tester đều được trải nghiệm ĐỦ CẢ 4 OPTIONS trên cùng chủ đề bài học.
> - [ ] Mỗi người trích xuất được log CSV thời gian thực và hoàn thiện Feedback Note cá nhân.

---

## 🤝 BƯỚC 2: HỌP NHÓM TỔNG HỢP & CHỐT NEXT CHANGE (CHẶNG 7 · 15 PHÚT)
* **Hình thức**: 👥 **CỘNG TÁC CẢ NHÓM**
* **Mục tiêu**: Ghép 4 bản ghi chép vào [group-feedback-synthesis.md](file:///c:/Users/Vxtor/Documents/workspace/ai20k/Track1_Day18_02495_LaiBaQuan/group-feedback-synthesis.md), rút ra quy luật chung và chốt 1 quyết định thay đổi tiếp theo.

### Các việc cần làm trong cuộc họp:
1. **Điền ma trận 4 testers**:
   - Từng thành viên đọc tóm tắt: Tester của mình đã bấm gì đầu tiên? Bị nghẽn ở đâu? Cách lấy lại control? Chọn option nào và than phiền điều gì?
   - Điền vào 4 cột tương ứng trong bảng so sánh tại [group-feedback-synthesis.md](file:///c:/Users/Vxtor/Documents/workspace/ai20k/Track1_Day18_02495_LaiBaQuan/group-feedback-synthesis.md).
2. **Tìm Quy luật chung (Pattern) hoặc Khác biệt nổi bật**:
   - So sánh định lượng thời gian từ log CSV và định tính từ phản hồi tester.
   - Ví dụ: *"Đa số tester thích sự chính xác của Option A và Option B nhưng ngại gõ chữ dài; Option C bị một số người phàn nàn vì tự động nhảy ra khi họ đang tập trung đọc bài; Option D được đánh giá cao khi gặp lỗi code phức tạp nhưng không phù hợp khi cần ôn nhanh lý thuyết"*.
3. **Chốt 1 Group Next Change duy nhất**:
   - Thống nhất câu trả lời cho: *"Ở vòng lặp tiếp theo, nhóm sẽ thay đổi gì?"*
   - *Ví dụ*: *"Nhóm quyết định kết hợp cơ chế chẩn đoán 3 câu của Option B làm lõi chính, nhưng tích hợp khả năng chạm chọn khối văn bản của Option A để người học tự định tuyến kiến thức khi AI chẩn đoán sai, đồng thời bổ sung cơ chế leo thang Option D khi làm sai quá 2 lần."*
4. **Ghi rõ các điểm Still Unproven**:
   - Thừa nhận khách quan giới hạn của 4 phiên test: *"Chưa chứng minh được hiệu quả của công cụ trong các bài lab dài đòi hỏi nhiều bước debug phức tạp và chưa đo lường được mức độ duy trì kiến thức lâu dài của người học sau khi rời khỏi VLearn."*

> 🏁 **CHECKPOINT BƯỚC 2**:
> - [ ] Bảng ma trận 4 testers được điền đầy đủ thông tin từ 4 thành viên.
> - [ ] Chốt 1 Group Next Change duy nhất dựa trên bằng chứng thực tế, không bình bầu theo cảm tính.

---

## 📦 BƯỚC 3: HOÀN THIỆN REPO CÁ NHÂN & NỘP BÀI (CHẶNG 8 · 15 PHÚT)
* **Hình thức**: 👤 **CÁ NHÂN TỰ LÀM VÀ NỘP REPO RIÊNG**
* **Tên thư mục / Repo**: `Track1_Day18_02495_LaiBaQuan`

### Checklist 6 files nộp bài bắt buộc ở thư mục gốc:
- [x] **`README.md`**: Đã điền sẵn thông tin nhóm 4 người, phân công 4 options, Hypothesis Problem, 4 Options trong prototype và phần đóng góp của bạn. Bạn chỉ cần cập nhật mục 5 (kết quả sau Bước 2).
- [x] **`three-option-design-sheet.md`**: Đã hoàn thành 100% (Evidence, Hypothesis, Shared Core, Comparison Contract, Human–AI Decision Table).
- [x] **`prototype-link.md`**: Đã chứa đầy đủ hướng dẫn mở file local [`prototype/index.html`](file:///c:/Users/Vxtor/Documents/workspace/ai20k/Track1_Day18_02495_LaiBaQuan/prototype/index.html), danh mục URL hash cho 4 options, bối cảnh dữ liệu và kịch bản test.
- [ ] **`prototype-feedback-note.md`**: Bản ghi chép phiên test với Tester 1 của chính bạn từ Bước 1 (dán log CSV và điền 4 lớp).
- [ ] **`group-feedback-synthesis.md`**: Bảng tổng hợp 4 testers và Group Next Change nhóm chốt từ Bước 2.
- [ ] **`ai-support-log.md`**: Tự điền nhật ký sử dụng AI cá nhân (đã có khung mẫu sẵn).

---

## ⚡ HÀNH ĐỘNG NGAY BÂY GIỜ
1. Mở file [`prototype/index.html`](file:///c:/Users/Vxtor/Documents/workspace/ai20k/Track1_Day18_02495_LaiBaQuan/prototype/index.html) trên trình duyệt, bấm thử thanh Prototype bar, chọn hash `#context/theory/A`.
2. Quân hẹn **Tester 1**, Việt Anh hẹn **Tester 2**, Minh Khánh hẹn **Tester 3**, Quang Huy hẹn **Tester 4**.
3. Tiến hành test 20 phút, bấm `Facilitator log` ➔ `Copy dạng CSV` ➔ Dán vào note cá nhân.
4. Nhóm họp nhanh 15 phút chốt `group-feedback-synthesis.md` và push code lên GitHub!
