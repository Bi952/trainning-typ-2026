# Tuần 5: Caching & Redis

---

## 1. Tìm hiểu Caching
- Caching là gì? Tại sao cần?
- Cache ở đâu? Application-level vs Distributed cache
- Khi nào nên cache, khi nào KHÔNG nên cache?

## 2. Chiến lược Caching
- Cache-Aside: app tự quản lý cache (check cache → miss → query DB → set cache)
- Write-Through: ghi vào cache và DB cùng lúc
- So sánh: khi nào dùng cái nào?

## 3. Redis cơ bản
- Redis là gì?
- Kiểu dữ liệu: String, Hash, List, Set, Sorted Set
- Các lệnh cơ bản: GET, SET, DEL, EXPIRE, TTL
- Cài đặt bằng Docker

## 4. Implement — Tích hợp Redis vào project
- Cài đặt Redis + thư viện client (Node: `redis`, Java: `jedis`/`lettuce`, Python: `redis-py`)
- Cấu hình kết nối
- Use case: Cache thông tin sản phẩm/user
  - Request → check cache → có thì trả ngay → không thì query DB → lưu cache với TTL

## 5. Các vấn đề thường gặp
- TTL: đặt bao lâu là hợp lý?
- Cache Invalidation: khi data thay đổi thì xóa/update cache thế nào?
- Cache Avalanche: nhiều key hết hạn cùng lúc → DB bị overload
- Cache Penetration: query data không tồn tại → luôn miss cache → query DB liên tục

---

## Output

- Trình bày lý thuyết
- Demo: gọi API lần 1 (cache miss, query DB) → gọi lần 2 (cache hit, nhanh hơn)
- So sánh response time có cache vs không cache
