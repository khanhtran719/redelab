# technical-advisor — immutable R1

```json
{
  "id": "10d78682-5049-4af6-ab38-d882a7fb7e1e",
  "agentId": "10d78682-5049-4af6-ab38-d882a7fb7e1e",
  "sessionId": "7d889320-b711-43ea-9c96-81b3ac60b712",
  "workspace": "/Users/trankhanh/MyFolder/innovation-lab",
  "continuationOf": null,
  "title": "Fokus R1 mobile feasibility",
  "status": "completed",
  "createdAt": "2026-11-20T10:17:06.182Z",
  "threadId": "01a1f878-f425-7b90-90d8-fdf5dd8d6eaf",
  "archived": false,
  "error": null,
  "attempts": 1,
  "toolsetVersion": 2,
  "startedAt": "2026-11-20T10:20:38.696Z",
  "retryAt": null,
  "warnings": [
    "Tool hub_fetch_url: web_http_404"
  ],
  "endedAt": "2026-11-20T10:24:00.338Z",
  "promptBytes": 3437,
  "outputLength": 17280,
  "offset": 0,
  "nextOffset": null
}
```

Tôi sẽ kiểm tra hướng dẫn dự án và tài liệu chính thức của Apple/Android, tập trung vào quyền chặn ứng dụng, giới hạn chạy nền và gánh nặng vận hành. Kết quả sẽ phân biệt rõ khả năng được tài liệu mô tả với quyền truy cập và hành vi chưa được kiểm chứng trên thiết bị.

Tôi đang áp dụng skill `feasibility-assessment`. Điểm cần làm rõ nhất là sự khác biệt giữa một phiên tập trung tự nguyện và lời hứa chặn ứng dụng: hướng chặn phụ thuộc vào quyền hệ điều hành, chính sách cửa hàng và khả năng người dùng thu hồi quyền.

Apple mô tả quyền tự quản lý Screen Time từ iOS 16, nhưng người dùng vẫn có thể thu hồi quyền và xóa ứng dụng. Google Play cũng không cấm toàn bộ cách dùng Accessibility ngoài mục đích trợ năng, song yêu cầu khai báo, xét duyệt và đồng thuận rõ ràng. Hai điểm này chưa đủ để hứa “chặn không thể vượt qua” trên cả hai nền tảng.

**Gửi CIO — SES-20261120-04, vòng R1, Technical Feasibility Advisor.**

**Kết luận:** hướng ít bất định kỹ thuật nhất là phiên tập trung tự nguyện → người dùng ghi nhận kết quả → xem lại lịch sử; có thể bổ sung phần thưởng đơn giản trên thiết bị. Chặn ứng dụng cần đánh giá riêng từng nền tảng. Chưa có căn cứ để hứa chặn không thể vượt qua, tương đương iOS/Android hoặc chứng minh người dùng thực sự tập trung.

Đây là nghiên cứu độc lập, chỉ đọc; không sửa tệp hay thực hiện tích hợp. `VERIFIED` dưới đây nghĩa là đã đọc nguồn hỗ trợ phát biểu, **không phải đã có entitlement, được cửa hàng duyệt hoặc chạy thử API**.

**R1-T-01 — Ranh giới workflow khả thi nhất**

`INFERENCE — MEDIUM`: người dùng chọn một việc và thời lượng → bắt đầu phiên → rời hoặc giữ ứng dụng mở → quay lại xác nhận hoàn thành/dừng sớm → ghi một kết quả ngắn → xem lịch sử. Giá trị cốt lõi không cần biết họ đã mở ứng dụng nào.

| Hướng | Phân loại khả thi | Ranh giới nhỏ nhất và phần loại trừ |
|---|---|---|
| Timer + phản tư kết quả | **Cả hai nền tảng, INFERENCE** | Phiên cá nhân và lịch sử trên thiết bị; thông báo kết thúc là tính năng phụ thuộc quyền. Không coi thời gian trôi qua là bằng chứng làm việc. |
| Gamification | **Cả hai nền tảng, INFERENCE** | Điểm/phần thưởng dựa trên phiên tự khai, hoạt động ngoại tuyến. Loại trừ tiền thưởng, vật phẩm giao dịch, chống gian lận và bảng xếp hạng cần xác minh. |
| Chặn xao nhãng iOS | **Đặc thù nền tảng, có điều kiện quyền** | Người dùng tự cấp quyền và chọn phạm vi hạn chế. Không hứa chống gỡ ứng dụng hoặc chống thu hồi quyền. |
| Chặn xao nhãng Android | **Có điều kiện chính sách; hiệu lực chặn UNKNOWN** | Chính sách Accessibility cho phép một số cách dùng ngoài trợ năng nhưng không xác nhận cơ chế chặn cụ thể của Fokus Time. |
| Đồng hành xã hội | **Cả hai nền tảng ở mức workflow, INFERENCE** | Một người quen nhận kết quả người dùng chủ động chia sẻ; không cần phòng trực tiếp, chat hay theo dõi ứng dụng đã mở. |
| Chặn cứng đồng nhất + xác minh tập trung + phòng trực tiếp | **Không phù hợp ranh giới MVP nhỏ hiện tại, INFERENCE** | Kết hợp quá nhiều bất định quyền, thời gian thực, chống gian lận và hỗ trợ vận hành trước khi có bằng chứng nhu cầu. |

Phương án đơn giản hơn cho trách nhiệm xã hội là người dùng chủ động gửi tóm tắt qua kênh sẵn có. Khả năng và quyền của luồng chia sẻ cụ thể chưa được kiểm tra trong lượt này.

**R1-T-02 — iOS có hai cửa quyền riêng biệt**

- `VERIFIED — HIGH`: Apple yêu cầu entitlement `com.apple.developer.family-controls` trước khi gọi các phương thức authorization liên quan; trước khi gửi ứng dụng lên App Store phải **xin phép sử dụng entitlement**. Đây là yêu cầu phía nhà phát triển, khác với đồng ý của người dùng. [T-SRC-01, mục Discussion]
- `VERIFIED — HIGH`, trong phạm vi WWDC22: từ **iOS 16**, người dùng độc lập có thể tự cấp quyền Family Controls. Họ có thể thu hồi quyền trong Settings; chế độ này không áp dụng hạn chế ngăn xóa ứng dụng hay đăng xuất iCloud của trường hợp parental control. [T-SRC-02, phần Family Controls]
- `UNKNOWN`: Fokus Time có được duyệt entitlement hay không; thời gian xét duyệt, điều kiện cho các extension và tính phù hợp với bản sản phẩm cụ thể. Không có tài khoản hay hồ sơ nào được kiểm tra.

`INFERENCE — HIGH`: nếu giá trị thương mại phụ thuộc vào “đã bắt đầu là không thể thoát”, hướng tự quản lý trên iOS không đáp ứng lời hứa đó theo tài liệu đã đọc. Nếu giá trị là tạo thêm trở ngại tự nguyện, cơ sở khả thi tốt hơn.

**R1-T-03 — ManagedSettings/DeviceActivity cung cấp hạn chế và tín hiệu sử dụng, không chứng minh đầu ra công việc**

`VERIFIED — HIGH`, phạm vi tài liệu WWDC22 [T-SRC-02]:

- Family Controls sử dụng token không lộ định danh trực tiếp để đại diện ứng dụng/website.
- ManagedSettings áp dụng hạn chế và màn hình che truy cập; nhiều store cùng áp dụng thì hạn chế chặt hơn thắng.
- DeviceActivity phản hồi khi bắt đầu/kết thúc khoảng giám sát và khi đạt ngưỡng sử dụng; báo cáo sử dụng được trình bày qua extension dành riêng.
- Tài liệu iOS 16 nêu tối đa **50 ManagedSettingsStore có tên mỗi process**. Đây là giới hạn store trong nguồn đó, không phải quota phiên, quota người dùng hay cam kết callback đúng từng giây.

`UNKNOWN`: thời lượng lịch ngắn nhất phù hợp với phiên Fokus Time; số lịch/ngưỡng giám sát được hỗ trợ hiện hành; độ trễ callback; độ đầy đủ của báo cáo; hành vi ngoại tuyến và sau khởi động lại trên các phiên bản mục tiêu.

Đáng chú ý, T-SRC-01 hiện liên kết tới entitlement **App & Website Usage** bổ sung. Chưa đọc trang này do giới hạn nguồn, nên **không kết luận tuyệt đối rằng Apple không cho truy cập dữ liệu sử dụng**, cũng không giả định có thể đưa dữ liệu đó lên máy chủ hoặc chia sẻ cho bạn bè.

`INFERENCE — HIGH`: số phút trong ứng dụng bị hạn chế không xác nhận chất lượng công việc, việc dùng thiết bị khác hay kết quả ngoài điện thoại. Phản tư kết quả vẫn là tự khai.

**R1-T-04 — Android Accessibility là phụ thuộc xét duyệt, không phải quyền chặn mặc định**

`VERIFIED — HIGH` [T-SRC-03]:

- Google Play không cấm toàn bộ ứng dụng ngoài lĩnh vực trợ năng dùng AccessibilityService; có quy trình khai báo và phê duyệt.
- Ứng dụng không đủ điều kiện `isAccessibilityTool` phải giải thích nổi bật ngay trong ứng dụng: dữ liệu truy cập/thu thập, mục đích sử dụng/chia sẻ và lấy đồng thuận chủ động.
- Công cụ trợ năng phải có mục đích chính là hỗ trợ người khuyết tật. Một ứng dụng năng suất thông thường không tự đủ điều kiện chỉ vì có ích cho một nhóm người dùng này.
- Tự động hóa theo quy tắc cố định được phân biệt với hành động tự chủ bị cấm; thay đổi cách sử dụng API phải cập nhật khai báo.

`UNKNOWN`: cơ chế nào đủ để chặn đáng tin cậy các ứng dụng mục tiêu, trên hãng máy/phiên bản Android nào; quyền bổ sung cần thiết; liệu hành vi cụ thể có được Google Play duyệt. Nguồn chính sách không chứng minh khả năng kỹ thuật khóa ứng dụng.

`INFERENCE — MEDIUM`: hướng này có gánh nặng hỗ trợ cao hơn timer: hướng dẫn quyền, xử lý quyền mất hiệu lực, khác biệt thiết bị và cập nhật hồ sơ chính sách. Không nên suy diễn rằng một API sử dụng được trong phát triển sẽ được chấp nhận khi phân phối.

**R1-T-05 — Độ chính xác thời lượng khác với thời điểm thông báo tới người dùng**

`VERIFIED — HIGH` [T-SRC-04]:

- Android có alarm hoạt động ngoài vòng đời ứng dụng, giúp tránh cần chạy dịch vụ liên tục.
- Alarm không chính xác trên Android 12+ có thể được giao trong vòng một giờ sau mốc yêu cầu khi không có hạn chế tiết kiệm pin; điều kiện pin/Doze làm thay đổi bảo đảm này. Đây không phải lựa chọn đủ để hứa chuông kết thúc phiên đúng giây.
- Exact alarm có điều kiện quyền và mục đích sử dụng. `SCHEDULE_EXACT_ALARM` do người dùng cấp, có thể bị thu hồi và không được cấp sẵn cho cài đặt mới nhắm Android 13+.
- Thu hồi quyền trên làm dừng ứng dụng và hủy exact alarm tương lai. Tắt thiết bị cũng hủy alarm mặc định.
- Đồng hồ elapsed realtime tính cả thời gian ngủ từ lúc khởi động, khác đồng hồ lịch có thể bị người dùng chỉnh. Exact alarm và đánh thức thiết bị làm tăng tiêu thụ tài nguyên.

Nguồn có ngoại lệ dùng `OnAlarmListener`; điều đó chưa chứng minh một lời nhắc vẫn tồn tại sau khi process chết. Trang cũng có ví dụ lặp cũ không nhất quán với phát biểu rằng từ Android 4.4 mọi repeating alarm đều không chính xác; không dùng ví dụ đó để cam kết thời điểm giao.

`INFERENCE — MEDIUM`: timer cần giữ được ý nghĩa “phiên đã trôi qua bao lâu” khi quay lại ứng dụng, kể cả khi âm báo không tới. Không cần giả định mỗi giây đều có tác vụ nền chạy. Sau reboot hoặc thay đổi đồng hồ, phiên không đủ bằng chứng nên được đánh dấu gián đoạn/chờ người dùng xác nhận.

`UNKNOWN`: quyền thông báo hiện hành trên cả hai nền tảng; hành vi iOS khi Focus/tắt âm/khóa màn hình; toàn bộ quy tắc foreground service Android; sai số và pin trên thiết bị thật. Không gộp quyền alarm với quyền hiển thị hoặc phát âm thông báo.

**R1-T-06 — Dữ liệu, quyền và phụ thuộc**

| Nhu cầu | Dữ liệu tối thiểu | Quyền/phụ thuộc | Đánh giá ngoại tuyến và phần còn thiếu |
|---|---|---|---|
| Timer/phản tư | Mốc phiên, thời lượng, trạng thái, ghi chú tự nhập | Lưu trữ trên thiết bị; quyền thông báo nếu dùng | `INFERENCE`: workflow cốt lõi dùng ngoại tuyến; phục hồi sau gián đoạn chưa thử. |
| Game đơn giản | Lịch sử phiên, điểm, lựa chọn người dùng | Không cần dữ liệu ứng dụng khác | `INFERENCE`: ngoại tuyến phù hợp; dễ sửa/gian lận nên không dùng làm bằng chứng khách quan. |
| Chặn iOS | Token lựa chọn, lịch/ngưỡng, trạng thái authorization | Apple entitlement + người dùng cấp quyền; FamilyControls/ManagedSettings/DeviceActivity | `VERIFIED` về cơ chế trong tài liệu; `UNKNOWN` về quyền cho Fokus Time, độ trễ và độ bền trạng thái thực tế. |
| Chặn Android | Lựa chọn ứng dụng và tín hiệu tối thiểu cần cho cơ chế được chọn | Có thể cần Accessibility và quyền khác; Google Play review | `UNKNOWN` về tập quyền đủ và mức chặn; không giả định cần đọc toàn bộ nội dung màn hình. |
| Đồng hành tích hợp | Danh tính tối thiểu, quan hệ đồng ý, trạng thái chia sẻ | Dịch vụ đồng bộ/thông báo chưa chọn | `INFERENCE`: phiên cá nhân vẫn ngoại tuyến, xác nhận từ người khác cần mạng; hạn mức, giá và thời gian giao `UNKNOWN`. |

**R1-T-07 — Chi phí, bảo trì và vận hành nhỏ**

`HYPOTHESIS`, chỉ là giả định tải để so sánh, không phải dự báo tăng trưởng hay báo giá:

- **Bản chỉ lưu cục bộ:** nếu không tài khoản, máy chủ, analytics hay đồng bộ, chi phí máy chủ do nhà phát triển vận hành là **0 USD/tháng theo ranh giới đó**. Đây không phải tổng chi phí sản phẩm: phí cửa hàng, thiết bị kiểm thử, hỗ trợ và công bảo trì chưa được định giá.
- **Bản xã hội:** giả sử 1.000 người hoạt động/tháng × 20 ngày × 1–3 phiên/ngày ⇒ **20.000–60.000 phiên/tháng**. Nếu mỗi phiên tạo 3 sự kiện và tối đa 2 lần gửi thông báo cho một người đồng hành ⇒ **60.000–180.000 sự kiện**, tối đa **40.000–120.000 lượt gửi/tháng**, chưa gồm đọc lại, thử lại và đa thiết bị. Với giả định 4 KB dữ liệu/phiên: khoảng **80–240 MB dữ liệu thô/tháng**, trước bản sao và chỉ mục.
- **Giá tiền bản xã hội: UNKNOWN.** Chưa chọn nhà cung cấp hoặc đọc pricing, nên không gán một dải USD thiếu căn cứ. Các đơn vị trên là đầu vào cần dùng để định giá tiếp.
- **Công hỗ trợ:** một kịch bản 10–50 ca/tháng × 15 phút/ca tương đương **2,5–12,5 giờ/tháng**, chưa gồm sửa lỗi. Đây là phép tính nhạy cảm theo tải giả định; chưa có tỷ lệ ticket quan sát được.

`INFERENCE — MEDIUM`: timer/game cục bộ có gánh bảo trì tương đối thấp hơn; chặn hai nền tảng cần năng lực native về quyền, lifecycle và kiểm tra thiết bị. Lựa chọn framework dùng chung không loại bỏ hai tập chính sách hệ điều hành. Trình độ và khả năng kiểm thử của nhóm hiện là `UNKNOWN`.

Vận hành phải có cách xử lý phiên mất trạng thái, quyền bị thu hồi, hạn chế không được gỡ như kỳ vọng, thông báo trễ và xác nhận xã hội trùng/mất. Với đồng hành tích hợp, thêm yêu cầu hỗ trợ tài khoản, hủy quan hệ, xóa dữ liệu và xử lý hành vi gây phiền. Không cần đưa chat, nhóm công khai hoặc giám sát thời gian thực vào ranh giới đầu.

**R1-T-08 — Riêng tư, khả năng tiếp cận và điều kiện loại bỏ**

`INFERENCE`: ghi chú công việc và thói quen dùng ứng dụng có thể tiết lộ lịch sinh hoạt hoặc nội dung riêng tư. Phạm vi ít rủi ro hơn là lưu ghi chú cục bộ, chia sẻ tối thiểu theo từng lựa chọn, không thu nội dung màn hình chỉ để chứng minh một phiên đã hoàn tất. Quyền Accessibility trên Android không đồng nghĩa giao diện Fokus Time đã tiếp cận được.

`UNKNOWN`: thị trường pháp lý, độ tuổi người dùng, thời hạn lưu dữ liệu, luồng xóa/xuất dữ liệu và nghĩa vụ khi chia sẻ với bên thứ ba. Chưa có kết luận pháp lý. VoiceOver/TalkBack, cỡ chữ lớn, giảm chuyển động và cách báo kết thúc không chỉ dựa vào màu/âm thanh đều chưa được kiểm tra.

Các điều kiện làm thay đổi khuyến nghị:

- Nếu chặn là giá trị duy nhất nhưng entitlement/Play review không khả dụng: hướng đó bị chặn về khả thi phân phối.
- Nếu cần đồng nhất mức chặn hoặc chống người dùng tự thoát: bằng chứng hiện tại không đáp ứng.
- Nếu cần chuông nền đúng giây trong mọi trạng thái quyền/pin: lời hứa vượt bằng chứng đã có.
- Nếu cần dữ liệu sử dụng thật để chấm điểm chung: phải xác minh quyền truy cập/chia sẻ trước; không thay bằng giả định.
- Nếu nhóm không có khả năng bảo trì native và kiểm tra nhiều thiết bị: giảm phạm vi xuống timer/phản tư/game cục bộ hoặc nghiên cứu một nền tảng trước.

**R1-T-09 — Bằng chứng cần bổ sung, chưa thực hiện**

1. Làm rõ hồ sơ entitlement phân phối Apple cho ứng dụng và extension; tài liệu dẫn tới https://developer.apple.com/contact/request/family-controls-distribution — chưa mở biểu mẫu hay gửi yêu cầu.
2. Đọc giới hạn DeviceActivity hiện hành và entitlement mới: https://developer.apple.com/documentation/bundleresources/entitlements/com.apple.developer.family-controls.app-and-website-usage — chưa đọc nội dung trang.
3. Đọc quyền thông báo Android tại https://developer.android.com/develop/ui/views/notifications/notification-permission và giới hạn foreground service tại https://developer.android.com/develop/background-work/services/fgs/restrictions-bg-start — chưa đọc.
4. Đọc lịch local notification iOS tại https://developer.apple.com/documentation/usernotifications/scheduling-a-notification-locally-from-your-app — chưa đọc.
5. Nếu có phạm vi kiểm chứng kỹ thuật được giao riêng: quan sát khóa màn hình, process bị kết thúc, reboot, đổi giờ, tiết kiệm pin, từ chối/thu hồi quyền và ngoại tuyến. Cần đo riêng sai số thời lượng, độ trễ thông báo, trạng thái gỡ hạn chế và pin; lượt nghiên cứu này chưa chạy bất kỳ kiểm tra thiết bị nào.

Không có finding của đồng nghiệp được cung cấp; chưa thực hiện phản biện chéo và không ghi nhận đồng thuận hội đồng.

**Sổ nguồn và giới hạn nghiên cứu**

Đã đọc `AGENTS.md`, skill `feasibility-assessment`, `protocols/evidence-policy.md`, backlog và Founder decision log. Web công khai sử dụng được. Truy cập ngày **2026-11-20, Asia/Ho_Chi_Minh**; tổng thời gian nghiên cứu trong giới hạn 5 phút.

| ID | Nguồn chính thức và URL chính xác | Phạm vi, ngày và hạn chế |
|---|---|---|
| **T-SRC-01** | Apple, *Family Controls entitlement*: https://developer.apple.com/documentation/bundleresources/entitlements/com.apple.developer.family-controls ; nội dung đọc qua bản dữ liệu cùng tài liệu: https://developer.apple.com/tutorials/data/documentation/bundleresources/entitlements/com.apple.developer.family-controls.json | Trang HTML chỉ trả tiêu đề; bản JSON có phần Discussion xác nhận yêu cầu entitlement và xin phép trước App Store. Không thấy ngày sửa nội dung; không chứng minh tài khoản được duyệt. |
| **T-SRC-02** | Apple, *What's new in Screen Time API*, WWDC22: https://developer.apple.com/videos/play/wwdc2022/110336/ | Đã đọc transcript; nội dung ra mắt iOS 16, năm 2022. Nguồn chính thức nhưng không phải toàn bộ hợp đồng API hoặc giới hạn hiện hành năm 2026. |
| **T-SRC-03** | Google Play, *Use of the AccessibilityService API*: https://support.google.com/googleplay/android-developer/answer/10964491?hl=en | Đã đọc chính sách/khai báo. Không thấy ngày cập nhật; không xác nhận khả năng chặn hay phê duyệt cho Fokus Time. |
| **T-SRC-04** | Android Developers, *Schedule alarms*: https://developer.android.com/develop/background-work/services/alarms ; URL ban đầu chuyển hướng: https://developer.android.com/develop/background-work/services/alarms/schedule | Ghi cập nhật **2026-10-28 UTC**. Đã đọc nội dung liên quan và phần cuối; có ví dụ cũ mâu thuẫn như nêu ở R1-T-05. Chưa đọc trang chính sách Play liên kết cho `USE_EXACT_ALARM`. |

**Phạm vi tìm kiếm:** 2 truy vấn tiếng Anh qua Bing RSS, nhắm tài liệu Apple; không lọc quốc gia và không dùng snippet làm chứng cứ:

1. `site:developer.apple.com "Family Controls" "distribution" "request" entitlement` — kết quả trả về không liên quan.
2. `Apple Family Controls entitlement distribution request developer` — đã gọi nhưng kết quả không được lưu vào đầu ra nghiên cứu; không dùng làm bằng chứng.

**Số nguồn:** 4 tài liệu gốc có nội dung được kiểm tra; HTML/JSON của T-SRC-01 tính là cùng tài liệu. Hai URL thử không có nội dung hợp lệ, không tính là nguồn chứng cứ: `https://developer.apple.com/documentation/familycontrols/distributing-your-app-with-the-family-controls-capability` trả HTTP 404; `https://developer.apple.com/help/account/capabilities/requesting-access-to-family-controls/` trả trang Page Not Found. Dừng thu thập ở trần nguồn; các mục bổ sung giữ `UNKNOWN`.

Khuyến nghị này phục vụ lựa chọn cơ hội của Founder; không phải quyết định chọn sản phẩm, quyền triển khai hay xác nhận sẵn sàng production.

