# Customer discovery R1 — Fokus Time

- Session: SES-20261121-01; tác giả: agent `/root/fokus_customer_sol`, vai Customer Discovery Researcher; access date: 2026-11-21.
- Phạm vi độc lập: chưa đọc ứng viên Fokus cũ hay phát hiện của agent khác. Chỉ điều tra vấn đề; không đề xuất hay xếp hạng giải pháp. Không phỏng vấn, không liên hệ khách hàng.
- Đọc: AGENTS.md, `.agents/skills/problem-discovery/SKILL.md`, `protocols/evidence-policy.md`.
- Ngân sách đã dùng: **3 search queries; 4 nguồn được open và kiểm tra**. Có 4 thao tác find trên chính các nguồn đã mở; không bổ sung nguồn. Dừng theo ngân sách. Nguồn Reddit có selection bias, danh tính/hoàn cảnh không xác thực; không thể ước lượng tỷ lệ dân số.

## Nhật ký tìm kiếm

Ngày 2026-11-21; ngôn ngữ Anh/Việt; web search, ưu tiên primary behavioral research và public discussion:

1. `site.ics.uci.edu Gloria Mark interrupted work stress faster pdf`
2. `site.reddit.com/r/productivity pomodoro timer stopped using developer student distractions`
3. `site.reddit.com/r/VietNam học tập tập trung điện thoại pomodoro`

Query 3 trả về r/vozforums: đó là tín hiệu thảo luận **tiếng Việt**, không tự chứng minh nơi cư trú hay đại diện thị trường Việt Nam. Không coi các search snippets chưa mở là bằng chứng.

## Source ledger

| ID | Nguồn và URL | Ngày xuất bản/sự kiện | Vị trí đã kiểm tra, nội dung và giới hạn |
|---|---|---|---|
| C-S1 | Mark, Gudith, Klocke, *The Cost of Interrupted Work: More Speed and Stress*, [PDF UCI](https://ics.uci.edu/~gmark/chi08-mark.pdf) | Theo file CHI08; ngày chính xác không hiện trong phần văn bản đọc được: UNKNOWN | Primary experiment, pp.2–4 / lines 98–197, 198–435. 48 người, 81% sinh viên Đức, mô phỏng xử lý email; ngắt quãng qua điện thoại/IM. Tác vụ bị ngắt hoàn thành nhanh hơn, không khác biệt lỗi đo được, nhưng stress/effort/frustration cao hơn. Nghiên cứu cũ, lab task; không chứng minh hiệu quả ứng dụng mobile hay tăng năng suất thực địa. |
| C-S2 | [Do you use pomodoro technique when studying? — r/GetStudying](https://www.reddit.com/r/GetStudying/comments/1io4b2c/) | Trang hiển thị “2y ago”; ngày chính xác UNKNOWN | Lines 21–24, 54–62, 87–124. Tự thuật khó bắt đầu/giữ nhịp, giờ nghỉ làm mất đà, điện thoại hẹn giờ kích hoạt mạng xã hội; một bình luận đã chuyển sang timer vật lý. Nhiều phản hồi cùng thread không phải mẫu độc lập đại diện; người đăng tự nghi ADHD không phải chẩn đoán. |
| C-S3 | [Làm sao để tập trung tgian học ở nhà — r/vozforums](https://www.reddit.com/r/vozforums/comments/1fbs4d4/) | Trang hiển thị “2 năm trước”; ngày chính xác UNKNOWN | Lines 19–21, 51–68, 129, 153–189. Người hỏi tự thuật học ở nhà bị cuốn vào máy tính; không thuận tiện ra ngoài do gia đình. Bình luận tự thuật quay timelapse, đặt điện thoại xa, dùng nhịp làm/nghỉ; có người nói 25–50 phút đầu khó nhất. Tiếng Việt, không xác thực địa lý; một thread, có nội dung bị xóa; tách lời khuyên khỏi hành vi đã tự báo cáo. |
| C-S4 | [I ditched Pomodoro and my productivity skyrocketed — r/productivity](https://www.reddit.com/r/productivity/comments/1gct6w0/) | Trang hiển thị “2y ago”; ngày chính xác UNKNOWN | Lines 21–28, 61–81, 98–100, 161. Tự thuật bỏ nhịp nghỉ cố định vì đang tập trung; người khác vẫn dùng timer để bắt đầu việc không thích hoặc dùng đồng hồ cát im lặng. Tiêu đề “skyrocketed” không có phép đo; không dùng phát biểu giới hạn deep work 4h như fact. Nghề của tác giả chưa xác minh. |

Tất cả nguồn được truy cập 2026-11-21. Recency: nghiên cứu cũ và thread khoảng hai năm tuổi; không có dữ liệu hành vi hiện thời 2026 hay mẫu mobile iOS/Android tách biệt.

## Claim ledger / phát hiện ban đầu

| ID | Nhận định và class | Căn cứ/phạm vi | Phản chứng, confidence, điều làm thay đổi kết luận |
|---|---|---|---|
| C1 | **VERIFIED:** Có người học công khai tự thuật việc sử dụng điện thoại làm timer dẫn sang mạng xã hội; có người báo cáo đã chuyển timer vật lý. | C-S2 lines 109–124; self-report, không phải quan sát của bộ phận. | Không biết tần suất/tỷ lệ hay kết quả lâu dài. MEDIUM cho sự tồn tại của pain; LOW cho độ phổ biến. Nhật ký hành vi có thể cho thấy timer chỉ là cái cớ, không phải nguyên nhân. |
| C2 | **VERIFIED:** Trong các thread đã xem, cố định giờ nghỉ có thể làm gián đoạn đà làm việc; một số người tự điều chỉnh hoặc bỏ nhịp cố định. | C-S2 lines 54–99; C-S4 lines 21–28, 61–81. | C-S4 cũng có người thấy timer hữu ích để bắt đầu việc nhàm chán. MEDIUM về tình huống, không về tác động năng suất. Không đồng nhất nhu cầu “bắt đầu” với “duy trì flow”. |
| C3 | **VERIFIED:** Có tín hiệu pain/workaround bằng tiếng Việt: khó học ở nhà, giải trí trên máy tính, dùng môi trường hoặc rào cản vật lý để tự điều chỉnh. | C-S3 lines 19–21, 51–68, 153–189. | Không có xác thực nơi cư trú, đại học/thi cử, chi phí, quy mô nhu cầu. MEDIUM về nội dung tự thuật, LOW cho VN market. |
| C4 | **VERIFIED:** Nghiên cứu email lab tìm thấy chi phí cảm nhận khi ngắt quãng dù thời gian làm tác vụ nhanh hơn. | C-S1; 48 người, đa số sinh viên Đức. | Không hỗ trợ tuyên bố chung “tắt ngắt quãng luôn tiết kiệm X phút” hay “app tăng output”. HIGH cho kết quả hẹp, LOW khi chuyển sang developer/mobile/VN. |
| C5 | **INFERENCE:** Phân khúc theo tình huống “khó bắt đầu” / “đang vào đà” / “phải phản hồi người khác” có thể hữu ích hơn chỉ theo nghề. | C1–C4; cùng timer có thể giúp khởi động và phá nhịp ở người/việc khác. | Hai tình huống đầu có self-report; tình huống thứ ba chủ yếu từ office-lab, chưa có customer field evidence. MEDIUM/LOW. Cần diary cùng người qua nhiều loại task. |
| C6 | **UNKNOWN:** Repeat use, retention, willingness-to-pay, ARPU, tần suất pain của từng nghề, tỷ lệ thiết bị iOS/Android, nhu cầu SEA ngoài VN. | Không có nguồn đã kiểm tra đo những biến này. | Không suy WTP từ sự bực bội hay việc dùng timer miễn phí. Không chuyển lời khen thành demand. |

## Bản đồ segment/JTBD — dữ kiện và giả thuyết tách biệt

| Actor / trigger / việc cần hoàn thành | Workflow, interruption, công cụ hiện tại/gap | Tần suất, bắt đầu/bỏ dùng, outcome có thể đo | User / buyer; repeat use và payment |
|---|---|---|---|
| Sinh viên/ôn thi: ngồi học bài, đọc ghi chép, làm bài trước deadline | **VERIFIED ở người tự nhận đang học:** mở notes rồi sang điện thoại; cố định 25 phút đôi khi không hợp; workaround theo milestone, timer vật lý, giấu điện thoại, thư viện/timelapse (C-S2/3). Không xác thực toàn bộ là đại học/ôn thi. | **UNKNOWN** tần suất trên quần thể. **VERIFIED self-report:** khó bắt đầu và mất đà sau nghỉ. **HYPOTHESIS đo:** thời gian từ ngồi vào bàn đến hành động học đầu tiên; số bài làm đúng/khối kiến thức nhớ lại; quay lại sau nghỉ; kết quả với cùng độ khó. Không coi phút chạy timer là học tốt. | User có thể tự quyết dùng; **UNKNOWN** ai trả tiền. **HYPOTHESIS:** nhu cầu lặp theo buổi học/đợt thi; có nguy cơ chỉ dùng mùa thi hoặc bỏ sau khi hình thành thói quen. WTP chưa có evidence. |
| Developer/designer: viết/debug code hoặc tạo thiết kế khi đã có task | **HYPOTHESIS chuyển giao:** chuông cố định có thể ngắt reasoning; tab/tra cứu vừa cần cho việc vừa gây phân tâm. C-S4 không xác thực nghề nên không gắn lời kể vào developer. **UNKNOWN** IDE/design-tool workflow và gap cụ thể. | **UNKNOWN** tần suất và tool abandonment theo nghề. **HYPOTHESIS đo:** thời gian khởi động lại task, hoàn thành đơn vị công việc có review/chất lượng, số lần tự chuyển sang việc ngoài scope; cần phân biệt tra cứu hữu ích. | Cá nhân có thể dùng; doanh nghiệp trả tiền là **UNKNOWN**. Repeat use/WTP chưa có căn cứ. Đừng suy dev có thu nhập nên sẽ mua. |
| Freelancer/remote/office: hoàn tất phần việc trong lúc khách hàng/đồng nghiệp liên lạc | **HYPOTHESIS:** cần vừa tập trung vừa giữ SLA phản hồi. C-S1 chỉ mô phỏng email công sở, không phải field evidence freelancer/remote. Workaround có thể là lịch/DND/batching nhưng **chưa xác minh trong mẫu này**. | **UNKNOWN** tần suất, ai tạo interruption và cái nào bắt buộc. **HYPOTHESIS đo:** output đạt yêu cầu, stress tự báo cáo, thời gian phản hồi cam kết; tránh tối ưu tập trung bằng bỏ lỡ tin cần thiết. | User/buyer có thể khác; quyền tắt thông báo bị ràng buộc là **HYPOTHESIS**. Repeat use và payment **UNKNOWN**. |
| Creator/dự án cá nhân: bắt đầu và hoàn thành một deliverable tự đặt ra | **HYPOTHESIS:** không deadline ngoài dễ trì hoãn; kế hoạch/phần mềm quản lý có thể thành việc thay thế. Không có bằng chứng khách hàng theo nghề này từ bốn nguồn. | **UNKNOWN** nguyên nhân là mất tập trung, thiếu next action, thiếu động lực, hay task không còn đáng làm. **HYPOTHESIS đo:** deliverable nhỏ hoàn tất đúng tiêu chí, số lần khởi động so với bỏ dở, mức công sức ghi chép. | Thường giả định tự mua, nhưng chưa xác minh. **HYPOTHESIS:** chỉ có repeat nếu dự án thực sự còn quan trọng; WTP/retention **UNKNOWN**. |

## Problem statements đáng kiểm tra

1. **INFERENCE có public user evidence:** Khi một người học dùng cùng thiết bị vừa làm timer vừa chứa giải trí, thao tác kiểm tra/hẹn giờ có thể kéo họ ra khỏi việc đang học; họ cần hoàn tất phần học đã định với ít lần lệch task hơn. Căn cứ C1/C3; chưa chứng minh app mobile giải quyết được nghịch lý này.
2. **INFERENCE có public user evidence:** Khi đã khó bắt đầu nhưng sau đó vào đà, một nhịp nghỉ áp đặt có thể trở thành cản trở; họ cần sự hỗ trợ tùy tình huống mà không làm tăng việc quản lý quy trình. Căn cứ C2; người khác vẫn thấy nhịp cố định hữu ích, giữ nguyên bất đồng.
3. **HYPOTHESIS chưa có customer evidence theo nghề:** Người phải phản hồi đồng nghiệp/khách hàng cần giới hạn interruption có chọn lọc; lời khuyên khóa mọi thứ có thể xung đột công việc. Cần khảo sát hành vi trước khi coi đây là opportunity.

## Câu hỏi và phương pháp học tiếp, không dẫn dắt

- Mời người thuộc từng nhóm kể lại **buổi làm/học gần nhất**: định làm gì, bắt đầu bằng hành động nào, lệch task lúc nào, tác nhân gì, có quay lại không; cho xem bằng chứng tự nguyện như ghi chú/lịch/task hoàn thành. Không hỏi “bạn có muốn app giúp tập trung không?”. Chưa thực hiện và không liên hệ trong session.
- Nhật ký ngắn nhiều ngày, phân biệt tự chuyển task / interruption bắt buộc / nghỉ chủ động; hỏi lý do lần gần nhất bỏ timer, dùng lại timer hoặc chọn không dùng. So sánh với không đổi công cụ và workaround hiện có.
- Để kiểm tra tiền: hỏi **lần gần nhất thực trả** cho công cụ nào, hoàn cảnh và lý do ngừng; chưa có dữ liệu đó thì không đặt WTP giả. Để kiểm tra repeat: ghi nhận lần tự quay lại dùng trong cùng bối cảnh sau lần đầu, thay vì hỏi ý định.
- Bác bỏ mức độ cần thiết nếu task completion không cải thiện, người dùng đã thỏa mãn với timer/DND miễn phí, pain chủ yếu đến từ điều kiện học/làm không thể kiểm soát, hoặc ghi chép tốn nhiều công hơn lợi ích.

**Kết luận phạm vi:** Có bằng chứng công khai về pain và workaround ở người học, kèm phản chứng rõ với nhịp nghỉ cứng. Chưa có bằng chứng demand cho Fokus Time, chưa có dữ liệu thanh toán/retention, chưa xác thực pain riêng của developer/designer/freelancer/creator hay đại diện VN/SEA. Không đề xuất Founder decision từ R1 này.
