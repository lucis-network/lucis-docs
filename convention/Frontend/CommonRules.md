# Lucis Frontend convention  
*Các quy ước phát triển frontend, sẽ được update dần trong tương lai.*  
1. Bắt buộc phải có blank state khi không có dữ liệu.
2. Khoảng cách giữa các block khi hiển thị trên giao diện không được gần quá hoặc xa quá.
3. Bắt buộc xử lý message lỗi trả về từ backend cho tất cả các trường hợp lỗi, message cần rõ nghĩa, giải thích về lỗi cho user hiểu, đưa ra gợi ý khắc phục lỗi,...
4. Bắt buộc phải có trạng thái loading cho các action mất thời gian chờ như tương tác với api.
5. KHÔNG ĐƯỢC XÓA những file .lock do yarn, npm,... tạo ra.
6. Khi làm việc với typescript, không lạm dụng any, unknown, luôn định nghĩa kiểu giá trị cho tất cả các biến, tham số, giá trị trả về của function,...
7. Không được reformat toàn bộ file code, chỉ reformat những dòng nào mình làm.
8. Luôn xử lý trường hợp lỗi file ảnh (ảnh không tồn tại phía server, response lỗi 400, 403,...) sẽ dùng ảnh placeholder mặc định bằng onError
9. Đối với html, javascript, typescript, css, sass phải config IDE/editor tab size 2 spaces, không được dùng 4 spaces hoặc 4 tabs.