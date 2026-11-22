# SES-20261120-01 — DISCOVER: cơ hội phần mềm đa lĩnh vực

## Phạm vi và trạng thái

- Ngày: 2026-11-20, Asia/Ho_Chi_Minh. Chủ trì thực tế: agent cha /root, vai trò điều phối CIO.
- Trạng thái: **BLOCKED_MULTI_AGENT — nghiên cứu một agent, hồ sơ tư vấn sơ bộ**. Chưa hoàn thành Innovation Council; không ghi AWAITING_FOUNDER như một hội đồng đã hoàn tất.
- Yêu cầu Founder: khám phá đa ngành tại Việt Nam, Đông Nam Á hoặc quốc tế; phù hợp solo/small team, phụ thuộc dữ liệu thực tế, vận hành ban đầu hợp lý, khác biệt có ý nghĩa, giá trị đo được; 3–5 ý tưởng nếu có cơ sở; không triển khai.
- Đầu ra hữu ích đã thực hiện: rà soát quy trình và cấu hình, nghiên cứu công khai, danh mục tám cơ chế, ba ứng viên cần kiểm chứng, phản chứng, bảng điểm thành phần và đề xuất nghiên cứu tiếp theo.
- Không thực hiện: subagent độc lập, trao đổi chéo, Red Team độc lập, phỏng vấn, demo sản phẩm đối thủ, thử API/tích hợp, thử nghiệm thị trường, code/prototype/UI/architecture, liên hệ người khác hoặc quyết định thay Founder.
- Backlog và decision log ban đầu trống. Không có ngành hoặc ý tưởng cũ được ưu tiên. Tên sản phẩm dưới đây là tên làm việc, chưa kiểm tra nhãn hiệu/domain.
- Giả định: một kỹ sư có kinh nghiệm và một người am hiểu nghiệp vụ có thể cộng tác; workflow đầu tiên dùng tài liệu khách hàng tự cung cấp, phạm vi hẹp, có người xác nhận. Năng lực cụ thể của Founder và khả năng tiếp cận khách hàng: UNKNOWN.
- Điều kiện dừng: kiểm tra đối thủ trực tiếp/gần kề và phương án thủ công cho từng ứng viên; lưu các giả thuyết quyết định. Dừng mở rộng khi thiếu bằng chứng khách hàng và khả năng phản biện độc lập trở thành giới hạn chính.

## Năng lực và người tham gia thực tế

| Khả năng | Cấu hình/phát hiện | Đã thực hiện |
|---|---|---|
| Sáu role của repository | Đã đọc .codex/agents/customer-researcher.toml, market-analyst.toml, creative-inventor.toml, product-strategist.toml, technical-advisor.toml, red-team-critic.toml | Chỉ đọc cấu hình; không có role nào được spawn |
| Model/effort | TOML dự án không đặt model/effort; cấu hình dự án ghi kế thừa, tối đa ba specialist đồng thời | Không có model/effort subagent thực tế để báo cáo; không áp model của roster global lên role dự án |
| Spawn/follow-up/message/wait/result subagent | Không có công cụ callable tương ứng; kiểm tra catalog đầu phiên và trước khi lưu | Không có runtime ID hoặc thông điệp chuyên gia; các công cụ sidebar chat không được dùng thay thế |
| Web | web__run trả route_not_found; tìm được mcp__codex_apps__search_service_web_run | Đã search/open/find nguồn công khai qua search_service |
| Filesystem | exec_command và apply_patch khả dụng | Đọc hướng dẫn; lưu nghiên cứu và backlog; không sửa cấu hình |
| Git | git status báo đây không phải Git repository | Không có git diff/commit; kiểm tra nội dung và liên kết bằng filesystem |

Các skill đã đọc và áp dụng phương pháp trong phạm vi một agent: expert-orchestration (và roster), problem-discovery, creative-ideation, market-intelligence, product-opportunity, feasibility-assessment, adversarial-review, idea-evaluation. Đọc AGENTS.md, ideation-session, evidence-policy, debate-rules, scoring-rubric, sessions/README.md, backlog và decision log. Đọc skill adversarial-review không đồng nghĩa đã có Red Team độc lập.

Quy trình áp dụng: protocols/ideation-session.md yêu cầu “If multi-agent coordination is missing, mark `BLOCKED_MULTI_AGENT`”; chỉ trả partial advisory brief. Đây là thiếu công cụ runtime, không phải Founder thiếu ủy quyền. Không tạo agent process, app điều phối hoặc chat sidebar để thay thế.

## Sổ nguồn

Tất cả ngày truy cập/xác minh trong bảng là **2026-11-20**. VERIFIED với trang vendor chỉ xác minh nội dung vendor công bố, chưa xác minh hiệu quả, khách hàng trả tiền hoặc khả năng chạy thực tế. Không suy diễn thiếu tính năng từ việc trang web không nhắc đến.

| ID | Nguồn và locator trực tiếp | Ngày xuất bản/sự kiện | Loại, giới hạn | Phát hiện hẹp |
|---|---|---|---|---|
| SRC-001 | [Abdi & Månsson — Understanding material shortage in Engineering-To-Order context](https://odr.chalmers.se/server/api/core/bitstreams/3c0d104c-2c6c-4b2b-8153-75e7b79434f2/content), abstract; §4.3.4, trang in 40–41/PDF 56–57 | 2025; acknowledgements June 2025 | Luận văn Chalmers, nghiên cứu một doanh nghiệp tự động hóa Thụy Điển, 14 phỏng vấn; không đại diện SME Việt Nam | Ghi nhận sai/thiếu revision làm chậm xử lý đơn ở nhà cung cấp |
| SRC-002 | [Specright Network](https://www.specright.com/blog/the-future-of-specification-management-is-specright-network/), Simplify Change Management | 2023-07-27 | Vendor; công bố cũ, kiểm tra bổ sung SRC-003 | Có Revision Management, theo dõi thay đổi từng field và Spec Compare |
| SRC-003 | [Specright Fall 2026 release](https://www.specright.com/blog/specright-fall-2026-product-release/), Supplier Network | Fall 2026; ngày chính xác không hiển thị | Vendor release, chưa demo | Nhận dữ liệu supplier theo định dạng họ dùng; thu BOM liên kết và tài liệu đi kèm |
| SRC-004 | [Qarma Quality](https://www.qarmainspect.com/quality), Every Stage of the Journey | Không hiển thị | Vendor, phạm vi chức năng công bố | Workflow lập kế hoạch, kiểm tra, báo cáo và theo dõi QC |
| SRC-005 | [Inspectorio QRM FAQ](https://docs.inspectorio.com/faqs/faq/qrm/), Integration/Data | Không hiển thị | Tài liệu chính thức, chưa kiểm tra entitlement tài khoản | Nhập file/API/SFTP; dữ liệu sản phẩm và PO phục vụ kiểm tra |
| SRC-006 | [SKUWorks — Packaging file handoff](https://www.skuworks.com/guides/posts/packaging-file-handoff-suppliers), Why handoffs go wrong | 2026-04-03 | Hướng dẫn vendor; không phải tần suất lỗi quan sát độc lập | Mô tả rủi ro bàn giao sai file/revision và quy trình kiểm soát thủ công |
| SRC-007 | [Shopee — Chính sách vận chuyển](https://help.shopee.vn/portal/4/article/77250), D.3 Bằng chứng khiếu nại | Ngày phiên bản không hiển thị trong trang đã mở | Chính sách nền tảng, riêng phạm vi Shopee VN; không phải tư vấn pháp lý | Liệt kê chứng cứ theo tình huống; có thời hạn cung cấp, ngoại lệ tùy vụ việc |
| SRC-008 | [Dohana — Khách khiếu nại thiếu hàng](https://donghangnhanh.vn/vi/baiviet/khach-khieu-nai-thieu-hang-shopee-shop-can-bang-chung-gi), mô tả sản phẩm | 2026-11-03 | Vendor, không dùng khẳng định tỷ lệ thắng khiếu nại | Quay và truy xuất video đóng hàng theo mã vận đơn; có lựa chọn miễn phí |
| SRC-009 | [MISA eShop — Xử lý trả hàng/hoàn tiền Shopee](https://helpeshop.misa.vn/kb/xu-ly-don-huy-yeu-cau-tra-hang-hoan-tien-tren-san-shopee), §2.2.1 | Không hiển thị trong phần đã đọc | Tài liệu chính thức, chưa thử tài khoản | Có gửi khiếu nại, đính kèm/bổ sung bằng chứng và theo dõi kết quả |
| SRC-010 | [Notion — Export your content](https://www.notion.com/help/export-your-content), Export entire workspace/FAQs | Không hiển thị | Tài liệu chính thức, chưa thử export | Export phụ thuộc quyền truy cập; tải lại export không tái tạo ngay workspace |
| SRC-011 | [Notion Backups — Restore](https://notionbackups.com/docs/restore), Limitations | Không hiển thị | Tài liệu vendor, chưa kiểm chứng restore | Nêu giới hạn phục hồi; điều kiện khôi phục relations và các loại dữ liệu bị thiếu |
| SRC-012 | [Restora](https://restora.cc/), Coverage report/Drift Auditor/Restore | Không hiển thị | Vendor; tính năng tuyên bố chưa được chạy độc lập | Công bố báo cáo coverage, đối chiếu backup với dữ liệu live và báo cáo restore |
| SRC-013 | [r/Notion — Need Help with Notion Backups & Collaboration](https://www.reddit.com/r/Notion/comments/1jfhn34/need_help_with_notion_backups_collaboration_how/), bài gốc | Ngày tuyệt đối không hiển thị; giao diện ghi 2y ago | Một người tự báo cáo, không xác minh danh tính; bình luận có vendor tự quảng bá | Người đăng hỏi về tính đầy đủ, relations và khả năng tái sử dụng export; không có bằng chứng mua |
| SRC-014 | [CRM Migration Checker — Show Up London](https://showuplondon.co.uk/crm-migration-checker/), Overview | Không hiển thị | Vendor, sample không phải khách hàng thật | Đối chiếu dữ liệu CRM trước/sau và xuất bằng chứng đã kiểm tra; gần trùng MoveProof |
| SRC-015 | [CoreCredit](https://corecredit.idlery.com/), Four steps/Features | Không hiển thị; footer 2026 | Vendor, chưa dùng app | Theo dõi core charge từ hóa đơn tới hoàn phụ tùng và ghi nhận credit; gần trùng CoreReturn |
| SRC-016 | [Rentman — Equipment combinations](https://support.rentman.io/hc/en-us/articles/360013703140-Create-Equipment-Combinations), Equipment types | Cập nhật 2026-11-11 | Tài liệu vendor | Theo dõi tổ hợp vật lý/ảo và thiếu thành phần; giảm tính mới của KitBack |
| SRC-017 | [Lokalise — QA checks](https://docs.lokalise.com/en/articles/2564656-qa-checks), Supported checks | 2026-09-28 | Tài liệu vendor, phân biệt Expert/Vantage | Đã kiểm tra placeholder, HTML, URL, số và nhiều loại sai khác; chưa bao phủ mọi trường hợp |
| SRC-018 | [FetchSandbox — Webhook sandbox](https://fetchsandbox.com/webhook-sandbox), Scenarios | Không hiển thị | Vendor; chưa thực thi | Công bố retry, duplicate, out-of-order và race scenarios; gần trùng ReplayLab |
| SRC-019 | [Kraft Heinz Printed Packaging Controls v5](https://kraftheinzsupplier.com/pdf_documents/KHC%20Printed%20Packaging%20Controls%20-%20Global%20Requirement%20-%20Version%205-%20December%202019.pdf) | Tên file ghi December 2019; chưa xác minh | Open trả 403; chỉ có search snippet | **Không dùng làm bằng chứng VERIFIED** |

Phạm vi tìm kiếm: tiếng Anh và tiếng Việt; VN cho ecommerce, quốc tế cho sản xuất, SaaS portability, developer tools và dịch vụ. Chưa có nghiên cứu riêng theo Indonesia/Thái Lan/Malaysia; không coi VN là đại diện cả SEA. Dùng search, sau đó mở trang và find đoạn liên quan; không liên hệ vendor, không mua báo cáo, không dùng nguồn riêng.

Các truy vấn quan trọng (ngày 2026-11-20):

- manufacturing supplier specification revision changes quality manual email Excel Qarma Inspectorio
- supplier specification revision purchase order acknowledgement software change impact Specright
- packaging supplier artwork revision acknowledgement obsolete stock change software
- CRM migration reconciliation validation CSV before after consultants data migration tool
- Vietnam giao hàng bồi thường mất hư hỏng hàng hồ sơ khiếu nại người bán
- Shopee seller claim evidence packing video software Vietnam bồi thường phần mềm
- phần mềm khiếu nại Shopee tự động hồ sơ bằng chứng Salework Sapo Pancake
- auto repair shop core returns tracking missed credits software
- rental equipment kits missing parts returns checklist software Rentman Booqable
- localization quality assurance placeholders context screenshots Vietnamese software Lokalise Crowdin
- webhook testing duplicate out of order idempotency replay test scenarios tool
- SaaS exit rehearsal export completeness attachments independent archive software Notion Slack
- Notion backup export validation restore NotionBackups ProBackup completeness
- site.reddit.com/r/Notion backup restore relations
- SaaS export audit portability tool offline archive

Đã kiểm tra phương án đối thủ, sản phẩm liền kề, dịch vụ tư vấn, checklist/file thủ công và giữ cách làm hiện tại. Nguồn SEO và thread có quảng bá được xem là lead, không cộng thành nhiều chứng cứ nhu cầu. Không tìm ra đối thủ bổ sung không chứng minh tính độc nhất. Không đánh giá pháp lý theo toàn bộ các quốc gia hoặc quyền dữ liệu cụ thể của khách hàng tương lai.

## Sổ luận điểm

| ID | Luận điểm/phạm vi | Loại | Nguồn/lập luận | Phản chứng và độ tin cậy |
|---|---|---|---|---|
| CLM-001 | Nghiên cứu tại một doanh nghiệp ETO ghi nhận sự lệch revision làm chậm supplier | VERIFIED | SRC-001, §4.3.4 | HIGH về việc nghiên cứu báo cáo điều này; không suy rộng tần suất sang VN |
| CLM-002 | Quản lý revision/spec compare đã có sản phẩm thương mại | VERIFIED | SRC-002, SRC-003 | HIGH về công bố; chưa đo triển khai/hiệu quả |
| CLM-003 | Các bộ QC có workflow dùng sản phẩm/PO và dữ liệu kiểm tra | VERIFIED | SRC-004, SRC-005 | HIGH về tài liệu; giá và quyền API cụ thể UNKNOWN |
| CLM-004 | Liên kết revision với lô áp dụng, tồn cũ và xác nhận điểm chuyển có thể tạo thêm giá trị cho SME bao bì | HYPOTHESIS | Cơ chế IDEA-0001 r2 từ CLM-001–003 và SRC-006 | LOW: chưa có khách hàng; ERP/PLM hoặc quy trình tốt có thể đáp ứng |
| CLM-005 | Lỗi dùng sai revision có thể gây tổn thất đủ đáng nghiên cứu | INFERENCE | CLM-001 và SRC-006; lỗi xảy ra sau in/sản xuất khó sửa rẻ | LOW cho phân khúc mục tiêu vì tần suất/chi phí chưa đo |
| CLM-006 | Shopee có yêu cầu chứng cứ theo loại khiếu nại và thời hạn cung cấp | VERIFIED | SRC-007, D.3 | HIGH trong phạm vi văn bản đọc tại ngày truy cập; thay đổi/ngoại lệ phải kiểm tra |
| CLM-007 | Video theo vận đơn và việc gửi khiếu nại đã được công cụ VN hỗ trợ | VERIFIED | SRC-008, SRC-009 | HIGH về công bố, chưa chạy tính năng |
| CLM-008 | Thu chứng cứ ngay lúc nhận/mở hàng hoàn có thể giảm hồ sơ thiếu dữ liệu và công tìm lại | HYPOTHESIS | IDEA-0002 r2; kết hợp CLM-006–007 | LOW: công cụ sẵn có và SOP có thể đã đủ |
| CLM-009 | Không còn chứng cứ đúng thời điểm có thể khiến một số hồ sơ khó bổ sung về sau | INFERENCE | CLM-006; tình trạng kiện thay đổi sau mở/di chuyển | MEDIUM cho cơ chế; chưa đo mức tiền có thể thu hồi thêm |
| CLM-010 | Notion export không chứa phần ngoài quyền người xuất và không tái lập workspace nguyên trạng ngay khi nhập lại | VERIFIED | SRC-010 | HIGH về giới hạn được công bố; đã đọc trang Export hiện tại, không dựa vào FAQ cũ về lịch export |
| CLM-011 | Người dùng công khai có thắc mắc về tính đầy đủ và portability của export | VERIFIED | SRC-013, chỉ bài gốc | LOW cho nhu cầu thị trường: một người không xác minh, không có cam kết mua |
| CLM-012 | Vendor backup đã có restore, cảnh báo giới hạn, coverage và đối chiếu dữ liệu | VERIFIED | SRC-011, SRC-012 | HIGH về công bố; không kết luận mọi vendor khôi phục cùng phạm vi |
| CLM-013 | Agency chuyển giao workspace có thể trả tiền để kiểm chứng các tác vụ đọc/tìm dữ liệu trong archive độc lập | HYPOTHESIS | IDEA-0008 r2 từ CLM-010–012 | LOW: vendor backup và kiểm tra thủ công có thể thay thế |
| CLM-014 | File export thành công chưa chứng minh mọi tác vụ tra cứu cần thiết sẽ thực hiện được | INFERENCE | CLM-010, CLM-012; cần tiêu chí đầu ra ngoài việc job thành công | MEDIUM về logic, LOW về mức thiệt hại thương mại ở phân khúc |
| CLM-015 | MoveProof, CoreReturn, KitBack, LocaleGate, ReplayLab có mức chồng lấn đáng kể | INFERENCE | SRC-014–018 so với mô tả ứng viên r1 | MEDIUM; chỉ so chức năng công bố, không kết luận toàn bộ thị trường đã đáp ứng |
| CLM-016 | Khả năng mua, ngân sách và mức sẵn sàng trả tiền của ba phân khúc mục tiêu | UNKNOWN | Chưa phỏng vấn, quan sát hoặc có giao dịch | Không dùng giá vendor làm bằng chứng nhu cầu |
| CLM-017 | Kênh tiếp cận có CAC hợp lý và tỷ lệ chuyển đổi | UNKNOWN | Đề xuất kênh trong briefs; chưa có quyền truy cập hay thử bán | Không coi cộng đồng hoặc danh sách chuyên gia là phân phối đã có |
| CLM-018 | Quyền xử lý tài liệu thương mại/video/dữ liệu khách hàng của một khách hàng cụ thể | UNKNOWN | Chưa có mẫu, hợp đồng, retention policy hoặc phạm vi quốc gia đầy đủ | Nhập file không tự tạo quyền xử lý; cần đánh giá riêng |
| CLM-019 | Một workflow hẹp có người xác nhận có thể phù hợp nhóm nhỏ | HYPOTHESIS | Biên MVP và các phụ thuộc của ba briefs | LOW: chưa có mẫu dữ liệu hay thử nghiệm; không cam kết lịch/cost |
| CLM-020 | Lịch sử quyết định và mẫu kiểm chứng có thể tạo retention, nhưng dễ bị sao chép | HYPOTHESIS | So CLM-002, CLM-007, CLM-012; tài liệu/quy trình xuất được | LOW; chưa có switching/retention quan sát |

## Khám phá ban đầu và bản đồ vấn đề

**Independent initial findings: NOT RUN.** Không có runtime identity/assignment/output của chuyên gia. Những ghi chú dưới đây là tổng hợp của CIO sau quá trình nghiên cứu tuần tự, không phải bản ghi độc lập được bảo toàn trước khi trao đổi.

| Finding của CIO | Tác nhân, trigger và công việc | Thiệt hại giả định/workaround | Chứng cứ/giới hạn |
|---|---|---|---|
| CIO-F01 | Điều phối supplier nhận revision mới trong lúc có đơn/tồn đang chạy | Tốn xác nhận; email/file có thể lệch với hàng đang làm | CLM-001–005; dữ liệu doanh nghiệp bao bì VN còn thiếu |
| CIO-F02 | Nhân viên kho/shop nhận hàng hoàn và phải chứng minh tình trạng | Tìm video/chứng từ; điện thoại, camera, công cụ bán hàng hiện có | CLM-006–009; chưa biết số ca/tháng hoặc nguyên nhân thua khiếu nại |
| CIO-F03 | Agency/ops chuẩn bị bàn giao hay rời workspace SaaS | Có file nhưng chưa chứng minh dùng được; kiểm tra tay hoặc backup | CLM-010–014; người mua lặp lại là giả thuyết |
| CIO-F04 | Người làm migration, sửa xe, cho thuê, localization, webhook QA | Những cơ chế hẹp có vẻ mới đã có chức năng sát ở đối thủ | CLM-015; cần phân khúc mới rõ ràng mới đáng quay lại |

## Danh mục ý tưởng và revision

Toàn bộ sản phẩm đề xuất là HYPOTHESIS. Cơ chế sáng tạo dùng: đổi thời điểm kiểm chứng, gắn sự kiện số với đối tượng vật lý, đóng vòng công việc bằng kết quả cuối cùng, kiểm chứng từ phía người tiếp nhận. Không tuyên bố phát minh mới trên thị trường.

| ID | Tên r1, khách hàng/job | Cơ chế ban đầu và giá trị đo được | Kết quả rà soát/r2 |
|---|---|---|---|
| IDEA-0001 | LotDelta — supplier/nhà in bao bì đổi quy cách | Bản thay đổi dẫn đến danh sách lô/PO chịu ảnh hưởng; đo giờ xác nhận và rework | Giữ nghiên cứu r2: chốt điểm chuyển revision và xử lý tồn/WIP; bỏ khác biệt chỉ dựa vào spec compare (CLM-002) |
| IDEA-0002 | ClaimReady — shop/đơn vị vận hành shop VN chuẩn bị hồ sơ hàng hoàn | Liên kết vận đơn–chứng cứ–hạn xử lý; đo thời gian chuẩn bị và hồ sơ thiếu | Giữ nghiên cứu r2: kiểm tra phần chứng cứ còn thiếu tại thời điểm nhận/mở hàng; gửi khiếu nại đã có MISA (CLM-007) |
| IDEA-0003 | MoveProof — agency chuyển CRM | Đối soát trước/sau theo field, chuyển lỗi thành bằng chứng bàn giao; đo công kiểm tra | Chưa vào danh sách sâu: CRM Migration Checker gần trùng (SRC-014) |
| IDEA-0004 | CoreReturn — gara nhỏ nhận lại core credit | Chỉ đóng nghĩa vụ khi credit thực nhận; đo tiền quá hạn | Chưa vào danh sách sâu: CoreCredit gần trùng cả cơ chế (SRC-015) |
| IDEA-0005 | KitBack — đơn vị cho thuê AV/event | Ghi đủ bộ lúc tháo/lắp/trả, phát hiện thành phần thiếu; đo vật tư thất lạc | Chưa vào danh sách sâu: Rentman đã có tổ hợp và thiếu thành phần (SRC-016) |
| IDEA-0006 | LocaleGate — team sản phẩm đa ngôn ngữ | Kiểm tra bất biến placeholder/số/ngữ cảnh trước phát hành; đo lỗi thoát QA | Chưa vào danh sách sâu: cơ chế cơ bản bị Lokalise bao phủ (SRC-017); chưa tìm khác biệt đáng tiền |
| IDEA-0007 | ReplayLab — developer tích hợp webhook | Thử event trùng/đảo thứ tự và kiểm tra side effect; đo lỗi tìm trước deploy | Chưa vào danh sách sâu: FetchSandbox công bố các scenario sát cơ chế (SRC-018) |
| IDEA-0008 | ExitDrill — agency bàn giao/rời SaaS | Kiểm tra archive dùng được trước đóng tài khoản; đo tác vụ tra cứu thành công | Giữ nghiên cứu r2: acceptance checklist theo tác vụ thực của khách hàng; coverage/restore report thông thường đã có (CLM-012) |

Lựa chọn ba hướng để trình bày sâu là phân bổ chú ý nghiên cứu của CIO, không phải thương mại đã được xếp hạng, không phải PARK/REJECT các hướng còn lại. Các lĩnh vực khác đã tìm lead nhưng không lập concept riêng: scope change agency, supplier promise tracking. Không dùng số lượng ý tưởng làm bằng chứng chất lượng.

## Trao đổi chéo và Red Team

- Critique → response giữa agent khác nhau: **NOT RUN**.
- Red Team độc lập và phản hồi của proponent: **NOT RUN**.
- Actual supporting/opposing agents cho IDEA-0001, IDEA-0002, IDEA-0008: **không có**. Không có phiếu ủng hộ, phản đối hoặc abstention từ chuyên gia đã được triệu tập.
- Exchange ID/runtime messages: **không tồn tại**. Không dựng hội thoại thay thế.

Tự phản biện dưới đây do cùng CIO thực hiện; những thay đổi là revision của một người nghiên cứu, không phải bất đồng thật giữa các agent.

| Self-review ID / ý tưởng | Lập luận thuận mạnh nhất | Phản biện và tác động | Điều chỉnh / điều kiện bác bỏ phản biện |
|---|---|---|---|
| SELF-01 / IDEA-0001 r2 | Một lần đổi quy cách có thể lan tới hàng đang làm; chốt điểm áp dụng có giá trị vận hành | Specright đã quản lý revision và nhận dữ liệu supplier; Excel/ERP có thể đủ. Nếu seller không kiểm soát buyer approvals, phần mềm chỉ thêm nhập liệu | Thu hẹp vào quyết định lô/tồn và xác nhận từ hai phía. Chỉ tiếp tục nếu dữ liệu thật cho thấy bước này hiện đứt và lợi ích ròng cao hơn SOP chuẩn hóa |
| SELF-02 / IDEA-0002 r2 | Thu chứng cứ ở thời điểm không thể tái tạo giúp chuẩn bị hồ sơ đúng hơn | Dohana + MISA + quy trình sàn có thể đủ; thua khiếu nại có thể do bản chất vụ việc. Phí lưu video/support có thể vượt doanh thu | Tập trung missing-evidence check và handoff kho–CSKH; giữ chứng cứ gốc. Nếu hồ sơ đủ mà kết quả không đổi hoặc giảm công không đáng kể, cơ hội yếu |
| SELF-03 / IDEA-0008 r2 | Doanh nghiệp cần dữ liệu dùng được khi bỏ một công cụ; agency có thể lặp lại job giữa khách hàng | Restora có coverage/drift/restore reports. Một file không cho biết những gì bị bỏ khỏi file; nhu cầu có thể chỉ một lần | Phân biệt danh mục kỳ vọng do chủ dữ liệu xác nhận với archive thực tế; thử tác vụ tra cứu. Nếu không hơn vendor reports + checklist tay, thiếu khác biệt đáng tiền |

## Ba brief tư vấn sơ bộ

### IDEA-0001 r2 — LotDelta

**Pitch:** Biến mỗi thay đổi quy cách/bao bì thành quyết định rõ ràng về lô nào áp dụng, tồn cũ xử lý thế nào và ai đã xác nhận.

- **Khách hàng và người mua (HYPOTHESIS):** doanh nghiệp in/chuyển đổi bao bì hoặc sourcing team nhỏ phục vụ nhiều buyer VN/SEA; người dùng là điều phối đơn và QA, người mua là chủ doanh nghiệp/head of operations. Bắt đầu với bao bì hàng tiêu dùng thông thường; chưa đánh giá ngành có yêu cầu chuyên biệt.
- **Vấn đề:** bản được duyệt mới không tự xác định ảnh hưởng lên PO mở, WIP và vật tư cũ. Cách hiện tại có thể là email, thư mục chung, ERP, gọi điện và Excel. Tần suất/thiệt hại tại phân khúc đích UNKNOWN.
- **Core workflow đề xuất:** nhận bản cũ/mới và danh sách PO/lô do khách cung cấp → người phụ trách xác nhận điểm thay đổi → xác định phạm vi lô bị ảnh hưởng → ghi quyết định dùng tiếp/sửa/giữ tồn và điểm chuyển revision → người có trách nhiệm xác nhận → chuyển bản hướng dẫn đã chốt cho ca sản xuất/QC. Không mặc định file mới có hiệu lực cho mọi hàng cũ.
- **Đối thủ/substitute:** Specright trực tiếp ở spec/change management; Qarma/Inspectorio ở QC; ERP/PLM đang dùng; checklist và release note theo quy trình SKUWorks. CLM-002–003 bác bỏ tuyên bố spec compare là mới.
- **Khác biệt có thể có:** ưu tiên giải quyết điểm áp dụng thay đổi trên hàng vật lý đang tồn tại cho supplier làm với nhiều buyer; sử dụng tài liệu sẵn có. Chưa xác minh đối thủ thiếu workflow này hoặc khách hàng cần thêm một công cụ.
- **Giá trị đo:** phút/giờ chốt một revision, số lần hỏi lại, rework thực sự do dùng sai phiên bản, công cập nhật dữ liệu. Giá trị ròng = công/rework tránh được trừ công nhập và duy trì. Chưa có kết quả thực đo.
- **Mô hình kinh doanh:** phí theo site hoặc số change packet đang hoạt động; onboarding có phạm vi cố định. Phân phối giả định qua tư vấn QC và nhóm sourcing; chưa có đối tác hoặc CAC.
- **MVP sơ bộ:** khó vừa, 3/5 trong biên một họ tài liệu và quyết định do người duyệt. Dữ liệu cần: file quy cách, PO/lô, tồn/WIP và người có quyền duyệt do khách cung cấp. Không cần dữ liệu công khai khan hiếm; chất lượng/khả năng cung cấp mẫu vẫn UNKNOWN.
- **Rủi ro chính:** quy trình buyer không chấp nhận xác nhận mới; mapping PO–lô kém; file scan/ngoại lệ tạo dịch vụ thủ công; trách nhiệm khi đọc sai revision; incumbent có sẵn; chưa đánh giá quyền thương mại/IP tài liệu. Cần đo công xử lý trên mỗi change packet, không chỉ hosting.
- **Bằng chứng:** MEDIUM cho cơ chế vấn đề trong ngành gần kề và cạnh tranh; LOW cho cơ hội SME bao bì VN/SEA. Một luận văn ở doanh nghiệp ETO khác ngành không xác thực thị trường mục tiêu.
- **Agent ủng hộ/phản đối:** chưa có. CIO giữ để nghiên cứu vì giá trị có thể gắn với tổn thất đo được; tự phản biện SELF-01 chưa giải quyết.
- **Lý do giữ:** job hẹp, tác động trước khi sản xuất sai, đường lấy dữ liệu có thể bắt đầu bằng file có quyền. Không cần phát triển cả bộ ERP để kiểm tra giả thuyết.
- **Kiểm chứng đề xuất, chưa chạy:** 5 doanh nghiệp trong cùng phân khúc, tổng 10 ca thay đổi gần đây gồm cả ca không gây lỗi; xin phép dùng bản ẩn danh và dựng lại dòng thời gian bằng tài liệu hiện có. So workflow hiện tại với một checklist packet làm thủ công, không prototype. Thành công giả định: ít nhất 3/5 doanh nghiệp có ca sai điểm áp dụng lặp lại hoặc mất ≥2 giờ/tuần; checklist giảm ≥30% công xác nhận mà không tăng tổng công nhập; ít nhất 2 người mua đồng ý một bước đánh giá có ngân sách/phạm vi cụ thể. Dừng/chuyển hướng nếu chỉ là kỷ luật đặt tên file hoặc ERP đã giải quyết. Ước lượng nghiên cứu 3–5 ngày công sau khi có mẫu; tuyển người/tiền khuyến khích UNKNOWN. Cần yêu cầu riêng trước outreach/trial, và quyền sử dụng tài liệu.

### IDEA-0002 r2 — ClaimReady

**Pitch:** Khi kiện hàng hoàn vừa về kho, cho nhân viên biết hồ sơ đang thiếu chứng cứ nào và gom đúng bộ tài liệu cho người xử lý khiếu nại.

- **Khách hàng và người mua (HYPOTHESIS):** shop hàng có serial/phụ kiện hoặc agency vận hành nhiều shop Shopee VN với số ca hàng hoàn đủ thường xuyên; kho/CSKH là người dùng, chủ shop hoặc operations lead trả tiền. Bắt đầu một sàn và một nhóm sự cố; chưa suy rộng chính sách sang SEA.
- **Vấn đề:** chứng cứ nằm ở camera, điện thoại, hóa đơn và người khác; tình trạng kiện sau khi mở khó ghi lại như lúc tiếp nhận. Tổn thất thực tế do thiếu chứng cứ, so với vụ việc không đủ căn cứ, UNKNOWN.
- **Core workflow đề xuất:** nhận mã đơn và loại tình huống → hướng dẫn ghi nhận tình trạng lúc nhận/mở kiện theo checklist đã được người phụ trách duyệt → ghép video gốc/chứng từ gửi và nhận → đánh dấu thiếu, người chịu trách nhiệm và hạn từ thông báo sàn → xuất danh mục chứng cứ cho CSKH nộp → ghi kết quả và lý do còn thiếu. Không hứa kết quả bồi thường.
- **Đối thủ/substitute:** Dohana ghi/truy video theo mã; MISA eShop đã hỗ trợ nộp khiếu nại và bằng chứng; workflow của Shopee; điện thoại + thư mục chung + checklist. Thêm nút upload hoặc viết đơn bằng AI không đủ khác biệt.
- **Khác biệt có thể có:** kiểm tra mức sẵn sàng hồ sơ ngay tại điểm nhận hàng và bàn giao kho–CSKH, khi chứng cứ còn thu được. Khả năng tích hợp video hiện có chưa xác minh; biên đầu dùng file khách cung cấp hoặc dẫn chiếu tài liệu có quyền, không giả định API sàn.
- **Giá trị đo:** thời gian gom hồ sơ, tỷ lệ hồ sơ thiếu/tới trễ, công bổ sung, số ca có thể sửa thiếu chứng cứ; tiền thu hồi tăng thêm chỉ được ghi sau so sánh thực tế, không suy từ số case đóng.
- **Mô hình kinh doanh:** thuê bao theo shop/kho và dung lượng hoặc quota case. Khả năng trả tiền chưa biết; chưa đề xuất success fee khi chưa phân biệt phần tiền do sản phẩm tạo ra. Kênh giả định: agency ecommerce/đơn vị vận hành kho.
- **MVP sơ bộ:** 3/5 trong biên nhập file, một tình huống, xuất packet và nhắc hạn do người dùng xác nhận. Phụ thuộc: quyền dùng video/hóa đơn, mapping mã đơn, bản chính sách có ngày và thông báo cụ thể; không tự kiểm tra được tất cả chứng cứ có được sàn chấp nhận.
- **Rủi ro chính:** tính năng đã nằm trong công cụ hiện tại; tần suất thấp; quy tắc thay đổi; chọn sai loại case/hạn; video lớn tạo storage/egress/support; thông tin người mua trong nhãn/video; thua vì không có quyền yêu cầu chứ không phải thiếu tài liệu. Không sửa nội dung chứng cứ hoặc giả định lưu file đồng nghĩa quyền xử lý.
- **Bằng chứng:** HIGH về sự tồn tại yêu cầu chứng cứ và tính năng đối thủ tại VN; LOW về nhu cầu mua, frequency và ROI. Chưa có case shop thật hay tỷ lệ thắng được xác minh.
- **Agent ủng hộ/phản đối:** chưa có. CIO giữ vì tác vụ có trigger và đầu ra cụ thể; SELF-02 là phản biện chưa giải quyết.
- **Lý do giữ:** có thể đo job ở từng case, tiếp cận bằng hồ sơ ẩn danh, biên sản phẩm nhỏ nếu người dùng tự nộp.
- **Kiểm chứng đề xuất, chưa chạy:** 6 shop cùng nhóm hàng, 30 case gần nhất gồm cả thắng và thua. Người chủ phân loại nguyên nhân theo tài liệu, đo công baseline; so checklist thủ công với workflow/công cụ họ đã mua. Ngưỡng đề xuất: ≥10/30 ca có thiếu chứng cứ có thể khắc phục bằng thay đổi thời điểm ghi nhận; giảm ≥40% thời gian chuẩn bị; ít nhất 2 người mua chấp nhận phạm vi đánh giá có ngân sách. Nếu hồ sơ đã đủ hoặc lợi ích chỉ đến từ nộp khiếu nại sẵn có, không có cơ sở tiếp tục cơ chế hiện tại. 2–4 ngày công sau khi được cấp hồ sơ; tuyển mẫu chưa ước lượng. Cần ủy quyền riêng cho outreach và dữ liệu được che thông tin cá nhân; không nộp claim thay khách trong thử nghiệm đề xuất này.

### IDEA-0008 r2 — ExitDrill

**Pitch:** Trước khi rời một SaaS, kiểm tra liệu người nhận có tìm và sử dụng được những dữ liệu quan trọng chỉ từ bản xuất hay không.

- **Khách hàng và người mua (HYPOTHESIS):** tư vấn/agency bàn giao workspace cho nhiều khách hàng; khởi đầu Notion, thị trường quốc tế. Người dùng là chuyên viên migration/ops, người mua là chủ agency. Tần suất job ở người mua lặp lại chưa xác minh.
- **Vấn đề:** export thành công không nói đủ về các tác vụ thực tế sau bàn giao; một số dữ liệu ngoài quyền xuất không xuất hiện. Export/read-back thủ công, backup vendor hoặc tiếp tục trả tiền tài khoản cũ là substitute.
- **Core workflow đề xuất:** chủ dữ liệu nêu danh mục kỳ vọng và 10 tác vụ tra cứu cần giữ → cung cấp archive có quyền và ghi rõ phạm vi export → kiểm tra file/link và đánh dấu phần không thể biết từ archive → người tiếp nhận làm tác vụ trên bản lưu độc lập trong khi nguồn vẫn được giữ nguyên → xuất báo cáo đạt/không đạt/chưa kiểm chứng và bằng chứng. Không cần đóng tài khoản để diễn tập.
- **Đối thủ/substitute:** Notion export; Notion Backups, Restora; checklist migration và người tư vấn. Restora đã có coverage/drift/restore report: chỉ đếm file hoặc báo thiếu quan hệ sẽ chồng lấn mạnh.
- **Khác biệt có thể có:** nghiệm thu theo tác vụ cần làm sau rời nền tảng, từ góc nhìn người nhận và một bản lưu đọc độc lập; tiêu chí do khách xác nhận, không chỉ xác nhận job backup. Chưa chứng minh người mua coi sự độc lập này là lợi ích đáng trả tiền.
- **Giá trị đo:** tỷ lệ tác vụ đọc/tìm thành công, thời gian xử lý thiếu sót trước bàn giao, giờ hỗ trợ phát sinh và số ngày còn phải giữ công cụ cũ. Không tuyên bố có thể phục hồi những thứ chưa từng xuất.
- **Mô hình kinh doanh:** phí theo dự án/archive và gói agency làm nhiều lần. Giữ doanh thu theo lần là phương án hợp lý cần thử khi job không thường xuyên; chưa có giá hoặc WTP. Kênh giả định: chuyên gia triển khai/migration có khách hàng sẵn.
- **MVP sơ bộ:** 3/5 với một định dạng export và bộ tác vụ đọc được giới hạn; độ khó tăng mạnh nếu đòi tái tạo toàn bộ nhiều SaaS. Cần archive thật, danh mục kỳ vọng do người có quyền xác nhận, quyền mở nội dung và tác vụ mẫu. Không cần API phục hồi trong biên này.
- **Rủi ro chính:** vendor backup đã đủ; công cụ chỉ là checklist dễ sao chép; không biết nội dung bị bỏ khỏi export nếu thiếu baseline độc lập; mẫu tác vụ thiên lệch tạo an tâm sai; tài liệu khách hàng nhạy cảm; định dạng biến đổi; hỗ trợ thủ công theo dự án; nhu cầu từng đợt làm retention yếu.
- **Bằng chứng:** HIGH về giới hạn export được Notion công bố và sự tồn tại cạnh tranh; LOW về agency segment, willingness-to-pay và lợi thế. Thread công khai chỉ là tín hiệu đau, có bình luận vendor nên không coi là xác thực khách hàng.
- **Agent ủng hộ/phản đối:** chưa có. CIO giữ như hướng khám phá có khác biệt cơ chế cần thử; SELF-03 có thể loại bỏ toàn bộ business case.
- **Lý do giữ:** dữ liệu có đường xuất chính thức, xác minh đầu ra là job nhỏ và có thể thử thủ công, phù hợp bán theo dự án nếu agency lặp lại.
- **Kiểm chứng đề xuất, chưa chạy:** 5 agency, 10 bộ archive được phép dùng; mỗi bộ có danh mục và 10 tác vụ chủ dữ liệu xác nhận, kể cả tập có ràng buộc quyền rõ. Đối chiếu bằng báo cáo vendor/checklist hiện có và một lượt người khác đọc thử. Ngưỡng đề xuất: ≥3/5 agency có job lặp lại; ≥3/10 archive phát hiện khoảng trống có tác động tác vụ mà cách hiện tại bỏ qua; giảm ≥30% công nghiệm thu; ≥2 người mua chấp nhận đánh giá có ngân sách. Dừng nếu không phát hiện thêm hoặc mỗi archive cần tư vấn tùy biến quá lớn. 3–5 ngày công sau cấp mẫu; không chạy restore hay thay đổi tài khoản. Cần yêu cầu riêng trước outreach/xử lý dữ liệu bên ngoài.

Mọi số lượng, tỷ lệ thành công và effort của các đề xuất trên là **HYPOTHESIS/ngưỡng phán đoán của CIO**, không phải benchmark ngành hay kết quả đã đạt. Đồng ý nghiên cứu hoặc nói muốn mua vẫn yếu hơn giao dịch thực tế.

## Chấm điểm sơ bộ theo rubric

Đây là bản nháp đánh giá một agent trước peer review/Red Team. Điểm 1–10, cao hơn thuận lợi hơn. UNKNOWN giữ nguyên, không thay bằng 0/5; không chuẩn hóa phần đã biết. Rationale của điểm không phải chứng minh sản phẩm có lợi thế.

### IDEA-0001 r2

| Tiêu chí | Trọng số | Điểm | Cơ sở/loại | Confidence | Phản biện tự rà soát |
|---|---:|---:|---|---|---|
| Mức độ vấn đề | 20% | 7 | CLM-005, INFERENCE: có thể phát sinh rework/chậm đơn | LOW: chưa đo phân khúc | Tần suất thấp hoặc SOP đủ |
| Bằng chứng nhu cầu | 15% | UNKNOWN | CLM-016 | LOW: không có hành vi mua | Có vấn đề chưa đồng nghĩa mua phần mềm |
| Khác biệt | 15% | 4 | CLM-002–004, INFERENCE: khoảng chồng lấn lớn | LOW về lợi thế; HIGH về tính năng đã công bố | Specright/ERP có thể đã đủ |
| Phân phối | 15% | UNKNOWN | CLM-017 | LOW | Chưa có kênh thực tế |
| Khả thi nhóm nhỏ | 10% | 6 | CLM-019, HYPOTHESIS: file + người duyệt | LOW | Chuẩn hóa dữ liệu gây dịch vụ thủ công |
| Kiếm tiền | 10% | UNKNOWN | CLM-016 | LOW | Giá trị thuộc buyer nhưng supplier chịu công |
| Pháp lý/dữ liệu | 5% | UNKNOWN | CLM-018 | LOW | Quyền dùng file và trách nhiệm sai số |
| Phòng thủ dài hạn | 5% | 3 | CLM-020, HYPOTHESIS | LOW | Incumbent dễ bổ sung workflow |
| Phù hợp MVP gọn | 5% | 7 | CLM-019, HYPOTHESIS: một loại thay đổi | LOW | Scope tăng nếu cần mọi buyer |

### IDEA-0002 r2

| Tiêu chí | Trọng số | Điểm | Cơ sở/loại | Confidence | Phản biện tự rà soát |
|---|---:|---:|---|---|---|
| Mức độ vấn đề | 20% | 7 | CLM-009, INFERENCE: có thể mất cơ hội chứng minh | LOW: chưa có case thật | Thua vì bản chất vụ việc |
| Bằng chứng nhu cầu | 15% | UNKNOWN | CLM-016 | LOW | Chưa biết số case và budget |
| Khác biệt | 15% | 4 | CLM-007–008, INFERENCE: công cụ đã có nhiều phần | LOW về lợi thế; HIGH về công bố đối thủ | Dohana/MISA + SOP đủ |
| Phân phối | 15% | UNKNOWN | CLM-017 | LOW | Agency chưa đồng ý phân phối |
| Khả thi nhóm nhỏ | 10% | 7 | CLM-019, HYPOTHESIS: một sàn, file tự cung cấp | LOW | Video và lệch mã đơn tăng support |
| Kiếm tiền | 10% | UNKNOWN | CLM-016 | LOW | Case hiếm và công cụ miễn phí |
| Pháp lý/dữ liệu | 5% | UNKNOWN | CLM-018 | LOW | Thông tin người mua, quyền dùng chứng cứ |
| Phòng thủ dài hạn | 5% | 2 | CLM-020, HYPOTHESIS | LOW | Bundled feature dễ thay thế |
| Phù hợp MVP gọn | 5% | 8 | CLM-019, HYPOTHESIS: packet checklist một tình huống | LOW | Phân loại nhiều policy dễ nở phạm vi |

### IDEA-0008 r2

| Tiêu chí | Trọng số | Điểm | Cơ sở/loại | Confidence | Phản biện tự rà soát |
|---|---:|---:|---|---|---|
| Mức độ vấn đề | 20% | 6 | CLM-014, INFERENCE: archive có thể không dùng được | LOW: mức thiệt hại target chưa đo | Giữ account thêm có thể rẻ hơn |
| Bằng chứng nhu cầu | 15% | UNKNOWN | CLM-011, CLM-016; người đăng không phải bằng chứng agency mua | LOW | Nhu cầu một lần hoặc đã chọn backup |
| Khác biệt | 15% | 3 | CLM-012–013, INFERENCE: report/coverage đã có | LOW về lợi thế; HIGH về công bố đối thủ | Acceptance checklist tay đủ |
| Phân phối | 15% | UNKNOWN | CLM-017 | LOW | Chưa có agency channel |
| Khả thi nhóm nhỏ | 10% | 6 | CLM-019, HYPOTHESIS: một export format | LOW | Thiếu baseline làm kết luận không chắc |
| Kiếm tiền | 10% | UNKNOWN | CLM-016 | LOW | Phí theo lần khó tạo doanh thu lặp |
| Pháp lý/dữ liệu | 5% | UNKNOWN | CLM-018 | LOW | Quyền bàn giao và lưu trữ từng khách |
| Phòng thủ dài hạn | 5% | 3 | CLM-020, HYPOTHESIS | LOW | Bộ tác vụ dễ bị sao chép |
| Phù hợp MVP gọn | 5% | 7 | CLM-019, HYPOTHESIS: đọc/archive một nền tảng | LOW | Mọi format/mọi tác vụ không còn gọn |

| Ý tưởng | Trọng số đã chấm | Evidence coverage | Tổng điểm | Tình trạng |
|---|---:|---:|---|---|
| IDEA-0001 r2 LotDelta | 55% | 35% | NOT RANKED | Exploratory, chưa đủ commercial comparison |
| IDEA-0002 r2 ClaimReady | 55% | 35% | NOT RANKED | Exploratory, chưa đủ commercial comparison |
| IDEA-0008 r2 ExitDrill | 55% | 35% | NOT RANKED | Exploratory, chưa đủ commercial comparison |

Evidence coverage 35% = 20% severity + 15% differentiation có nguồn để suy luận; không phải 35% khách hàng hoặc 35% cơ hội được xác thực. Ba tiêu chí mang điểm HYPOTHESIS cộng 20% assessed weight nhưng không tăng coverage. 45% còn UNKNOWN gồm demand 15, distribution 15, monetization 10, legal/data 5. Không có tổng điểm hoặc ranking trá hình từ phần đã chấm. Điểm khác biệt thấp phản ánh cạnh tranh, không phải đánh giá chất lượng UI.

Độ nhạy: demand và distribution chiếm 30% và có thể đảo mọi thứ tự. Việc một agency/shop cung cấp dữ liệu và ngân sách thật sẽ có giá trị quyết định hơn chênh 1 điểm feasibility. Nếu điểm áp dụng revision đã được ERP giải quyết, nếu đủ chứng cứ không tạo thêm lợi ích ở shop, hoặc nếu backup report đã đáp ứng nhiệm vụ archive, luận điểm chính của ý tưởng tương ứng sụp đổ. Không điểm tổng nào bù được dữ liệu không có quyền dùng.

## Bảng so sánh và điểm dừng

| Hướng | Job có thể đo | Khác biệt cần kiểm chứng | Rào cản thương mại lớn | Rào cản kỹ thuật/vận hành lớn | Điều cần biết trước |
|---|---|---|---|---|---|
| LotDelta | Chốt revision và giảm rework đúng nguyên nhân | Điểm chuyển theo lô/tồn, nhiều buyer | Buyer/supplier chịu đổi quy trình? | Mapping revision–PO–WIP và ngoại lệ file | Có đủ ca đau ngoài khả năng SOP/ERP? |
| ClaimReady | Chuẩn bị chứng cứ đúng thời điểm | Readiness tại kho, bàn giao CSKH | Đã mua công cụ khác; case ít | Video, mã đơn, rule version và support | Thiếu chứng cứ thực sự gây mất giá trị bao nhiêu? |
| ExitDrill | Người nhận tìm/đọc được dữ liệu quan trọng | Nghiệm thu theo tác vụ với archive độc lập | Job từng đợt; report backup sẵn có | Baseline bị thiếu, format drift, an tâm sai | Kiểm chứng độc lập có tạo lợi ích thêm? |

**Kết luận tư vấn sơ bộ:** ba giả thuyết đáng đưa tới dữ liệu khách hàng, nhưng chưa có đề cử thương mại đủ chứng cứ và chưa có hội đồng hoàn thành. Không chọn người thắng. Ưu tiên bước nghiên cứu theo nơi Founder có thể tiếp cận dữ liệu thật hợp pháp, chưa biết nơi nào hiện thuận lợi nhất.

**Founder Decision Gate:** Founder có thể chỉ định IDEA-ID + EXPLORE / CHALLENGE / REFINE / PARK / REJECT / SELECT, kèm phạm vi nếu muốn. Chưa có quyết định nào được ghi. SELECT chỉ ghi nhận ưu tiên, không mở implementation. Không tự chạy experiment hoặc tạo nhiệm vụ theo dõi tiếp.

Để tiếp tục thành council thật cần công cụ spawn và follow-up/nhận kết quả callable. Phần còn thiếu: Round 1 độc lập (inventor không nhận các ứng viên trong hồ sơ này nếu muốn khám phá độc lập), đánh giá product/technical thực tế, ít nhất một critique→response cho mỗi ứng viên, Red Team riêng và phản hồi, rồi chấm lại. Không gán các ghi chú CIO thành thông điệp của sáu role. Nếu Founder chỉ chọn một hướng, phạm vi nghiên cứu tiếp theo theo đúng chỉ định của Founder.

## Kiểm tra hồ sơ đã thực hiện

2026-11-20: kiểm tra bằng Python standard library, chỉ đọc các Markdown, kết quả PASS. Đã kiểm tra source/claim IDs liên tục, tám idea IDs duy nhất, ba scorecard mỗi bảng đủ chín tiêu chí/tổng trọng số 100%, assessed weight 55% và UNKNOWN 45%, số cột các bảng Markdown, liên kết nội bộ tồn tại, trạng thái blocked và decision log chưa có dòng quyết định Founder. Đây là kiểm tra nhất quán tài liệu, không xác minh nhu cầu thị trường, chức năng sản phẩm, tích hợp hoặc review độc lập. Không chạy product tests vì không thay đổi sản phẩm.
