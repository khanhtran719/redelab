# Strategy response to actual independent Red Team — PD-X5

22/11/2026 · SES-20261121-01 · IDEA-0014 · actual respondent `/root/ft_define_strategy_sol`. Đã nhận PD-X5 từ CIO `/root`, đọc đầy đủ `redteam-initial.md` của `/root/ft_define_redteam_sol` và `redteam-cio-response.md` của `/root`. Không đọc thay reviewer, không tự sửa normative files, không web/agent/model/build mới. Reply này là trách nhiệm proponent SP2/3/4 về first-save/one-open/goal split; không claim bản normative đã được sửa hay reviewer đã chấp nhận.

## RTD1 — traceability correction được chấp nhận, không phải approval mới

**Accept** phát hiện Red Team: cùng product-local DEC002 không thể vừa chỉ documentation authority APPROVED vừa primary segment PROPOSED. Tôi đồng ý CIO sửa target reference sang DEC004 và giữ DEC002 chỉ documentation authority. Đây là lỗi tổng hợp của CIO, không gán ngược cho Strategy; không có căn cứ suy Founder đã approve segment chi tiết. Global DEC0001 không đổi. Tôi không kiểm lại canonical files trong turn này nên trạng thái phía tôi là **accept proposed correction**, không VERIFIED-FIXED.

**Observable AC:** ở gói normative revision được freeze tiếp, mọi reference DEC002 đều trỏ documentation-only authority; DEC004 trỏ proposed primary segment; không human approval mới. Reviewer cần kiểm trên exact revision mới, không chỉ response này.

## RTD2 — accept ambiguity và chọn một nghĩa deterministic

**Named concern nhận:** Red Team RTD2 nêu đúng cạnh initial New→Back/Discard trước lần Save/Start acknowledged đầu tiên. SP2/3/4 của tôi nói draft và one slot nhưng không phân biệt transient preparation form với persisted DRAFT. Sau explicit-save contract, hai cách hiểu “New đã tạo saved empty draft” và “New chỉ mở form” đều có thể sinh từ notes; không nên bắt implementer tự chọn.

**Reply: concede, accept CIO deterministic correction.** Chọn New chỉ mở **unsaved preparation form**. Nó không phải phase persisted thứ năm, không phải phiên đã bắt đầu và chưa chiếm local persisted open-record slot. Chỉ acknowledgement cho explicit Save draft hoặc Start mới cho UI khẳng định đã lưu. First successful Save tạo DRAFT; first successful Start tạo LEARNING trực tiếp và freeze commitment, không cần Save draft riêng trước đó.

### Boundaries để AC không để lại ghost hoặc form bị overwrite

1. **New khi không có saved open record:** mở một transient form. New lặp điều hướng tới chính form đó, không reset input, không form thứ hai. Không saved label; dataset không thay đổi chỉ vì mở form.
2. **Back trước first acknowledged save:** form chưa sửa → Home, dataset giữ nguyên. Form đã sửa → Save / Tiếp tục nhập / Bỏ thay đổi. Bỏ thay đổi → Home, không DRAFT/slot mới. Bỏ thay đổi không phải xóa một saved record vì chưa có record như vậy. Lựa chọn Save phải được acknowledge trước điều hướng; thất bại giữ form để retry.
3. **Save draft khác Start validation:** Save draft được lưu incomplete; nó vẫn là DRAFT và chưa freeze commitment. Start mới yêu cầu commitment nonblank và các readiness/source rules theo revision đã chọn. Save incomplete không được tự Start hoặc báo người học đã có đích sư phạm hợp lệ.
4. **Saved DRAFT đã tồn tại:** một local slot có thật. Edit tạo unsaved changes trên bản đó; Discard chỉ bỏ changes, giữ saved record/slot. New không tạo form độc lập thứ hai mà dẫn tới draft ấy. Muốn bỏ bản saved phải dùng delete có xác nhận; không dùng cùng chữ Discard để ngầm delete.
5. **Transient form chưa save nhưng user chọn một entry point khác** (ví dụ dùng gap cũ để tạo successor draft): không được overwrite hoặc sinh form thứ hai chỉ vì persisted slot hiện đang free. Resolve unsaved edits bằng Save / Tiếp tục nhập / Bỏ thay đổi trước. Save tạo một persisted DRAFT nên successor action sau đó phải tuân guard slot và không được thay draft ấy; Discard trước first save để dataset unchanged, rồi user mới có thể xác nhận successor action. Đây là guard bảo toàn nội dung đang nhập, không phải slot persisted thứ hai.
6. **Retry/lost acknowledgment:** không coi timeout là đã thất bại chắc chắn hay thành công chắc chắn. Reopen/retry phải dẫn tới whole prior state hoặc whole new state của cùng action, không empty ghost record, không duplicate. Nếu state thực đã có acknowledged/recovered DRAFT hoặc LEARNING thì UI tiếp tục record ấy; stale form không được Start lại thành record khác. Cơ chế thực hiện thuộc scope kỹ thuật tương lai; đây chỉ observable contract.
7. **Privacy/disclosure:** trước thao tác đầu tiên có thể lưu dữ liệu, gồm first Save draft hoặc first Start, user thấy thông tin local/OS-backup theo NFR hiện hành. Chỉ New chưa lưu không được báo đã lưu. Goal-change/past-gap tạo saved draft cũng phải tuân whole-action contract và disclosure nếu đó là first actual save theo dataset state; không có exemption vì entry point khác.

### One-slot và goal-split không mâu thuẫn với New unsaved

PROPOSED slot guard áp dụng **persisted open record** DRAFT/LEARNING/CHECKING; CLOSED không chiếm slot. Transient form chỉ được mở khi không có open record, và mỗi UI context chỉ có một form như vậy. Unsaved form có thể mất khi process chết trước first acknowledged save; không được hứa recovered keystrokes. Whole-state recovery sau một lost ack có thể thấy prior no-record hoặc full new record; đó là uncertainty được xử lý, không được báo dữ liệu chắc chắn chưa từng lưu.

Đổi goal từ LEARNING/CHECKING là một action rõ đã confirm, old record kết thúc UNASSESSED(reason goal changed) và successor **saved DRAFT** cùng hoàn tất, hoặc toàn trạng thái cũ giữ nguyên. Không tạo một khoảng persisted intermediate old-CLOSED mà successor thất lạc. Successor chưa Start, không có attempt/comparison/verdict cũ. Tổng open record trước/sau đều không vượt một; hai record lịch sử không là hai buổi học đã được xác minh. Edit goal trước Start chỉ edit DRAFT, không split.

Nếu request đổi goal đang ở transient first-New form hoặc saved DRAFT, không phải goal-split: người học chưa Start nên sửa commitment trực tiếp. New và goal-split có entry semantics khác nhau nhưng cùng bất biến: không silent replacement, không duplicate, không false saved/started label.

## Observable acceptance bổ sung cho RTD2

Các case sau là **PROPOSED AC**, chưa chạy trên sản phẩm:

| ID trong reply | Precondition / action | Oracle mong đợi |
|---|---|---|
| SR-RT2-A | Không open record → New → Back, chưa sửa | Home; dataset không thêm DRAFT/open slot; reopen không có ghost draft |
| SR-RT2-B | Không open record → New → nhập text → Back → Discard | Text bị bỏ theo xác nhận; dataset unchanged; New tiếp mở form mới blank, không record cũ |
| SR-RT2-C | New → Save incomplete acknowledged → edit → Discard edits | Saved incomplete DRAFT còn đúng nội dung last acknowledged save, chiếm một slot; không tự freeze/Start |
| SR-RT2-D | New nhập hợp lệ → Start acknowledged, chưa Save riêng | Đúng một LEARNING record, original commitment frozen; không còn một DRAFT riêng |
| SR-RT2-E | First Save/Start fails chắc chắn trước commit | Không success, giữ input trong process; no new record nếu whole prior no-record; không claim input sống qua kill |
| SR-RT2-F | First Save/Start lost ack → kill/reopen/retry | Whole no-record hoặc whole DRAFT/LEARNING đúng action; không partial/ghost/duplicate; state đã tồn tại không bị Start thành bản thứ hai |
| SR-RT2-G | New transient có text → chọn tạo draft từ gap cũ | Chặn overwrite bằng resolve-unsaved flow; Continue giữ form, Discard mới cho action khác, Save giữ draft riêng và successor bị slot guard |
| SR-RT2-H | Saved LEARNING/CHECKING → confirm goal change; lost ack/retry | Whole old-open hoặc old-CLOSED-Unassessed + đúng một saved successor-DRAFT; không old-only-closed và không successor duplicates |
| SR-RT2-I | Bất cứ first-save entry point nào | Disclosure hiện trước action có thể ghi actual data; success chỉ sau ack; không claim OS backup deletion/restore guarantee |

## Before → after và trạng thái trả lời

**Before:** draft chưa có timing rõ giữa New, input, Save acknowledged và slot occupancy; không có first-New Discard oracle. **After PROPOSED:** New = unsaved form; first Save = persisted incomplete DRAFT; first Start = persisted LEARNING trực tiếp; Discard semantics phân theo trước/sau acknowledged save; transient form được bảo vệ khỏi overwrite; one saved-open + whole goal-split giữ nguyên.

Tôi **accept RTD2 và CIO correction**, thêm SR-RT2-G để chốt entry-point conflict; không rebut bằng lý do “implementation tự xử lý”. Đánh giá coherence tăng sau khi quy tắc này được đưa vào exact normative revision và reviewer kiểm lại. Hiện chỉ có **RESPONDED** từ Strategy; chưa tự ghi FIXED/READY hoặc completed reviewer acceptance. Specification review không là test hành vi, usability, learning/app increment hoặc business validation.
