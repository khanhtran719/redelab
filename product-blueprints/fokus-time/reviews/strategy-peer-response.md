# Strategy peer response — PD-X1

SES-20261121-01 · IDEA-0014 · 22/11/2026 · respondent `/root/ft_define_strategy_sol`. Đã nhận **PD-X1 SENT** qua CIO `/root`; đọc đầy đủ `peer-customer-strategy-packet.md` và `customer-initial.md` của `/root/ft_define_customer_sol`. Đây là phản hồi thực với named findings; không thay initial. Không web mới, delegation, implementation hoặc đổi lựa chọn Founder. Tất cả thay đổi hành vi dưới đây **PROPOSED**; confidence về coherence MEDIUM, efficacy/business UNKNOWN.

## Nhận định sau phản biện

Customer chỉ đúng hai hạn chế trong initial của tôi: **SP2 coi source-ready trước Start là điều kiện quá mạnh** và **SP7 đánh đồng có trợ giúp với không có kết luận hữu ích**. Tôi revise cả hai. Tôi giữ phản đối với **CP5 goal revision trong cùng phiên**: không sai về nguyên tắc nhưng cần semantics nhiều hơn một nhãn “đã đổi đích”, chưa cần cho vòng nhỏ. Với **CP8**, tôi concede immutable outcome của SP14 quá cứng: một self-report nhầm nên được sửa mà không bắt xóa cả commitment. Tôi đề xuất correction giới hạn, giữ original closure cùng latest correction, không cho viết lại đích hoặc mốc đã xảy ra.

Đây là thay đổi phán đoán do record thật, không bằng chứng usability hay khách hàng thích defaults nào. Tôi không phê duyệt toàn bộ CIO synthesis: đồng ý phần 1/2/3/4 có điều kiện dưới đây; phản đối default 5 cấm mọi correction; phần 6 có một điều chỉnh tránh fake Resume.

## CP2 versus SP2 — source chưa sẵn sàng

**Strongest Customer argument:** đến cuối buổi mới phát hiện đáp án không đủ là tình huống hợp lý; text không chứng minh adequate rubric, nên mandatory text trước Start tạo formal compliance mà không bảo vệ truth. CP2 còn cho lối học/chưa kiểm mà không ép tìm nguồn để thoát.

**Response: concede + revise SP2.** Trước Start bắt buộc đích tự làm và locator phần/bài không rỗng. Phần đối chiếu phải có một lựa chọn rõ: **Đã có cách đối chiếu** (mô tả nguồn/tiêu chí không rỗng) hoặc **Chưa có cách đối chiếu** (không bắt nhập nội dung giả). Start với lựa chọn sau được, hiển thị “Chưa sẵn sàng đối chiếu”, không phải cảnh báo ngăn học. Criterion/ability vẫn được đặt trước, còn source có thể bổ sung thực tế ở cuối. Bổ sung source không tự đổi đích.

**Bounded AC:** có goal+locator, chọn chưa có → Start được, original snapshot ghi chưa có; đến self-check vẫn thiếu/không đủ → chỉ đóng Unassessed hoặc quay lại, không chọn verdict. Sau đó tìm được source: nhập actual-used reference và tự khai nó đủ để đối chiếu, không rewrite planned source. Chọn source-ready trước Start rồi phát hiện không đủ → cùng đường Unassessed. App không xác minh “đủ” từ text.

**Before → after:** mandatory source text → explicit readiness plus source-text only when ready. Segment chính vẫn learner có bài/rubric thường dùng; đường thiếu rubric là recovery hợp lệ, không promise phục vụ mọi buổi học hoặc app tìm/chấm nguồn. Việc goal có thực sự kiểm được vẫn UNKNOWN, không có heuristic cứu.

## CP3 / OPEN-CP-A versus SP7 — attempt có trợ giúp

**Strongest objection tôi từng giữ:** nếu cùng “Đạt” bao cả nhìn lời giải rồi viết lại, summary có thể được hiểu là bằng chứng tự làm được, đi ngược selected promise. **Strongest Customer reply:** assisted comparison có thể xác định gap; ép làm lại khi không còn câu tương đương có thể tạo formality hoặc tick sai, không tạo evidence independent.

**Response: concede CP3/A, nhưng label phải là contract kết hợp, không qualifier dễ bị mất.** Attempt mode là **Tự thử không xem lời giải / Có trợ giúp hoặc đã xem lời giải / Chưa thử hoặc không chắc đã thử**. Actual attempt (hai mode đầu) + actual-used reference do user khai đủ + explicit đã đối chiếu mới cho verdict Đạt/Một phần/Chưa đạt. Mode 3 hoặc comparison/source thiếu → Unassessed. Không dùng “assessed” trên UI để ngụ ý người ngoài đã đánh giá.

**Bounded AC:** verdict luôn được render cùng mode ngay tại summary, history row và detail nơi verdict xuất hiện. Với assisted+met dùng câu hoàn chỉnh **“Tự đánh giá đạt khi có trợ giúp”**, không badge “Đạt” riêng; với independent dùng **“Tự đánh giá đạt sau tự thử”**. Nếu chưa từng thử, xem lời giải thụ động không đủ để chọn assisted assessed: cần tự khai đã thực hiện một lần thử có trợ giúp. Tự khai không chắc phải được chọn mode 3 chứ không ép nói “có trợ giúp”. Không mode nào sinh mastered/proven progress.

Nếu không muốn thêm lựa chọn chữ thứ tư, gộp chưa thử/không chắc như trên; đừng map không chắc thành independent/assisted ngầm. Selfcheck không cần nhập toàn bài, ảnh hay timer.

**Before → after:** independent-only verdict → cho qualified assisted verdict. Tăng độ bao phủ kết luận trung thực, không tăng confidence về năng lực thật. Dissent còn lại: nếu tài liệu/UI chỉ có một “Đạt” và ẩn mode trong chi tiết thì tôi **không** ủng hộ synthesis đó.

## CP4 / CP6 versus SP9 — gap và bất định

Đồng ý gói CIO: assessed Một phần/Chưa đạt yêu cầu short gap/next step **hoặc** lựa chọn “Chưa xác định được”; thiếu cơ sở/không chắc verdict là Unassessed, reason optional. Không buộc người học tự chẩn đoán lỗi để kết thúc. Phân biệt **biết có phần chưa đạt nhưng chưa biết vì sao** với **chưa biết đã đạt hay chưa**; trường hợp thứ hai không được ép chọn PARTIAL.

**AC bổ sung:** chọn “Không biết đã đạt hay chưa” → Unassessed, giữ ghi chú có sẵn; chọn “Chưa đạt, nhưng chưa biết vướng gì” → self-reported Not-yet + unknown-gap. Hai đường hiển thị khác nhau. Before → after SP9 giữ, làm rõ uncertainty ở verdict không phải chỉ ở gap.

## CP5 versus SP13 — đổi goal

**Strongest objection đối với CP5:** nhãn “đã đổi đích” cùng goal cũ/chỉ goal hiện tại chưa đủ xác định attempt nào, criteria nào và answer knowledge nào tạo ra verdict. Có thể đổi lúc selfcheck sau xem đáp án rồi tự coi cùng attempt đã đạt goal mới. Cách CP5 vẫn có thể đúng nếu đặc tả rõ nhiều goal/attempt versions, nhưng scope đó không cần để đáp ứng selected one-bout mechanism.

**Response: giữ SP13 + accept CIO part 4, có guard thêm.** Original commitment không đổi; explicit “Đổi đích” có review nói rõ: phiên cũ kết thúc **Chưa tự kiểm theo đích cũ — đã đổi đích**, một draft mới được chuẩn bị, chưa Start. Dùng chữ “chưa tự kiểm theo đích cũ” như trạng thái ghi nhận, không tuyên bố tất cả công học cũ vô ích. Goal-change operation có old-ended+new-draft together hoặc unchanged; retry không tạo duplicate. Nguồn actual-used có thể khác planned source mà không là goal-change, miễn ability/criterion vẫn đúng đích.

**AC bổ sung:** thao tác goal-change từ Self-check khi đã có draft verdict yêu cầu confirm bỏ draft verdict; Cancel confirmation giữ nguyên exact prior state/input. Bản mới không mang theo attempt mode, comparison confirmation hay verdict của bản cũ. Sau Start mới, người học phải tự khai attempt/comparison của phiên mới; không auto-reuse kết luận từ attempt trước Start. App không thể kiểm tra freshness, nên vẫn self-report.

**Before → after:** split-session giữ; làm rõ partial operation/retry và selfcheck confirmations không được carry. Không đồng thuận CP5 trong-session revision vì scope/coherence, không phải vì goal change có động cơ xấu. Nếu Founder muốn một phiên bằng mọi giá, cần chọn một bounded revision contract mới; không giả đây là impossibility.

## CP8 versus SP14 — correction nhầm sau Close

**Strongest Customer argument:** không thưởng self-certification nhưng vẫn cho sửa/xóa kết luận nhầm; record tự báo cáo sai không nên bị đóng băng như sự thật. SP14 bắt delete mất cả thông tin hữu ích hoặc tạo phiên mới cho typo không phải smallest complete recovery.

**Response: concede, phản đối CIO part 5 default no-correction.** Đề xuất bounded correction thay SP14:

- Chỉ hành động rõ **“Sửa kết luận đã ghi”** cho Closed có verdict tự báo cáo; không sửa original commitment, Start/Close time hoặc tạo attempt mới giả.
- Có thể sửa self-report mode, actual-used reference, verdict và gap hoặc hạ về Unassessed. Chỉ sửa mô tả **điều đã xảy ra tại phiên cũ**; nếu mới làm/đối chiếu sau khi Close, tạo draft/phiên mới, không dùng correction để claim đã làm lúc trước.
- Giữ original closure + latest corrected report; marker **“Đã sửa sau khi kết thúc”**, thời điểm correction và nội dung gốc có thể đọc trong detail. Intermediate edits không cần một audit-log sản phẩm/phần mềm quản lý versions. Mọi lần correction đều là tự khai, không chứng minh bản mới chính xác hơn.
- Closed-Unassessed không được nâng thành assessed qua correction: chưa có verdict ban đầu để sửa; muốn tự kiểm mới thì phiên mới. Canceled không có assessment để sửa. Không thêm correction vào commitment, không cho Resume terminal session.

**Bounded AC:** người học click nhầm met thay notyet → correction đổi current summary thành notyet + gap/unknown-gap theo rule hiện hành, marker không thể tắt, original met còn đọc được; không sửa phiên khác. Cancel edit giữ nguyên kết luận. Save lỗi không đổi current record hoặc báo đã lưu; input edit giữ được để retry. Selfcheck mới sau Close không được gán vào thời điểm Close cũ. Nếu mới phát hiện kết luận cũ thiếu cơ sở → hạ Unassessed được và original vẫn còn; không ép giữ verdict sai.

**Before → after:** no-edit terminal → amend self-report transparently; original commitment/closure vẫn immutable, không correction engine chung. Chi phí thêm một original/latest distinction là có thật, nhưng tôi coi nó proportionate với lỗi tự khai. Confidence usability LOW vì chưa thử. Nếu Founder/CIO vẫn chọn no-correction, phải giữ dissent và nêu recovery chỉ delete/create-new; đừng gọi đó là Customer-consensus hoặc path sửa lỗi đầy đủ.

## CIO part 6 — quay lại học từ selfcheck

Đồng ý Back điều hướng không đổi phase. Explicit “Quay lại học” là event phase, không OS Back. Đồng ý có confirm discard selfcheck draft nếu đó là contract đơn giản đã chọn; nói rõ sẽ bỏ lựa chọn/kết luận đang nhập, Cancel giữ nguyên. Nhưng **không tự Resume phiên Paused** chỉ vì người học bỏ Selfcheck: quay lại source phase Active/Paused như SP6 là default tôi khuyến nghị. Nếu nút tên đúng “Tiếp tục học ngay” thì chuyển Active là được, đó phải là hành động có nghĩa Resume.

**AC:** Paused → Selfcheck → Back màn hình giữ Selfcheck phase; explicit “Quay lại phiên đang tạm dừng” + confirm → Paused, frozen goal giữ, selfcheck draft xóa theo thông báo. Active-source → quay Active. Nếu dùng một nút “Tiếp tục học ngay”, summary trạng thái chuyển Active rõ; không ngầm gắn focus liên tục. Từ selfcheck bắt đầu một attempt mới phải có xác nhận mới, không reuse verdict cũ.

## Receipt / remaining dissent

Origin `/root/ft_define_customer_sol` CP2/3/4/5/6/8 → respondent `/root/ft_define_strategy_sol`, CIO relay PD-X1. **RESPONDED** tại file này; chưa có reply của Customer với các rebuttal của tôi, không tự ghi completed debate/consensus. Trước: independent rigid source/no-assist/no-correction; sau: readiness path, qualified assisted reports, bounded correction; giữ split-session goal-change và source-phase return. Không thay Selected direction, không tăng efficacy/business confidence.
