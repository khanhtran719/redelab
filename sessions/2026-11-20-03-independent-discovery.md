# SES-20261120-03 — Independent DISCOVER council

Status: AWAITING_FOUNDER

Started: 2026-11-20T15:12:36+07:00 (first successful spawn). Reserved: 2026-11-20T15:12:53.037511+07:00

Objective: broad software opportunity discovery for Vietnam, SEA and international markets; solo/small team; research/advisory only. No implementation.

Budget: 30 minutes elapsed, 12 queries, 20 inspected external sources across participants, at most 8 concepts; one peer critique-response and one Red Team-response cycle for each shortlisted concept. Token/cost UNKNOWN.

Existing IDs IDEA-0001–0008 inspected; no Founder decisions. Prior session remains BLOCKED_MULTI_AGENT; new discovery is independent.

Reservation base hashes:
```json
{
  "portfolio/idea-backlog.md": "b935f3e1a8e75d0d5fe5f7ae680163399596b2babd85ff907164889341a831fc",
  "portfolio/decision-log.md": "2dbfbbd350e9c52f109b4e66dae754b220944a97f56aa0a6b17131c77d37513b",
  "sessions/README.md": "fdd600f24e6f3a74e44368bf9cadae28dbf4fd304d62100bc04d2de9be2699ee"
}
```

Reservation publication at 15:12:53 +07:00: file reserved exclusively; index addition only. No backlog or Founder decisions changed at that time.

---

Trạng thái công bố: **AWAITING_FOUNDER**. Ngày nghiên cứu: 20/11/2026, Asia/Ho_Chi_Minh. Bản cơ chế cuối: **r3**, sau phản hồi R5. Tên sản phẩm là tên làm việc, chưa kiểm tra nhãn hiệu.

Hội đồng giữ **hai hướng khám phá có điều kiện: ClassRelay và GuideExpiry**. Chưa có ứng viên đủ điều kiện xếp hạng thương mại. Bảy cơ chế được tạo độc lập, bốn được phản biện và nhận phản hồi đầy đủ. Không bổ sung ý tưởng yếu để đạt chỉ tiêu 3–5. Đây là kết quả sàng lọc, không phải xác nhận nhu cầu thị trường, tính mới toàn cầu hay quyết định sản phẩm.

## Phạm vi, giới hạn và ngân sách

Mục tiêu: cơ hội phần mềm cho Việt Nam, SEA hoặc quốc tế, phù hợp solo developer/nhóm nhỏ, dữ liệu và vận hành ban đầu khả thi. Không giới hạn theo ngành hoặc ý tưởng cũ. Các nguồn cho ClassRelay/GuideExpiry chủ yếu quốc tế; tính chuyển giao sang Việt Nam/SEA là UNKNOWN. Không có phỏng vấn, dữ liệu khách hàng riêng, cam kết mua, chạy sản phẩm đối thủ hoặc thử nghiệm người dùng.

Ngân sách nghiên cứu: 30 phút từ lần spawn đầu tiên, 12 truy vấn, 20 nguồn được mở, tối đa tám cơ chế. Thực tế: **12 truy vấn thành công, 17 nguồn được mở, bảy cơ chế**; tất cả nguồn do CIO thu thập. Bắt đầu worker 15:12:36.916; phản hồi nghiên cứu cuối 15:30:26.558 (+07:00), khoảng **17 phút 50 giây**. Thời gian tổng hợp, bàn giao và công bố được ghi riêng trong audit, không khởi động lại ngân sách. Dừng tìm kiếm vì đã chạm trần truy vấn và phản biện không cần nguồn mới. Token/chi phí UNKNOWN.

Lỗi route của web ban đầu xảy ra trước khi nhận kết quả; bốn truy vấn được thử lại thành công qua connected search service. Đếm 12 truy vấn thành công, đồng thời công khai bốn lượt yêu cầu thất bại, không coi là thêm bốn kết quả nghiên cứu. Bộ nguồn là khảo sát hẹp bằng tiếng Anh và một truy vấn tiếng Việt, không phải bao phủ thị trường.

## Năng lực và sự tham gia thực tế

MCP Agent Hub đã được gọi thật qua `hub_status`, `session_open`, `agent_spawn`, `agent_wait`. Group: `5756c7cf-a422-419a-a77c-4b274c8198b6`. Runtime báo `gpt-6-astra`, `ultra`, `read-only`, `codex-app-server`; đây là cấu hình runtime được trả về, không phải metadata model riêng của từng job. Role TOML kế thừa cấu hình. Không áp dụng override model. Không có native spawn hoặc công cụ follow-up cùng worker trong inventory sử dụng.

CIO chuyển nguyên văn/trích đoạn có quy nguồn hoặc tóm tắt trung thành cho **worker thay thế có danh tính mới**. Không gọi các phản hồi thay thế là cùng một người hoặc phát minh độc lập. Các receipt giữ prompt thực gửi, job/thread ID, thời điểm gửi/kết thúc và output. Hub không trả message ID riêng; job ID là định danh tác vụ, không được giả làm message ID.

| Mã vai trò/lượt | Job ID | Kết quả / giới hạn |
|---|---|---|
| C1 — customer-researcher R1 | 3d0e370a-7cc4-45aa-9be9-743cd0ad40f2 | Hoàn thành bốn giả thuyết vấn đề; không duyệt web |
| M1 — market-analyst R1 | 3f414fb0-5a80-43d6-973a-b8e73e18457a | Hoàn thành năm giả thuyết quy trình; đầu mối nhà cung cấp chưa kiểm chứng |
| I1 — creative-inventor R1 | 58853777-9f36-42ec-9e78-ea2dd05a218f | Bảy cơ chế độc lập, chưa xem giải pháp của C1/M1 hoặc backlog |
| P2 — product-strategist R2 | 839684bc-ef88-4b3e-a8c7-2a31a884179d | Phản biện thương mại bốn ứng viên |
| T2 — technical-advisor R2 | ccf1c4f3-c629-414d-9ca7-ce7a035e4643 | Phản biện khả thi bốn ứng viên |
| M2 — market R2 bổ sung | 37ca4b41-efd4-47ba-a458-25626883cd6d | FAILED 429; không có phản biện |
| I3a — inventor R3 lần đầu | 132261d7-c1db-4555-9718-98250acf79d2 | FAILED 429; không có phản hồi |
| C3 — customer R3 bổ sung | 830298b7-76f0-42e3-ab93-3c4120534140 | FAILED 429; không có review bổ sung |
| I3 — inventor R3 thay thế duy nhất | 2efbea3d-451c-41d1-b982-3a980c5b2342 | Trả lời đích danh cả P2 và T2 cho bốn ứng viên |
| R4 — red-team-critic | 4c211ab5-572d-4b74-b21c-a8eb10e9b442 | Phản biện độc lập gói bằng chứng/r2; không tự duyệt web |
| I5 — inventor R5 thay thế | 9f68563d-0fbe-49b9-9f2b-57c75dd3bc91 | Trả lời bốn phản biện R4; đóng băng r3 |

Tổng cộng **tám job hoàn thành, ba job thất bại**, sáu vai trò có đầu ra thực. Hai dispatch R2 quá lớn bị từ chối trước khi tạo worker; gửi lại gói ngắn thành công. Các job lỗi không được tính là phiếu phản biện. Worker R1 không đọc được tệp vì sandbox, không có web; họ chỉ tạo giả thuyết dựa trên brief. CIO đã đọc hướng dẫn; R2 trở đi được cung cấp role/skill/policy inline. Do vậy, đã có sáng tạo và phản biện độc lập nhưng **chưa có thu thập nguồn độc lập bởi từng chuyên gia hoặc customer discovery thực địa**. Nguồn chung tạo giới hạn tương quan trong đánh giá.

Skills CIO đã dùng: expert-orchestration cùng roster; bảy project skills problem-discovery, market-intelligence, creative-ideation, product-opportunity, feasibility-assessment, adversarial-review, idea-evaluation. Các role ở `.codex/agents/` được truyền nội dung thực; không tuyên bố worker R1 đã đọc thành công các skill. Chi tiết [runtime](2026-11-20-03-runtime.json), [job audit](2026-11-20-03-hub-before-close.json).

## Nguồn, luận điểm và khám phá ban đầu

[Sổ nguồn và 12 truy vấn](2026-11-20-03-research-receipts.json) ghi 17 nguồn SRC-001–017, URL, ngày xuất bản nếu biết, ngày truy cập 20/11/2026, loại nguồn và giới hạn. [Sổ luận điểm](2026-11-20-03-claims.json) ghi CLM-001–014, lớp bằng chứng, suy luận/đối chứng và độ tin cậy. Đây là hai phần của hồ sơ phiên, không phải danh sách nguồn chưa đọc. Snapshot evidence-v1/v2/v3 là lịch sử; ledger research-receipts là bản đã sửa mới nhất.

**VERIFIED** chỉ cho phát biểu hẹp được nguồn hỗ trợ; **INFERENCE** là suy luận có truy vết; **HYPOTHESIS** là giả thuyết; **UNKNOWN** là khoảng trống. Trang vendor xác nhận công bố tính năng, không chứng minh hiệu quả, nhu cầu hoặc WTP. SRC-004/013 cùng Claimlane, không phải hai xác nhận độc lập. SRC-003 là trường sử dụng Opus1. Không có đối thủ được tìm thấy không đồng nghĩa độc quyền hoặc mới toàn cầu.

| Phát hiện vật chất | Bằng chứng / giới hạn |
|---|---|
| ChangeReceipt chồng lấn đáng kể | INFERENCE CLM-001 từ Clearstory SRC-001 và Faceworks SRC-014; chưa chạy sản phẩm |
| Trường nhạc có tổ chức đổi suất | VERIFIED CLM-003 từ chính sách SRC-003/015/017; mẫu chọn lọc ngoài VN, SRC-015 cũ; Prelude chỉ đổi dài hạn |
| Công cụ hiện hữu có học bù/tự đặt lịch và quảng bá đổi suất | VERIFIED CLM-004, Opus1 SRC-002 và Stundenplan-berechnen SRC-016; hỗ trợ chu trình ba suất đang kín UNKNOWN |
| Claimlane mô tả xử lý phụ tùng và nhận diện mã bộ phận | VERIFIED CLM-006, SRC-004/013; không xác lập kinh tế của cửa hàng nhỏ |
| Có báo cáo hướng dẫn hỏng vì API/config thay đổi | VERIFIED CLM-008, Godot SRC-010 và Besu SRC-011; hai issue được chọn, một issue đã đóng, không tái hiện |
| GuideExpiry có thay thế gần | INFERENCE CLM-009 từ Swimm SRC-006, ghim phiên bản SRC-011 và ABP validator SRC-012; chưa đối chứng thực thi |
| WTP, kênh bán và quyền dữ liệu chưa được xác nhận | UNKNOWN CLM-011/013 cho cả bốn ứng viên |

Đầu ra R1 được giữ nguyên trong [r1-results](2026-11-20-03-r1-results.json), trước tổng hợp. C1 nêu đối soát tiền bán hàng, thu hồi quyền cộng tác viên, hồ sơ nghiệm thu và ca tái hiện lỗi; tất cả HYPOTHESIS. M1 khảo sát giả thuyết thuê thiết bị, hiệu chuẩn, duyệt artwork, đối soát và thu thập hồ sơ; các tên vendor là đầu mối chưa xác minh và không được nâng thành nguồn. I1 tạo bảy hướng dưới đây. Không coi sự trùng ý giữa C1/M1/I1 là xác nhận nhu cầu.

## Danh mục bảy cơ chế và các sửa đổi

| Gốc / ID | Khách hàng, vấn đề và cơ chế HYPOTHESIS | Sàng lọc / trạng thái cuối |
|---|---|---|
| R1-I-01 / IDEA-0009 — ChangeReceipt r3 | Nhà thầu nội thất/gian hàng VN: xác nhận phạm vi, giá và thẩm quyền trước thi công để giảm tranh chấp | Phản biện đầy đủ; khác biệt yếu trước Clearstory/Faceworks; không vào hai hướng giữ lại |
| R1-I-02 — chưa cấp ID portfolio | Xưởng may VN/SEA: duyệt trước phạm vi thay vật tư theo thuộc tính, chỉ hỏi ngoại lệ; đo giờ chờ/làm lại | SRC-008 chỉ là hướng dẫn supplier ngành giày, bằng chứng yếu; gần lãnh địa LotDelta IDEA-0001 nhưng khác quyết định. Chưa đủ để nhập chung hoặc mở ID mới; chưa debate |
| R1-I-03 / IDEA-0010 — ClassRelay r3 | Trung tâm nhạc/ngôn ngữ: đổi chỗ trống → cặp → chu trình tối đa ba suất; đo ca hoàn tất tăng thêm và tổng phút điều phối | Giữ khám phá có điều kiện; từ lịch khả thi chuyển sang hoàn tất với đồng thuận thật |
| R1-I-04 / IDEA-0011 — PartRoute r3 | Nhà bán nội thất lắp ráp: chuyên gia xác định bộ phận, khách tự chọn nhận phụ tùng trước hoàn hàng; đo tổng chi phí giải quyết | Phản biện đầy đủ; Claimlane trùng mạnh, vận hành quyết định giá trị; không vào hai hướng giữ lại |
| R1-I-05 / IDEA-0012 — GuideExpiry r3 | Nhóm phần mềm nhỏ: gắn hướng dẫn với bằng chứng, thay đổi liên quan làm mất xác nhận; chủ tài liệu kiểm tra lại | Giữ khám phá có điều kiện; phụ thuộc chưa biết luôn là chưa xác minh |
| R1-I-06 — chưa cấp ID portfolio | Đơn vị du lịch nhóm SEA: thu điều kiện phủ quyết trước sở thích để giảm vòng sửa lịch trình | SRC-009 Claira có nội dung sát về ngân sách/dealbreakers; mới là index vendor; chưa xác lập khoảng trống hoặc debate |
| R1-I-07 — chưa cấp ID portfolio | Công ty nghiên cứu nhỏ: ưu tiên xác minh bản ghi bất đồng, giữ mẫu ngẫu nhiên; đo công mỗi lỗi và lỗi bỏ sót | SRC-007 SurveyCTO có kiểm tra chất lượng/back-check; khác biệt chưa rõ, chưa debate |

R1 là bản gốc; r2 là phạm vi sau P2/T2 và trả lời I3; r3 là bản cuối sau R4/I5. Không ghi Founder REJECT/PARK thay cho kết luận sàng lọc của CIO. Các gợi ý vấn đề C1/M1 không tính thêm vào bảy concept của I1.

## Trao đổi thực tế và bất đồng

Bảng dưới là **diễn giải trung thành của CIO**, không phải hội thoại giả hoặc trích nguyên văn. Mã vai trò ánh xạ tới job ID ở trên. [Exchange ledger](2026-11-20-03-exchanges.json) lưu từng nguồn, đích, finding ID, thời gian, payload và đường dẫn trả lời. `RESPONDED` chỉ dùng khi output thực trả lời đích danh phản biện; cả tám chu trình dưới hoàn tất.

| Exchange / ứng viên | Luồng trao đổi | Phản biện → phản hồi và thay đổi | Còn bất đồng / điều kiện bác bỏ |
|---|---|---|---|
| EX-P-01 / ChangeReceipt | I1 → P2,T2 → I3 | R2-P/T-01: trùng vendor, thiếu quyền/ý chí xác nhận. R3-I-01 thừa nhận; r2 thu hẹp một nghề và không giữ luận cứ khác biệt | Mẫu + chat có thể đủ; cần xác nhận đến trước việc làm và tiền thực thu sau công theo đuổi |
| EX-P-03 / ClassRelay | I1 → P2,T2 → I3 | R2-P/T-03: ít vòng tương thích, lịch cũ, không suy ra đồng ý từ lịch sử. R3-I-03 giữ một trung tâm, chỗ trống/cặp trước, vòng tối đa ba | Lợi ích tăng thêm sau công điều phối UNKNOWN; đối thủ có chu trình ba bên UNKNOWN |
| EX-P-04 / PartRoute | I1 → P2,T2 → I3 | R2-P/T-04: Claimlane và hậu mãi hiện có, thiếu tồn phụ tùng/khả năng phục vụ. R3-I-04 thừa nhận nhận diện bộ phận không còn là luận cứ khác biệt | Product Strategist vẫn thích nghiên cứu kinh tế hồi cứu; Inventor không giữ sản phẩm khác biệt |
| EX-P-05 / GuideExpiry | I1 → P2,T2 → I3 | R2-P/T-05: Swimm/ABP/pinning thay thế; liên kết thiếu gây bỏ sót. R3-I-05 giữ thử hẹp, trạng thái chưa xác minh khi thiếu liên kết | Chi phí bảo trì có thể lớn hơn rà toàn bộ; chưa có lợi thế hoặc WTP |
| EX-R-01 / ChangeReceipt | I3 → R4 → I5 | R4-R-01: cạnh tranh không đủ phủ định thị trường; người thiệt không kiểm soát người duyệt. R5-I-01 thừa nhận và giữ không đề xuất shortlist khác biệt | R4 để mở cơ hội phục vụ phân khúc; I5 yêu cầu bằng chứng lợi thế trước khi giữ |
| EX-R-03 / ClassRelay | I3 → R4 → I5 | R4-R-03: chu trình khả thi không bằng đổi thực; nguồn Prelude không chứng minh đổi hàng tuần. R5-I-03 chuyển thước đo sang ca hoàn tất, tách tạm thời/dài hạn | Đủ mật độ, đồng thuận lặp lại và tổng công dưới trần trung tâm vẫn UNKNOWN |
| EX-R-04 / PartRoute | I3 → R4 → I5 | R4-R-04: giao lại/lắp đặt xóa tiết kiệm; ngưỡng 6/20 và 20% không có căn cứ. R5-I-04 rút các ngưỡng này | 20 hồ sơ chỉ giúp tìm lỗi giả định; phản thực không chứng minh tiết kiệm thực hoặc WTP |
| EX-R-05 / GuideExpiry | I3 → R4 → I5 | R4-R-05: hai issue không chứng minh phổ biến; cảnh báo tất cả xóa tiết kiệm. R5-I-05 giữ đối chứng rà đầy đủ độc lập và tính toàn bộ công | Hai release chỉ sàng lọc; không khẳng định độ tin cậy dài hạn |

Receipt theo giai đoạn: [R2](2026-11-20-03-r2-results.json), [R3 thay thế](2026-11-20-03-r3-retry-result.json), [Red Team](2026-11-20-03-red-result.json), [R5](2026-11-20-03-r5-result.json). Prompt thực được giữ cả trong result và các tệp dispatch. R4 nói tại thời điểm trả lời rằng chưa nhận phản hồi; receipt R5 sau đó hoàn tất chu trình, không sửa lịch sử R4.

Bất đồng chính là **ưu tiên học**, không phải bỏ phiếu chọn sản phẩm. P2 đề nghị học kinh tế PartRoute vì giá trị dễ quy tiền; I3/I5 không thấy luận cứ sản phẩm khác biệt còn đứng vững; R4 chưa thấy lý do ưu tiên sản phẩm mới. Với ChangeReceipt, R4 phản đối việc loại chỉ vì có đối thủ, còn I5 đồng ý giữ thị trường là câu hỏi mở nhưng không đưa vào shortlist hiện tại. T2 chỉ xác nhận luồng hẹp khả thi có điều kiện, không xác nhận lợi nhuận hay cấp phép triển khai. M2/C3 thất bại không có quan điểm cuối để gán.

## Hai hướng giữ lại

### IDEA-0010 — ClassRelay r3

**Pitch — HYPOTHESIS:** giúp trung tâm hoàn tất những ca đổi suất mà chỗ trống và đổi đôi bỏ sót, bằng chu trình tối đa ba suất có đồng thuận.

**Khách hàng/vấn đề:** chủ và điều phối viên một trung tâm nhạc có lịch cá nhân; trung tâm ngoại ngữ là mở rộng chưa kiểm chứng. Học viên muốn đổi lịch nhưng suất phù hợp đã kín. Phân khúc VN/SEA hay quốc tế cụ thể chưa được chọn; bằng chứng hiện chủ yếu trường nhạc quốc tế. Người mua giả định là chủ trung tâm; học viên/giáo viên hưởng lợi. CLM-003/005/011.

**Workflow đề xuất:** nhận lịch được phép sử dụng và yêu cầu → kiểm tra tương thích giáo viên/trình độ/chính sách → giải quyết chỗ trống, sau đó đổi đôi, cuối cùng vòng tối đa ba → lấy đủ đồng thuận → kiểm tra lịch hiện hành → điều phối viên cập nhật lịch chính. Một người rút lui thì không chốt vòng. Dữ liệu lịch sử chỉ chứng minh khả thi toán học.

**Đối thủ/thay thế — VERIFIED ở mức công bố:** [Opus1](https://kb.opus1.io/how-do-i-set-up-makeup-lessons) có credit học bù/tự đặt lịch (SRC-002). [Stundenplan-berechnen](https://www.stundenplan-berechnen.de/en/home-en/) quảng bá đổi suất nhưng diễn đạt chi tiết không nhất quán; chu trình ba suất đang kín UNKNOWN (SRC-016). [Prelude](https://www.preludestudio.com/student/parentresources) dùng form/danh sách/điều phối cho đổi dài hạn, không phải hàng tuần (SRC-017). Bảng lịch và người điều phối là đối chứng trực tiếp.

**Khác biệt và giá trị — HYPOTHESIS:** chỉ có giá trị nếu thêm được ca **hoàn tất** sau hai bước đơn giản hơn và giảm tổng phút điều phối mỗi ca, không tăng giờ giáo viên hoặc sai lịch. Chưa chứng minh đối thủ thiếu chức năng hoặc khách chịu trả thêm.

**Kinh doanh — HYPOTHESIS:** phí tháng/cơ sở; tiếp cận qua người tư vấn vận hành trung tâm như P2 đề xuất. Chưa xác minh kênh, giá, ngân sách hoặc conversion. Giữ khách cần lượng yêu cầu đều; vendor lịch dễ thêm tính năng, lợi thế phòng thủ yếu.

**Độ khó MVP — INFERENCE, trung bình:** phạm vi một trung tâm, lịch nhập thủ công/CSV và người điều phối chốt có thể giới hạn phụ thuộc nền tảng (R2-T-03). Không có ước lượng sprint/chi phí triển khai hoặc chứng minh export được; API không được mặc định. Công cập nhật lịch, chờ trả lời, rút lui và xử lý sai là rủi ro chính, không chỉ việc tìm chu trình.

**Bằng chứng:** chính sách [Omaha Conservatory](https://omahacm.org/wp-content/uploads/2025/05/FAQs-about-the-2025-26-Academic-Year-1.pdf) xác nhận thực hành đổi suất (SRC-003), không xác nhận nhu cầu mua. Độ tin cậy thương mại LOW; demand tại VN, mật độ ca, WTP, phân phối và quyền dữ liệu UNKNOWN. Lịch có thể chứa dữ liệu trẻ em; quyền sử dụng và sự đồng ý phù hợp chưa được xác nhận (CLM-013), không kết luận pháp lý.

**Vị trí agent/lý do giữ:** I3/I5 và R4 giữ câu hỏi hẹp vì cơ chế có thể giải ca mà đổi đôi bỏ sót. P2 phản đối lợi ích gia tăng và phòng thủ chưa rõ; T2 phản đối lịch cũ/đồng thuận. CIO giữ vì có hành vi đổi lịch thật và phép bác bỏ trực tiếp; không tuyên bố cơ hội thương mại được ủng hộ nhất trí.

**Kiểm chứng tiếp, chưa thực hiện:** nếu Founder chọn hướng này và có quyền dữ liệu, lấy toàn bộ yêu cầu liên tiếp bốn tuần, tách tạm thời/dài hạn; thực hiện thủ công theo chỗ trống → cặp → vòng. Ghi ca tăng thêm hoàn tất, rút lui, đồng thuận và toàn bộ công lấy/làm sạch dữ liệu, liên hệ, kiểm tra, cập nhật. Ngưỡng sàng lọc do I5 đề xuất: ca tăng thêm ở ít nhất hai tuần và công/ca dưới trần thống nhất trước với trung tâm. Đây là phán đoán, không benchmark; ít yêu cầu là chưa kết luận. Nếu cơ chế không thắng quy trình đơn giản, không có lý do xây thêm. Sau đó vẫn cần xác minh người trả tiền và lựa chọn có giá cụ thể.

### IDEA-0012 — GuideExpiry r3

**Pitch — HYPOTHESIS:** giúp nhóm phần mềm biết hướng dẫn nào cần kiểm tra lại khi UI/cấu hình thay đổi, dựa trên bằng chứng xác minh còn hiệu lực.

**Khách hàng/vấn đề:** nhóm phần mềm nhỏ có hướng dẫn thao tác/setup hay thay đổi; người dùng là người duy trì tài liệu, người mua giả định là trưởng kỹ thuật. Hướng dẫn còn mở được nhưng các bước đã sai. Quốc tế là giả thuyết thị trường đầu; chưa xác lập ngành, tần suất hay mức thiệt hại tại VN/SEA. CLM-008/010/011.

**Workflow đề xuất:** chọn nhóm hướng dẫn → liên kết thủ công với phần UI/config và bằng chứng lần kiểm tra → khi thay đổi liên quan, chuyển sang cần xác minh → chủ tài liệu chạy lại các bước và lưu bằng chứng/phiên bản. Liên kết chưa biết luôn là chưa xác minh; không suy ra “an toàn” từ việc không có cảnh báo.

**Đối thủ/thay thế:** [Swimm Auto-sync](https://swimm.io/blog/how-does-swimm-s-auto-sync-feature-work) mô tả theo dõi mã/liên kết và yêu cầu review (SRC-006); [ABP AI Tutorial Validator](https://github.com/abpframework/ai-tutorial-validator) mô tả chạy từng bước tutorial (SRC-012). Ghim phiên bản, checklist định kỳ và rà toàn bộ là đối chứng. Chưa chạy hai công cụ hoặc xác minh quyền sử dụng hiện tại; không khẳng định công cụ thiếu tính năng.

**Khác biệt và giá trị — HYPOTHESIS:** tập trung vào bằng chứng hết hiệu lực do UI/config để giảm tổng giờ rà soát, vẫn phát hiện lỗi nghiêm trọng; ưu thế chỉ có ý nghĩa nếu vượt công thiết lập và bảo trì phụ thuộc. “Tài liệu tự cập nhật” hoặc “kiểm thử tutorial” tổng quát không còn là luận cứ khác biệt.

**Kinh doanh — HYPOTHESIS:** phí tháng/nhóm, tiếp cận qua cộng đồng người duy trì tài liệu theo P2. Cộng đồng không đồng nghĩa có buyer hoặc kênh bán kinh tế; giá và WTP UNKNOWN. Có thể giữ khách theo nhịp release, nhưng spreadsheet hoặc công cụ mở có thể đủ tốt; chưa thấy lợi thế bền vững.

**Độ khó MVP — INFERENCE, trung bình:** danh mục hẹp với liên kết thủ công và chủ tài liệu kiểm tra lại có biên vận hành rõ (R2-T-05). Phần khó là độ đầy đủ của phụ thuộc, chất lượng bằng chứng và số cảnh báo. Không đề xuất tự hiểu mọi framework hoặc kiến trúc chi tiết; quyền tài liệu/mã/môi trường chưa được cấp. Thiếu liên kết gây bỏ sót; gắn quá rộng buộc rà gần toàn bộ.

**Bằng chứng:** [Godot issue 10020](https://github.com/godotengine/godot-docs/issues/10020) và [Besu issue 1035](https://github.com/besu-eth/besu-docs/issues/1035) xác nhận có báo cáo lỗi hướng dẫn (SRC-010/011); chưa tái hiện, không cho biết tỷ lệ thị trường, một issue đã đóng. Độ tin cậy cơ chế vấn đề MEDIUM, thương mại LOW. Bằng chứng nguồn nhiều hơn không đồng nghĩa khả năng thành công cao hơn.

**Vị trí agent/lý do giữ:** I3/I5 và R4 giữ phép học hẹp. P2 nhấn mạnh Swimm/ABP và quyền truy cập repo; T2 nhấn mạnh liên kết thiếu hoặc rộng quá. CIO giữ vì có lỗi được báo cáo và có thể đối chứng trực tiếp với rà đầy đủ, không phải vì đã chứng minh mới hoặc dễ bán.

**Kiểm chứng tiếp, chưa thực hiện:** với quyền dữ liệu và hai người tham gia, chọn trước toàn bộ nhóm hướng dẫn qua hai release có thay đổi UI/config liên quan. Một người duy trì bằng chứng; người khác rà đầy đủ độc lập, chưa xem cờ cảnh báo. Tính tổng công thiết lập, bảo trì, xác minh và lỗi nghiêm trọng bỏ sót. Ngưỡng sàng lọc đề xuất: không bỏ sót lỗi nghiêm trọng mà đối chứng phát hiện và tổng công thấp hơn; vi phạm thì dừng giả thuyết. Hai release không chứng minh độ tin cậy lâu dài, không có thay đổi liên quan thì chưa kết luận; cần kiểm tra lợi ích so với công cụ hiện có và hành vi trả tiền sau đó.

## Hai ứng viên đã đánh giá sâu nhưng không giữ trong shortlist

**IDEA-0009 — ChangeReceipt r3.** Pitch giả thuyết: thu đủ tiền phát sinh nhờ xác nhận đúng phạm vi/giá trước khi làm. Buyer giả định là chủ nhà thầu nội thất/gian hàng nhỏ VN; luồng yêu cầu → tác động giá/thời gian → người có thẩm quyền xác nhận phiên bản → đối soát. [Clearstory](https://www.clearstory.build/subcontractor-software) và [Faceworks](https://faceworks.vn/chi-tiet/phan-mem-phe-duyet-phat-sinh-xay-dung-faceworks/) công bố luồng gần; mẫu phụ lục + chat là thay thế rẻ. Khác biệt phân khúc và giá trị vượt mẫu UNKNOWN. Phí tháng/doanh nghiệp, kênh kế toán ngành là HYPOTHESIS. MVP hẹp LOW theo T2, nhưng ý chí/thẩm quyền duyệt và công theo đuổi quyết định kết quả. Bằng chứng trùng công bố mạnh, demand yếu; không có kết luận pháp lý về hồ sơ. I3/I5 không đề xuất; R4 giữ khả năng có lợi thế phân khúc chưa chứng minh. Học tiếp nếu Founder muốn: xem liên tiếp mọi phát sinh trong một nghề, cả bị từ chối/bỏ qua, so với mẫu + chat; đo xác nhận đến trước thực hiện, thời gian và tiền thực thu. Không vào shortlist vì chưa thấy khác biệt hữu ích, không phải Founder REJECT.

**IDEA-0011 — PartRoute r3.** Pitch giả thuyết: thay đúng bộ phận để giải quyết lỗi nội thất với tổng chi phí thấp hơn trả cả món. Buyer là chủ cửa hàng/phụ trách hậu mãi; luồng ảnh/mã → kỹ thuật viên → kiểm tồn → khách tự chọn → giao → xác nhận giải quyết, vẫn giữ phương án trả hàng. [Claimlane](https://www.claimlane.com/industry/furniture) và [Product Parts](https://support.claimlane.com/en/articles/16772515-product-parts) mô tả luồng và định danh phụ tùng; checklist + catalog có thể đủ. Giả thuyết phí tháng/cửa hàng, kênh nhà cung cấp phụ tùng chưa kiểm chứng. MVP MEDIUM và phụ thuộc chuyên gia/tồn kho/giao hàng; quyền dùng ảnh, an toàn và quy định thị trường UNKNOWN. I3/I5 và R4 chưa thấy căn cứ sản phẩm mới; P2 ưu tiên nghiên cứu kinh tế hồi cứu vì dễ gắn chi phí. Nếu học tiếp, xét hồ sơ liên tiếp có toàn bộ giao lại/hỗ trợ/lắp đặt/kết quả cuối, so với checklist. Các ngưỡng 6/20 và tiết kiệm 20% được R4 phản biện và I5 rút; không dùng làm chuẩn. Không vào shortlist vì trùng mạnh và lợi ích có thể nằm ở dịch vụ, không ở phần mềm.

## So sánh và chấm điểm

Tất cả là **EXPLORATORY / NOT RANKED**. Scoring do CIO tổng hợp sau R5, không phải điểm đồng thuận của agent. [Scorecards đầy đủ](2026-11-20-03-scorecards.md) và [dữ liệu điểm](2026-11-20-03-scorecards.json) có đủ chín tiêu chí, trọng số, rationale, evidence class, claim/finding, confidence, ý kiến đối lập và khoảng điểm. Trọng số: đau20, cầu15, khác biệt15, phân phối15, kỹ thuật10, kiếm tiền10, pháp lý/dữ liệu5, phòng thủ5, MVP gọn5 =100.

| Ứng viên | Khó MVP (T2) | Khác biệt /10 | Trọng số có điểm | Bao phủ bằng chứng | Tổng thương mại | Kết luận CIO |
|---|---|---:|---:|---:|---|---|
| IDEA-0009 ChangeReceipt | Thấp, có điều kiện | 2 | 55% | 25% | NOT RANKED | Chưa giữ vào hai hướng |
| IDEA-0010 ClassRelay | Trung bình | 5, giả thuyết | 70% | 25% | NOT RANKED | Giữ khám phá có điều kiện |
| IDEA-0011 PartRoute | Trung bình, vận hành nặng | 2 | 55% | 25% | NOT RANKED | Chưa giữ; có bất đồng ưu tiên học |
| IDEA-0012 GuideExpiry | Trung bình | 3 | 70% | 60% | NOT RANKED | Giữ khám phá có điều kiện |

Bao phủ là tổng trọng số có VERIFIED hoặc INFERENCE truy vết được, **không phải tỷ lệ chắc chắn, điểm chất lượng tổng thể hay xác suất thành công**. Trọng số có điểm bao gồm điểm HYPOTHESIS; UNKNOWN không thay bằng 0/5 và không chuẩn hóa lại. Demand 4/10 của ClassRelay/GuideExpiry chỉ phản ánh hành vi/báo cáo vấn đề yếu, không phải nhu cầu trả tiền. Legal/data, distribution và monetization đều UNKNOWN. Kỹ thuật có thể đạt điểm suy luận dù chưa chạy tích hợp; không phải chứng minh triển khai.

Chưa có thứ tự thương mại để đảo. Chỉ riêng phân phối15 + kiếm tiền10 + dữ liệu5 =30% chưa đánh giá; nhu cầu trả tiền và khác biệt cũng chưa chứng minh. ClassRelay mất luận cứ nếu chu trình thêm không hoàn tất; GuideExpiry mất luận cứ nếu công bảo trì không giảm. ChangeReceipt/PartRoute có thể đáng nghiên cứu hơn khi có dữ liệu buyer/kinh tế, dù novelty thấp. Không có blocker chí mạng được chứng minh; sự thiếu bằng chứng về blocker không phải thông qua.

| Hướng / ưu tiên học CIO | Câu hỏi làm đổi đánh giá | Bằng chứng, công và quyền cần | Lý do / điều kiện dừng |
|---|---|---|---|
| ClassRelay — MEDIUM có điều kiện, confidence LOW | Có ca hoàn tất tăng thêm lặp lại và giảm tổng công? | Một trung tâm cho phép; toàn bộ yêu cầu bốn tuần; công thực chưa biết | Phép bác bỏ trực tiếp; dừng nếu không hơn chỗ trống/cặp; ít mẫu là chưa kết luận |
| GuideExpiry — MEDIUM có điều kiện, confidence LOW | Có tiết kiệm tổng công mà không bỏ sót lỗi nghiêm trọng? | Hai người và quyền tài liệu/môi trường; hai release liên quan; công chưa biết | Có đối chứng độc lập; dừng nếu bỏ sót hoặc không tiết kiệm |
| PartRoute — LOW có điều kiện theo CIO; P2 ưu tiên học hơn | Giá trị thuộc phần mềm hay hậu mãi hiện hữu? | Hồ sơ đầy đủ, kỹ thuật viên và chi phí mọi lần giao/hỗ trợ; quyền/effort UNKNOWN | Có thể bác bỏ bằng checklist; không dùng ngưỡng 20% tùy ý |
| ChangeReceipt — LOW có điều kiện, confidence LOW | Xác nhận trước làm và thu tiền tốt hơn mẫu + chat? | Một nghề, hồ sơ cả yêu cầu bị bỏ qua và quyền chia sẻ; effort UNKNOWN | Chỉ tiếp nếu có lợi thế phân khúc; trùng không tự chứng minh thất bại |

Ưu tiên học là nhận định tư vấn có điều kiện, không chuyển trạng thái sang Founder EXPLORE hoặc tự khởi chạy thí nghiệm.

## Founder Decision Gate

**Chưa có quyết định Founder.** Founder có thể chọn `EXPLORE`, `CHALLENGE`, `REFINE`, `PARK`, `REJECT` hoặc `SELECT` theo tên/ID và phạm vi mong muốn, hoặc không chọn hướng nào. Quyết định không bị ràng buộc bởi điểm hay số người ủng hộ.

Phiên dừng ở danh mục tư vấn này. Không có thử nghiệm khách hàng, sản phẩm, prototype, scaffold, UI hoặc kiến trúc triển khai được tạo. `SELECT` chỉ ghi nhận ưu tiên; cần yêu cầu phát triển riêng với phạm vi mới trước mọi triển khai. Backlog là chỉ mục nghiên cứu; Founder decision log không thay đổi. Các phiên cũ và trạng thái BLOCKED_MULTI_AGENT của chúng được giữ nguyên.

Kiểm tra công bố, hash bases, ID được cấp và trạng thái Hub được ghi ở [publication audit](2026-11-20-03-publication.json). Kiểm tra tài liệu chỉ xác nhận tính nhất quán hồ sơ, không xác minh giả thuyết kinh doanh.

## Publication bases and intended changes

Shared-write lock acquired by this session. Base SHA-256 values and proposed allocation, recorded before shared writes:

```json
{
  "hashes": {
    "portfolio/idea-backlog.md": "b935f3e1a8e75d0d5fe5f7ae680163399596b2babd85ff907164889341a831fc",
    "portfolio/decision-log.md": "2dbfbbd350e9c52f109b4e66dae754b220944a97f56aa0a6b17131c77d37513b",
    "sessions/README.md": "b5934677e281fc63a1c2113cfd2d5fba585397e723755899ffc7aa328f3c1ded",
    "sessions/2026-11-20-03-independent-discovery.md": "302479a44b6916aa1ae88d32cbb463932da47e657b9202bf63abec0ba553de90"
  },
  "allocation": {
    "ChangeReceipt": "IDEA-0009",
    "ClassRelay": "IDEA-0010",
    "PartRoute": "IDEA-0011",
    "GuideExpiry": "IDEA-0012"
  },
  "changes": {
    "allocate": {
      "ChangeReceipt": "IDEA-0009",
      "ClassRelay": "IDEA-0010",
      "PartRoute": "IDEA-0011",
      "GuideExpiry": "IDEA-0012"
    },
    "backlog": "Append four r3 exploratory candidates; preserve old rows and Founder NONE",
    "index": "Update only current session to AWAITING_FOUNDER",
    "report": "Complete final synthesis and preserve reservation history",
    "decisionLog": "UNCHANGED"
  }
}
```
