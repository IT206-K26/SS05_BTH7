# BÀI THỰC HÀNH 7

---

## 1. BỘ 4 PROMPT HOÀN CHỈNH THEO CẤU TRÚC CREATE

### PROMPT 1: Phân tích tính khả thi & Rủi ro (Chain-of-Thought)
- **C – Character:** Bạn là Chuyên gia Quản trị Sự kiện Công nghệ dành cho sinh viên đại học.
- **R – Request:** Phân tích tính khả thi cho sự kiện **AI Innovation Day** với các thông số cố định: Quy mô **150 sinh viên**, thời gian **1 ngày**, ngân sách tối đa **15.000.000 VNĐ**, nhân sự tổ chức **10 người**, mục tiêu giúp sinh viên **hiểu và trải nghiệm ứng dụng AI trong học tập và công việc**. Thực hiện suy luận **Chain-of-Thought** qua 4 bước: (1) Đánh giá Ngân sách/Quy mô, (2) Đánh giá Nhân sự/Quy mô, (3) Đánh giá Mục tiêu trong 1 ngày, (4) Nêu 3 rủi ro lớn nhất và kết luận.
- **E – Examples:** Ví dụ Bước 1: *"15.000.000 VNĐ / 150 SV = 100.000 VNĐ/người → Khả thi nếu mượn được hội trường trường miễn phí."*
- **A – Adjustments:** Giữ nguyên tuyệt đối 4 thông số cứng (150 SV, 1 ngày, ≤ 15 triệu, 10 nhân sự); không đề xuất xin tài trợ ngoài để vượt mức ngân sách bài toán.
- **T – Type of output:** Báo cáo phân tích chia theo 4 bước đánh số rõ ràng, kết thúc bằng 1 câu kết luận mức độ khả thi.
- **E – Extras:** Kết quả bước này sẽ làm đầu vào cho bước lập kế hoạch chi tiết tiếp theo (Prompt Chaining).

### PROMPT 2: Lập Lịch trình, Dự toán ngân sách & Phân công 10 nhân sự (Prompt Chaining – Bước 2)
- **C – Character:** Bạn là Trưởng Ban Tổ chức sự kiện công nghệ giàu kinh nghiệm thực chiến.
- **R – Request:** Dựa trên `[Kết quả Bước 1]`, hãy xây dựng 3 hạng mục cốt lõi:
  1. Lịch trình chi tiết 1 ngày theo khung giờ (đủ 2 phần: hiểu kiến thức và trải nghiệm thực hành AI).
  2. Bảng dự toán ngân sách chi tiết (cộng tổng chính xác ≤ 15.000.000 VNĐ, có quỹ dự phòng).
  3. Bảng phân công nhiệm vụ cụ thể cho đúng **10 nhân sự** (trước sự kiện và trong ngày sự kiện).
- **E – Examples:** Bảng ngân sách gồm cột: `STT | Hạng mục | Diễn giải chi tiết | Thành tiền (VNĐ) | Tỷ trọng (%)`.
- **A – Adjustments:** Tổng ngân sách không được vượt 15.000.000 VNĐ dù chỉ 1 đồng; phân công đủ từ Nhân sự 1 đến Nhân sự 10; không đưa cơm trưa vào ngân sách nếu làm vỡ quỹ.
- **T – Type of output:** 3 bảng Markdown độc lập, dễ theo dõi và đối chiếu.
- **E – Extras:** Đảm bảo các đầu mục nhân sự trong Lịch trình khớp với tên vị trí trong Bảng phân công.

### PROMPT 3: Kế hoạch truyền thông & Tóm tắt ngữ cảnh
- **C – Character:** Bạn là Trưởng ban Truyền thông kiêm Quản lý Dự án (PMO).
- **R – Request:** Dựa trên `[Kết quả Bước 2]`, hãy thực hiện 2 nhiệm vụ:
  1. Xây dựng kế hoạch truyền thông trước sự kiện trong **14 ngày** để thu hút đủ 150 sinh viên tham dự (sử dụng đúng khoản ngân sách truyền thông đã duyệt ở Bước 2).
  2. Viết **Bản tóm tắt ngữ cảnh dự án (Project Context Summary)** để truyền sang một hội thoại AI mới thực hiện kiểm tra độc lập.
- **E – Examples:** Bản tóm tắt ngữ cảnh gồm: Thông số cố định, Mục tiêu, Các quyết định đã chốt, Yêu cầu cho phiên làm việc tiếp theo.
- **A – Adjustments:** Ngân sách truyền thông trong kế hoạch 14 ngày phải khớp 100% với Bảng dự toán ở Bước 2; bản tóm tắt ngữ cảnh ngắn gọn dưới 200 từ nhưng không bỏ sót thông số quan trọng nào.
- **T – Type of output:** 1 Bảng kế hoạch truyền thông 4 giai đoạn + 1 khung trích dẫn (Blockquote) chứa Bản tóm tắt ngữ cảnh dự án.
- **E – Extras:** Đặt mục tiêu đăng ký dự phòng (180–200 đơn) để bù tỷ lệ vắng mặt (no-show).

### PROMPT 4: Kiểm tra tính thống nhất & Hiệu chỉnh kế hoạch 
- **C – Character:** Bạn là Kiểm toán viên Dự án (Project Auditor) độc lập.
- **R – Request:** Dựa trên `[Bản tóm tắt ngữ cảnh dự án + các bảng kế hoạch từ Bước 2 & 3]`, kiểm tra chéo toàn bộ kế hoạch theo **Chain-of-Thought**: (1) Kiểm tra ràng buộc cứng, (2) Kiểm tra tính liên kết giữa các bảng, (3) Chỉ ra ít nhất 3 lỗ hổng/rủi ro vận hành thực tế và đề xuất phương án hiệu chỉnh cụ thể.
- **E – Examples:** `Vấn đề: Quá tải check-in đầu giờ | Mức độ: Cao | Hiệu chỉnh: Huy động 4 nhân sự chia 2 line quét QR.`
- **A – Adjustments:** Các phương án hiệu chỉnh không được làm tăng tổng ngân sách vượt 15.000.000 VNĐ và không được tăng thêm nhân sự quá 10 người.
- **T – Type of output:** Nhận xét kiểm tra ràng buộc + Bảng tổng hợp 3 vấn đề phát hiện và phương án hiệu chỉnh.
- **E – Extras:** Tập trung vào các điểm nghẽn thực tế thường xảy ra tại sự kiện sinh viên (check-in, nước uống, hỗ trợ kỹ thuật buổi chiều).

---

## 2. KẾT QUẢ

### A. Bản phân tích tính khả thi (Kết quả Bước 1 – CoT)
- **Bước 1 – Ngân sách & Quy mô:** 15.000.000 VNĐ cho 150 sinh viên tương đương **100.000 VNĐ/người**. Mức này **khả thi** nếu tận dụng hội trường miễn phí của trường đại học và mời diễn giả cựu sinh viên/chuyên gia hỗ trợ cộng đồng (chi phí ở mức quà cảm ơn).
- **Bước 2 – Nhân sự & Quy mô:** Tỷ lệ **10 nhân sự / 150 sinh viên (1:15)** là hợp lý, nhưng sẽ quá tải vào giờ cao điểm (Check-in, Teabreak, Workshop). Cần phân công kiêm nhiệm linh hoạt theo khung giờ.
- **Bước 3 – Mục tiêu trong 1 ngày:** Chia 2 buổi rất tối ưu: **Buổi sáng** tập trung *Hiểu* (Keynote + Panel Talk), **Buổi chiều** tập trung *Trải nghiệm* (Workshop thực hành AI + Mini-Challenge).
- **Bước 4 – 3 Rủi ro lớn nhất & Kết luận:**
  1. *Hạ tầng Wi-Fi & ổ cắm điện* quá tải khi 150 sinh viên thực hành AI cùng lúc.
  2. *Vỡ quỹ ăn uống* nếu bao cơm trưa → Giải pháp: Chỉ phục vụ Teabreak/nước uống, sinh viên tự túc ăn trưa.
  3. *Tỷ lệ vắng mặt (No-show)* → Giải pháp: Nhận 180–200 đơn đăng ký dự phòng.
  - **Kết luận:** Sự kiện **KHẢ THI** nếu kiểm soát chặt chi phí địa điểm, ăn uống và điều phối nhân sự theo khung giờ.

### B. Lịch trình sự kiện theo khung giờ (1 ngày)

| Khung giờ | Nội dung hoạt động | Mục tiêu đáp ứng | Nhân sự phụ trách chính |
| :--- | :--- | :--- | :--- |
| **07:30 – 08:30** | Đón khách, Check-in QR, phát tài liệu & ổn định chỗ ngồi | Quản lý quy mô 150 SV | Ban Hậu cần & Truyền thông |
| **08:30 – 08:45** | Khai mạc, giới thiệu CLB & mục tiêu AI Innovation Day | Dẫn nhập chương trình | Trưởng BTC & MC (Nội dung) |
| **08:45 – 10:00** | **Keynote 1:** *"Tư duy sử dụng AI hiệu quả trong học tập đại học"* | Giúp SV **hiểu** về AI | Ban Nội dung & Kỹ thuật |
| **10:00 – 10:20** | **Teabreak** & Giao lưu kết nối | Giữ năng lượng | Ban Hậu cần |
| **10:20 – 11:30** | **Panel Talk:** *"Ứng dụng AI trong công việc thực tế & Tuyển dụng"* + Q&A | Giúp SV **hiểu** ứng dụng thực tế | Ban Nội dung & Kỹ thuật |
| **11:30 – 13:30** | Nghỉ trưa tự túc (BTC kiểm tra lại thiết bị, ổ cắm cho buổi chiều) | Chuẩn bị hạ tầng thực hành | Toàn bộ BTC (luân phiên) |
| **13:30 – 15:00** | **Workshop thực hành:** *"Trải nghiệm bộ công cụ AI cho học tập & làm việc"* | Giúp SV **trải nghiệm** trực tiếp | Ban Nội dung & Kỹ thuật |
| **15:00 – 16:00** | **AI Mini-Challenge:** Thi giải bài toán nhanh bằng AI theo nhóm | Củng cố kỹ năng thực hành | Ban Nội dung & Hậu cần |
| **16:00 – 16:45** | Chấm điểm, trao giải Mini-Challenge, khảo sát & Bế mạc | Tổng kết & đo lường hiệu quả | Toàn bộ BTC |

### C. Bảng dự toán ngân sách (Tối đa 15.000.000 VNĐ)

| STT | Hạng mục chi phí | Diễn giải chi tiết | Thành tiền (VNĐ) | Tỷ trọng |
| :---: | :--- | :--- | :---: | :---: |
| 1 | **Địa điểm & Thiết bị hỗ trợ** | Mượn hội trường trường (0đ); thuê thêm micro, dây nối, bộ phát Wi-Fi phụ | 1.500.000 | 10,0% |
| 2 | **Quà tặng & Cảm ơn Diễn giả** | 3 diễn giả/khách mời × 1.000.000 VNĐ | 3.000.000 | 20,0% |
| 3 | **Teabreak & Nước uống** | 160 suất (150 SV + 10 BTC) × 25.000 VNĐ | 4.000.000 | 26,7% |
| 4 | **In ấn & Trang trí** | Backdrop sân khấu, 2 standee, 10 thẻ BTC, phiếu/bảng tên | 2.000.000 | 13,3% |
| 5 | **Giải thưởng AI Mini-Challenge** | 1 Giải Nhất (700k), 1 Giải Nhì (500k), 1 Giải Ba (300k) | 1.500.000 | 10,0% |
| 6 | **Truyền thông trước sự kiện** | Chạy quảng cáo bài viết Facebook/TikTok tiếp cận SV trong trường | 1.000.000 | 6,7% |
| 7 | **Hậu cần & Văn phòng phẩm** | Bút, giấy note, ổ cắm điện chia nhánh cho khu vực thực hành | 500.000 | 3,3% |
| 8 | **Quỹ dự phòng phát sinh** | Dự phòng 10% cho sự cố kỹ thuật hoặc phát sinh nhỏ | 1.500.000 | 10,0% |
| | **TỔNG CỘNG** | **Đảm bảo không vượt mức 15.000.000 VNĐ** | **15.000.000** | **100%** |

### D. Bảng phân công nhiệm vụ cho 10 nhân sự

| STT | Vị trí / Vai trò | Nhiệm vụ trước sự kiện | Nhiệm vụ trong ngày sự kiện |
| :---: | :--- | :--- | :--- |
| 1 | **Trưởng BTC** | Quản lý tiến độ chung, xin phép hội trường, duyệt ngân sách. | Điều phối tổng thể, xử lý sự cố phát sinh, phát biểu khai mạc. |
| 2 | **Phó BTC & Thủ quỹ** | Quản lý thu chi 15 triệu, chốt báo giá in ấn & Teabreak. | Thanh toán đối tác, giữ quỹ dự phòng, giám sát bàn Check-in. |
| 3 | **Trưởng ban Nội dung** | Xây dựng kịch bản chương trình, chốt slide với 3 diễn giả. | Dẫn chương trình (MC), kiểm soát timeline sân khấu. |
| 4 | **Thành viên Nội dung** | Thiết kế đề bài Mini-Challenge và tài liệu hướng dẫn thực hành. | Điều phối Q&A, hỗ trợ Workshop, chấm điểm & trao giải. |
| 5 | **Trưởng ban Truyền thông** | Lập kế hoạch truyền thông 14 ngày, quản lý 1 triệu chạy ads. | Điều phối chụp ảnh, quay video tư liệu trong hội trường. |
| 6 | **Thành viên Truyền thông** | Thiết kế Backdrop, Standee, Banner online, Thẻ BTC. | Hỗ trợ Check-in đầu giờ, cập nhật tin ảnh lên Fanpage. |
| 7 | **Trưởng ban Kỹ thuật** | Kiểm tra âm thanh, máy chiếu, test Wi-Fi hội trường. | Trực bàn kỹ thuật (âm thanh, slide) xuyên suốt chương trình. |
| 8 | **Thành viên Kỹ thuật** | Chuẩn bị ổ cắm điện, bộ phát Wi-Fi phụ, tài khoản AI mẫu. | Hỗ trợ kỹ thuật trực tiếp cho SV trong phiên Workshop. |
| 9 | **Trưởng ban Hậu cần** | Đặt Teabreak, nước uống, nhận hàng in ấn & quà diễn giả. | Điều phối Check-in, phân phát Teabreak, đón tiếp diễn giả. |
| 10 | **Thành viên Hậu cần** | Mua văn phòng phẩm, sắp xếp 150 chỗ ngồi hội trường. | Hỗ trợ Check-in, hỗ trợ Workshop, dọn dẹp sau sự kiện. |

### E. Kế hoạch truyền thông trước sự kiện (14 ngày – Ngân sách 1.000.000 VNĐ)

| Giai đoạn | Thời gian | Nội dung triển khai | Ngân sách |
| :--- | :--- | :--- | :---: |
| **1. Khởi động (Teasing)** | Ngày 1 – 4 | Đăng bài hé lộ chủ đề *"AI Innovation Day"* & khảo sát ngắn nỗi lo của SV khi dùng AI. | 0 VNĐ |
| **2. Mở đăng ký (Launching)** | Ngày 5 – 9 | Công bố lịch trình, 3 diễn giả & giải thưởng 1,5 triệu; mở Form đăng ký; đặt Standee tại trường. | 600.000 VNĐ |
| **3. Đẩy mạnh (Boosting)** | Ngày 10 – 12 | Chia sẻ lợi ích phiên Workshop thực hành; nhờ các lớp/CLB bạn bè chia sẻ chéo. | 400.000 VNĐ |
| **4. Đóng đơn & Nhắc lịch** | Ngày 13 – 14 | Đóng form khi đủ 180–200 đơn; gửi Email xác nhận kèm hướng dẫn mang laptop & tạo sẵn tài khoản AI. | 0 VNĐ |

### F. Bản tóm tắt ngữ cảnh dự án

> **[PROJECT CONTEXT SUMMARY – AI INNOVATION DAY]**
> - **Thông số cố định:** Sự kiện 1 ngày | Quy mô 150 sinh viên | Ngân sách tối đa 15.000.000 VNĐ | Nhân sự 10 người.
> - **Mục tiêu:** Giúp sinh viên hiểu (buổi sáng: Keynote + Panel Talk) và trải nghiệm thực tế (buổi chiều: Workshop + Mini-Challenge) ứng dụng AI.
> - **Quyết định đã chốt:** Tận dụng hội trường trường miễn phí; không bao cơm trưa (chỉ Teabreak 4.000.000 VNĐ); tổng dự toán đúng 15.000.000 VNĐ (gồm 1.500.000 VNĐ dự phòng và 1.000.000 VNĐ truyền thông); 10 nhân sự chia 5 mảng (Điều hành, Nội dung, Truyền thông, Kỹ thuật, Hậu cần – mỗi mảng 2 người); truyền thông 14 ngày mục tiêu 180–200 đơn đăng ký.
> - **Yêu cầu cho hội thoại mới:** Kiểm tra chéo tính nhất quán, phát hiện lỗ hổng vận hành và đề xuất hiệu chỉnh không vượt ngân sách/nhân sự.

### G. Báo cáo kiểm tra và hiệu chỉnh kế hoạch
- **Kiểm tra ràng buộc & liên kết:** Tổng ngân sách = 15.000.000 VNĐ (Đạt); ngân sách truyền thông khớp 100% (1.000.000 VNĐ = 600k + 400k); đủ 10 nhân sự và đúng quy mô 150 sinh viên.

| STT | Vấn đề / Lỗ hổng phát hiện | Mức độ | Phương án hiệu chỉnh cụ thể |
| :---: | :--- | :---: | :--- |
| 1 | **Quá tải bàn Check-in (07:30 – 08:30):** 150 SV đến dồn trong 60 phút, nếu check-in thủ công dễ gây ùn tắc và trễ giờ khai mạc. | **Cao** | Huy động **4 nhân sự** (Nhân sự 2, 6, 9, 10) chia làm 2 line check-in bằng mã QR (tạo sẵn qua Google Form/Sheets) để xử lý dưới 15 giây/người. |
| 2 | **Thiếu nước uống buổi chiều:** Ngân sách mới tính Teabreak 1 lần buổi sáng (25.000đ/suất), trong khi buổi chiều kéo dài hơn 3 tiếng. | **Trung bình** | Tách 25.000đ/suất thành **18.000đ** (bánh + trà buổi sáng) và **7.000đ** (1 chai nước suối/người cho buổi chiều), giữ nguyên tổng 4.000.000 VNĐ. |
| 3 | **Thiếu người hỗ trợ kỹ thuật buổi chiều:** 150 SV thực hành AI cùng lúc nhưng chỉ có 1 nhân sự kỹ thuật (Nhân sự 8) đi hỗ trợ là không đủ. | **Cao** | Khung 13:30 – 15:00 điều động thêm **Nhân sự 4 (Nội dung)** và **Nhân sự 10 (Hậu cần)** cùng hỗ trợ thao tác cơ bản; gửi trước hướng dẫn tạo tài khoản AI qua email ở Ngày 13–14. |
