# PROTOTYPE FEEDBACK NOTE (CÁ NHÂN)

> **Người thực hiện facilitate & ghi chép:** Nguyễn Thị Minh Khánh (2A202602546)  
> **Phương án phụ trách chính:** Option C (AI gợi ý chủ động - Proactive Nudge Card & Confidence Reasoning)  
> **Quy định**: Phiên này do chính bạn trực tiếp điều phối độc lập với 1 tester ngoài nhóm. Tester được trải nghiệm ĐỦ CẢ 4 OPTIONS (A, B, C, D) trên cùng một chủ đề bài học và cùng một Outcome Task.

---

## 1. THÔNG TIN PHIÊN TEST
- **Tester (Tên viết tắt / Mã):** Tester 3 - `N.T.T` *(Học viên ngành AI & Data Engineering, Khóa 3)*
- **Bối cảnh thực tế (Relevant Context):** Tester từng nhiều lần bối rối khi đọc tài liệu về Token và Context Window, đặc biệt khi làm việc với API LLM. Khi không hiểu thường ngồi đọc lại 2–3 lần, nếu vẫn kẹt mới copy sang ChatGPT nhưng thường nhận câu trả lời dài dòng, mất thời gian.
- **Chủ đề test:** Context Window (Slide 12 · Lý thuyết) - URL: `prototype/index.html#context/theory/C`
- **Thời gian thực hiện:** 05/10/2026 · 10:15 - 10:45 · Trực tiếp tại phòng Lab
- **Thứ tự trải nghiệm các options:** **C ➔ A ➔ B ➔ D** *(Ưu tiên thử phương án chủ động Option C trước)*

---

## 2. BẢNG GHI NHẬN HÀNH VI (OBSERVATION LOG)

| Tiêu điểm quan sát | Ghi nhận chi tiết trong lúc test |
| :--- | :--- |
| **First Action** *(Hành động đầu tiên họ làm khi thấy màn hình)* | Đọc lướt tiêu đề Slide 12 và công thức. Đang đọc đến dòng thứ 2 (khoảng giây thứ 13), thẻ gợi ý **Option C** tự động trượt ra ghim vào khối công thức `context window`. Tester dừng lại nhìn thẻ khoảng 3 giây với vẻ bất ngờ nhưng chăm chú đọc ngay. |
| **Chỗ dừng, do dự hoặc hiểu sai** *(Điểm khựng lại, bấm nhầm, ngập ngừng)* | Tester nhìn thấy chip *"6/10 học viên bí ở đây"* và *"4 phút ở slide này"*, liền bấm ngay vào nút **`Vì sao AI nghĩ vậy?`** để xem lý do AI xuất hiện. Tester gật đầu khi thấy AI giải trình rõ ràng. Khi chuyển sang Option B, tester hơi ngập ngừng ở câu hỏi số 2 của Quiz chẩn đoán vì phải tính nhẩm token. |
| **Evidence & Uncertainty** *(Họ có đọc giải thích/căn cứ, trích dẫn nguồn, thước đo độ chắc chắn không?)* | Rất quan tâm đến phần **Độ tin cậy (85%)** và lý do suy luận của Option C. Ở Option A, tester đọc kỹ phần trích dẫn nguồn Slide 12. Ở Option B, tester chú ý đến đồ thị minh họa SVG. |
| **Cách tester sửa sai hoặc lấy lại control** *(Nút Làm lại, Đóng ×, Bỏ qua, Tắt tự nhắc, Không đúng chỗ họ dùng thế nào?)* | Sau khi đọc xong thẻ gợi ý Option C, tester bấm nút **`Đúng chỗ, đã rõ hơn`** để xác nhận. Sau đó tester chủ động thử bấm nút **`Tắt tự nhắc trong buổi này`** để xem hệ thống phản ứng ra sao, và nhận thấy nút bật lại xuất hiện nhỏ gọn ở góc dưới. |
| **Option được chọn cuối cùng** | **Option C kết hợp Option A** *(Tester đánh giá cao nhất Option C vì không cần phải tự nghĩ xem mình bí ở đâu, nhưng muốn có thêm tính năng chạm của Option A khi cần)* |
| **Lý do lựa chọn & Trade-off** *(Họ thích điểm gì và chấp nhận đánh đổi điều gì?)* | **Thích**: Không mất công bấm nút tìm kiếm, AI xuất hiện đúng lúc đang ngập ngừng và giải thích ngắn gọn, trúng trọng tâm. **Chấp nhận đánh đổi**: Đôi khi AI có thể nhảy ra sớm 2-3 giây khi người học chỉ đang suy nghĩ chậm chứ chưa hẳn là bị kẹt. |
| **Evidence đi ngược lại kỳ vọng của nhóm** *(Điểm gì tester làm khiến nhóm bất ngờ?)* | Nhóm từng lo ngại việc AI tự động trượt ra (Proactive) sẽ gây khó chịu (intrusive), nhưng tester lại phản hồi: *"Nếu có giải thích rõ 'Vì sao AI nghĩ vậy' và nút tắt nhanh 1 chạm thì không hề khó chịu, trái lại cảm thấy AI rất thông minh và tinh tế"*. |

---

## 3. PHÂN TÍCH 4 LỚP DỮ LIỆU (FOUR-LAYER ANALYSIS)

### 1. OBSERVED (Dữ liệu quan sát khách quan)
*Dữ liệu nhật ký CSV trích xuất từ nút `Facilitator log` ➔ `Copy dạng CSV` của prototype:*
```csv
time,option,t_sec,event,detail
10:15:02,C,0,start,topic:context,mode:theory
10:15:15,C,13,c-nudge,auto_trigger:idle_12s,target:formula_block
10:15:19,C,17,c-expand,why_ai_reasoning:viewed
10:15:32,C,30,c-feedback,action:correct_spot_understood
10:15:45,C,43,quick-question,selected:cut_short,result:correct
10:16:10,A,0,switch_option,opt:A
10:16:18,A,8,open-help,user_clicked
10:16:22,A,12,a-select,target:context_formula
10:16:26,A,16,a-send,mode:explain_easier
10:16:38,A,28,quick-question,result:correct
10:17:00,B,0,switch_option,opt:B
10:17:08,B,8,open-help,user_clicked
10:17:15,B,15,b-answer,q1:token_def,correct
10:17:28,B,28,b-answer,q2:budget_calc,correct
10:17:39,B,39,b-answer,q3:memory_drop,correct
10:17:42,B,42,b-diag,result:overload_risk,confidence:high
10:18:15,D,0,switch_option,opt:D
10:18:22,D,7,open-help,user_clicked
10:18:29,D,14,d-privacy,toggle_item:quiz_history_unchecked
10:18:34,D,19,d-send,recipient:TA_Ha
```

*Ghi lại chính xác những gì tester đã nói (nguyên văn quotes) và thao tác thực tế:*
- *"Ủa hay thế, mình vừa lướt đến chỗ công thức chưa kịp nghĩ thì nó đã hiện gợi ý đúng đoạn này luôn rồi."*
- *"Cái dòng 'Vì sao AI nghĩ vậy' này làm mình thấy tin tưởng hơn, biết là nó dựa vào thời gian dừng chứ không phải đoán mò lung tung."*
- *"Option B hỏi 3 câu cũng hay nhưng đang vội làm bài mà phải trả lời thêm 3 câu nữa thì hơi mất kiên nhẫn một chút."*

### 2. INTERPRETED (Diễn giải ý nghĩa)
- Người học có xu hướng **thụ động khi gặp khó khăn** (thường đọc đi đọc lại trong im lặng thay vì chủ động bấm nút trợ giúp). Vì vậy, cơ chế **Proactive Nudge (Option C)** kích hoạt đúng lúc là điểm chạm cực kỳ đắt giá giúp kéo người học ra khỏi trạng thái bế tắc.
- Tính **minh bạch (Transparency)** qua giải trình *"Vì sao AI nghĩ vậy"* và thang đo độ tin cậy giúp xóa bỏ hoàn toàn cảm giác bị "theo dõi ngầm" hoặc "bị làm phiền", biến tính năng tự động thành một trợ lý tận tâm.

### 3. DECIDED — NEXT CHANGE (Đề xuất thay đổi)
- **Giữ lại Option C làm cơ chế thông minh nền tảng**, nhưng cần tinh chỉnh ngưỡng thời gian kích hoạt tự động linh hoạt hơn (tăng từ 12s lên khoảng 18–20s đối với đoạn code dài để tránh can thiệp quá sớm khi người học đang tập trung đọc).
- **Tích hợp tính năng chạm chọn của Option A vào Option C**: Khi người học bấm nút *"Không phải chỗ này"*, lập tức kích hoạt thanh Pickbar của Option A để người học chạm trực tiếp vào đoạn họ thực sự đang muốn hỏi.

### 4. STILL UNPROVEN (Điều vẫn chưa thể khẳng định)
- Chưa thể khẳng định ngưỡng kích hoạt 12–18s có phù hợp với tất cả các dạng bài học hay không (ví dụ bài Lab code phức tạp so với slide lý thuyết ngắn).
- Chưa kiểm chứng được phản ứng lâu dài của người học sau 2–3 tuần sử dụng: Liệu họ có hình thành phản xạ ỷ lại vào AI gợi ý mà giảm bớt nỗ lực tự đọc hiểu ban đầu hay không?
