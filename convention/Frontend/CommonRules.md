# Lucis Frontend convention  
*Các quy ước phát triển frontend, sẽ được update dần trong tương lai.*  
1. Bắt buộc phải có blank state khi không có dữ liệu.
2. Khoảng cách giữa các block khi hiển thị trên giao diện không được gần quá hoặc xa quá.
3. Bắt buộc xử lý message lỗi trả về từ backend cho tất cả các trường hợp lỗi, message cần rõ nghĩa, giải thích về .
4. Bắt buộc phải có trạng thái loading cho các action mất thời gian chờ như tương tác với api.
5. KHÔNG ĐƯỢC XÓA những file .lock do yarn, npm,... tạo ra.
6. Khi làm việc với typescript, luôn định nghĩa kiểu giá trị cho tất cả các biến, tham số, giá trị trả về của function,...