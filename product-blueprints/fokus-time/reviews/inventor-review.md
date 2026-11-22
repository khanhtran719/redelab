# Inventor review — tối giản định nghĩa Fokus Time

22/11/2026 · SES-20261121-01 · IDEA-0014 · reviewer thật `/root/ft_define_inventor_sol`, requested `gpt-6.1-sol`. Đây là **independent simplification judgment**, không phải independent idea invention: prompt và tài liệu đã cho thấy giải pháp được chọn và finding của Customer/Strategy. Không đề xuất hướng sản phẩm khác, không web mới, không tạo code/prototype/mockup/kiến trúc; chỉ file này do reviewer chỉnh sửa.

## Phạm vi, nguồn và phương pháp

**VERIFIED về hồ sơ đã đọc 22/11/2026:** Founder phê duyệt đúng định hướng “Fokus Time — giúp sinh viên biến một buổi tập trung thành tiến bộ học tập có thể tự kiểm tra”, và giới hạn documentation được ghi tại [intake](00-definition-intake.md). Đọc [vision v0.1](../01-product-vision.md), toàn bộ [Customer initial](customer-initial.md), [Strategy initial](strategy-initial.md), [packet PD-X1](peer-customer-strategy-packet.md), project AGENTS, creative-ideation skill và evidence/debate rules. CP/SP là đề xuất thật của hai agent, không evidence người dùng đã thích/chấp nhận.

**INFERENCE / MEDIUM:** bất biến có giá trị là giữ lời định làm trước buổi; phân biệt kết luận sau đối chiếu với cảm giác/thời lượng; cho quay lại đúng việc đang làm. Các trạng thái không đổi bất biến này cần chứng minh lợi ích trước khi thêm. **HYPOTHESIS / LOW:** ít thao tác hơn giúp loop đáng dùng hơn giấy; chưa có usability hay dữ liệu tăng trưởng học tập. **UNKNOWN:** hiệu quả, cầu, mức chịu nhập liệu và willingness-to-pay.

Dùng first principles: mỗi input phải phục vụ một quyết định cuối buổi. Dùng inversion: tìm chỗ sản phẩm ép người học khai sai hoặc tạo phiên giả để thoát. Dùng elimination/constraint: không timer, chấm bài hay quản lý nhóm ⇒ bỏ trạng thái chỉ phục vụ các cơ chế đó. Mọi correction dưới đây là **PROPOSED**, AC là tiêu chí tài liệu/hành vi tương lai, chưa chạy.

## Phản biện gắn nguồn và correction

### IP1 — Một cam kết kiểm được, không thêm form “goal” và “criterion” trùng nhau

- **Current claim / actual proponent:** Strategy SP2 yêu cầu phần/bài, điều muốn tự làm được, nguồn/cách đối chiếu; Customer CP1 cho gộp đích với bài/nguồn. Vision nói goal + comparison reference nhưng chưa làm rõ liệu criterion thành trường riêng.
- **Objection:** nếu “mục tiêu” là “học giải tích” còn “tiêu chí” là một trường khác, người dùng phải dịch cùng một ý hai lần; nếu chỉ yêu cầu goal không rỗng thì app vẫn không biết goal kiểm được hay không. Không được giải quyết bằng heuristic giả năng lực.
- **Rationale:** đối chiếu chỉ cần biết “mình định tự làm được gì” gắn với phần bài; môn, tên buổi và criterion phụ không cần để ra kết luận. App không thể xác nhận chất lượng sư phạm của câu nhập.
- **Correction:** một trường cam kết có prompt “Cuối buổi, tôi muốn tự làm được…”; vị trí bài có thể nằm trong chính câu hoặc một locator ngắn. Cách/nguồn đối chiếu là thông tin riêng vì có thể chưa sẵn. Không có trường criterion bắt buộc thứ hai; criterion là nghĩa của cam kết, không đối tượng quản lý mới. Ví dụ “Tự giải câu 3 tr.42 với các bước lập luận” là minh họa, không validation rule.
- **Observable AC:** sinh viên nhập một cam kết và chỉ vị trí bài một lần vẫn Start được; “học giải tích” được gợi ý làm cụ thể hơn nhưng app không giả là đã xác minh/chặn bằng đánh giá nội dung; khoảng trắng là rỗng; summary lặp đúng cam kết ban đầu khi đối chiếu.

### IP2 — Bỏ Paused và Canceled riêng trong vòng không timer

- **Current claim / actual proponent:** Strategy SP5/SP12 tạo Paused và Canceled riêng, CP6 muốn “rời để quay lại” khác “kết thúc chưa kiểm”. SP17 đồng thời loại timer; SP12 Canceled và SP11 Closed-Unassessed đều kết thúc mà không đánh giá.
- **Objection:** Paused không đổi việc người dùng được làm hoặc số phút đáng tin nào; Canceled và Closed-Unassessed cùng giải phóng slot, giữ cam kết, không Resume và không có verdict. Hai cặp trạng thái tạo lựa chọn người dùng phải hiểu nhưng không thêm giá trị loop.
- **Rationale:** app không đo tập trung; rời app không chứng minh dừng hay học tiếp. Ý định “quay lại” được biểu đạt bằng giữ phiên đang mở, không cần một chứng nhận pause. CP6 cần hai khả năng tiếp tục/kết thúc, không nhất thiết hai trạng thái focus.
- **Correction:** các phase đủ là Nháp → Đang học → Tự kiểm → Đã kết thúc. “Rời và quay lại sau” chỉ điều hướng; giữ phase/draft. “Kết thúc chưa tự kiểm” kết thúc bất cứ phase đã Start, outcome chưa kiểm; không Cancel riêng. Nháp được bỏ/xóa trước Start. Phase Tự kiểm chứa attempt rồi compare như hai việc tuần tự, không bắt thêm lifecycle state.
- **Observable AC:** rời/khóa app lúc học quay lại vẫn thấy phiên đang học; rời ở self-check quay lại đúng dữ liệu check; không có pause duration/active-focus claim; kết thúc sớm giải phóng slot và giữ nhãn chưa kiểm; không cần chọn “cancel” hay “unassessed” cho cùng ý định dừng.
- **Giới hạn:** nếu Founder sau này yêu cầu timer có pause thì cần một bounded timer contract mới; tên sản phẩm chưa đủ để thêm contract đó.

### IP3 — Assisted không phải Unassessed; qualification phải đi cùng verdict

- **Current claim / actual proponent:** SP7 ban đầu chỉ cho assessed khi tự thử không xem lời giải; Customer CP3/OPEN-CP-A cho phép kết luận có trợ giúp; PD-X1 §2 đề nghị INDEPENDENT / ASSISTED / NOT_ATTEMPTED.
- **Objection với SP7:** làm cùng gợi ý vẫn có thể phát hiện một bước còn vướng; ép unassessed có thể bỏ mất kết luận hữu ích. **Objection với synthesis nếu nhãn yếu:** một “Đạt” đứng riêng trong list khiến người xem suy “tôi tự làm được”, dù detail có ghi assisted.
- **Correction:** giữ ba mode nhưng hỏi bằng ngôn ngữ tự khai: “Đã tự thử chưa xem lời giải / Đã thử có trợ giúp hoặc đã xem lời giải / Chưa thử”. Chỉ hai mode đã thử + nguồn dùng được + đã đối chiếu mới cho ghi kết luận; mọi nơi hiển thị outcome kèm mode và “bạn tự đối chiếu”. Assisted có thể đạt tiêu chí **ở lần thử có trợ giúp**, không evidence năng lực độc lập. Không phải bắt thử bài mới ngay để cứu một nhãn.
- **Observable AC:** assisted + compare + đạt → list và detail đều đọc được “Tự đối chiếu · Có trợ giúp · Đạt tiêu chí”; chưa thử không sinh bất cứ đạt/một phần/chưa đạt nào; mất/không đủ nguồn vẫn chưa kiểm dù đã thử. Không badge “tự làm được/mastered”.
- **Before → after:** trước đọc CP3 tôi ưu tiên strict independent gate vì promise nhấn tự kiểm; sau phản biện CP3 tôi chấp nhận assisted có kết luận qualified. Điều chưa đổi: một verdict chung không thể là proof tiến bộ hay tự làm độc lập. Usability của wording còn UNKNOWN.

### IP4 — Source-not-ready là thiếu điều kiện đối chiếu, không thêm trạng thái học

- **Current claim / actual proponent:** SP2 chặn Start khi thiếu source; CP2 và PD-X1 §1 cho học khi chưa có source, chỉ không được assessed. Vision đã có unassessed path.
- **Objection với SP2:** chặn học vì thiếu đáp án thay promise hỗ trợ tự học thành gatekeeper tài liệu; bắt người dùng điền placeholder để tiếp tục. **Objection với expansion:** không cần thêm trạng thái “học chưa sẵn sàng”, màn đi tìm nguồn hay quản lý source.
- **Correction:** Start cần cam kết/phần bài; hỏi “Có cách đối chiếu?” sẵn/chưa có. Nếu chưa có, một thông điệp ngắn cho biết kết thúc có thể chưa tự kiểm. Cuối buổi hỏi cách/nguồn thực sự đã dùng; người dùng tự đánh giá đủ cơ sở hay chưa. Planned source và actual source có thể khác; không rewrite cam kết. Không tự mở/fetch/đánh giá URL hay lưu học liệu.
- **Observable AC:** chưa có source vẫn Start, không điền text giả; cuối buổi có nguồn hợp lệ mới vẫn cho compare; nguồn dự tính có nhưng thực tế thiếu/không đủ không sinh verdict; lịch sử chỉ hiển thị nguồn đã dùng khi thực có đối chiếu. Không có claim app xác minh legitimacy/adequacy.
- **Before → after:** CP2 thuyết phục tôi bỏ source như Start gate; vẫn giữ source-used như điều kiện của assessed. Đây là product inference, chưa có quan sát customer preference.

### IP5 — Frozen commitment không buộc frozen kết luận nhầm

- **Current claim / actual proponent:** SP14 và PD-X1 §5 không cho sửa terminal record; Customer CP8 yêu cầu sửa/xóa kết luận nhầm. Lý do SP14 là tránh biến quá khứ thành đã kiểm đúng lúc.
- **Objection:** goal và outcome bảo vệ hai bất biến khác nhau. Goal là lời định làm trước buổi nên phải giữ. Outcome là self-report có thể sai; ép xóa hoặc tạo phiên mới để sửa một tick có thể tạo lịch sử học giả và mất gap hữu ích. Không analytics/score/chứng nhận độc lập thì không cần một audit-history engine chỉ để sửa note.
- **Correction đề nghị:** cho “Sửa kết luận” sau Close, chỉ sửa outcome/gap và nguồn tự khai của **cùng lần thử**; commitment/start/attempt mode gốc giữ nguyên. Kết quả sửa có nhãn rõ “Đã cập nhật sau buổi”, không tuyên bố đã ghi đúng vào lúc Close; không cần hiển thị mọi phiên bản cũ. Không tạo một session/attempt mới do correction. Muốn đánh giá bằng lần thử mới → tạo nháp/Start mới. Unassessed vì chưa thử không thể đổi thành assessed bằng correction, vì thiếu lần thử gốc; vẫn có thể sửa note/nguồn mà giữ unassessed. Xóa vẫn là thao tác riêng.
- **Observable AC:** sửa nhầm đạt → còn thiếu giữ đúng một session, giữ goal/attempt gốc và thêm nhãn cập nhật; không âm thầm đổi cam kết hoặc independent/assisted; cancel sửa giữ nguyên record; mở lại thấy nhãn cập nhật trong list/detail; unassessed-NOT_ATTEMPTED không thể thành assessed bằng form correction.
- **Đánh đổi và giản lược hơn:** bounded correction thêm quy tắc terminal edit nhưng tránh ép ghi giả. Nếu chọn immutable để giữ scope, phải ghi đây là trade-off bất lợi được đề xuất, cho xóa dễ và đừng tuyên bố “đơn giản hơn cho người học”. Không coi vấn đề này là reason reopen SELECT.

### IP6 — Không tạo goal-version engine; đổi goal phải là quyết định rõ

- **Current claim / actual proponent:** CP5 giữ revisions trong phiên; SP13 đóng cũ unassessed + draft mới; PD-X1 §4 chọn SP13 và atomic unchanged-or-both.
- **Objection với CP5:** goal revisions kéo theo goal nào áp dụng, outcome trước/sau và sửa khi đã biết đáp án; không chứng minh cần thiết trong loop nhỏ. **Objection với SP13 nếu wording cứng:** “đóng cũ” không được gọi là học thất bại hay làm mất việc đang nhập mà người dùng chưa chấp nhận.
- **Correction:** đồng ý SP13/PD-X1: trước Start sửa nháp tự do; sau Start hành động riêng “Đổi đích và bắt đầu nháp mới” mô tả đóng phiên cũ chưa kiểm. Draft mới chưa Start, cho sửa. Không tự tạo conclusion cho goal mới. Lưu old + new cùng hoàn tất hoặc giữ nguyên; không cần trình bày đó như kiến trúc.
- **Observable AC:** goal 5 câu đổi 1 câu không bao giờ làm phiên 5 câu đạt; bấm quay lại trước xác nhận không đổi dữ liệu; sau xác nhận thấy phiên cũ chưa kiểm và một nháp mới chưa Start; retry không nhân đôi; không yêu cầu lý do đổi goal.
- **Before → after:** trước đọc CP5/SP13 tôi thấy edit giữ dấu goal-changed có vẻ nhẹ; sau so sánh nghĩa outcome tôi ưu tiên phiên cũ + draft mới trong phạm vi nhỏ. Giá phải trả là thêm một record và xác nhận, không giả là zero friction.

## Giao diện nhỏ nhất theo trách nhiệm, không mockup

Đề nghị **bốn trách nhiệm**, không phải bốn route/màn hình bắt buộc: (1) quay lại/xem lại: phiên đang dở và danh sách kết luận; (2) chuẩn bị: một cam kết, locator nếu cần, source readiness; (3) đang học: nhắc goal, chuyển self-check hoặc rời/kết thúc; (4) self-check: attempt → source-used/compare → outcome/gap → lưu, rồi hiện chi tiết trong trách nhiệm xem lại. Không cần success screen riêng, màn pause, màn canceled, màn tìm nguồn, mood/course/timer settings. Trợ năng, saved/unsaved feedback và đường thoát vẫn bắt buộc xuyên các trách nhiệm.

**Relevant missing behavior:** không nên bỏ lửng thao tác quay lại học sau khi đã nhập check. Đồng ý PD-X1 §6 chọn một contract: hành động riêng “Quay lại học”, mô tả xóa self-check draft, xác nhận; hủy giữ nguyên, đồng ý về phase học với goal gốc. Screen/OS Back chỉ điều hướng, không tự đổi phase/xóa dữ liệu. Cảnh báo chỉ xuất hiện khi thật sự có check draft sẽ mất. Nếu muốn giữ attempt cũ để so sau cần một stale-attempt contract lớn hơn, chưa có need chứng minh.

**Simpler alternative để so giá trị:** cùng một cam kết, một dòng nguồn, một kết luận/gap trên giấy hoặc note hiện có. Đây vẫn là substitute thật về cơ chế. Bốn trách nhiệm trên chỉ đáng giữ nếu giúp người dùng quay lại đúng việc và nhớ gap với ít công hơn; chưa được chứng minh. Không thêm dashboard/timer/streak để che thiếu evidence.

## Kết luận ban đầu để relay

Ủng hộ definition nhỏ có điều kiện: remove Paused/Canceled, không nhân đôi goal/criterion; accept assisted/source-not-ready với truth labels; chọn rõ một correction rule. Bất đồng mạnh nhất với SP14 là frozen goal không đòi frozen nhầm outcome. Confidence MEDIUM về logic đơn giản hóa, LOW về người học hiểu/thấy hữu ích. Chưa có peer response vào IP1–IP6 tại thời điểm ghi initial này; đề nghị CIO relay IP2/IP5 tới Strategy/Customer và giữ phản hồi thật, không suy đồng ý từ im lặng.
