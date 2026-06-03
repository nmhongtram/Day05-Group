# Thin SPEC — Booking Assistant (Vinpearl)

## 1. Track, product/app và user

**Track:** Booking Assistant
**Product/app thật:** Vinpearl

**User cụ thể:** Khách lưu trú 

**Nhóm có phải user thật không? Nếu không, khác ở đâu?**

* Nhóm không hoàn toàn là user thật
* Khác ở:
  * Nhóm hiểu tech → thao tác nhanh hơn
  * User thật dễ bị rối khi có nhiều lựa chọn
  * User thường so sánh nhiều nền tảng

---

## 2. Evidence summary

| Evidence           | Nguồn                   | User/pain nói lên điều gì?                    | SPEC phải đổi gì?       |
| ------------------ | ----------------------- | --------------------------------------------- | ----------------------- |
| Review app du lịch | App Store / Google Play | Không đặt được phòng vì toàn hết phòng, app lỗi liên tục, phải xem phòng từng ngày nên mất thời gian  | Tự động tìm ngày có phòng |
| Observation        | Test flow thực tế       | Không thể tìm được bất kỳ kết quả nào dù đổi ngày di chuyển | Minh bạch trạng thái + đề xuất thay thế |

---

## 3. Pain statement

```text
Người dùng không thể nhanh chóng tìm phòng khả dụng do phải kiểm tra từng ngày và thiếu gợi ý thay thế, khiến trải nghiệm tìm kiếm tốn thời gian và kém hiệu quả.
```

---

## 4. Build slice

```text
Cho khách du lịch đang lên kế hoạch nghỉ dưỡng,
prototype sẽ dùng AI để tự động gợi ý combo phòng + vé phù hợp
(theo budget, số người, thời gian),

tạo ra danh sách 2–3 combo tối ưu (giá + tiện ích + lý do chọn),

và xử lý failure mode (input mơ hồ) bằng cách hỏi lại có hướng dẫn.
```

---

## 5. Auto/Aug decision

* [ ] Augmentation
* [x] Conditional automation
* [ ] Automation

**Lý do chọn:**

* Booking liên quan tiền, thời gian → không thể auto hoàn toàn
* Có thể auto trong case rõ

**Human role:**

* Decider
* Reviewer

---

## 6. Four paths

| Path           | Prototype phải thể hiện gì?               |
| -------------- | ----------------------------------------- |
| Happy          | Người dùng nhập ngày, địa điểm → AI gợi ý 2–3 combo rõ ràng + nút đặt      |
| Low-confidence | Người dùng nhập yêu cầu thiếu thông tin → AI hỏi lại           |
| Failure        | Người dùng nhập yêu cầu thiếu thông tin → AI báo không có combo → fallback sang chọn riêng |
| Correction     | User sửa input → AI cập nhật lại          |

---

## 7. Failure mode nguy hiểm nhất

```text
Nếu user nhập ngày mơ hồ ("cuối tuần này", "dịp lễ", "tháng sau"),
AI có thể parse sai ngày hoặc dùng ngày mặc định mà không thông báo,
hậu quả là user nhìn kết quả không khớp nhu cầu thật,
mất tin tưởng vào AI hoặc nghiêm trọng hơn là đặt nhầm ngày.
Prototype sẽ xử lý bằng: luôn echo lại ngày AI đã hiểu trước khi render
("Tôi hiểu bạn muốn nhận phòng 07/06 – trả phòng 08/06, đúng không?")
— user confirm hoặc sửa trước khi kết quả hiện ra.
Owner kiểm thử path này là: [tên thành viên phụ trách test].
```

---

## 8. Owner plan cho sáng Day 06

| Thành viên | Việc phụ trách      | Bằng chứng cần có trong repo |
| ---------- | ------------------- | ---------------------------- |
| A          | Research / evidence | Screenshot review            |
| B          | SPEC                | File SPEC                    |
| C          | Prototype           | Demo AI flow                 |
| D          | Test                | Case failure                 |
| E          | Demo                | Script + README              |

---
