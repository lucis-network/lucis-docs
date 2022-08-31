# Lucis BE convention

1. Release flow

- Cần viết checklist những việc cần làm khi release như Env, đăng ký key bên thứ 3, cài đặt proxy với url đặc biệt trong app
- Cần cập nhật checklist và các file liên quan ngay khi code để tránh quên
- Định dạng file:

```
{not_release|date}:
    * Features:
        [commit_id|issue]{description}
    * Fixes:
        [commit_id|issue]{description}
    * Step release:
        - Add to env
```

> Những release mới sẽ để lên đầu, nếu chưa release thì để not_release (thêm những note release mới vào đây, không tạo mới header), khi release rồi thì nhập ngày tháng release vào

2. Toàn vẹn dữ liệu

- Khi code phải check toàn vẹn dữ liệu, không phụ thuộc vào foreign key trong db
  > VD:

3. Checklist

- Chỉ ghi vào release_log khi thêm biến env
- Thay đổi database (migrations, sql tự viết) tổng hợp vào một file sql theo đúng thứ tự trước khi merge feature vào nhánh dev

4. Coding

- Khi dùng ORM luôn luôn phải để ORM generate ra SQL/query đúng ý dev, cần bật query logger để check
