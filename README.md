```mermaid
sequenceDiagram
User->>System: Login
alt Đăng nhập thành công
System-->>User: Welcome
else Sai mật khẩu
System-->>User: Error
end
loop Kiểm tra mỗi 5 phút
System->>Database: Health check
end
```
```mermaid
sequenceDiagram
participant A as Người dùng
participant B as Hệ thống
participant C as Database
A->>B: Đăng nhập
B->>C: Kiểm tra user
C-->>B: Thông tin user
B-->>A: Đăng nhập thành công
```
