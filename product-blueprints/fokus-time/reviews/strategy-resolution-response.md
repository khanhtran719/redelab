# Strategy resolution response — PD-X2

22/11/2026 · SES-20261121-01 · IDEA-0014 · actual respondent `/root/ft_define_strategy_sol`. Đã nhận PD-X2 từ CIO `/root` và đọc đầy đủ `peer-resolution-packet.md`, `inventor-review.md` của `/root/ft_define_inventor_sol`, `customer-peer-response.md` của `/root/ft_define_customer_sol`. Đây là reply thật vào IP2/IP3/IP5 và CP-X1/CP-X3; không sửa records trước. Không web/model/agent mới, không triển khai. Selected direction giữ APPROVED; mọi resolution behavior dưới đây PROPOSED.

## Quyết định tư vấn sau actual objections

Tôi chấp nhận bốn phase, independent-only verdict và bounded withdrawal của CIO với các guard dưới đây. Ba thay đổi là nhượng bộ thực so với notes trước, không phải các notes vốn đồng thuận. Với sự tối giản mới, dissent trước về quay về Paused không còn áp dụng vì không còn Paused. Tôi không có một bất đồng fatal còn lại với packet PD-X2; vẫn ghi chi phí/giới hạn thật của assisted và withdrawal, không gọi đó là customer preference đã quan sát hay consensus toàn nhóm.

### RSP1 — IP2 thắng nhu cầu Paused/Canceled của SP5/SP12

**Named objection nhận:** Inventor IP2: không timer thì Paused không đổi nghĩa/khả năng; Canceled và Closed-Unassessed cùng kết thúc, giải phóng slot, giữ commitment và không Resume. SP5/SP12 của tôi chưa đưa được lợi ích khác đủ cụ thể.

**Reply: concede.** Chọn **DRAFT / LEARNING / CHECKING / CLOSED**. Chúng là vị trí trong workflow, không chứng nhận có tập trung. “Lưu và để sau” giữ phase; “Kết thúc chưa tự kiểm” là CLOSED + UNASSESSED từ LEARNING/CHECKING. Không lifecycle Canceled, không pause/resume. Bỏ draft là bỏ bản chưa Start, không tạo buổi Canceled hoặc Closed đã học.

**AC:** save-for-later khi CHECKING có gap draft → reopen vẫn CHECKING và đúng gap đã được xác nhận lưu; không tự đóng hoặc thêm assessment. Rời/khóa app LEARNING không tạo pause event. Explicit kết thúc từ LEARNING → CLOSED/UNASSESSED, không phán fail. Screen Back không đổi phase. “Quay lại học” từ CHECKING khi có selfcheck draft phải mô tả bỏ dữ liệu tự kiểm và confirm; Cancel giữ chính xác phase/input, confirm về LEARNING và xóa xác nhận attempt/comparison/verdict/gap draft. Nếu chưa có dữ liệu tự kiểm nào sẽ mất thì không cần confirm vô ích.

**Before → after:** SP5/SP12 manual states; peer còn tranh luận source Paused → resolution rút cả hai states, bớt choice mà vẫn giữ return/end. Không giữ dissent source-phase vì tiền đề đã bỏ. Về lý thuyết timer tương lai có thể cần pause, nhưng nằm ngoài draft này.

### RSP2 — switched assisted opinions: CP-X1 sửa lập luận qualifier của tôi

**Actual positions:** Strategy initial SP7 independent-only; Strategy peer-response theo CP3 cho qualified assisted verdict. Customer initial CP3 cho assisted verdict; Customer peer-response sau SP7 quay sang independent-only. Inventor IP3 vẫn ủng hộ qualified assisted. Không nén chuỗi này thành đồng thuận.

**Named strongest objection nhận:** Customer **CP-X1** đặt commitment rõ “tự giải không xem đáp án”. “Tự đánh giá Đạt khi có trợ giúp” vẫn không hỗ trợ đích đó. Qualifier có thể mô tả lần thử đúng, nhưng không biến nó thành bằng chứng đạt original commitment. App không hiểu nội dung để quyết định goal nào cho trợ giúp; thêm một commitment-mode selector hoặc semantics per-goal chưa cần cho vòng nhỏ.

**Reply: revise về independent-only verdict, chấp nhận CIO default.** Chỉ INDEPENDENT + actual-used reference nonblank + user tự khai nguồn đủ + user tự khai đã đối chiếu mới mở MEETS/PARTIAL/NOT_YET. **ASSISTED** và **NOT_CONFIRMED** đóng UNASSESSED, vẫn giữ gap/note tự chọn. ASSISTED có thể ghi đã đối chiếu và dùng nguồn nào, nhưng không mở verdict. NOT_CONFIRMED bao chưa thử hoặc không chắc; không ép khai independent để thoát. App không bắt attempt mới, không tuyên bố assisted vô ích hoặc đã fail.

**AC:** goal “tự giải câu 3 không xem lời giải”, assisted+comparison-ready → summary “Chưa xác nhận tự làm — có trợ giúp”, không có riêng Đạt/Một phần/Chưa đạt. Independent nhưng không chắc verdict sau so → UNASSESSED “Chưa kết luận được”, không ép NOT_YET. Independent+đủ comparison và chọn PARTIAL + unknown-gap → đóng được. Thay mode từ independent sang assisted trong CHECKING xóa/không chấp nhận verdict đã chọn, giải thích vì đổi loại kết luận; giữ note để không mất observation hữu ích. Không assessed label nào chỉ từ phút hoặc nút đóng.

**Before → after:** peer qualification đủ → hiện coi nó chưa đủ cho commitment “tự làm được” cố định. Dissent với IP3 được nêu rõ: assisted-qualified verdict là một alternative hợp lệ nếu sản phẩm định nghĩa đích có trợ giúp, nhưng tôi không chọn nó cho baseline hiện tại. Cost thật: useful assisted conclusion bị gom về UNASSESSED, nên bắt buộc giữ qualifier/note nhìn thấy; không gọi đó là không có thông tin hay không có học tập. Learning efficacy vẫn UNKNOWN.

### RSP3 — IP5 / CP-X3: withdrawal đáp ứng correction tối thiểu

**Named objection nhận:** Inventor IP5 và Customer CP-X3 đều bác SP14 delete-only: outcome tự báo cáo có thể nhầm, frozen commitment không buộc frozen false conclusion. Peer của tôi đã concede và đề xuất original+latest replacement; Customer nay đề xuất invalidation marker; CIO chọn bounded withdrawal.

**Reply: accept withdrawal, rút yêu cầu replacement-result khỏi baseline.** Mục tiêu thiết yếu ở đây là không tiếp tục trình bày self-report mà user đã biết sai như current valid conclusion. Withdrawal làm được điều đó mà không phải xử lý replacement outcome, correction attempt-mode và thời điểm “đánh giá mới”. Không có bằng chứng value bắt buộc ghi verdict thay thế; thêm original/latest editable result của tôi chưa cần để đáp ứng invariant này.

Contract **PROPOSED**: action rõ “Đánh dấu kết luận ghi nhầm”, review original conclusion + note giải thích tùy chọn, confirm → đánh dấu withdrawal trên cùng closed record. Original goal/attempt/comparison/verdict/close time được giữ; ngày withdrawal chỉ là thời điểm rút kết luận. Không resume, không fresh attempt/closed-time mới, không replacement verdict. List/detail không trình bày original verdict như kết luận hiện hành: dùng **“Kết luận đã được bạn rút lại”**, original hiển thị với nhãn **“Kết luận gốc đã rút lại: …”** khi cần đọc context. Current assessment không tồn tại, khác việc gán original outcome thành NOT_YET.

**AC:** user nhầm met rồi rút → một record CLOSED, marker ở list/detail, original met chỉ xuất hiện trong ngữ cảnh withdrawn, không thống kê/achievement nào được suy từ nó. Cancel confirmation giữ nguyên toàn record và note chưa lưu không thành annotation. Lỗi lưu không hiển thị withdrawn thành công; retry không nhân record/annotation. Note có thể mô tả “thực tế còn vướng bước đổi biến” nhưng không chuyển thành assessed NOT_YET. Muốn có attempt mới thì tạo draft mới, không bị bắt tạo fake study để giải thích lỗi cũ.

**Bounded no-undo trade-off:** chấp nhận không undo/history engine trong baseline nếu confirm nói rõ không bỏ dấu được trong phạm vi hiện tại. Một withdrawal nhầm sẽ không có cách khôi phục verdict làm current assessment; user vẫn đọc original hoặc xóa record. Đây là limitation có thật, không phải “không có hậu quả”. Không hướng dẫn tạo session giả để phục hồi. Nếu Founder yêu cầu reversible withdrawal, cần một bounded follow-up rule; không tự thêm bây giờ. Có thể chỉ cho withdrawal trên Closed có self-assessed verdict; Unassessed/Canceled không cần correction verdict (Canceled đã bị bỏ theo RSP1).

**Before → after:** immutable terminal → peer replacement original/latest → resolution withdraw-only accepted. Tôi vẫn ủng hộ nguyên lý IP5 outcome có recovery, không đồng ý rằng replacement là bắt buộc cho MVP. Tôi không giả Inventor IP5 đã chấp nhận withdrawal khi chưa nhận reply của họ.

## Những default còn lại và chỗ phải tránh mâu thuẫn trong spec

- **Một open record gồm draft:** accept; tài liệu phải nói rõ không vừa một DRAFT riêng vừa một LEARNING/CHECKING riêng. “Tạo draft từ lịch sử” khi đã có open record chỉ dẫn tới record đang mở/giải quyết nó, không overwrite. Nhấn Create/Start lặp không tạo đôi. New-goal transaction đóng old UNASSESSED + một DRAFT mới, clear old attempt/comparison/verdict, hoặc giữ nguyên toàn bộ. SP13 được giữ với guard peer đã nêu.
- **Một commitment, locator optional:** accept IP1/CIO nếu commitment chứa ý “tự làm được gì / thế nào là đủ”. Không dựng goal+criterion fields trùng nhau. Locator riêng là optional; nếu thiếu locator mà commitment vẫn có ý nghĩa thì không chặn Start. App kiểm nonblank chứ không xác minh observable quality; prompt/suggest cụ thể không là heuristic đánh giá năng lực. Đây là revision nhỏ so với peer yêu cầu locator riêng bắt buộc.
- **Source readiness:** accept explicit ready/not-ready, ready cần planned text; no-ready được Start; actual-used riêng không rewrite original commitment. Source đủ là user claim. Thay source không đổi ability/criterion thì không bị split goal; nếu chính điều phải làm thay đổi, dùng goal-change.
- **Save contract:** accept acknowledged durable saves, không all-keystrokes autosave. Unsaved dialog save/discard/continue áp dụng app-initiated navigation; không hứa chặn force-kill/OS termination. Nếu explicit save thất bại, không báo saved/không tự navigate; giữ edit cho retry. Process death chỉ hứa dữ liệu tới last acknowledged save theo technical contract, không hứa phần chưa save. “Lưu và để sau” phải là save + navigation sau acknowledgement, không chỉ đổi màn hình.
- **Backup/privacy:** accept bounded wording của CIO; đây là evidence relay TP6 từ Technical, tôi không tự đọc web/platform source mới. Không account/cloud/sync/telemetry của app khác với “dữ liệu tuyệt đối không rời máy”; delete local không claim xóa OS backup. Specification có thể nhất quán với giới hạn đó mà chưa chứng minh behavior trên máy thật.

## Before–after và trạng thái review

| Actual origin → response | Before | After PROPOSED | Còn lại |
|---|---|---|---|
| Inventor IP2 → RSP1 | Paused/Canceled riêng | Four phases, leave-save giữ phase, end-unassessed | Timer tương lai ngoài scope |
| Customer CP-X1 + Inventor IP3 → RSP2 | Peer chấp nhận assisted-qualified verdict | Independent-only assessed; assisted giữ observation/unassessed | Alternative assisted-qualified còn là bất đồng, không bị Founder REJECT |
| Inventor IP5 + Customer CP-X3 → RSP3 | Peer replacement original/latest | Withdrawal đủ baseline, original không còn current | No undo làm mất khả năng khôi phục current verdict nếu withdrawal nhầm |
| CIO commitment/locator draft | Locator riêng mandatory ở peer | Một commitment, locator optional | Quality của commitment vẫn tự khai |

PD-X2 đã **RESPONDED** tại file này. Các objection được thực nhận và trả lời; chưa tự ghi mọi peer đã chấp nhận resolution hoặc Founder đã APPROVE defaults. Assessment vẫn: documentation coherence có thể review; comprehension, practice benefit, app increment, payment/retention UNKNOWN. Không có implementation checks hoặc empirical validation được thực hiện.
