# Technical R1 — đánh giá nền tảng độc lập

SES-20261121-01 · 2026-11-21, Asia/Ho_Chi_Minh. Vai trò technical-advisor; runtime task `/root/fokus_technical_sol`; mô hình theo cấu hình spawn của CIO, không tự đổi. Chỉ nghiên cứu tài liệu; chưa chạy integration, xin entitlement, cài app, thử thiết bị hay nộp store. Phạm vi ban đầu độc lập với ứng viên của các vai trò khác. Dùng skill feasibility-assessment và evidence/debate policy. Không có quyền triển khai.

## Kết luận có điều kiện

**T1 — INFERENCE, MEDIUM: BOTH-PLATFORM FEASIBLE** cho vòng tự quản lý nhỏ nhất: người dùng đặt việc/ý định, bắt đầu phiên, quay lại xem thời lượng/trạng thái, tự ghi kết quả, xem lịch sử cục bộ. Không cần đọc dữ liệu app khác để cung cấp vòng này. Đây là đánh giá tính khả thi, không phải bằng chứng nhu cầu, retention hay chất lượng sản phẩm đã đạt. Căn cứ giới hạn hẹn giờ/notification ở T-S5–8; các phần ghi tay/lịch sử là giả định chức năng thông thường chưa kiểm thử.

**T2 — VERIFIED trong docs; CONDITIONAL khi phân phối, HIGH về nội dung tài liệu:** iOS cho phép individual authorization từ iOS 16; ManagedSettings có shielding. Người dùng vẫn có thể thu hồi; các hạn chế ngầm về xóa app/iCloud sign-out của parental mode không áp dụng cho individual mode. T-S1, 02:35–04:10, 05:xx–07:02. Trước App Store phải xin phép entitlement Family Controls riêng (T-S2). Chưa biết tài khoản/ứng dụng Fokus được cấp hay review duyệt; không gọi đây là blocker tuyệt đối hoặc đã bảo đảm quyền.

**T3 — INFERENCE từ API reference, HIGH về giới hạn bằng chứng:** Android UsageStats là đường quan sát usage, không phải chứng cứ về API chặn app tùy ý. Quyền usage của phần lớn phương thức còn phải được người dùng bật trong Settings; một số truy vấn có giới hạn thời gian hoặc trả null trước unlock (T-S3). Không suy từ việc đo usage sang khả năng ép khóa.

**T4 — CONDITIONAL, MEDIUM:** Accessibility có đường chính sách cho app không phải accessibility tool nhưng phải khai báo, disclosure, consent và approval. T-S4 phân biệt automation theo quy tắc người đặt với hành động tự chủ bị cấm; không thể kết luận mọi blocker đều bị cấm, cũng không thể bảo đảm blocker cụ thể được duyệt. Không gắn cờ trợ năng chỉ vì sản phẩm mang nhãn productivity/ADHD. Chưa kiểm chứng cơ chế chặn kỹ thuật, khả năng thoát hay ứng xử trên từng hãng.

**T5 — INFERENCE, HIGH về phân biệt yêu cầu:** thời lượng đúng khi mở lại khác chuông báo đúng lúc. Một deadline/trạng thái được lưu bền cho phép khôi phục hiển thị sau app bị ngừng, nhưng không chứng minh callback luôn chạy nền. Phải định nghĩa pause, kết thúc sớm, đổi giờ, reboot và phiên bỏ dở; nếu mơ hồ thì không nên tự tính thành phiên thành công. T-S5, T-S7–8 là tiền đề hạn chế thực thi nền; cách tái dựng thời lượng này chưa được thực thi.

**T6 — VERIFIED trong Android docs, HIGH:** exact alarms có quyền/điều kiện; quyền SCHEDULE có thể bị thu hồi và alarm tương lai bị hủy, không mặc định cấp cho fresh installs target 33+. Reboot hủy alarms nếu không khôi phục. Inexact không đáp ứng cam kết phút/giây chính xác; Doze còn hoãn công việc chuẩn (T-S5, T-S7). Trang T-S5 có đoạn cũ gợi ý repeating exact mâu thuẫn với khẳng định repeating đều inexact; không dùng đoạn đó làm cam kết.

**T7 — VERIFIED, HIGH trong Android docs; UNKNOWN về hiện trạng iOS đầy đủ:** Android 13+ cần POST_NOTIFICATIONS cho thông báo không ngoại lệ; từ chối sẽ chặn và fresh installs mặc định tắt (T-S6). Apple archive xác nhận OS có thể giao local notification khi app không chạy (T-S8), nhưng nguồn này cũ, không đủ xác nhận toàn bộ permission/Focus/Scheduled Summary/battery trên iOS hiện hành. Không bảo đảm người dùng sẽ nghe hoặc nhìn thấy báo kết thúc.

**T8 — UNREALISTIC cho lời hứa MVP tự quản lý:** “không thể vượt qua, chính xác tuyệt đối, chặn mọi app/web trên cả hai OS, mọi máy” không có cơ sở. T2 có revocation rõ ràng; T4 và T6 còn conditional; việc người dùng có thể gỡ quyền không phải lỗi bảo mật cần tìm cách né. Một lời hứa hẹp như “hỗ trợ ngăn xao nhãng trên thiết bị/quyền được hỗ trợ, có đường dừng an toàn” còn khả thi có điều kiện.

**T9 — UNKNOWN:** độ phủ máy tại VN/SEA, OEM battery behavior, OS minimum hợp thị trường, work profile/multi-user, iPad/Android tablet, store availability theo vùng, ngôn ngữ, accessibility và chi phí hỗ trợ thực tế. Nguồn OS chung không xác minh các điều này. Cần mẫu thiết bị gắn đúng phân khúc, không lấy một máy chạy được làm parity.

**T10 — INFERENCE, MEDIUM:** nhóm nhỏ chịu được workflow T1 dễ hơn phạm vi blocker + sync + social. T2/T4/T6 kéo theo hai bộ quyền, store review, hỗ trợ recovery và kiểm tra thay đổi OS. Nếu giá trị chỉ xuất hiện khi anti-bypass mạnh hoặc parity tuyệt đối, đó là điều kiện thất bại của phạm vi nhỏ, không phải tính năng “thêm sau”.

## Ranh giới workflow và phụ thuộc

| Lớp | Phạm vi nhỏ nhất / quyền dữ liệu | Đánh giá |
|---|---|---|
| Phiên cục bộ | Ý định, thời điểm/trạng thái, kết quả do chính người dùng nhập; sửa/xóa được | BOTH-PLATFORM FEASIBLE, INFERENCE T1/T5; không chứng minh người dùng cần nó |
| Nhắc kết thúc | Local notification; quyền người dùng, trạng thái OS; cảnh báo trạng thái khi quyền thiếu | CONDITIONAL T6/T7; không hứa giao đúng giây |
| iOS shield | Chọn app/domain qua cơ chế Screen Time, individual auth + entitlement phân phối | PLATFORM-LIMITED và CONDITIONAL T2; không chống thu hồi |
| Android usage | Usage access rõ lý do; dữ liệu nhạy cảm về hành vi | CONDITIONAL T3; observation không phải blocking |
| Android blocking | Accessibility nếu cách dùng cụ thể phù hợp chính sách và được duyệt | CONDITIONAL/UNVERIFIED T4; cần capability riêng có phép ở phạm vi tương lai |
| Account, cloud, AI, nhóm, desktop, parental/MDM | Không cần cho vòng T1; tăng dữ liệu/đồng bộ/quyền/phục hồi | Ngoài baseline; chưa đánh giá là bắt buộc |

**HYPOTHESIS về lựa chọn đơn giản hơn:** timer/ghi chú không quyền nhạy cảm, hoặc hướng dẫn dùng giới hạn native hiện có, có thể đáp ứng đủ nhu cầu mà giảm permission abandonment. Chưa kiểm tra trực tiếp tính năng native hôm nay trong ngân sách này; cần so tác vụ thật, không mặc định app riêng vượt trội.

## Vận hành, riêng tư, truy cập và chi phí

- **INFERENCE:** phục hồi phải có đường thoát an toàn: phiên quá hạn, máy khởi động lại, đổi giờ, mất quyền, app bị dừng, báo đến trễ hoặc hai báo lặp. Không phạt hoặc tính thưởng từ callback đơn lẻ. Phải nói rõ dữ liệu nào mất khi xóa app/mất máy; baseline không hứa backup/sync.
- **INFERENCE:** ý định/công việc có thể chứa dữ liệu khách hàng; usage/Accessibility có thể mở rộng bề mặt truy cập hơn điều người dùng chấp nhận. Mặc định tối thiểu dữ liệu, tránh đưa tên việc vào màn khóa và tránh thu thập nội dung màn hình cho nhu cầu chỉ cần phiên. Apple dùng opaque tokens trong cơ chế Screen Time (T-S1); không suy token làm mọi hoạt động app tự động “an toàn”.
- **UNKNOWN về pháp lý:** cơ sở xử lý dữ liệu, thông báo quyền riêng tư/xóa dữ liệu, trẻ vị thành niên, chuyển dữ liệu quốc tế và nội dung công việc tại VN/SEA/các nước khác chưa được chuyên gia kiểm tra. Không quảng cáo chữa ADHD hay lợi ích y khoa từ đánh giá kỹ thuật này. Không cần mở nghiên cứu pháp lý rộng khi chưa chốt dữ liệu/địa lý.
- **HYPOTHESIS cần xác minh:** khả dụng với VoiceOver/TalkBack, cỡ chữ lớn, giảm chuyển động, tương phản, trạng thái không dựa mỗi màu và dừng/thoát bằng trợ năng; chưa có UI để kiểm. Quyền Accessibility dùng cho blocking khác chất lượng accessibility của giao diện.
- **Giả định chi phí, không phải báo giá:** baseline local không cần API tính tiền theo phút phiên; vẫn có chi phí account/store, phần cứng kiểm thử, support và công bảo trì. Các mức phí store hiện hành chưa được mở trong ngân sách nguồn nên ghi UNKNOWN. Đơn vị cần theo dõi: thiết bị × OS × trạng thái quyền, số ticket/100 người hoạt động/tháng, giờ xử lý mỗi đổi OS/review, dung lượng backup/người nếu bổ sung cloud. Không đưa USD hoặc số tuần giả chính xác. Nếu chưa có năng lực native cả hai OS, phải cộng chi phí học/hỗ trợ; năng lực đội hiện tại UNKNOWN.

## Bằng chứng nên thu tiếp — chỉ là đề xuất, chưa làm

1. Chốt nghĩa của “tập trung”, “phiên thành công”, quyền rút lui và ngưỡng báo trễ người dùng chấp nhận. Đo lợi ích tác vụ sau khi trừ thao tác nhập/quyền.
2. Nếu giá trị phụ thuộc blocker: xác minh entitlement/account và khả năng review theo workflow cụ thể; không coi docs chung là quyền tài khoản. Làm rõ cần chặn đến mức nào trước xin phạm vi thử kỹ thuật riêng.
3. Trong phạm vi thử tương lai được cấp riêng, so expected state với đồng hồ độc lập khi background, kill/force-stop, reboot, offline, battery saver/Doze, đổi giờ/timezone và revoke/deny từng quyền; tách sai thời lượng khỏi notification trễ. Kiểm tra thoát khẩn và phục hồi không double-count.
4. Chọn ma trận thiết bị từ phân khúc thực; kiểm trợ năng, máy cũ và ít nhất các OS/quyền làm thay đổi hành vi. Store review, battery measurements và app install đều NOT RUN hôm nay.

## Source ledger — nguồn sơ cấp đã mở mới

Mọi nguồn dưới truy cập **2026-11-21**. Ngày công bố/sửa không hiển thị ghi UNKNOWN, không lấy crawl date thay. Wordlim công cụ 200/source; tóm tắt hẹp, không trích dài.

| ID | Nguồn / URL | Ngày và locator / giới hạn |
|---|---|---|
| T-S1 | Apple, [What's new in Screen Time API](https://developer.apple.com/videos/play/wwdc2022/110336/) | WWDC22 (2022); transcript 02:35–04:10 và shielding example 05:xx–07:02; docs/demo lịch sử, không device test |
| T-S2 | Apple, [Family Controls entitlement](https://developer.apple.com/documentation/bundleresources/entitlements/com.apple.developer.family-controls) · [official Markdown](https://developer.apple.com/documentation/bundleresources/entitlements/com.apple.developer.family-controls.md) | UNKNOWN; Discussion lines 25–29; HTML đòi JS, đọc bản Markdown cùng nguồn, không phải quyền đã cấp |
| T-S3 | Google, [UsageStatsManager](https://developer.android.com/reference/android/app/usage/UsageStatsManager) | UNKNOWN; class overview/permissions và queryEvents/queryUsageStats; reference có API mới, không tự suy thiết bị cũ hỗ trợ |
| T-S4 | Google Play, [Use of AccessibilityService API](https://support.google.com/googleplay/android-developer/answer/10964491?hl=en) | UNKNOWN; automation guidance, disclosure, declarations; chính sách không phải phán quyết review Fokus |
| T-S5 | Google, [Schedule alarms](https://developer.android.com/develop/background-work/services/alarms) | Sửa 2026-10-28 UTC; permissions, exact/inexact, reboot; có đoạn repeating mâu thuẫn đã giữ ở T6 |
| T-S6 | Google, [Notification runtime permission](https://developer.android.com/develop/ui/compose/notifications/notification-permission) | Sửa 2026-10-28 UTC; redirect từ views URL; deny/new installation sections |
| T-S7 | Google, [Optimize for Doze and App Standby](https://developer.android.com/training/monitoring-device-state/doze-standby) | Sửa 2026-10-22 UTC; Doze restrictions và test guidance; không chứng minh OEM |
| T-S8 | Apple archive, [Scheduling and Handling Local Notifications](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/SchedulingandHandlingLocalNotifications.html) | Sửa 2018-06-04; opening paragraphs; cũ, không dùng cho bảo đảm delivery/current notification policy |

## Search receipt và điểm dừng

Ngày 2026-11-21; tiếng Anh, website Apple/Google; không nguồn riêng VN/SEA. Hai query thực chạy:

1. `site.developer.apple.com videos wwdc2022 110336 individual authorization Screen Time API revoke FamilyControls`
2. `site:developer.android.com UsageStatsManager PACKAGE_USAGE_STATS notification permission exact alarms schedule alarms`

**2/4 queries; 8/8 nguồn logic đã mở.** T-S2 HTML và Markdown là hai representation cùng tài liệu; không mở nội dung nguồn thứ chín. T-S6 redirect không tính thêm nguồn. Search snippets chỉ là leads; chỉ 8 nguồn trong ledger hỗ trợ kết luận. Đã đọc ledger SES-20261120-04 như leads; không gọi các nguồn cũ chưa mở lại là freshly verified. Không còn query cần thiết trong vòng initial; dừng nguồn để dành peer critique, không mở rộng architecture.

## Trạng thái peer work

R1 này được chốt trước nhận ứng viên của vai trò khác. Chưa có phản hồi cross-agent trong bản initial; CIO sẽ gửi critique có finding ID và phản hồi được append, không sửa lại ghi chú ban đầu.
