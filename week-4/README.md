# Tuần 4: Message Queue

---

## 1. Tìm hiểu Message Queue
- Message Queue là gì?
- Tại sao cần MQ? Bài toán: user đặt hàng xong cần gửi email + cập nhật kho + ghi log — nếu gọi tuần tự thì chậm, 1 cái fail thì cả flow fail
- Sync vs Async communication
- Khi nào dùng MQ, khi nào gọi trực tiếp?

## 2. Các mô hình Message Queue
- Point-to-Point (Queue): 1 producer → 1 consumer xử lý
- Publish/Subscribe (Topic): 1 producer → nhiều consumer cùng nhận
- So sánh: khi nào dùng mô hình nào?

## 3. Chọn 1 Message Queue & tìm hiểu kiến trúc
- Gợi ý: RabbitMQ (dễ bắt đầu) hoặc Kafka (phổ biến trong production)
- Các khái niệm chính: Producer, Consumer, Queue/Topic, Exchange (RabbitMQ) hoặc Partition (Kafka)
- Cài đặt bằng Docker

## 4. Implement — Phát triển từ project tuần 2-3
- Use case gợi ý:
  - User đặt hàng → gửi message vào queue → consumer gửi email xác nhận
  - Hoặc: user đăng ký → gửi message → consumer gửi email welcome
- Flow: API nhận request → xử lý logic chính → đẩy message vào queue → trả response cho user ngay (không chờ email gửi xong)

## 5. Các vấn đề cần chú ý khi dùng MQ
- Message bị gửi trùng (duplicate) → Idempotency: xử lý 1 lần hay nhiều lần đều cho cùng kết quả
- Message bị mất → Acknowledge mechanism: consumer xác nhận đã xử lý xong
- Consumer chết giữa chừng → Dead Letter Queue: chứa message xử lý fail để retry sau
- Thứ tự message có quan trọng không? (ordering)

---

## Output

- Trình bày lý thuyết: MQ là gì, tại sao dùng, mô hình nào, kiến trúc MQ đã chọn
- Demo: gọi API → message vào queue → consumer xử lý → kết quả
- Giải thích được: nếu không dùng MQ thì flow này sẽ có vấn đề gì?
