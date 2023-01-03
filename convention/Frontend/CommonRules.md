# Lucis Frontend convention  
*Các quy ước phát triển frontend, sẽ được update dần trong tương lai.*  
1. Bắt buộc phải có blank state khi không có dữ liệu, mục tiêu để người dùng không bị bối rối và đứt flow:

   BlankState nên:
   - Để user hiểu tại sao lại không có data ở đây
   - Gợi ý làm sao để có data ở đây
   
   Ví dụ:
   - Khi không dự án nào đang đầu tư trong list: Thêm text báo "Chưa có dự án nào đang đầu tư" + thêm nút "Các dự án có thể đầu tư" để đưa ng dùng tới chỗ mua, ...

3. Khoảng cách giữa các block khi hiển thị trên giao diện không được gần quá hoặc xa quá.
4. Bắt buộc xử lý message lỗi trả về từ backend cho tất cả các trường hợp lỗi, message cần rõ nghĩa, giải thích về lỗi cho user hiểu, đưa ra gợi ý khắc phục lỗi,...
5. Bắt buộc phải có trạng thái loading cho các action mất thời gian chờ như tương tác với api.
6. KHÔNG ĐƯỢC XÓA những file .lock do yarn, npm,... tạo ra.
7. Khi làm việc với typescript, không lạm dụng any, unknown, luôn định nghĩa kiểu giá trị cho tất cả các biến, tham số, giá trị trả về của function,...
8. Không được reformat toàn bộ file code, chỉ reformat những dòng nào mình làm.
9. Refactor format code phải dùng commit riêng, không được commit chung với logic
10. Luôn xử lý trường hợp lỗi file ảnh (ảnh không tồn tại phía server, response lỗi 400, 403,...) sẽ dùng ảnh placeholder mặc định bằng onError
11. Đối với html, javascript, typescript, css, sass phải config IDE/editor tab size 2 spaces, không được dùng 4 spaces hoặc 4 tabs.
