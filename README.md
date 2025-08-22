```mermaid
erDiagram
KHACH_HANG ||--o{ DON_HANG : dat
DON_HANG ||--|{ CHI_TIET : co
SAN_PHAM ||--o{ CHI_TIET : trong
KHACH_HANG {
string ma_kh PK
string ten
string email
string sdt
}
DON_HANG {
string ma_don PK
string ma_kh FK
date ngay_dat
float tong_tien
}
SAN_PHAM {
string ma_sp PK
string ten_sp
float gia
int ton_kho
}
```
```mermaid
gantt
title Kế hoạch dự án
dateFormat YYYY-MM-DD
section Phân tích
Khảo sát :done, a1, 2024-01-01, 7d
Thiết kế :active, a2, after a1, 10d
section Phát triển
Backend :b1, 2024-01-15, 20d
Frontend :b2, after b1, 15d
section Testing
Test :c1, after b2, 10d
Deploy
