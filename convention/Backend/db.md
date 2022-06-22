# Lucis db convention

Các quy ước trong phát triển db nhằm mục đích nhất quán, dễ hiểu trong quá trình làm việc

1. Tên table:

- nên là số ít.

  > Exp: user, not [users] nhằm thống nhất với tên trong foreign_key và không phải suy nghĩ về trường hợp số nhiều trong tên

- đặt prefix cho các table liên quan
  > Exp: user, user_profile
- Các table dùng tạm để tính toán thêm suffix: "\_tmp"
- Các table dùng tạm sau sẽ xóa thêm prefix: "tmp\_"

2. Tên trường

- phải đầy đủ, rõ ràng,
  > Exp: Exp: middle_name, not mid_name
- dùng snake_case, không dùng quotes
  > Exp: Exp: middle_name, not "Middle_name"
- có tính tự giải thích
- không dùng kiểu dữ liệu
- không dùng từ khóa của sql
- không quá dài (64 ký tự)
- Không thêm các tiền tố vào trường
  > Exp: product.name, not product.product_name
- thêm prefix "is" cho các trường boolean
  > Exp: is_active
- Lưu thời điểm tạo, update, delete record
  > Exp: created_at, updated_at, deleted_at

3. Constraint

- rằng buộc cũng cần đặt tên mô tả rõ ràng.
  > Exp: đặt tên foreign key: [table_name]\_[field]\_fkey, exp: user_id_fkey
- Thêm tiền tố idx cho các index

4. Migrations

- Tạo migration cho riêng từng table
- Sử dụng mẫu `move_[colume_name]_[from_table]_[to_table]` khi chuyển dữ liệu colume giữa các bảng
- Sử dụng mẫu `create_{table_name}_table` khi tạo table

- Sử dụng mẫu `update_{table_name}_table` khi update nhiều trong table

- Sử dụng mẫu `{action}_{column_name}_to_{table_name}_table` khi thao tác với colume, action như add, remove, update
