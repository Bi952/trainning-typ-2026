# Project: Thực hành tổng hợp

---

## Mô tả

Xây dựng một Backend Project dựa trên kiến thức đã học trong 5 tuần. Tự chọn domain (bán hàng, đặt vé, quản lý khóa học,...).

## Yêu cầu

- Project cần có 1–2 chức năng có độ khó cao để áp dụng kiến thức Backend
- Khuyến khích tích hợp các kiến thức: Database, ORM, Authentication, Message Queue, Redis, Pagination

### Gợi ý chức năng áp dụng kiến thức

| Chức năng | Kiến thức áp dụng |
|-----------|-------------------|
| Đăng ký + Đăng nhập | JWT, Password Hashing, Refresh Token, Role-based Authorization |
| CRUD + danh sách | REST API, ORM, Pagination, Index |
| Đặt hàng / Đặt vé | Transaction, Locking (xử lý concurrent) |
| Gửi email/notification sau khi đặt | Message Queue (async processing) |
| Xem thông tin sản phẩm | Caching Redis, TTL, Cache Invalidation |

## Output

- Source code chạy được
- Trình bày kiến trúc, các chức năng chính và những vấn đề kỹ thuật đã xử lý dưới dạng 1 báo cáo
