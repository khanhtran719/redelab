# Innovation Lab

Phòng AI Innovation & Product R&D giúp Founder khám phá, tranh luận và đánh giá cơ hội sản phẩm phần mềm. Đầu ra là danh mục hỗ trợ quyết định. Founder là người duy nhất quyết định; kể cả `SELECT` cũng chưa cho phép phát triển sản phẩm.

## Bắt đầu một phiên

Mở workspace này trong Codex. Dùng một chat mới hoặc khởi động lại phiên CLI để nạp cấu hình và skill vừa tạo. Không cần cài dependency. Có thể mở CLI bằng:

```sh
# Chạy từ thư mục workspace
codex -C .
```

Gửi nguyên prompt sau, thay phần trong ngoặc vuông:

```text
CIO, bắt đầu phiên DISCOVER theo protocols/ideation-session.md.
Chủ đề: [lĩnh vực hoặc nhóm khách hàng].
Thị trường: [địa lý/ngôn ngữ].
Ràng buộc: [thời gian, ngân sách, năng lực solo/nhóm nhỏ].
Dùng subagent thật cho nghiên cứu độc lập, tranh luận và Red Team.
Kiểm tra công cụ trước; nếu thiếu subagent, báo giới hạn, không giả lập hội đồng.
Lưu bằng chứng, bất đồng và portfolio. Dừng ở cổng quyết định Founder.
Không phát triển sản phẩm.
```

Các chế độ khác:

```text
CIO, chạy DEBATE cho [IDEA-0001, IDEA-0002] theo protocol,
tập trung vào [giả định cần phản biện]. Dùng subagent thật và dừng ở Founder gate.
```

```text
CIO, chạy DEEP DIVE cho [IDEA-0001] theo protocol,
tập trung vào [bằng chứng khách hàng, đối thủ, dữ liệu hoặc thương mại còn thiếu].
Không tạo prototype, code hay kế hoạch triển khai.
```

Tra ID và revision hiện tại trong [backlog](portfolio/idea-backlog.md) trước khi dùng prompt. Có thể gọi một skill riêng, ví dụ `$market-intelligence`, cho một câu hỏi có giới hạn mà không mở cả hội đồng.

## Đội ngũ

| Agent | Trách nhiệm riêng | Skill chính |
|---|---|---|
| CIO — phiên chính | Điều phối, giữ bằng chứng và bất đồng, trình portfolio | `idea-evaluation` |
| `customer-researcher` | Khách hàng, JTBD, vấn đề, giải pháp đang dùng | `problem-discovery` |
| `market-analyst` | Đối thủ, sản phẩm thay thế, định vị, trùng lặp | `market-intelligence` |
| `creative-inventor` | Cơ chế sản phẩm khác biệt, giả thuyết sáng tạo | `creative-ideation` |
| `product-strategist` | Giá trị, tiếp cận khách hàng, mô hình kinh doanh | `product-opportunity` |
| `technical-advisor` | Dữ liệu, tích hợp, chi phí, khả thi với nhóm nhỏ | `feasibility-assessment` |
| `red-team-critic` | Kiểm tra giả định mạnh nhất và lý do thất bại | `adversarial-review` |

Tối đa ba specialist đồng thời, hoặc ít hơn theo runtime. Các vai chạy theo đợt. Không cố định model mới: kế thừa cách chọn model/effort của Codex hiện có; xem [báo cáo khởi tạo](protocols/setup-validation.md). File vai trò và cờ bật multi-agent không bảo đảm phiên chat có công cụ spawn.

## Cấu trúc và cách vận hành

```text
innovation-lab/
├── AGENTS.md
├── README.md
├── .codex/config.toml
├── .codex/agents/                 # 6 vai trò TOML độc lập
├── .agents/skills/                # 7 SKILL.md
├── protocols/
│   ├── ideation-session.md        # 7 vòng và ba mức nghiên cứu
│   ├── debate-rules.md            # Phản biện và phản hồi thật
│   ├── evidence-policy.md         # Nguồn, ngày kiểm chứng, độ chắc chắn
│   ├── scoring-rubric.md          # 9 tiêu chí, tổng 100%
│   ├── portfolio-writes.md        # Một writer giữa các phiên, khóa và phục hồi
│   └── setup-validation.md        # Khả năng đã kiểm tra và giới hạn
├── portfolio/
│   ├── idea-backlog.md
│   └── decision-log.md
└── sessions/README.md             # Quy ước và mẫu hồ sơ phiên
```

Quy trình: khám phá độc lập → tạo cơ hội → phản biện liên ngành và phản hồi → Red Team độc lập → chấm điểm → đề xuất hội đồng → Founder quyết định. Mục tiêu khoảng 5–8 cơ chế khác nhau khi đủ cơ sở; trình 3–5 cơ hội tốt nhất hoặc ít hơn, kể cả không có cơ hội đủ mạnh. Ý tưởng thăm dò vẫn được lưu khi chưa đủ bằng chứng để xếp hạng.

Quyết định theo cú pháp:

```text
Founder: EXPLORE IDEA-0001.
Lý do: [tùy chọn]. Giới hạn: [phạm vi nghiên cứu tiếp theo].
```

Thay `EXPLORE` bằng `CHALLENGE`, `REFINE`, `PARK`, `REJECT` hoặc `SELECT`. Quyết định được ghi nối tiếp, không sửa âm thầm. `PARK`, `REJECT`, `SELECT` chỉ ghi nhận và dừng; với ba lựa chọn nghiên cứu, CIO chỉ tiếp tục trong phạm vi Founder đã nêu. Không lựa chọn nào tự động cấp quyền triển khai.

Đã có một [phiên nghiên cứu một agent](sessions/2026-11-20-01-broad-discovery.md) và tám ý tưởng exploratory; chưa có sản phẩm được chọn. [Kiểm tra Phase 2](sessions/2026-11-20-02-runtime-validation.md) ghi rõ discovery, công cụ đã chạy và phần bị chặn. Bộ cấu hình tồn tại trên đĩa; cuộc tranh luận thật vẫn cần runtime cung cấp subagent và công cụ trao đổi. Nếu thiếu, báo `BLOCKED_MULTI_AGENT` và lưu phần việc đã làm với đúng nhãn. Mở chat mới không bảo đảm công cụ sẽ xuất hiện.

Trước khi cập nhật các hồ sơ dùng chung, áp dụng [quy tắc ghi portfolio](protocols/portfolio-writes.md). Xếp hạng thương mại và ưu tiên nghiên cứu là hai kết quả riêng theo [rubric](protocols/scoring-rubric.md).
