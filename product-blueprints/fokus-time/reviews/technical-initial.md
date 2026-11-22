# Technical initial — ràng buộc hành vi và khả thi

22/11/2026 Asia/Ho_Chi_Minh · SES-20261121-01 / IDEA-0014 / DEC-0001 · agent `/root/ft_define_technical_sol` · assigned `gpt-6.1-sol`.

Đánh giá độc lập ban đầu, trước khi đọc đề xuất của các specialist cùng đợt. Đã đọc intake, `05-platform-feasibility.md`, technical R2 và skill feasibility-assessment. Chỉ ghi file notes độc quyền. Không sửa tài liệu thẩm quyền; không triển khai, không thiết kế kiến trúc và không mở Dev Studio. Các TP dưới đây đều **PROPOSED**, trừ khi chỉ rõ OPEN; chúng không đổi phạm vi APPROVED của Founder. **INFERENCE** khả thi cho vòng văn bản tự nhập cục bộ; confidence vừa, chưa kiểm ứng dụng hay thiết bị. Không có SLA dịch vụ vì baseline không cần dịch vụ của Fokus.

## TP1 — đơn vị giá trị và workflow nhỏ nhất

Một phiên duy nhất chưa đóng: nêu bài/đích → ghi tiêu chí có thể đối chiếu trên tài liệu sẵn có → bắt đầu học ngoài điện thoại → tự quay lại → tự đối chiếu tiêu chí → ghi kết quả và điều còn thiếu → đóng phiên. Không cần account, mạng, ảnh, AI, quyền usage/blocking hay timer để hoàn tất vòng này. Quyền đối với bài/đáp án thuộc người dùng; baseline không nhập/xuất bản học liệu. Ứng dụng lưu lời người dùng, không xác nhận đó là bài làm đúng hoặc tiến bộ đo khách quan. Lưu một kết quả “đạt” phải hiển thị là **tự đánh giá**, không thành chứng nhận của app.

AC ví dụ: bật chế độ máy bay và từ chối mọi quyền tùy chọn; vẫn tạo, bắt đầu, đối chiếu, lưu, xem/sửa/xóa một phiên bằng văn bản. Failure: bắt đăng nhập, cấp notification hoặc tải nội dung mới được đóng phiên; suy “đạt” từ hết giờ. Độ khả thi **INFERENCE**, không phải device VERIFIED.

## TP2 — một phiên đang mở và thao tác lặp

Đề nghị chỉ có một phiên đang mở trên **bản cài đặt hiện tại**, gồm lúc đang học hoặc đang nhập đối chiếu. Mở app lại phải trỏ về phiên đó. Nếu bấm bắt đầu phiên mới khi còn phiên mở, đưa người dùng về phiên hiện tại hoặc cho họ chủ động đóng/bỏ phiên trước; không âm thầm thay thế, không tự chấm phiên cũ. Bản nháp chuẩn bị chưa bắt đầu không được lén tăng số phiên đã học; số bản nháp tối đa nên giữ một để tránh thêm quản lý danh sách.

AC: bấm nhanh hai lần “Bắt đầu” chỉ tạo một phiên; bấm hai lần “Lưu kết quả” chỉ tạo một kết quả/đóng một phiên. Sau lỗi hoặc restart, thử lại cùng hành động không tăng lịch sử trùng. Xóa rồi bấm lại xác nhận không xóa sang bản ghi khác. Không hứa điều phối giữa nhiều máy vì không có sync/account. Cơ chế kỹ thuật khử trùng thuộc Dev Studio sau này; sản phẩm sở hữu kết quả nhìn thấy này.

## TP3 — “đã lưu” có nghĩa gì

Mỗi thao tác cam kết cần có kết quả nguyên vẹn ở mức người dùng: dữ liệu liên quan và trạng thái phiên đi cùng nhau. “Lưu kết quả” thành công phải giữ cả kết quả, điều thiếu nếu bắt buộc, và trạng thái đã đóng; không có bản ghi “đã đóng” nhưng mất kết quả. “Bắt đầu” thành công phải giữ đích/tiêu chí áp dụng cho chính phiên đó và trạng thái đang mở. Chỉ xác nhận “Đã lưu trên thiết bị” khi có bằng chứng lưu thành công. Nhãn này không có nghĩa đã sao lưu hệ điều hành.

AC: tắt app tại các điểm quanh lúc lưu; mở lại cho thấy trạng thái trước thao tác hoặc trạng thái sau đầy đủ, không nửa phiên. Nếu lần đầu thật sự đã lưu nhưng UI chưa nhận xác nhận, lần mở lại phải trình bày trạng thái đã lưu và thao tác thử lại không nhân bản. Khi ghi thất bại do hết chỗ/lỗi, giữ nội dung đang nhập khi tiến trình còn sống, nói chưa lưu và cho thử lại; không hiển thị thành công và không tự điều hướng làm mất nội dung. Không cam kết giữ phần chưa xác nhận sau tiến trình chết; tính chất mất tối đa phần sửa sau lần lưu cuối phải được nói chính xác.

Đề xuất tối thiểu cho bản đầu: hành động lưu rõ ràng tại các mốc; khi rời màn hình có sửa chưa lưu, cho lưu/tiếp tục sửa/bỏ thay đổi. Nếu nhóm chọn autosave cho nháp để giảm thao tác, phải có cùng trạng thái đang lưu/đã lưu/lỗi và ngưỡng mất dữ liệu mô tả được; không viết “tự lưu mọi lúc” khi chưa chọn/test. **OPEN:** explicit-save hay autosave cho phần đang soạn; semantics cam kết của đoạn trên không OPEN.

## TP4 — restart, gián đoạn và sự trung thực của trạng thái

Khóa màn hình, chuyển app, cuộc gọi, tiến trình bị OS dừng, reboot hoặc mất mạng không đồng nghĩa học xong, bỏ cuộc hay thất bại. Sau mở lại, phục hồi phiên cam kết gần nhất; cho tiếp tục học, chuyển sang tự đối chiếu, hoặc chủ động bỏ phiên. Không tự chuyển phiên qua đêm thành hoàn thành. Nếu thời gian rất dài, nhắc kiểm tra phiên đang mở bằng lựa chọn, không phạt hoặc đoán thời gian học.

AC: đang học → restart → vẫn phiên đó, cùng đích/tiêu chí; đang đối chiếu → chỉ phần đã cam kết được đảm bảo, không giả có kết quả; mở ngày hôm sau → không có “hôm qua đã đạt” tự động. Nếu phát hiện dữ liệu không đọc được, hiển thị lỗi dữ liệu thay vì màn hình trống giả như chưa từng học; không tự ghi đè lịch sử bằng dữ liệu mới. Cho thử mở lại và hướng dẫn giới hạn phục hồi; việc bắt đầu lại/xóa toàn bộ cần xác nhận hậu quả riêng.

## TP5 — manual baseline so với timer tùy chọn

**Khuyến nghị manual baseline**: “Bắt đầu học” / “Quay lại đối chiếu” do người dùng chọn. Bỏ sự phụ thuộc chạy nền, notification permission và độ đúng giờ khỏi cơ chế giá trị. Không ghi phút tập trung như phút học được xác minh. Timer là **OPEN**, không mặc nhiên thuộc MVP từ tên Fokus Time hoặc sản phẩm timer trước đây.

Nếu Founder sau này chọn timer: nó là mốc dự kiến/hỗ trợ định hướng, không tự tạo outcome hoặc đóng phiên; từ chối notification vẫn dùng toàn bộ vòng; countdown khi mở app lại phải dựa trạng thái đã lưu và có quy tắc rõ với reboot/đổi giờ; nhắc đúng giây ở mọi trạng thái không được hứa. “Đã qua mốc” khác “bạn đã học đủ”. Timer phải được kiểm khi app mở/khóa/mất tiến trình/reboot, đổi giờ/múi giờ, quyền cho/từ chối/thu hồi, chế độ hạn chế nền và Focus/Doze. Đây là danh sách xác minh nếu timer được chọn, không là feature list được duyệt.

## TP6 — local, backup, mất máy và xóa là các phạm vi khác nhau

**VERIFIED tài liệu**, chưa test app: Android Auto Backup có thể tự bao gồm dữ liệu ứng dụng; điều kiện, OS và cấu hình ảnh hưởng. Android nêu riêng một số hãng có khác biệt giữa chặn cloud backup và chuyển thiết bị. Apple mô tả iCloud Backup chứa dữ liệu app không sync, khi backup bật. Vì vậy “không account/sync của Fokus” không đủ để nói “dữ liệu không bao giờ rời thiết bị”. [Nguồn S1](https://developer.android.com/identity/data/autobackup), [S2](https://support.apple.com/en-us/108770).

Đề nghị ngôn ngữ baseline: “Fokus lưu dữ liệu học trên thiết bị này, không cung cấp tài khoản hay đồng bộ. Sao lưu/chuyển máy của hệ điều hành có thể xử lý dữ liệu tùy cài đặt và hỗ trợ. Fokus không bảo đảm khôi phục khi mất máy, xóa dữ liệu hoặc cài lại.” Đây là **PROPOSED** thông điệp; phải khớp cấu hình thực mới dùng được.

**OPEN quyết định sản phẩm trước triển khai:** cho phép nội dung phiên tham gia backup/transfer của OS khi người dùng đã bật (khuyến nghị, để giữ cơ hội phục hồi nhưng không hứa); hoặc chủ động loại trừ ở nơi nền tảng hỗ trợ để tăng riêng tư nhưng chấp nhận nguy cơ mất dữ liệu. Không mặc định “local” chọn hộ chính sách. Không thêm cloud/account/export vào baseline để che bất định này.

Phân biệt AC/failure: (a) mất thiết bị mà không có bản sao hợp lệ: app không có kênh phục hồi; (b) restore bản cũ: không tuyên bố khôi phục mọi chỉnh sửa mới, không tự hoàn tất phiên cũ đang mở; (c) xóa phiên/xóa toàn bộ trong app: sau xác nhận thành công không còn thấy trong dữ liệu app hiện tại, giữ nguyên dữ liệu còn lại theo phạm vi; (d) xóa app/xóa dữ liệu OS và offload/restore có hành vi riêng, phải kiểm trên matrix hỗ trợ trước khi viết hướng dẫn cụ thể; (e) bản backup lịch sử có thể tái xuất dữ liệu cũ khi restore, nên “xóa vĩnh viễn khỏi mọi nơi” không được hứa. Fokus không có thẩm quyền xóa mọi backup của OS. Trạng thái dữ liệu cũ khi restore không là đồng bộ hay gộp hai máy.

## TP7 — sửa, xóa và dữ liệu sai/hỏng

Cho sửa ghi chú hoặc tự đánh giá là hợp lý nhưng không được vô tình sửa tiêu chí đã áp dụng rồi trình bày như tiêu chí ban đầu. **PROPOSED:** tiêu chí/đích của phiên sau bắt đầu giữ là bối cảnh phiên; nếu user phải sửa lỗi gõ, thể hiện đã sửa, không dùng revision để khẳng định tiêu chí được đặt trước. Quy tắc mức sửa cho phép cần Strategist quyết định; không yêu cầu dựng audit hệ thống.

Xóa một phiên đang mở cần nói rõ xóa phần đã nhập và kết thúc phiên mở; xóa toàn bộ cần hiển thị rõ cả phiên đang mở/lịch sử bị xóa, quyền hủy trước xác nhận. Nếu thao tác thất bại, không báo xóa thành công. Không yêu cầu nhập tài khoản/mật khẩu vốn không tồn tại. Sau xóa thành công không còn tổng hợp đếm phiên đó. Không mặc định undo/bản thùng rác vì đó là retention thêm cần quyết định riêng.

## TP8 — riêng tư/bảo mật ở mức sản phẩm

Baseline văn bản tự chọn, tối thiểu đích/tiêu chí/kết quả/gap/trạng thái; không đòi tên thật, trường, điểm, tuổi, danh bạ, vị trí, camera/mic hoặc usage. Không có nội dung học gửi tới AI, analytics, quảng cáo hay dịch vụ Fokus trong baseline đề xuất. Nếu có telemetry về sau là quyết định phạm vi và thông báo riêng; không ngầm thêm SDK. Không đưa nội dung đích/ghi chú lên thông báo/màn khóa trong baseline manual. Tôn trọng bảo vệ/khóa thiết bị; không hứa mã hóa đầu-cuối, ẩn khỏi người đang cầm máy đã mở khóa, hay bảo mật tuyệt đối. Thông tin debug/support không nên chứa nguyên văn nội dung học mặc định.

AC: có thể hoàn tất lần đầu không cấp quyền nhạy cảm; lỗi lưu không lộ nội dung sang log/support mà chưa có quyết định; tài liệu riêng tư phân biệt dữ liệu app và OS backup. **NOT RUN:** kiểm lưu trữ, lưu lượng mạng, log, privacy manifests/store disclosures hay audit bảo mật. Product quyết định dữ liệu/retention/backup/copy; Dev Studio chứng minh những cam kết này trên sản phẩm thật.

## TP9 — trợ năng và chất lượng có thể kiểm, không bịa số

Toàn bộ vòng chính dùng được với VoiceOver/TalkBack và chữ lớn; focus đọc được chuyển tới lỗi và nút hành động liên quan; nhãn kết quả không chỉ dùng màu; cỡ chữ lớn không che/làm mất nút đóng/lưu; nhập tiếng Việt có dấu và xuống dòng không mất nội dung; trạng thái lưu/lỗi được đọc hiểu, không chỉ toast thoáng qua. Không ép thời hạn nhập đối chiếu, rung/âm thanh hay chuyển động để hoàn tất. Đây là **PROPOSED AC**, không phải WCAG certification hay đã test.

NFR đề nghị: vòng chính không phụ thuộc mạng; save semantics TP3 và recovery TP4 là invariants; lỗi phải có đường quay lại/thử lại; thay đổi bản app không âm thầm mất dữ liệu đã lưu; dữ liệu không đọc được không bị ghi đè. **OPEN:** OS minimum, thiết bị chuẩn/thấp, dung lượng và số phiên cam kết, độ dài văn bản, ngưỡng thời gian mở/lưu, mức pin và matrix trợ năng. Product chọn trải nghiệm/cohort/giới hạn có lý do; Dev Studio khảo sát thiết bị và đo để đề xuất ngưỡng rồi Founder chốt. Không điền “<2s”, “99.9%”, RAM hay OS version từ trí nhớ.

## TP10 — handoff: ai quyết định, ai phải chứng minh

Product/Founder cần chốt: manual hoặc timer; semantics lưu nháp; nghĩa kết quả và kết thúc/bỏ phiên; mức sửa sau bắt đầu; giữ/xóa dữ liệu; OS backup policy và thông điệp mất dữ liệu; nền tảng/cohort ưu tiên và tiêu chí chất lượng. Dev Studio chỉ sau ủy quyền triển khai riêng mới xác minh: ghi nguyên vẹn/duplicate/restart/storage-full/corruption; offline sau khởi động lạnh; dữ liệu qua update/backup/restore và các khác biệt OS/OEM; network/log/privacy; VoiceOver/TalkBack/chữ lớn; notification/time nếu có; matrix và performance đo thực. Tài liệu public chỉ hỗ trợ giới hạn nền tảng; không chứng minh app/access/account đã có.

Trước → sau so với council cũ: local text-only vẫn là đường khả thi hẹp (**INFERENCE**, không đổi thành VERIFIED). Làm rõ thêm OS backup khiến lời hứa “local” cần tách khỏi “không có bản sao cloud”; làm rõ nguyên vẹn và thao tác lặp khiến “lưu được” không đủ làm AC. Manual session giữ cơ chế học mà loại dependency timer khỏi baseline; không nâng confidence về hiệu quả học/thương mại.

## Source-refresh receipt và giới hạn

Ngày truy cập: 22/11/2026 (Asia/Ho_Chi_Minh). 2/4 query dùng; 2/6 logical primary documents dùng; canonical open không tính thêm document. Không dùng market/news/nguồn thứ cấp trong findings. Search result phụ không được coi là nguồn đã kiểm.

- Query 1 exact: `site.developer.android.com identity data autobackup Android 12 device to device transfer allowBackup manufacturers`
- Query 2 exact: `site.support.apple.com iCloud backup includes app data delete app remove backup iPhone`
- S1 canonical: https://developer.android.com/identity/data/autobackup — opened full current page. VERIFIED docs: auto participation/default scope, điều kiện và hạn chế backup, cấu hình/cloud-vs-transfer khác nhau. Không kiểm implementation; không suy cross-platform transfer là tính năng Fokus.
- S2 canonical: https://support.apple.com/en-us/108770 — opened; trang ghi Published May01,2025. VERIFIED docs: dữ liệu app thuộc iCloud Backup, khác sync, user có thể dừng backup app. Không kiểm bản sao hiện có hay restore app cụ thể.

Device/app/offline/save/recovery/permission/OS-backup/assistive-technology/security/performance đều **NOT RUN**. Không có phần mềm được viết để kiểm. Không nêu chi phí, thời gian lịch, quyền account hay API được cấp. Còn2queries/4documents trong allocation kỹ thuật; trả về CIO nếu không cần follow-up.
