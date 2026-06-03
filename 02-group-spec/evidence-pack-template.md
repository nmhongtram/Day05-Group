# Template — Evidence Pack

Nộp kèm thin SPEC cuối Day 05.

## 1. Nhóm và track

**Tên nhóm:**  
**Track:**  
**Product/app đã chọn:**  
**Build slice đang nghĩ:**  

## 2. Self-use evidence

Nhóm tự dùng app/workflow và ghi lại điểm gãy.

| Observation | Screenshot/link | Path liên quan | Điều học được |
|---|---|---|---|
|  |  | Happy / Low-confidence / Failure / Correction |  |
|  |  | Happy / Low-confidence / Failure / Correction |  |

## 3. User / review / social evidence

Nguồn có thể là review App Store/Play, group, comment, phỏng vấn nhanh, hoặc nguồn public khác.

| Quote / review / observation | Nguồn | User là ai? | Pain/failure mode |
|---|---|---|---|
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

Nếu chưa có nguồn ngoài nhóm, ghi rõ:

```text
Đây là giả định. Nhóm sẽ kiểm bằng [cách] trước checkpoint M1 Day 06.
```

## 4. Competitor / analog evidence

"Đặt phòng/vé máy bay + Xử lý đổi hủy phòng và giải thích chính sách hoàn trả"

| App / mô hình tham khảo                     | Họ xử lý task này thế nào?                                                                                                                                                                                                                                          | Pattern học được                                                                                                                                                    | Có áp dụng trong 1 ngày không?                                            |
| ------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| Expedia AI (ChatGPT integration)            | Chat + Action cards (nút "Book on Expedia", xem chuyến); gọi tool tra cứu pricing & supply data real-time; Happy path: gợi ý → click book; Low-confidence: hỏi clarifying questions (địa điểm, ngày, ngân sách); Failure: chuyển human agent + tóm tắt 30+ ngôn ngữ | Augmented decision (AI gợi ý, user click book); Action cards UI; Clarification questions khi low-confidence; Human escalation khi complex customerexperiencedive+2  | Có — UI action cards + prompt clarification + mock data linkedin          |
| Airbnb Support Bot                          | Chat + Action cards (nút "Cancel reservation", "Request refund"); gọi tool tra cứu reservation/account người dùng; Happy path: AI nhận diện hủy → action card → tự động xử lý; Low-confidence: hỏi lại + 2-3 lựa chọn action; Failure: đề xuất nói với người thật   | Hybrid decision (AI tự động routine, escalates complex); Action cards cho đổi/hủy; Human escalation pattern; Dẫn link Help Center article yourstory+2               | Có — Action cards + escalation pattern + prompt yourstory+1               |
| Booking.com AI (Smart Filter, Property Q&A) | Chat + Smart Filter UI (lọc giá, tiện ích); gọi tool tóm tắt review/policy; Happy path: AI tóm tắt → user click book; Low-confidence: đề xuất filter hẹp lại; Failure: routing đến human agent                                                                      | Augmented decision (AI gợi ý, user quyết định); UI filter cho clarification; Review summaries customerexperiencedive+1                                              | Có — UI filter + review summary prompt news.booking                       |
| Hopper HT Assist (AI travel agent)          | Chat thuần + nút "my trips/contact support"; gọi tool tra cứu bookings/modifications; Happy path: AI đề xuất rebook/refund → user click xác nhận; Low-confidence: hỏi lại loại phòng, ngày tháng; Failure: escalates human support                                  | Hybrid decision (AI xử lý rebook/refund cơ bản); Chat + confirmation buttons; Human escalation fastcompany                                                          | Có — Chat + nút xác nhận + mock data fastcompany                          |
| Perplexity AI (travel policy queries)       | Chat thuần + inline citations (hover preview source cards); gọi tool browsing/real-time Search; Happy path: trả lời + citations ngay; Low-confidence: đề xuất follow-up prompts; Failure: hiển thị "Browsing sources..." + báo không tìm thấy                       | Citations/Sources LUÔN C三更 (tránh hallucination); Showing work (hiển thị "Đang tra cứu..."); Follow-up prompts cho clarification; User tự kiểm tra nguồn linkedin+1 | Có — Inline citations + follow-up prompts + prompt engineering linkedin+1 |
| Google AI Flight Deals (Search)             | Chat + visual cards (hiển thị flight deals); gọi tool AI display bargains; Happy path: user mô tả → AI hiển thị deal → book; Low-confidence: hỏi nơi/khi nào/ngân sách; Failure: routing đến Google Travel                                                          | Visual cards UI; Clarification questions (where, when, budget); Augmented decision techcrunch+2                                                                     | Có — Visual cards + clarification prompt techcrunch                       |

## 5. Evidence -> Insight

```text
Evidence nổi bật nhất:

Insight:
User không chỉ gặp [surface problem].
Thật ra họ cần [deeper need / decision support / trust / recovery].

Opportunity:
AI có thể giúp bằng cách [augment/automate hành động hẹp].
```

## 6. Evidence đổi SPEC như thế nào?

- [ ] Đổi user chính.
- [ ] Đổi pain statement.
- [ ] Đổi build slice.
- [ ] Đổi Auto/Aug decision.
- [ ] Đổi 4 paths.
- [ ] Đổi failure mode.
- [ ] Đổi owner/test plan.

Ghi rõ 1-2 thay đổi quan trọng:

```text
Trước evidence, nhóm định...
Sau evidence, nhóm đổi thành...
Lý do:
```
