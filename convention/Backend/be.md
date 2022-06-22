# Lucis BE convention

1. Release flow

- Cần viết checklist những việc cần làm khi release như Env, đăng ký key bên thứ 3, cài đặt proxy với url đặc biệt trong app
- Cần cập nhật checklist và các file liên quan ngay khi code để tránh quên
- Định dạng file:

```
{date}:
    * Features:
        [commit_id|issue]{description}
    * Fixes:
        [commit_id|issue]{description}
    * Step release:
        - Add to env
```
