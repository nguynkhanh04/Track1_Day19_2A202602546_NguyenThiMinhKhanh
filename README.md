# BÁO CÁO LAB: TỪ EVIDENCE ĐẾN 4 HUMAN–AI PROTOTYPES

## 1. THÔNG TIN CÁ NHÂN VÀ NHÓM
- **Mã học viên (MHV):** 2A202602546
- **Họ và tên:** Nguyễn Thị Minh Khánh
- **Tên nhóm:** Tung Tung Tung Sahur
- **Thành viên trong nhóm & Phân công nhiệm vụ (4 người - mỗi người 1 option):**
  1. **Lại Bá Quân (2A202602495)**: Phụ trách **Option A (Chỉ vào chỗ kẹt - Inline Inspector & Contextual Help)** & Điều phối Tester 1
  2. **Đỗ Lê Việt Anh (2A202602491)**: Phụ trách **Option B (Chẩn đoán 3 câu - 3-Question Diagnostic Micro-Quiz)** & Điều phối Tester 2
  3. **Nguyễn Thị Minh Khánh (2A202602546)**: Phụ trách **Option C (AI gợi ý chủ động - Proactive Nudge Card & Confidence Reasoning)** & Điều phối Tester 3
  4. **Nguyễn Quang Huy (2A202602421)**: Phụ trách **Option D (Hỏi người thật kèm bối cảnh - Human Escalation & Auto Context Docket)** & Điều phối Tester 4
- **Case study được chọn:** Case A - AI Tutor: Diagnostic Refresher *(Tiếp tục từ Day 17)*

---

## 2. HYPOTHESIS PROBLEM
- **Vấn đề giả định tiếp tục từ Day 17:**  
  *Khi **bắt đầu ôn tập kiến thức bị hổng trước kỳ thi hoặc làm bài Lab trên VLearn**, **học viên CNTT** gặp khó khăn trong việc **xác định chính xác và ôn luyện đúng phần kiến thức mình còn yếu** vì **các khái niệm trừu tượng (như Token, Context Window, Tool Calling, Gradient Descent) trên slide bài giảng quá cô đọng, bài kiểm tra chẩn đoán thông thường quá dài và giải thích của AI ngoài chưa trúng ngữ cảnh**, dẫn đến **người học bị đứt mạch học, mất 30–60 phút phải chuyển tab sang ChatGPT ngoài với prompt chưa chuẩn nhận về câu trả lời lan man, và thường xuyên không hoàn thành được bài học trong 4 tiếng trên lớp**.*
- **Bằng chứng thực tế ban đầu hỗ trợ giả thuyết (từ 4 Practice Notes):**  
  - 100% người học được phỏng vấn (4/4) đều sử dụng ChatGPT bên ngoài như một phương án chữa cháy bắt buộc khi không hiểu bài.
  - Hậu quả thực tế được ghi nhận từ 4 người học: Người học trong phiên của Việt Anh mất 30–60 phút tra cứu ngoài; người học trong phiên của Bá Quân thường xuyên không kịp nộp bài trong ca 4 tiếng; người học trong phiên của Quang Huy chịu áp lực lớn vì prompt chưa chuẩn nên AI trả lời lan man; và người học trong phiên của Minh Khánh (Lan) khẳng định sẽ bỏ sang ChatGPT nếu công cụ bắt chờ quá 3 phút.
- **Điều quan trọng vẫn chưa được chứng minh:**  
  - Liệu việc đưa sự trợ giúp trực tiếp ngay tại ngữ cảnh bài học (In-context) có thực sự giúp người học hiểu bản chất và làm lab nhanh hơn, hay họ vẫn giữ thói quen copy/paste sang ChatGPT bên ngoài?

---

## 3. FOUR SOLUTION OPTIONS TRONG PROTOTYPE
*(Hiện thực hóa hoàn chỉnh trong mã nguồn [`prototype/index.html`](file:///d:/New%20folder/LAB_D19/Track1_Day19_2A202602546_NguyenThiMinhKhanh/prototype/index.html))*

- **Option A (Chỉ vào chỗ kẹt - Inline Inspector & Contextual Help - Quân lead):**  
  Người học bấm nút *"Tôi vẫn chưa hiểu"* ➔ Màn hình hiện Pickbar ở dưới, các đoạn nội dung/code sáng viền vàng ➔ Chạm chọn đoạn chưa hiểu ➔ Chọn kiểu giúp (*"Giải thích dễ hơn"*, *"Cho ví dụ"*, *"Ôn kiến thức nền"*) hoặc tự gõ câu hỏi ➔ AI hiển thị thẻ `icard` giải thích ngay bên dưới đoạn đó kèm link trích dẫn nguồn bài giảng. *Agency: Don't Act (User-initiated).*
- **Option B (Chẩn đoán 3 câu - 3-Question Diagnostic Micro-Quiz - Việt Anh lead):**  
  Người học bấm nút *"Tôi vẫn chưa hiểu"* ➔ Side panel trượt ra với 3 câu trắc nghiệm 1 chạm (~1 phút) nhằm kiểm tra kiến thức nền ➔ AI đưa ra thẻ chẩn đoán `dcard` phân loại lỗ hổng tri thức, thang đo độ chắc chắn (*Cao / Trung bình / Thấp*), bài ôn có đồ thị SVG minh hoạ trực quan. Cho phép bấm *"Không đúng chỗ"* để tự chọn chủ đề ôn khác. *Agency: Ask (Co-creation).*
- **Option C (AI gợi ý chủ động - Proactive Nudge Card & Confidence Reasoning - Minh Khánh lead):**  
  Hệ thống tự động phát hiện dấu hiệu ngập ngừng (dừng >12 giây trên slide hoặc vừa trả lời sai câu hỏi kiểm tra) ➔ Tự động trượt thẻ `icard nudge` vào đúng khối nghi ngờ kẹt kèm chip tín hiệu hành vi thực tế, mục giải trình minh bạch *"Vì sao AI nghĩ vậy"* và thang đo độ tin cậy. Cho phép bấm *"Đúng chỗ, đã rõ hơn"*, *"Không phải chỗ này"* để chọn lại đoạn bí thật sự, hoặc *"Tắt tự nhắc trong buổi này"*. *Agency: Act (Proactive, User Reviews/Dismisses).*
- **Option D (Hỏi người thật kèm bối cảnh - Human Escalation & Auto Context Docket - Quang Huy lead):**  
  Khi AI chưa thỏa mãn: Người học bấm *"Tôi vẫn chưa hiểu"* ➔ Mở modal tự động thu thập bối cảnh học tập (slide/task đang mở, thời gian kẹt, lịch sử trả lời sai) ➔ Người học tick/untick bảo vệ quyền riêng tư, chọn người gửi (*TA Hà - Mentor lớp* hoặc *Tuấn - Nhóm Lab*) ➔ Gửi yêu cầu và theo dõi tiến trình trong side panel (*Đã gửi ➔ Đã xem ➔ Đang trả lời ➔ Đã trả lời* sau 15 giây mô phỏng). *Agency: Suggest (AI drafts context, User edits & sends).*
- **Link trải nghiệm Prototype:** Xem chi tiết tại [prototype-link.md](file:///d:/New%20folder/LAB_D19/Track1_Day19_2A202602546_NguyenThiMinhKhanh/prototype-link.md). Mở file trực tiếp: [`prototype/index.html`](file:///d:/New%20folder/LAB_D19/Track1_Day19_2A202602546_NguyenThiMinhKhanh/prototype/index.html).
- **Tài liệu phân tích chi tiết của nhóm:** Xem tại [three-option-design-sheet.md](file:///d:/New%20folder/LAB_D19/Track1_Day19_2A202602546_NguyenThiMinhKhanh/three-option-design-sheet.md).

---

## 4. ĐÓNG GÓP CỦA TÔI TRONG NHÓM (MY CONTRIBUTIONS)
- **Đóng góp Dữ liệu Khảo sát Thực tế (Chặng 1):**
  - Trực tiếp thực hiện và đóng góp **Practice Note 2** từ cuộc phỏng vấn học viên Lan (VLearn), phát hiện thời điểm vàng nhận biết lỗ hổng kiến thức là khi làm sai Checkpoint/Quiz và insight quyết định: *Nếu công cụ AI bắt chờ quá 3 phút, 100% người học sẽ chuyển tab sang ChatGPT ngoài*.
  - Cùng nhóm thảo luận, bóc tách Fact vs. Interpretation và đồng thuận chốt Hypothesis Problem, Comparison Contract cho 4 options.
- **Thiết kế & Triển khai Phương án Phụ trách (Lead Option C - Chặng 2, 3, 4):**
  - **Trực tiếp thiết kế và làm chủ Option C (AI gợi ý chủ động - Proactive Nudge Card & Confidence Reasoning)**: Xác định logic bộ đếm hành vi (idle >12s hoặc trả lời sai câu hỏi), thẻ `icard.nudge` trượt ra ghim trực tiếp vào vị trí kẹt, các chip dữ liệu thực tế (*"4 phút ở slide này", "Lật slide 2 lần", "6/10 học viên bí ở đây"*), mục mở rộng minh bạch *"Vì sao AI nghĩ vậy?"*, các nút phản hồi (*"Đúng chỗ", "Không phải chỗ này", "Tắt tự nhắc"*).
  - Phối hợp cùng 3 thành viên (Quân phụ trách Opt A, Việt Anh phụ trách Opt B, Quang Huy phụ trách Opt D) hiện thực hóa trọn vẹn 4 phương án vào web micro-prototype độc lập tại [`prototype/index.html`](file:///d:/New%20folder/LAB_D19/Track1_Day19_2A202602546_NguyenThiMinhKhanh/prototype/index.html) với 3 chủ đề kiến thức (*Context Window*, *ReAct Agent*, *Gradient Descent*), bộ đo logging tự động và nút Copy CSV.
- **Thử nghiệm & Thu thập dữ liệu Người dùng (Chặng 6):**
  - Trực tiếp điều phối và phỏng vấn độc lập với **Tester 3** (học viên ngoài nhóm) trải nghiệm qua 4 options; quan sát kỹ lưỡng phản ứng với Option C và các phương án so sánh, trích xuất log CSV khách quan vào [prototype-feedback-note.md](file:///d:/New%20folder/LAB_D19/Track1_Day19_2A202602546_NguyenThiMinhKhanh/prototype-feedback-note.md).
- **Tổng hợp & Phản biện Quyết định Nhóm (Chặng 7):**
  - Cùng nhóm tổng hợp ma trận 4 testers tại [group-feedback-synthesis.md](file:///d:/New%20folder/LAB_D19/Track1_Day19_2A202602546_NguyenThiMinhKhanh/group-feedback-synthesis.md) và chốt quyết định *Group Next Change*.

---

## 5. DỮ LIỆU KIỂM THỬ & BÀI HỌC (TESTING DATA & SYNTHESIS)

### 5.1. Tóm tắt phiên kiểm thử cá nhân (Tester 3 - Nguyễn Thị Minh Khánh điều phối)
- **Đối tượng:** Tester 3 (`N.T.T`) - Học viên ngành AI & Data Engineering (Khóa 3).
- **Thứ tự trải nghiệm:** **Option C ➔ Option A ➔ Option B ➔ Option D**.
- **Dữ kiện quan sát cốt lõi:**
  - *First Action:* Đang chăm chú đọc Slide 12 đến giây thứ 13 thì thẻ **Option C tự động trượt ra**. Tester giật mình dừng đọc khoảng 3s và chuyển ngay sự chú ý sang thẻ gợi ý.
  - *Phản hồi minh bạch:* Tester bấm ngay vào nút **`Vì sao AI nghĩ vậy?`** để kiểm tra căn cứ của AI; đánh giá cao độ tin cậy 85% và chip tín hiệu thực tế (*"6/10 học viên bí ở đây"*).
  - *Lấy lại quyền kiểm soát (Control):* Tester bấm *"Đúng chỗ, đã rõ hơn"*, sau đó thử nghiệm bấm *"Tắt tự nhắc trong buổi này"* và thấy nút bật lại nhỏ gọn ở góc dưới.
  - *Lựa chọn & Trade-off:* Tester chọn **Option C kết hợp Option A** vì thích sự chủ động xuất hiện đúng lúc kẹt, nhưng không muốn bị ngắt mạch khi đang tập trung suy nghĩ sâu.
- *Xem toàn bộ ghi chép và log CSV tại:* [prototype-feedback-note.md](file:///d:/New%20folder/LAB_D19/Track1_Day19_2A202602546_NguyenThiMinhKhanh/prototype-feedback-note.md).

### 5.2. Bảng tổng hợp chéo 4 phiên của cả nhóm (Cross-Tester Synthesis)
| Tiêu chí | Phiên 1 (T1 - Quân lead Opt A) | Phiên 2 (T2 - Việt Anh lead Opt B) | Phiên 3 (T3 - Minh Khánh lead Opt C) | Phiên 4 (T4 - Quang Huy lead Opt D) | Pattern chung & Insight cốt lõi |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **First Action** | Đọc bài 15s ➔ Bấm nút *"Tôi vẫn chưa hiểu"*. | Làm **Quiz** trước ➔ Làm sai mới tìm trợ giúp. | Đang đọc 13s thì thẻ **Opt C tự trượt ra**. | Cuộn xuống làm câu hỏi nhanh trước. | **50% làm Quiz trước, 50% đọc bài**. Thời điểm vàng kích hoạt là khi làm sai câu hỏi kiểm tra. |
| **Breakdown chính** | Do dự 10s khi chọn giữa các khối kẹt. | AI giải thích xong không cho chọn tiếp khối khác; tính nhẩm câu hỏi 2 lâu. | Bị phân tâm ngắt mạch khi AI nhảy ra quá sớm. | E ngại gửi thông tin bối cảnh nhạy cảm cho Mentor. | **Mọi bước đệm hay tự động hóa sai lúc đều gây ma sát**; cần giữ quyền chủ động cho người học. |
| **Recovery** | Bấm *"Làm lại"* / *"Đóng ×"*. | Bấm *"Không đúng chỗ"*. | Bấm *"Tắt tự nhắc"*. | Bỏ tick context chips. | **100% testers** tìm và sử dụng ngay các nút phục hồi kiểm soát (Human Agency). |
| **Option chọn** | **Option A** | **Option C** | **Option A** | **Option B** | Ưu tiên giải pháp **In-context, thao tác trực tiếp tại chỗ (<10s)** thay vì rời trang hay chờ đợi. |

### 5.3. Quyết định Next Change của cả nhóm (Group Next Change)
- **Quyết định chung:** Nhóm thống nhất chọn **Option A (Chạm chọn vùng kẹt - Inline Inspector)** làm khung tương tác cốt lõi, tích hợp cơ chế **Kích hoạt thông minh dựa trên Checkpoint (từ Opt C)**, **Rút gọn micro-diagnostic 1 câu (từ Opt B)**, và **Escalation sang Mentor khi kẹt sâu (Opt D)**:
  1. *Trigger chuẩn xác:* Không tự trượt thẻ ra ngắt dòng suy nghĩ sau 12s, chỉ hiện nút gợi ý hỗ trợ ngay cạnh câu hỏi khi người học **trả lời sai Quiz/Checkpoint**.
  2. *Thao tác 1 chạm liên tục:* Chạm sáng viền vàng để chọn thẳng đoạn kẹt và cho phép chạm liên tục nhiều đoạn nối tiếp.
  3. *Chẩn đoán 1 câu siêu ngắn:* AI hỏi 1 câu trắc nghiệm (~10s) để bóc tách lỗ hổng và xuất thẻ giải thích in-line có trích dẫn nguồn.
  4. *Escalation tự động sang người thật:* Nếu sau 2 lần giải thích in-line vẫn làm sai, tự động đề xuất mở Modal gửi Mentor (TA Hà).
- *Xem tài liệu chi tiết tại:* [group-feedback-synthesis.md](file:///d:/New%20folder/LAB_D19/Track1_Day19_2A202602546_NguyenThiMinhKhanh/group-feedback-synthesis.md).

### 5.4. Những ẩn số chưa được chứng minh (Still Unproven)
1. **Tính hiệu quả trên bài Lab code thực hành:** Chưa kiểm chứng khi người học gặp code Python/Shell nhiều dòng hoặc lỗi traceback runtime phức tạp.
2. **Độ duy trì kiến thức lâu dài (Knowledge Retention):** AI giải thích nhanh (<5s) giúp vượt qua quiz tức thì, nhưng chưa có dữ liệu đo lường mức độ ghi nhớ sau 1 tuần.
3. **Quy mô mẫu thử và tính đại diện:** Dữ liệu thử nghiệm từ 4 tester có người quan sát; hành vi khi tự học một mình sát deadline có thể biến thiên lớn.

---

## 6. AI SUPPORT LOG SUMMARY
- **Cam kết liêm chính học thuật:** 100% dữ liệu khảo sát người dùng (Note 2 - Lan) và biên bản thử nghiệm người dùng (Tester 3) đều được thu thập từ con người thật ngoài nhóm.
- **Tóm tắt phạm vi ứng dụng AI & Sàng lọc cá nhân:**
  | Hạng mục ứng dụng | AI đã hỗ trợ khâu nào? | Sự can thiệp / Sửa sai thực tế của tôi |
  | :--- | :--- | :--- |
  | **Gợi ý cơ chế tương tác (Opt C)** | Đề xuất mô hình nhận diện idle time và thẻ giải trình minh bạch. | Rút gọn giải trình, thêm chip số liệu thực tế (*"4 phút ở slide này", "6/10 học viên bí ở đây"*), thiết kế nút tắt 1 chạm. |
  | **Sinh dữ liệu mẫu (Fixtures)** | Sinh câu hỏi trắc nghiệm và nội dung giải thích cho 3 chủ đề kỹ thuật (*Context Window, ReAct, Gradient Descent*). | Tự tay kiểm tra tính chính xác của công thức toán học và căn chỉnh sát với slide bài giảng VLearn. |
  | **Xây dựng Prototype** | Hỗ trợ cấu trúc HTML5/CSS/JS thuần, bộ đếm thời gian và trích xuất log CSV. | Tinh chỉnh giao diện tiếng Việt, màu sắc viền vàng/đỏ, tối ưu trải nghiệm chạm trên desktop/tablet. |
  | **Rà soát kịch bản kiểm thử** | Phát hiện câu hỏi định hướng (*"Bạn có thấy tự nhắc tiện lợi không?"*). | Viết lại thành câu hỏi mở trung tính: *"Khi thẻ này xuất hiện, bạn cảm thấy thế nào và suy nghĩ đầu tiên là gì?"*. |
- *Xem chi tiết nhật ký tại:* [ai-support-log.md](file:///d:/New%20folder/LAB_D19/Track1_Day19_2A202602546_NguyenThiMinhKhanh/ai-support-log.md).
