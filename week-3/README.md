# Tuần 3: Authentication & Authorization

---

## 1. Khái niệm
- Authentication (Xác thực) là gì?
- Authorization (Phân quyền) là gì?
- Phân biệt 2 khái niệm này

## 2. Phân biệt cơ chế xác thực
- Session-based: flow hoạt động, cookie, server lưu session
- Token-based: flow hoạt động, stateless, client giữ token
- So sánh: khi nào dùng session, khi nào dùng token

## 3. JWT (JSON Web Token)
- JWT là gì?
- Cấu trúc: Header, Payload, Signature
- Lợi ích của JWT
- Hạn chế và rủi ro bảo mật

## 4. Password Hashing
- Tại sao không lưu password dạng plain text?
- Tại sao không dùng MD5/SHA? (brute force, rainbow table)
- Dùng bcrypt/argon2: salt, cost factor

## 5. Thực hành — Phát triển từ project tuần 2
- Tạo API đăng ký + đăng nhập trả về JWT
- Hashing mật khẩu khi đăng ký
- Tạo Middleware/Filter kiểm tra JWT cho các API protected
- Phân quyền: role-based access (admin vs user)
- Refresh Token: tại sao cần, flow hoạt động, implement

---

## Output

- Trình bày lý thuyết
- Demo đầy đủ: đăng ký → đăng nhập → gọi API protected → phân quyền → refresh token
- Chụp/quay kết quả
