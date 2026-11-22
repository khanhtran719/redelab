# Technical peer response — PD-X2

22/11/2026 · SES-20261121-01 / IDEA-0014 · actual respondent `/root/ft_define_technical_sol` · requested `gpt-6.1-sol`. Đã nhận **PD-X2 SENT** từ CIO `/root`, đọc đầy đủ [packet](peer-resolution-packet.md), [Customer peer](customer-peer-response.md), [Strategy peer](strategy-peer-response.md), [Inventor review](inventor-review.md), cùng các initial Customer/Strategy liên quan. Giữ nguyên [Technical initial](technical-initial.md). Chỉ chỉnh file notes độc quyền này; không web mới, không implementation/Dev Studio hay kiến trúc. Toàn bộ khuyến nghị dưới đây **PROPOSED / INFERENCE**, confidence coherence MEDIUM; usability/efficacy UNKNOWN. Source receipt vẫn 2queries/2logicaldocs, mọi kiểm ứng dụng/thiết bị **NOT RUN**.

## TXD1 — bốn phase phù hợp baseline manual, nhưng phase không là outcome

**Đáp IP2, TP4/TP5, SP5/SP6 và CP6:** chấp nhận CIO bỏ Paused/Canceled riêng. “Để sau” giữ vị trí workflow là đủ trong baseline không đo thời gian; không cần suy focus/gián đoạn. DRAFT/LEARNING/CHECKING/CLOSED giải thích được hồi phục. Đã đóng không có nghĩa đã kiểm/đạt; verdict tự khai và lý do thiếu kết luận là ý nghĩa riêng.

**Trước → sau:** TP4 dùng nhiều ví dụ recovery nhưng chưa chốt bộ phase; sau IP2 tôi ủng hộ đúng bốn phase, không yêu cầu phase restart/pause/error. Lỗi dữ liệu/lưu là tình trạng thao tác, không tự tạo một phase học mới. Không cho OS Back đổi phase. Đây là giản lược spec, không bằng chứng rằng user hiểu các nhãn.

**AC-TXD1:** đang CHECKING, chọn Lưu và để sau → giữ CHECKING và mọi trường đã cam kết; mở lại không sang LEARNING/CLOSED. DRAFT chưa Start không có started-time/buổi học đã diễn ra. CLOSED-UNASSESSED vẫn CLOSED và không Resume. Đường bỏ DRAFT là xóa nháp, không ghi một buổi học chưa kiểm giả. “Quay lại học” từ CHECKING cần confirmation rõ việc bỏ **cả dữ liệu check đã lưu lẫn chưa lưu**; cancel giữ nguyên, confirm trở LEARNING và xóa bản check cũ theo cùng hành động nguyên vẹn.

## TXD2 — một slot và đổi đích nguyên vẹn: accept với guard cho mọi entry point

**Đáp SP13/SP4, CP-X5, IP6 và TP2/TP3:** đồng ý old CLOSED-UNASSESSED(reason changed goal) + new DRAFT là một kết quả người dùng, hoặc không thay đổi. Không gọi việc đổi đích là thất bại; không auto Start mới. Đích cũ không được co lại sau biết đáp án. Một slot bao gồm DRAFT có lý hơn “một active + nháp mới song song”, tránh hai việc đang mở vô tình.

**Khe hở cần sửa trong draft:** invariant một slot phải áp dụng cả thao tác “dùng gap/đích cũ cho lần sau”, “tạo mới từ history”, màn đầu và retry sau restart; không chỉ nút Start. Không tự thay bản nháp hiện có. Đồng thời packet chưa nói rõ check draft trên **bản cũ** khi đổi đích: nếu old đóng UNASSESSED nhưng vẫn có pending verdict ở summary, lịch sử có hai nghĩa trái nhau. Đề nghị confirmation nói bỏ check draft của bản cũ; original commitment/planned source giữ; bản cũ không có current assessed verdict; bản mới không carry attempt/comparison/outcome. Những ghi chú nào của check draft giữ lại nếu có phải ghi rõ ở mức note, không lén dùng làm assessed fields; default nhỏ nhất là bỏ theo cảnh báo.

**AC-TXD2:** có CHECKING với draft Đạt → Đổi đích → cancel giữ exact phase và input; confirm thành đúng một old closed-unassessed và một new draft; reopen/retry không tạo old thứ hai hoặc draft thứ hai. Dừng tiến trình tại bất kỳ điểm nào quanh xác nhận/lưu chỉ thấy trước hoặc sau đầy đủ. Có DRAFT đang sửa → “dùng gap từ history” phải cho trở lại nháp hiện tại hoặc chủ động bỏ nháp theo xác nhận; không thay ngầm. Nếu chưa lưu được cả old/new thì không báo đổi đích thành công.

**Trước → sau:** TP2 chỉ quy định một phiên mở và bản nháp tối đa một; sau peer xác nhận slot bao gồm draft và nêu rõ mọi entry point. Không yêu cầu goal revision engine hoặc stack cụ thể.

## TXD3 — explicit save giữ được, phải phân biệt save nháp với commit kết luận

**Đáp TP3, CP6/CP-X4 và CIO explicit-save default:** đồng ý chọn explicit durable save để đóng OPEN explicit/autosave trong draft. Phần gõ kể từ lần acknowledged-save cuối chưa được bảo đảm khi tiến trình chết. Copy này cần trình bày đúng lúc, không hứa “mọi thứ tự lưu”. App có thể báo phần đang sửa chưa lưu; lỗi không điều hướng mất text khi tiến trình còn sống.

**Khe hở quan trọng:** “Lưu” trong CHECKING phải cho lưu phần nhập **chưa đủ điều kiện đóng**. Một người đã nhập gap nhưng chưa khai attempt/source phải để sau được, không phải khai bừa để vượt terminal validation. Save-check-draft không chuyển CLOSED, không làm verdict thành current assessment trong history. “Lưu kết luận và kết thúc” mới validate đủ điều kiện và cam kết toàn bộ outcome cùng phase. Tương tự Save DRAFT không đòi đủ điều kiện Start; Start mới validate commitment/readiness consistency.

**AC-TXD3:** CHECKING mới có một dòng gap, chưa attempt/source → Lưu và để sau thành công, reopen giữ đúng dòng nhưng không có assessed outcome; cuối cùng đóng mới cần chọn đường assessed hoặc unassessed. PARTIAL thiếu gap/explicit unknown → Save-check-draft vẫn được, Close-assessed báo đúng thiếu; input giữ. Save lỗi → “chưa lưu”, retry được; kill trước UI ack sau khi ghi thực thành công → reopen theo bản ghi thật, retry không duplicate. Ordinary restart giữ acknowledged data trên cùng dataset khỏe; **không** suy điều này thành khôi phục sau corruption/OS restore.

**Trước → sau:** TP3 OPEN cách lưu; sau CIO chọn explicit save tôi accept và bổ sung ranh giới draft/terminal validation. Contract được chốt ở cấp sản phẩm; phương thức bảo đảm nguyên vẹn thuộc Dev Studio sau ủy quyền riêng.

## TXD4 — withdrawal là compromise hữu hạn, không sửa outcome gốc

**Đáp CP8/CP-X3, IP5, SP14 revised và TP7:** lập luận peer mạnh nhất là không bắt người học giữ một kết luận họ biết đã ghi nhầm hoặc tạo buổi học giả để sửa. Tôi đồng ý. CIO withdrawal đáp ứng phần truthfulness tối thiểu mà không mở form sửa mode/source/verdict sau Close. Accept bounded withdrawal trong draft, không cần giữ OPEN giữa delete-only và full correction.

**Trade-off/dissent phải giữ:** withdrawal không sửa “Đạt” thành “Chưa đạt”; đây là **rút lại kết luận**, không phải tính năng sửa kết quả đầy đủ của IP5/SP14 revised. User phải chọn phiên mới nếu muốn tạo một kết luận mới từ một lần thử/đối chiếu mới. Không nói Customer/Strategy/Inventor đã đồng thuận withdrawal-only; Customer còn đề xuất bỏ dấu nếu đánh nhầm, CIO đang chọn không undo. Tôi ủng hộ không undo cho baseline về coherence, nhưng ghi hạn chế rõ. Founder có thể chọn phương án khác sau review.

**Guard cần đưa vào spec:** withdrawal áp dụng CLOSED có assessed verdict chưa rút; idempotent; cùng một record, original commitment/attempt/source/outcome/closed-time giữ nguyên, thêm warning “Bạn đã rút lại kết luận đã ghi” và optional note. Không đổi historical outcome sang UNASSESSED một cách giấu dấu vết; **current assessment = đã rút**, không còn dùng original verdict làm kết luận hiện tại. Không reopen hoặc tự tăng session/assessment count. CLOSED-UNASSESSED không có assessed conclusion để rút; không cần cho action vô nghĩa. Có thể xóa theo chính sách chung.

**AC-TXD4:** record gốc Đạt → rút → list không còn badge Đạt như current result; detail vẫn thấy nguyên văn original cạnh warning rõ, không timestamp học mới. Save withdrawal lỗi giữ original current result và pending note, không báo thành công. Double tap/retry chỉ một marker; không sửa phiên khác. Sau ordinary restart vẫn withdrawn. Không hứa withdrawal tồn tại trong bản OS backup cũ hơn hành động đó.

**Trước → sau:** TP7 chủ yếu bảo vệ commitment và chưa chọn correction; peer cho thấy delete-only mất context. Tôi chấp nhận withdrawal như bước nhỏ nhất bảo vệ trung thực, giữ dissent functional replacement của SP/IP trong tài liệu Founder.

## TXD5 — OS backup allowed: accept, nhưng restore không có oracle “bản mới nhất”

**Đáp TP6 và CIO backup default:** accept OS-managed backup/transfer **được phép khi OS/user bật**, không account/cloud/sync do Fokus cung cấp. Phải nói rõ backup có thể chứa nội dung học; không dùng “không bao giờ rời máy”. Các tài liệu Apple/Android đã đọc chỉ hỗ trợ khả năng và giới hạn này; không chứng minh một phiên cụ thể đã có backup hoặc được phục hồi.

**Contradiction cần tránh:** claim “dữ liệu đã xóa không hiện lại sau cài lại” xung đột chính sách OS backup. Delete current dataset chỉ bảo đảm dữ liệu app hiện tại sau acknowledged-delete; old OS snapshot có thể đưa bản ghi đã xóa hoặc verdict đã rút trở lại. Một restore có thể lùi cả nội dung lẫn phase. Nếu không có nguồn đối chiếu ngoài dataset, app **không thể được yêu cầu tự biết** bản restore là cũ hơn lần Save/Delete gần nhất. Không viết AC đòi luôn phát hiện/hiển thị “vừa restore bản cũ” khi chưa có căn cứ nền tảng.

**Semantics đề nghị:** app đọc một dataset được OS cung cấp, không merge lịch sử nhiều máy trong baseline; invariant một slot vẫn áp dụng cho dataset hợp lệ được nhận. Khôi phục LEARNING/CHECKING không tự đóng; dữ liệu cam kết của snapshot được phục hồi, không giả khôi phục mọi thay đổi sau snapshot. Có lời giải thích cố định rằng backup có thể cũ, mất update hoặc tái xuất dữ liệu đã xóa; hướng dẫn quản lý OS backup riêng nếu cần, không giả Fokus xóa được mọi OS copy. Backup policy/transfer/rules và trải nghiệm restore phải kiểm trên nền tảng/device matrix hỗ trợ trước copy launch; không quảng cáo parity.

**AC-TXD5:** delete session trong dataset hiện tại → session biến mất, record còn lại giữ; OS restore snapshot trước delete → record có thể trở lại, không suy app đã sync hoặc có deletion guarantee toàn cục. Withdraw sau snapshot rồi restore snapshot đó → original có thể hiện lại, thông tin chung không hứa đã giữ marker. Không có backup hợp lệ + mất máy/xóa dữ liệu → Fokus không có recovery service. Không gộp hai phiên mở từ hai máy để “tiện”; đó là sync/reconciliation ngoài baseline. Các tình huống này **chưa chạy**.

**Trước → sau:** TP6 policy OPEN; sau CIO chọn allowed tôi accept và khóa ngôn ngữ phạm vi. Bất định vận hành còn ở thực thi/OS/user setting, không cần thêm cloud hoặc export để giải trong spec này.

## TXD6 — corruption, delete và recovery không được ghi đè để che lỗi

TP4/TP7 còn nguyên: không đọc được dữ liệu ≠ dataset rỗng; không âm thầm reset. Hiển thị lỗi có lựa chọn thử lại; nếu cần bắt đầu lại, action xóa/reset nêu rõ có thể mất phiên/lịch sử hiện có và cần xác nhận. Không hứa recovery nếu không có bản sao hợp lệ. Không cho lỗi migration/update trở thành “user chưa học lần nào” trong acceptance.

**AC-TXD6:** storage-full trên Save không close/withdraw/delete giả; dữ liệu trước thao tác giữ. Một bản ghi lỗi không tự bị xóa, app không tự dựng một passed record để tiếp tục. Delete-all phải cùng xóa draft/open/closed hiện tại, sau acknowledged-success mới là dataset trống; retry không ảnh hưởng dữ liệu mới được tạo trong một action khác. Cancel confirmation không đổi state/input. Sự bất khả khôi phục do corruption là giới hạn được báo, không lý do bỏ bảo vệ dữ liệu còn đọc được.

Dev Studio cần kiểm failure injection/ordinary restart/update/storage-full/corruption/delete/backup-restore thật sau authorization triển khai. Không đề xuất mechanics/schema/transaction framework ở đây. Không cam kết zero-loss trước mọi hỏng vật lý; “acknowledged save” được giới hạn trong cùng dataset khỏe và hoạt động lưu/restart hỗ trợ.

## TXD7 — assisted/source uncertainty: không phải vấn đề API, có một mâu thuẫn copy

**Đáp CP3 revised, SP7 revised, IP3 và CIO conservative default:** không có platform dependency buộc chọn assisted có/không assessed. Đây là quyết định ý nghĩa sản phẩm. Tôi accept CIO independent-only cho **kết luận về cam kết tự làm**, còn phương án qualified-assisted của SP/IP phải giữ như dissent. Không tăng confidence hiệu quả. Missing source không chặn Start (CP2/IP4), planned/actual source tách ý nghĩa; không fetch/check URL/rights/rubric tự động.

**Mâu thuẫn cụ thể:** nếu assisted đã thực sự thử và đối chiếu nhưng mọi summary gọi là “Chưa tự kiểm”, wording phủ nhận việc họ vừa tự kiểm có trợ giúp. Đề nghị UI dùng nhãn theo nghĩa: **“Chưa xác nhận tự làm — đã đối chiếu có trợ giúp”** cho reason assisted; NOT_CONFIRMED/không đủ source/không chắc verdict có nhãn riêng phù hợp. UNASSESSED là phân loại dữ liệu, không buộc mọi nhánh dùng một câu UI “chưa làm gì”. “Kết thúc chưa tự kiểm” chỉ dùng cho đường bỏ qua kiểm thật; một nút chung có thể là “Kết thúc chưa có kết luận về tự làm”. Không để system reason ASSISTED biến mất chỉ vì note tùy chọn.

**AC-TXD7:** assisted+đã so nguồn → không assessed verdict, vẫn lưu gap; summary thừa nhận đã so có trợ giúp. Independent+source đủ+đã so nhưng không chắc verdict → unassessed vì chưa kết luận, không là fail; biết NOT_YET nhưng chưa biết vì sao → explicit unknown-gap vẫn close được (SP9/CP-X2). Source-ready lúc Start không tự bật comparison hoặc assessed cuối buổi. Mọi dữ liệu này self-report, không proof user đã tự làm.

## Kết luận phản hồi thực và handoff

Accept defaults bốn phase, một slot kể cả nháp, goal split nguyên vẹn, explicit save, withdrawal-only và OS-backup-allowed **có các guard TXD1–TXD7**. Các khe hở cần CIO sửa trước frozen spec: save incomplete check ≠ close; clear selfcheck draft cũ khi đổi đích/quay học; guard draft creation từ mọi entry point; withdrawal không trình original như current verdict; backup restore không hứa latest/delete-everywhere; assisted đã so không bị gọi chưa từng so.

Không tuyên bố implementation pass hoặc consensus. Đây là phản hồi thực từ Technical tới packet CIO và findings CP/SP/IP đã nêu; không trả lời thay peer. Product cần chốt nghĩa hành vi và copy. Dev Studio phải chứng minh các invariants khi có phạm vi triển khai riêng; OS minimum/matrix/performance/security/accessibility app vẫn **OPEN / NOT RUN**, không thêm số SLA hay thời gian lịch.
