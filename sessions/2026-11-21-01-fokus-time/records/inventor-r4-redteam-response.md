# SES-20261121-01 — Inventor R4: phản hồi Red Team, rút nhãn candidate app

Ngày 2026-11-21. Tác giả: `/root/fokus_inventor_sol`. Origin: `/root/fokus_redteam_sol`, RT1–RT6 trong [redteam-r1.md](redteam-r1.md); relay thực D9 tại [redteam-proponent-sent.md](redteam-proponent-sent.md). Đã đọc cả hai đầy đủ và giữ nguyên R1/R3. Không web mới, build, thử app, outreach, delegation hoặc thay model. RT-S1/RT-S2 là **nguồn Red Team đã kiểm tra và relay**, không phải nguồn tôi tự duyệt. Không có thí nghiệm nào trong tài liệu này đã thực hiện.

## Đổi đánh giá sau phản biện

**INFERENCE — I-R4-01, confidence MEDIUM về thiếu lập luận increment; viability thương mại vẫn UNKNOWN:** tôi rút **F1-N và F3-N khỏi nhãn candidate standalone mobile app** trong khuyến nghị của mình. R3 đã gọi chúng là hai research hypotheses chứ không phải sản phẩm xác nhận; R4 làm rõ hơn: ngay cả lý do coi app riêng là đơn vị nghiên cứu tiếp theo cũng chưa được chứng minh. Hiện chỉ còn câu hỏi pain/practice nếu Founder muốn khám phá, không có shortlist sản phẩm để tôi bảo vệ. Không kết luận hai cơ chế vô ích, toàn bộ thị trường bị chiếm, hoặc Fokus chắc chắn thất bại.

Không đổi segment, không nhảy sang bài luận/bài toán dài, không thêm tính năng để cứu candidate. Một pain mới hoặc hypothesis mới không thừa hưởng validation từ session này. Đây là điều chỉnh recommendation của proponent, **không phải Founder `PARK`/`REJECT`** và không sửa decision log.

| Hướng | Trước R4 | Sau R4: cơ chế và phạm vi còn lại | Confidence/trạng thái |
|---|---|---|---|
| F1-N | Giữ câu hỏi bàn giao chủ động cho phone-primary task, có gate mobile hơn note tại task | Bàn giao vẫn là practice hypothesis; chưa có lỗi note cụ thể nên chuyển về **khám phá pain trước**, rút app riêng | Lợi ích practice LOW/UNKNOWN; mobile increment UNKNOWN, không có bằng chứng nâng viability |
| F3-N | Giữ chu trình dự báo–làm–đối chiếu với rubric có sẵn, so worksheet/current workflow | Nhận overlap trực tiếp trong recall subset; chưa có increment ngoài prompt nên rút app riêng. Practice có thể thực hiện trong công cụ học hiện có | Claim nhu cầu app yếu hơn sau RT-S1/2; learning/efficiency/payment vẫn UNKNOWN |

## RT1 — Không có lỗi task-local note cụ thể để bảo vệ surface riêng

**Trả lời trực tiếp:** hiện tôi **không chỉ ra được một lỗi lặp cụ thể** của note ngay tại draft/reader mà cơ chế F1-N đã giữ giải được. “Một active handoff ít nhiễu hơn kho notes lớn” chỉ là so với đối chứng yếu; một note duy nhất cạnh task có thể làm đúng việc đó. Phone-primary chỉ bỏ chi phí đổi thiết bị; rời chủ động chỉ làm capture khả thi. Cả hai không chứng minh có pain restart đủ lớn hoặc cần surface mới.

Tôi đồng ý cách gọi Red Team đề nghị: **câu hỏi khám phá pain trước, không candidate app**. Không viện dẫn bookmark Apple Books như capability đã xác minh: RT-X1/2 đã thất bại, category reader/bookmark vẫn là đối chứng cần kiểm tra trong workflow thực.

**Câu hỏi còn lại — HYPOTHESIS, không là roadmap.** Trong những lần quay lại thực, người dùng mất gì ngoài vị trí đọc/next action, có thường xuyên không, và note gắn task họ đang dùng có bỏ sót điều gì? Nếu không có lỗi thật chưa giải, dừng hướng app. Nếu handoff cải thiện so với không ghi nhưng hòa same-prompt note, lợi ích thuộc practice/template. Nếu lợi ích sau ghi–tìm–mở–resume không dương, không giữ cả lời hứa practice cho target đó. Không cần chế thêm cơ chế để buộc có lỗi.

**Mobile reason sau R4:** chưa có lý do tăng thêm được xác lập. Tôi không đề nghị test/build một surface riêng trước khi có bằng chứng cho lỗi cần giải. Việc khảo sát pain không được mô tả là đã kiểm chứng interaction mobile.

## RT2 — Anki/RemNote làm yếu thêm F3-N; không chuyển sang loại bài khác để né

**Trả lời trực tiếp:** với RT-S1/2 được relay, F3-N **không còn khác biệt chức năng đủ rõ** ngoài dự báo trước và ghi lỗ hổng mà tôi có thể bảo vệ bằng evidence hiện tại. Những prompt đó có thể dùng cùng công cụ học hoặc trên worksheet. Vì vậy tôi **rút standalone app**, thay vì chỉ giữ candidate rồi yêu cầu đối thủ chứng minh equivalence toàn phần.

Phạm vi evidence được giữ đúng: RT-S1 xác minh Anki có question→reveal→compare→rating/next review; RT-S2 xác minh RemNote mô tả exam-linked scheduling và tùy chọn hai câu đúng liên tiếp trước mastered. Đây là vendor capability, **không** chứng minh mastery, outcome target, WTP hoặc toàn bộ F3-N tương đương. Tuy vậy, đủ để tăng rủi ro trùng cơ chế ở recall subset so với R3. Tôi không cần claim “bản sao hoàn toàn” để rút một đề xuất thiếu increment.

**Cơ chế trước → sau:** từ dự kiến một lớp mobile riêng chốt tiêu chí và đối chiếu, sang practice hypothesis có thể nằm trong **workflow học đang có**. Không đề xuất sản phẩm thay thế mới. Không chuyển sang bài luận/bài toán nhiều bước với lý do flashcard không bao phủ: đó sẽ là thay đổi target/job và vấn đề rubric, chưa có evidence trong packet.

**Điều có thể mở lại — chưa quan sát:** một lỗi có thật, lặp lại trong workflow learner đang dùng, có tiêu chí kiểm tra được; cơ chế giới hạn hiện tại giải lỗi đó ròng tốt hơn công cụ hiện tại và same-prompt artifact. Đối chứng có Anki/RemNote **khi learner thực dùng chúng**, không ép chuyển sang chúng chỉ để làm đối chứng; không chỉ worksheet. Nếu không có lỗi hoặc increment, không app. Nếu learning/practice có lợi nhưng delivery hiện tại đủ, giữ practice chứ không app.

## RT5 — Chấp nhận dừng, không cứu bằng scope expansion

**Trả lời trực tiếp:** có, nếu baseline giới hạn không thắng note/worksheet/current study workflow thì tôi chấp nhận **dừng đề xuất app**, không cứu bằng import, context links, sync, AI, tutor engine, nội dung tự tạo hoặc quyền đọc mọi app. R4 đã rút cả hai trước khi có performance evidence; không hứa phần mở rộng sẽ sửa điểm yếu.

**Invariant phạm vi:** một kết quả chỉ xuất hiện khi có engine nội dung/chấm bài/integration mới là evidence cho **hypothesis khác**, không validation Fokus hiện tại. Chỉ xem xét nếu Founder mở scope riêng; session advisory này không authorize triển khai. Không tái đưa blocker/social/camera/streak vào để tạo retention hoặc justify giá.

Tôi đồng ý giữ phân biệt RT5: local text có thể nhẹ về kỹ thuật nhưng đó không phải value proof; chưa có device test/team-cost evidence. Không kết luận cần infrastructure đắt, cũng không coi privacy/legal đã clearance khi jurisdiction/age/data flow chưa chọn. Điểm yếu cốt lõi hiện nay là **lợi ích tăng thêm**, không phải fatal technical barrier được chứng minh.

**Kill đã chấp nhận:** chỉ còn cách đổi opportunity hoặc tạo nhiều phần phụ thuộc mới để làm app đáng dùng → dừng recommendation Fokus hiện tại, ghi khác biệt scope nếu sau này được xem xét. Không biến stop rule thành lệnh Founder đã ban hành.

## RT6 — Nhận sửa phép đo: efficiency cũng có thể là giá trị, không dùng để cứu kết quả xấu

**Trả lời trực tiếp:** tôi chấp nhận một utility có **learning không kém nhưng tổng công sức thấp hơn** là giá trị hợp lệ. R3 đã đặt learning oracle chống self-tick nhưng diễn đạt gate “learning tốt hơn” có thể quá hẹp. Tôi sửa **lời hứa đánh giá được phép**, không tuyên bố sản phẩm đạt lời hứa mới. Hai hướng đánh giá phải tách, định trước và được người dùng coi trọng:

1. **Learning superiority:** delayed performance tốt hơn ở nội dung/độ khó tương đương, với tổng thời gian/công sức được giữ ở điều kiện so sánh đã định.
2. **Efficiency utility:** delayed performance **không kém theo biên có ý nghĩa được định trước**, đồng thời tổng thời gian/công sức giảm đủ để có ích. Đây không phải điều kiện “không thấy khác biệt thống kê”; thiếu lực đo hoặc score ngang tình cờ không chứng minh non-inferiority.

Không đặt biên số giả khi chưa chọn domain, độ tin cậy bài đánh giá, tập người và chi phí chấp nhận. Không đổi từ superiority sang efficiency sau khi thấy kết quả kém rồi tuyên bố thắng. Nếu muốn khảo sát cả hai, phải ghi trước hai lời hứa, thước đo và cách diễn giải; không dùng nhiều outcome để chọn một cái đẹp sau cùng.

**Oracle vẫn độc lập.** Delayed equal-difficulty task/rubric tách khỏi tự tick là quality floor. Tính toàn bộ chọn mục tiêu, tổ chức/chuyển tài liệu, capture, xem lại, sửa lỗi và công chuẩn bị; cảm nhận đỡ nặng là một kết quả người dùng có thể coi trọng nhưng không thay oracle chất lượng. Nếu chưa có phép đo hợp lệ thì learning non-inferiority và efficiency đều UNKNOWN.

**Tách practice với delivery đúng RT6.** Cùng nội dung/prompt có thể làm learning tốt hơn baseline mà app không hơn worksheet/flashcards. Ngược lại app có thể tiết kiệm công điều phối so với cùng prompt mà chất lượng học giữ được. Hai quan hệ phải đo riêng. Self-ticks, ảnh tải lên, số phiên, opens hoặc retention không chứng minh quan hệ nào. Với F3-N hiện tại, chưa biết công điều phối thừa cụ thể là gì nên **chấp nhận efficiency về nguyên tắc không mở lại candidate app**.

**Trước → sau đánh giá:** tôi sửa logic đánh giá từ “phải tăng learning để có ích” sang “learning tăng với chi phí phù hợp, hoặc chất lượng không kém với effort giảm, tùy promise định trước”. Confidence viability không tăng: đây là sửa phương pháp tránh false negative, chưa có value evidence.

## RT3/RT4 — ghi nhận trong phạm vi proponent

Tôi đồng ý rằng học được prompt rồi chuyển nó về notes/worksheet có thể là customer success mà app không giữ được khách. Không thêm streak/nhắc để che điều này. Nếu tương lai khảo sát repeat, denominator là **cơ hội job thật** sau hết hướng dẫn, không phải mọi ngày lịch hay số opens. Dù app hoàn hảo, job ít lặp, người dùng không cần nữa, không có payment hoặc không có đường tiếp cận hợp lý vẫn có thể khiến business thất bại.

Không có evidence cho kênh, acquisition/support cost, giao dịch hoặc lợi thế VN/SEA/quốc tế. Các câu trả lời chiến lược/kinh tế chi tiết thuộc Strategy; tôi không viết hộ phản hồi hay đồng thuận của họ. Không suy từ việc app nhỏ rằng thị trường chắc có lời, cũng không suy crowded market rằng người dùng chắc không trả.

## Receipt D9 và câu trả lời cuối của proponent

- Đã xử lý thực RT1/RT2/RT5/RT6; RT3/RT4 được ghi nhận đúng phạm vi, không thay câu trả lời của Strategy.
- Trạng thái recipient: **RESPONDED**, locator tài liệu này. R1/R3 không sửa; không invented peer message, test, source inspection hoặc Founder decision.
- Recommendation hiện tại: **không giữ candidate standalone Fokus app nào từ hai revision F1-N/F3-N**. Nếu Founder muốn tiếp tục, đầu ra hợp lý trước hết là học xem có pain/lỗi workflow cụ thể chưa được giải hay không; không phải phát triển hay mặc định tổ chức một thử nghiệm app.
- Remaining uncertainty: practice có lợi không; có incremental delivery value nào thật không; job có lặp/tự dùng lại không; có đường kinh tế và quyền tiếp cận nghiên cứu nào không. Chưa xảy ra falsifier thực nghiệm; việc rút nhãn candidate là phán đoán về evidence và lập luận hiện có, không kết luận đã chứng minh bất khả thi.
