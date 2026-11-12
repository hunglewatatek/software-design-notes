# 📚 Software Design: Ghi chú tự học

Bộ ghi chú đi từ thiết kế ở mức code (nguyên lý, design pattern) lên kiến trúc phần mềm, rồi tới thiết kế hệ thống phân tán (scalability, database, cache, message queue, resilience, bảo mật).

Mỗi file gồm:
- Nội dung chính theo từng chủ đề.
- Các khối **💡 Giải thích** viết lại cho dễ hiểu.
- Các khối **📌 Mở rộng** cho kiến thức nâng cao.
- Hình minh họa, sơ đồ.
- Bảng tóm tắt.
- Câu hỏi tự kiểm tra (bấm để xem đáp án) và bài tập kèm lời giải gợi ý.

**🖼️ Hình ảnh** nằm sẵn trong thư mục [`images/`](images/), nên đọc offline vẫn thấy hình. Bên dưới mỗi sơ đồ có mục "🔧 Mã nguồn sơ đồ" chứa mã mermaid để chỉnh sửa.

Nên mở bằng **VS Code** (nhấn `Ctrl+Shift+V` để xem preview), Typora, Obsidian hoặc GitHub để thấy hình và các ô đáp án bấm được.

---

## 🗺️ Lộ trình học

| # | File | Chủ đề | Từ khóa chính |
|---|---|---|---|
| 1 | [01-design-principles-solid.md](01-design-principles-solid.md) | Nguyên lý thiết kế | Coupling, Cohesion, SOLID, DRY, KISS, YAGNI, Code smell |
| 2 | [02-design-patterns.md](02-design-patterns.md) | Design Patterns | GoF, Creational/Structural/Behavioral, Strategy, Observer |
| 3 | [03-software-architecture.md](03-software-architecture.md) | Kiến trúc phần mềm | Pipe-and-Filter, Batch, Layered, Client-Server, P2P, Event-driven, SOA |
| 4 | [04-system-design-fundamentals.md](04-system-design-fundamentals.md) | Nền tảng System Design | Latency, Throughput, Scalability, Availability, Consistency, CAP, Quorum |
| 5A | [05a-database-selection-sharding-index.md](05a-database-selection-sharding-index.md) | Lựa chọn Database | SQL/NoSQL, Sharding, Index, OLTP/OLAP |
| 5B | [05b-database-advanced.md](05b-database-advanced.md) | Database nâng cao | Inverted Index, Elasticsearch, Replication, ACID/BASE, 2PC/3PC, SAGA, Paxos/Raft |
| 6 | [06-scaling-loadbalancer-cache-queue.md](06-scaling-loadbalancer-cache-queue.md) | Mở rộng & hiệu suất | Load Balancer L4/L7, Cache strategies, LRU/LFU, Message Queue |
| 7A | [07a-fault-tolerance-resilience.md](07a-fault-tolerance-resilience.md) | Chịu lỗi & phục hồi | SPOF, Failover, Retry/Backoff, Circuit Breaker, Bulkhead, HA/FT, SLA/SLO, MTBF/MTTR |
| 7B | [07b-message-queues.md](07b-message-queues.md) | Message Queues | Producer-Consumer, Pub/Sub, Backpressure, Kafka, RabbitMQ |
| 8 | [08-security-ratelimit-locking.md](08-security-ratelimit-locking.md) | Bảo mật & khóa | Session/JWT, RBAC/ABAC, OAuth2, Rate limiting, Idempotency, Optimistic/Pessimistic locking |

---

## 🧭 Cách học

1. **Học theo thứ tự**, mỗi buổi một file:
   - Bài 1 đến 3 là thiết kế ở mức code và kiến trúc.
   - Bài 4 đến 8 là thiết kế hệ thống phân tán. Các bài này dùng lại khái niệm của bài trước, ví dụ CAP và consistency ở bài 4 xuất hiện lại ở bài 5A, 5B và 6.
2. Với mỗi file:
   - Đọc mục **🎯 Mục tiêu** để biết cần nắm gì.
   - Đọc nội dung chính, chú ý các khối **💡 Giải thích**.
   - Gấp tài liệu lại, tự trả lời **❓ Câu hỏi tự kiểm tra**, rồi mới mở đáp án.
   - Làm **📝 Bài tập** ra giấy (vẽ sơ đồ kiến trúc) trước khi xem gợi ý.
3. Trước khi thi, chỉ cần ôn các mục **🧠 Tóm tắt nhanh** của mọi file.

## 🔗 Các mạch kiến thức xuyên suốt

- **Trade-off là chủ đề trung tâm.** Không có lựa chọn tốt nhất tuyệt đối, chỉ có lựa chọn phù hợp với yêu cầu.
- **Consistency và Availability:** Strong/Eventual/Weak (bài 4), ACID/BASE (bài 5B), Write-Through/Write-Back (bài 6), Optimistic/Pessimistic locking (bài 8).
- **Decoupling:** DIP/DI (bài 1), Observer (bài 2), Event-driven (bài 3), Message Queue (bài 6, 7B), SAGA Choreography (bài 5B).
- **Loại bỏ Single Point of Failure:** Replication và Failover (bài 4, 5B), Load Balancer (bài 6), Redundancy và Circuit Breaker (bài 7A).
