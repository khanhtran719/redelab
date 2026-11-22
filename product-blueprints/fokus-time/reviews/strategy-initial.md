# Strategy initial — product definition

SES-20261121-01 · IDEA-0014 · DEC-0001 · 22/11/2026 · author runtime `/root/ft_define_strategy_sol`, requested `gpt-6.1-sol`. Independent first pass: chưa đọc đề xuất product-definition của peer. Chỉ ghi file độc quyền này. Không web mới, không nghiên cứu thực địa, không triển khai.

## Authority và evidence

**APPROVED / VERIFIED theo intake đã đọc:** Founder chọn chính xác “Fokus Time — giúp sinh viên biến một buổi tập trung thành tiến bộ học tập có thể tự kiểm tra”, đồng thời cho phép tài liệu định nghĩa sản phẩm. Detailed requirements chưa APPROVED. Toàn bộ hành vi SP bên dưới là **PROPOSED**, cơ chế/value còn **HYPOTHESIS**, không phải evidence hiệu quả.

Nguồn nội bộ đã đọc ngày 22/11/2026: `reviews/00-definition-intake.md`; `sessions/2026-11-21-01-fokus-time/08-top-proposals.md` phần F3-N và final status; `06-red-team-assessment.md`; `records/strategy-r3-redteam-response.md`; project AGENTS, product-opportunity skill, evidence policy, debate rules. Phạm vi mới của Founder ưu tiên hơn giới hạn PRD trong skill; chỉ documentation, không implementation. Không mở lại DISCOVER/selection.

**INFERENCE / MEDIUM:** một spec nhất quán có thể làm rõ việc người dùng đã tự khai điều gì, trước/sau thời điểm nào, và còn thiếu bước nào. **UNKNOWN:** liệu thao tác ấy đem increment trên worksheet/Anki/RemNote/công cụ thật, delayed learning, effort ròng, repeat hay willingness-to-pay. Viết đúng spec không kiểm chứng các vấn đề đó. Prior screening bài toán nhiều bước là giả thuyết bất đồng, không được biến thành target đã chọn.

## Primary segment và vòng nhỏ nhất

**PROPOSED SP1 — segment:** sinh viên đại học tự học một phần/dạng bài đủ nhỏ trong một buổi, có bài và đáp án/rubric hợp lệ đang dùng bên ngoài Fokus, có thể tự đối chiếu. Không mặc định chỉ môn toán, chỉ recall hay bài nhiều bước; không cần lựa chọn môn/major riêng. User và beneficiary là người học; buyer chưa chọn, giả thuyết buyer là chính người học; không gán trường/phụ huynh làm purchaser.

Job: trước buổi biết sẽ tự làm được điều gì; cuối buổi có một kết luận tự báo cáo gắn đúng tiêu chí và một điều cần làm tiếp nếu còn thiếu. Substitute nghiêm túc: một dòng commitment và kết luận trên worksheet/note/current learning tool. HYPOTHESIS value: ít công điều phối hoặc kết luận hữu ích hơn; không dùng số phiên/phút/tick làm bằng chứng học. Switching friction gồm nhập lại đích, chuyển app, nhớ mở cuối buổi, tự chấm và mất flow. Không có evidence đủ để định giá/subscription, channel hay moat; không thêm retention features để chữa khoảng trống.

Primary loop **PROPOSED**: chuẩn bị đích + chỗ học/đối chiếu → bắt đầu → tự học ngoài app (có thể chủ động tạm dừng) → tự làm và đối chiếu ngoài app → tự khai kết quả → đóng và đọc lại kết luận. Có lối thoát trung thực không tự kiểm. Activation candidate là hoàn tất vòng có kết luận được người học coi là hữu ích; chỉ là khái niệm để định nghĩa, chưa là metric/analytics plan.

## Requirement candidates và observable acceptance

Tất cả SP2–SP17 **PROPOSED**, không APPROVED. Các AC dưới đây là tình huống kiểm tra specification/hành vi dự kiến, chưa test execution.

| ID | Quy tắc đề xuất và lý do | Observable acceptance / edge & recovery |
|---|---|---|
| SP2 | Một draft tại một thời điểm; draft không là phiên đã bắt đầu. Ba nội dung trước Start: phần/bài đang học (locator text), điều cụ thể muốn tự làm được, cách/nguồn đối chiếu tiêu chí đang có. Có prompt ngắn nhưng không app xác nhận tiêu chí tốt. | Bỏ trống hoặc chỉ khoảng trắng một nội dung → chỉ đúng chỗ thiếu, giữ phần đã nhập, chưa Start. Draft sửa/xóa tự do. Không tuyên bố nhập đủ = mục tiêu hợp lệ về sư phạm. |
| SP3 | Start là hành động rõ ràng. Chốt snapshot ba nội dung và thời điểm bắt đầu; không tự Start do mở màn hình hay hết onboarding. | Tap Start hợp lệ một lần → đúng một phiên Active, giữ đúng commitment trước buổi. Tap lặp/reopen không tạo phiên thứ hai. Chưa Start không được tính là buổi học. |
| SP4 | Tối đa một phiên chưa kết thúc trên một bộ dữ liệu cục bộ: Active, Paused hoặc Self-check đều chiếm cùng slot. Không claim một phiên trên mọi máy khi chưa có sync/account. | Có một phiên chưa kết thúc → mở lại phiên ấy; tạo/Start phiên khác bị chặn với lựa chọn quay lại hoặc kết thúc phiên hiện tại. Draft mới chỉ được tạo khi slot rảnh; không tự đóng phiên cũ. |
| SP5 | Active không có nghĩa “đang tập trung” đã xác minh. Manual Pause/Resume là trạng thái tự khai; không tự pause khi rời app, khóa màn hình hoặc mất mạng. | Pause → Paused, Resume → Active. Mở lại app giữ trạng thái cũ, không ghi người học đã học liên tục. Paused vẫn có thể đi đến Self-check hoặc kết thúc không đánh giá. |
| SP6 | Đi đến Self-check không bắt buộc timer/chờ một thời lượng. Commitment vẫn thấy được; app không có lời giải, không tạo/chấm bài. | Active/Paused → Self-check theo thao tác rõ ràng; Back giữ dữ liệu đang điền và trạng thái nguồn, không kết thúc. Quay lại học cũng rõ ràng; không tự đánh dấu kết quả khi mở bước. |
| SP7 | Kết luận có đánh giá chỉ dựa trên tự khai: người học xác nhận đã tự thử không xem lời giải rồi đã đối chiếu bằng nguồn/tiêu chí đã chọn. Nếu chưa/còn không chắc, có thể tiếp tục học hoặc đóng Chưa tự kiểm; không ép nói đã làm. | Chưa xác nhận đủ hai hành động → không cho ghi nhãn “đạt/một phần/chưa đạt”; cho đóng Unassessed. App ghi nhãn “Bạn tự đánh giá sau đối chiếu”, không “đã xác minh/học được/mastered”. Xác nhận không là proof người dùng nói thật. |
| SP8 | Ba kết quả sau đối chiếu: Đạt tiêu chí; Đạt một phần; Chưa đạt. Đây là mức tự báo cáo tại lần thử, không verdict vĩnh viễn hoặc điểm số. Mục tiêu có nhiều vế mới có “một phần”; người dùng tự phân biệt, app không suy luận text. | Có xác nhận SP7 + một lựa chọn → có thể đóng. Không tự chọn Đạt do thời gian/số lần. Nhãn lịch sử luôn gắn “tự đánh giá”. Không chuyển Chưa đạt thành thất bại cá nhân. |
| SP9 | Với Một phần/Chưa đạt, yêu cầu một ghi chú ngắn “còn vướng gì hoặc bước tiếp theo”; cho lựa chọn rõ “Chưa xác định được” để không ép bịa diagnostic. Với Đạt, ghi chú tùy chọn. | Chọn “Chưa xác định được” → vẫn đóng được, hiển thị đúng là chưa xác định, không tự sinh next action. Thông báo thiếu ghi chú không xóa lựa chọn/kết quả. Không yêu cầu kế hoạch ôn/ngày ôn. |
| SP10 | Close là một hành động review kết quả rõ ràng, không đồng nghĩa vào Self-check. Phiên Closed giữ commitment và kết luận cùng nhau. | Rời app ở Self-check → vẫn chưa kết thúc, quay lại tiếp. Close hợp lệ → phiên kết thúc một lần; màn xác nhận hiển thị mục tiêu, kết quả, ghi chú nếu có. Không cho Close lại tạo bản sao. |
| SP11 | Đóng Chưa tự kiểm/Unassessed là kết thúc hợp lệ từ Active/Paused/Self-check, không có nhãn đạt hoặc không đạt. Lý do tùy chọn, không hỏi bắt buộc. | “Hôm nay dừng ở đây, chưa tự kiểm” → Closed-Unassessed, không tự suy thiếu năng lực hay chưa tiến bộ. Sau đó slot rảnh. Nếu muốn kiểm lại sau khi đã đóng, tạo phiên mới từ commitment cũ, không sửa quá khứ thành đã kiểm đúng lúc. |
| SP12 | Cancel là từ bỏ phiên đã Start, khác xóa dữ liệu và khác Close-Unassessed. Lưu trạng thái Canceled + commitment tối thiểu, không đánh giá học. Cần lựa chọn xác nhận vì mất continuation nhưng không vòng guilt. | Cancel từ Active/Paused/Self-check → Canceled, slot rảnh; nháp kết luận không thành assessment. Quay lại trước xác nhận → tiếp tục nguyên trạng. Draft chưa Start dùng “Bỏ bản nháp”, không tạo Canceled session. |
| SP13 | Đổi đích sau Start không âm thầm sửa snapshot. Mặc định scope nhỏ nhất: hành động “Đổi đích” kết thúc phiên cũ Unassessed với reason “đổi đích”, sao chép nội dung sang draft sửa được; Start mới sau khi người học duyệt. Không goal-version engine trong một phiên. | Người học giảm từ 10 bài còn 3 → phiên cũ không thành Đạt 10; bản mới chỉ thành phiên khi Start, commitment mới thấy được. Hủy thao tác đổi đích trước xác nhận không đóng phiên. Công học ở phiên cũ không bị tuyên bố vô ích. Có friction nhưng giữ trung thực và ít state. |
| SP14 | Không sửa commitment phiên Closed/Canceled; correction kết luận có thể làm sai mốc “đã kiểm tại cuối buổi”. Default scope nhỏ: có thể xóa phiên, hoặc tạo draft mới từ nội dung cũ; không sửa retrospectively. | Lỗi chính tả snapshot được giữ; người học có thể xóa nếu không muốn giữ hoặc tạo phiên tiếp, không rewrite quá khứ thành đích dễ hơn. Nếu Founder chọn post-close correction sau này cần ghi rõ correction semantics, chưa tự thêm log engine. |
| SP15 | Danh sách ngắn toàn bộ phiên cục bộ và mở chi tiết là core tối thiểu để dùng lại lỗ hổng. Hiển thị commitment, kết quả/trạng thái, ghi chú; mới nhất trước. Không dashboard, streak, completion score hay tổng giờ. Không tùy tiện giới hạn 7/30 ngày gây mất dữ liệu. | Mở phiên Một phần → đọc được đích và gap đã ghi. Canceled/Unassessed không hòa vào Đạt/Chưa đạt. Xóa một phiên có xác nhận, không xóa cả danh sách. Dữ liệu cũ không bắt buộc dùng lại. |
| SP16 | Local/offline cho vòng cốt lõi; nháp/phiên chưa kết thúc được giữ khi rời app. Độ bền qua sự cố, thay máy/xóa app phải có contract kỹ thuật riêng; không ngầm hứa backup. | Mất mạng không chặn Start/self-check/Close/xem lại. Reopen không tự hoàn tất/cancel. Khi không lưu được, không báo thành công; giữ nội dung phục hồi được và đưa lựa chọn thử lại. Chuyển trạng thái chỉ được báo hoàn tất khi nội dung tương ứng đã được giữ theo contract. |
| SP17 | Timer/Pomodoro, background alarm, số phút, blocker là PROPOSED OUT OF SCOPE cho MVP định nghĩa này. Người dùng có thể dùng timer riêng bên ngoài. Trợ năng/riêng tư và đường thoát không là tính năng tùy chọn. | Không có thời gian cài đặt bắt buộc; 3 phút hay 2 giờ không quyết định assessed outcome. Clock/device change không đổi learning label. Không timer hết giờ tự Close hay tự cho Đạt. Không countdown vẫn hoàn tất đủ primary loop. |

## State contract tối thiểu

PROPOSED: `Draft → Active ↔ Paused`; `Active/Paused → Self-check → Closed-Assessed`; `Self-check → trạng thái nguồn` hoặc chủ động quay lại Active; `Active/Paused/Self-check → Closed-Unassessed | Canceled`. `Đổi đích` là kết thúc Unassessed(reason goal-changed) + một Draft mới chưa Start. Closed/Canceled là terminal, chỉ đọc/xóa/tạo draft tiếp; không Resume. Draft không chiếm active slot nhưng default không tạo draft thứ hai trong lúc slot bận.

Không dùng các từ “hoàn thành” mơ hồ cho cả phiên kết thúc và mục tiêu đạt. Một phiên có thể đã kết thúc mà chưa tự kiểm; một phiên có thể tự đánh giá Chưa đạt nhưng vẫn hữu ích về biết lỗ hổng. App biết trình tự thao tác, không biết người dùng thực sự tập trung/làm độc lập/so đúng rubric.

Quay lại từ Self-check về nguồn Paused cần nhớ nguồn một lần, không là phiên khác. Nếu CIO muốn tối giản hơn nữa có thể quy định “Quay lại học” luôn Active nhưng phải báo đúng nghĩa; không tự Resume vì nút Back.

## Điểm cần Founder quyết định và default để review hoàn chỉnh

Chưa có lựa chọn nào chặn việc viết spec draft hoàn chỉnh: dùng defaults sau và ghi PROPOSED. Trước một implementation scope tương lai, các hành vi chưa APPROVED cần quyết định, nhưng không tạo gate giả cho việc viết tài liệu đã cho phép.

1. **Timer:** default không có trong MVP; tên Fokus Time không tự authorize stopwatch. Nếu Founder muốn timer phải định rõ nó giúp job nào, rồi thêm bounded behavior thay vì mặc định Pomodoro.
2. **Mục tiêu đổi sau Start:** default kết thúc Unassessed + draft mới (SP13). Đánh đổi là friction/phiên bị chia nhưng không có hệ version phức tạp hoặc post-hoc success. Alternative giữ phiên và goal revisions là hợp lệ nhưng scope lớn hơn; không được ghi hai cách cùng là requirement.
3. **Outcome vocabulary:** default Đạt/Một phần/Chưa đạt **theo tự đánh giá sau đối chiếu**, và Chưa tự kiểm riêng. Nếu muốn “tiến bộ được chứng minh”, cần evidence/measurement khác, không sửa label là đủ.
4. **Lịch sử/correction:** default readable local list, xóa được, không sửa phiên kết thúc. Nếu giá trị học cần sửa kết luận sau buổi, phải phê duyệt correction semantics riêng; không tự mở analytics/export/scheduler.
5. **Primary segment:** giữ one-bout self-study với bài/rubric sẵn của F3-N; không tự thu hẹp bài nhiều bước để né competitor, không expand platform học liệu. Chọn môn/cohort thực tế còn UNKNOWN, không blocker của spec cơ chế nhưng blocker của validation có ý nghĩa.

## Boundary và cách đánh giá về sau

Spec correctness có thể kiểm bằng transition/AC: một slot, snapshot trước Start, no silent rewrite, kết quả không suy từ phút, thoát không đánh giá, phục hồi không báo thành công giả. Không có check nào trong tài liệu này đã được thực thi trên sản phẩm.

Learning efficacy cần oracle ngoài self-report và đánh giá phù hợp; business validation cần lợi ích tăng thêm trước current workflow, repeat ở cơ hội thật, payment/channel evidence riêng. Founder SELECT không chứng minh hay waive các gap đó. Không có giá, recurring payment, marketing claim tăng điểm, retention mechanism, recruitment hay thử nghiệm được authorize ở đây.

## Initial assessment

PROPOSED phạm vi nhỏ nhưng hoàn chỉnh là commitment → attempt/compare outside app → truthful self-report → readable conclusion. Kết luận chiến lược chưa đổi: **definition coherent có thể soát; learning/app increment/business còn UNKNOWN**. Confidence MEDIUM về sự nhất quán yêu cầu, LOW về value thực nghiệm. Không kết luận đây là app đáng mua; cũng không dùng khoảng trống evidence để reopen lựa chọn Founder.
