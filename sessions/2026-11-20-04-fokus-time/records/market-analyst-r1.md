# market-analyst — immutable R1

```json
{
  "id": "4bb53525-57c7-4553-8cbe-0e5d9929ccca",
  "agentId": "4bb53525-57c7-4553-8cbe-0e5d9929ccca",
  "sessionId": "7d889320-b711-43ea-9c96-81b3ac60b712",
  "workspace": "/Users/trankhanh/MyFolder/innovation-lab",
  "continuationOf": null,
  "title": "Fokus R1 competitor landscape",
  "status": "completed",
  "createdAt": "2026-11-20T10:16:03.185Z",
  "threadId": "01a1f874-bf8a-7fe1-8cf4-f92c7ffd4688",
  "archived": false,
  "error": null,
  "attempts": 1,
  "toolsetVersion": 2,
  "startedAt": "2026-11-20T10:16:03.187Z",
  "retryAt": null,
  "warnings": [
    "Tool hub_fetch_url: web_timeout",
    "Tool hub_fetch_url: web_http_404",
    "Tool hub_fetch_url: web_http_404",
    "Tool hub_fetch_url: web_timeout",
    "Tool hub_fetch_url: web_http_404",
    "Tool hub_fetch_url: web_http_404",
    "Tool hub_fetch_url: web_http_404",
    "Tool hub_fetch_url: web_http_404"
  ],
  "endedAt": "2026-11-20T10:20:38.693Z",
  "promptBytes": 3339,
  "outputLength": 18768,
  "offset": 0,
  "nextOffset": null
}
```

Tôi sẽ dùng skill market-intelligence để kiểm tra độc lập 11 sản phẩm, ưu tiên một trang chính thức hoặc trang cửa hàng cho mỗi sản phẩm. Tôi sẽ ghi rõ nguồn đã đọc, giá có thể xác minh và các điểm chưa đủ bằng chứng, trong giới hạn 3 truy vấn và 11 nguồn ngoài.

Công cụ tìm kiếm trả về kết quả không liên quan cho cả ba truy vấn theo tên sản phẩm, nên các kết quả đó không dùng làm bằng chứng. Tôi đang kiểm tra trực tiếp website chính thức; phần giá, nền tảng hoặc phản hồi người dùng không được nguồn xác nhận sẽ giữ là UNKNOWN.

Nguồn đã đọc cho thấy mức chồng lấn lớn: Forest có cả chặn ứng dụng, phòng tập trung nhóm và nghỉ theo nhịp thở; Flora kết hợp trồng cây với danh sách việc và bạn bè. Focus Plant có phản hồi ngày 15/11/2026 về quá nhiều lời nhắc và thời gian tải; đây là phản hồi công khai đơn lẻ, chưa chứng minh vấn đề phổ biến. Tôi đã chạm trần 11 trang đọc thành công; Study Bunny vẫn chưa xác minh vì URL thử truy cập trả về 404.

Gửi CIO — **SES-20261120-04, nghiên cứu độc lập vòng 1, ngày 20/11/2026.**

**INFERENCE — R1-M-12:** Nguy cơ trùng lặp của một sản phẩm “Pomodoro + trồng cây + chặn ứng dụng + học cùng bạn” là cao: các nguồn chính thức đã mô tả phần lớn tổ hợp này. Chưa có đặc tả hoặc nhóm khách hàng của Fokus Time, nên đây là đánh giá về không gian cạnh tranh, chưa phải kết luận về concept hay đề xuất lựa chọn.

Đã đọc nguồn hợp lệ cho **10/11 sản phẩm**. Study Bunny chưa xác minh được. Web hoạt động, nhưng cả ba truy vấn tìm kiếm trả kết quả không liên quan. Đã dừng ở trần **11 trang ngoài đọc thành công**, gồm 10 trang sản phẩm và một domain sai đích; không sửa file, cài ứng dụng hoặc thực hiện trao đổi với agent khác.

Các mô tả chức năng dưới đây là **VERIFIED về nội dung nhà cung cấp công bố**, không phải kết quả dùng thử. Tính khả dụng ở cửa hàng Việt Nam, độ ổn định và tính tương đương giữa các nền tảng vẫn chưa được kiểm chứng. **UNKNOWN về giá** nghĩa là chưa xác minh đầy đủ mức tiền, tiền tệ, khu vực và chu kỳ thanh toán.

| Finding / sản phẩm | Khả dụng, workflow và định vị đã đọc | Giá và cơ sở thanh toán |
|---|---|---|
| **R1-M-01 — Forest** [M-SRC-01] | iOS, Android, Chrome/Firefox. Chọn thời lượng → trồng cây → ghi nhận phiên. FAQ làm rõ: khi bật Deep Focus, phải bỏ cuộc để mở ứng dụng bị chặn và cây chết; không bật chế độ này thì chuyển ứng dụng không bị phạt. Có lịch chặn Time Guard, thống kê, âm thanh, nghỉ theo nhịp thở, phòng Plant Together chung iOS/Android. Định vị học tập, công việc và digital detox. | Core **miễn phí không hết hạn**, có quảng cáo ngoài phiên tập trung. Plus là thuê bao; số tiền, tiền tệ, chu kỳ cụ thể **UNKNOWN**, phụ thuộc vùng/nền tảng. Pro mua một lần không còn bán mới; người mua trước giữ trạng thái Pro. |
| **R1-M-02 — Focus To-Do** [M-SRC-02] | Android, iPhone/iPad, Apple Watch, Mac, Windows, Chrome. Tạo nhiệm vụ → thực hiện Pomodoro → xem thời gian và mức hoàn thành theo dự án. Có deadline, nhắc việc, việc con, lặp lại, ghi chú và đồng bộ. Định vị quản lý thời gian gắn với việc cần làm. | **UNKNOWN**; homepage không cung cấp bảng giá. |
| **R1-M-03 — Focus Plant** [M-SRC-03] | Listing Google Play US xác nhận Android; iOS **UNKNOWN** trong nguồn đã đọc. Tập trung → nhận nước → nuôi/sưu tập cây, phục hồi thế giới. Có Pomodoro, lịch sử, nhiệm vụ thưởng, tương tác xã hội; changelog nêu tùy chọn phòng tập trung riêng tư. Nhà phát triển công bố nhập thời gian thiền qua Google Fit; chưa kiểm chứng khả năng hoạt động hiện tại của tích hợp. | Có quảng cáo và mua trong ứng dụng. Số tiền, tiền tệ, gói/chu kỳ **UNKNOWN**. Listing được truy cập với `gl=US`, `hl=en`. |
| **R1-M-04 — Flora** [M-SRC-04] | Website có liên kết App Store, Google Play và Chrome Extension. Chọn thời lượng → trồng cây → cây chết nếu rời sang ứng dụng gây xao nhãng; trồng cùng bạn, chat/chia sẻ tiến độ, gắn cây với to-do và theo dõi mục tiêu. Định vị tập trung, thói quen và tác động môi trường. | Website công bố **miễn phí**. Dịch vụ Price/Care tự chọn liên quan trồng cây thật; mức phí, tiền tệ, chu kỳ và vùng **UNKNOWN**. |
| **R1-M-05 — Tide** [M-SRC-05] | iPhone/iPad, Android, HarmonyOS, Chrome được liệt kê. Pomodoro đi cùng âm thanh thiên nhiên; ngoài tập trung còn có ngủ/ngủ ngắn, báo thức, thiền và thở. Định vị trạng thái bình tĩnh, sức khỏe tinh thần và nghỉ ngơi. | **UNKNOWN**. |
| **R1-M-06 — Session** [M-SRC-06] | macOS, iOS/iPadOS. Nêu mục tiêu → làm phiên 25 phút → phản tư và xem tiến độ. Chặn app/website được ghi rõ **Mac Only**. Pro có cập nhật trạng thái Slack tự động. Đồng bộ iPhone, iPad, Mac. Android **UNKNOWN**; trang chỉ hiển thị câu hỏi về kế hoạch hỗ trợ. | **UNKNOWN**. Trang có nhắc Pro và câu hỏi về subscription nhưng không hiện mức giá/gói cụ thể. |
| **R1-M-07 — Structured** [M-SRC-07] | Timeline trực quan cho nhiệm vụ và lịch; nhập calendar, xem tuần/tháng, lập kế hoạch bằng AI, sử dụng trên điện thoại/máy tính/đồng hồ. Có Web App. Nội dung homepage trích xuất không xác nhận rõ từng hệ điều hành: iOS/Android **UNKNOWN ở cấp trang trực tiếp**. M-SRC-03 có nhắc Structured trong mục ứng dụng tương tự trên Google Play, chỉ là bằng chứng bổ trợ. | “Start planning for free”; giá Pro, tiền tệ, vùng, chu kỳ **UNKNOWN**. Testimonial nói về lifetime membership không xác minh việc gói đó còn bán. |
| **R1-M-08 — Opal** [M-SRC-08] | iPhone, Mac, Android. Thiết lập quy tắc chặn → chạy focus timer → xem Opal Score và mở khóa Focus Gems. Công bố Hard Mode, allow-only, soundscapes và lịch sử điểm số. Định vị bảo vệ sự chú ý tự động. | Có lời mời dùng thử miễn phí; giá, thời hạn thử, mức miễn phí lâu dài và chu kỳ **UNKNOWN**. |
| **R1-M-09 — Freedom** [M-SRC-09] | macOS, Windows, iOS, Android, Chromebook, Linux được liệt kê. Chọn thiết bị → chọn app/web/toàn bộ internet → đặt phiên và tần suất. Có đồng bộ phiên chặn, lịch lặp, Locked Mode, blocklist và âm thanh. Định vị giảm xao nhãng trên nhiều thiết bị. | Free không hết hạn, phiên tối đa 2 giờ; lịch chặn, Locked Mode và phiên dài hơn thuộc Premium. Homepage niêm yết **$39.99/năm**, có thử 7 ngày, hoặc **$8.99/tháng**. Ký hiệu `$` được xác nhận; **mã tiền tệ, khu vực áp dụng và thuế UNKNOWN**. Có link Freedom Forever nhưng chưa xác minh giá/điều kiện. |
| **R1-M-10 — one sec** [M-SRC-10] | iOS, Android; extension trên Windows/macOS/Linux. Khi mở ứng dụng, chèn bước dừng/thở/phản tư → người dùng quyết định tiếp tục; đồng thời có chặn theo lịch, giới hạn thời gian, ghi ý định/cảm xúc và gợi ý hành vi thay thế. Công bố tích hợp Structured để chặn xao nhãng khi nhiệm vụ chưa hoàn thành. | Essentials miễn phí; giá cá nhân **UNKNOWN**. Team/school quảng bá “từ **83ct/người/tháng, thanh toán hằng năm**”; tiền tệ, vùng và điều kiện đạt mức này **UNKNOWN**. |
| **R1-M-11 — Study Bunny** | URL website được thử trả HTTP 404. M-SRC-03 có nhắc tên Study Bunny, nhưng điều này không xác minh workflow hoặc tình trạng sản phẩm. Khả dụng, iOS/Android, cơ chế, giá và phản hồi: **UNKNOWN**. | **UNKNOWN**. HTTP 404 của URL thử không chứng minh ứng dụng ngừng hoạt động. |

**INFERENCE — đối chiếu người mua, phân phối và gánh nặng chuyển đổi.** Đây là suy luận từ workflow công bố, không phải quan sát khách hàng đã mua hoặc chuyển sản phẩm. Các website tiếng Anh hướng tới thị trường rộng; chưa xác minh phân bố khách hàng theo quốc gia.

| Sản phẩm | Người dùng/người mua có khả năng phù hợp; kênh quan sát | Điểm mạnh cấu trúc và giới hạn khác biệt hóa; gánh nặng chuyển đổi dự kiến |
|---|---|---|
| Forest | Cá nhân học/làm việc; app stores, extension, lời mời bạn bè | Tổ hợp timer, chặn, phần thưởng, nhóm và nghỉ ngơi rất rộng. Lịch sử, bộ sưu tập cây, bạn bè và quyền lợi Pro cũ có thể làm tăng chi phí chuyển đổi. |
| Focus To-Do | Cá nhân cần hoàn thành nhiệm vụ; mobile, desktop, extension | Gắn phút tập trung với công việc cụ thể. Sản phẩm mới chỉ thêm to-do vào timer khó khác biệt; người dùng có thể phải chuyển dự án, việc lặp và lịch sử. |
| Focus Plant | Người học/làm việc thích phần thưởng dạng game; Google Play | Bộ sưu tập và tiến triển dài hạn tạo động lực. Cũng có nguy cơ thao tác game cạnh tranh với thời gian tập trung; chuyển đổi có thể mất giá trị cảm nhận của tiến trình. |
| Flora | Cá nhân và nhóm bạn học; app stores, extension, giới thiệu bạn bè | Đã kết hợp cây, nhóm, to-do, thói quen và trồng cây thật. Mạng bạn bè và lịch sử mục tiêu có thể giữ chân người dùng. |
| Tide | Người cần tập trung và thư giãn/ngủ; nhiều nền tảng | Cạnh tranh bằng trải nghiệm trạng thái và nội dung âm thanh. Chuyển đổi có thể phụ thuộc âm thanh quen thuộc và thói quen, chưa đo lường. |
| Session | Người làm việc sâu trong hệ Apple; tải trực tiếp và mobile | Vòng lặp đặt ý định–làm việc–phản tư, cộng trạng thái Slack. Chuyển đổi cần tái lập blocklist, lịch sử và workflow liên quan. |
| Structured | Cá nhân tổ chức lịch ngày; web/mobile, website và các kênh xã hội được dẫn | Sở hữu bước lập kế hoạch trước phiên tập trung; AI đã được quảng bá. Chuyển timeline, calendar và nếp dùng có thể tốn công. |
| Opal | Cá nhân; trang còn có lối vào schools/students/coaching | Chặn theo quy tắc cộng điểm số và phần thưởng đã phủ cả kiểm soát lẫn gamification. Chi phí chuyển đổi gồm cấu hình quy tắc và lịch sử. |
| Freedom | Cá nhân; công ty/trường học cũng được mời mua | Đồng bộ chặn trên nhiều thiết bị; việc phải cài và cấu hình lại nhiều thiết bị có thể tăng ma sát chuyển đổi. |
| one sec | Cá nhân, team/trường học; mobile, extension, tích hợp và affiliate | Can thiệp ngay thời điểm định mở app, cộng chặn và kết nối planner. Chuyển đổi gồm thiết lập can thiệp, lịch chặn và tích hợp. |
| Study Bunny | **UNKNOWN** | Chưa đủ nguồn để đánh giá. |

Không có đánh giá nào ở trên chứng minh khả năng xuất/nhập dữ liệu, mức giữ chân hoặc hiệu quả thực tế. Không xem việc homepage không nhắc một tính năng là bằng chứng tính năng đó không tồn tại.

**R1-M-13 — bản đồ cơ chế đã hiện diện trong mẫu khảo sát:**

| Cơ chế / công việc | Bằng chứng đã đọc |
|---|---|
| Pomodoro | Forest, Focus To-Do, Focus Plant, Tide, Session. |
| Deep work | Session nối ý định với phản tư; Forest, Opal, Freedom hỗ trợ phiên tập trung và giảm xao nhãng. |
| Chặn ứng dụng/website | Forest, Flora, Session trên Mac, Opal, Freedom, one sec. Focus Plant cũng được nhà phát triển mô tả là app blocker trong phản hồi review, nhưng chưa rõ chi tiết. |
| Gamification | Forest/Flora trồng cây; Focus Plant nước, cây và thế giới; Opal Focus Gems. |
| Phòng học/tập trung | Forest mô tả phòng đồng bộ có mã mời; Focus Plant changelog nhắc phòng riêng tư. Chưa xác minh video room hoặc body doubling có người điều phối. |
| Accountability | Forest có hậu quả chung khi một người bỏ cuộc; Flora trồng cùng bạn, chat và chia sẻ tiến độ. |
| Thói quen | Forest challenge/streak; Flora mục tiêu và khu vườn; one sec can thiệp hành vi mở app. |
| Mindfulness | Tide thiền/thở/ngủ; Forest Mindful Space; one sec thở và phản tư. |
| AI | Structured công bố “plan with AI”; chất lượng, chi phí và mức cá nhân hóa chưa kiểm tra. |
| Native/manual | Chỉ là các hướng thay thế chưa kiểm chứng riêng trong vòng này, nêu bên dưới. |

**VERIFIED — R1-M-14: phản hồi thực sự quan sát được và phản chứng.**

- **Focus Plant, Google Play, 15/11/2026:** một review phàn nàn quá nhiều prompt/hướng dẫn và thời gian tải. Nhà phát triển trả lời 16/11 rằng sẽ xem lại, đồng thời hướng dẫn chế độ offline. Điều xác minh được là phản hồi và câu trả lời tồn tại; chưa tái hiện lỗi, chưa biết tỷ lệ ảnh hưởng.
- **Focus Plant, 27/10/2019:** review cho rằng phải dành quá nhiều thời gian trong menu và chờ tưới cây, cảm giác phải trả tiền để tập trung. Đây là tín hiệu lịch sử, **không được coi là lỗi còn tồn tại năm 2026**.
- **Phản chứng cùng listing, 28/09/2019:** một người thích thành tích thúc đẩy học và thích chơi trong giờ nghỉ. Vì vậy, “gamification luôn gây hại” không được bằng chứng này hỗ trợ.
- **Freedom:** website đăng testimonial nói người dùng chuyển từ Opal vì thấy Freedom rẻ, đơn giản và dễ tuân thủ hơn. **VERIFIED rằng Freedom đăng lời này**; chưa kiểm tra review gốc, ngày đăng hoặc chênh lệch giá thực tế. Không coi đây là xác nhận khách quan Freedom rẻ hơn.
- Với các sản phẩm còn lại, **chưa thu được khiếu nại trực tiếp đủ nguồn**. Các “điểm yếu” khác chỉ là giả thuyết cần kiểm chứng.

**R1-M-15 — tín hiệu thị trường và giới hạn diễn giải.**

Google Play của Focus Plant hiển thị **1M+ lượt tải**. Đầu trang ghi 4,2 sao/58,1K reviews, còn phần đánh giá theo thiết bị ghi 4,1/54,4K; giữ nguyên khác biệt phạm vi này, không chọn một số làm chuẩn duy nhất.

Forest công bố 60M+ lượt tải; Structured công bố 15M+ downloads và 500K+ Pro users. Đây là **VERIFIED về tuyên bố của vendor**, chưa kiểm toán, không chứng minh người dùng hoạt động, doanh thu hiện tại hoặc nhu cầu tại Việt Nam. Các số tiết kiệm thời gian/hiệu quả của Opal, Freedom và one sec cũng chưa được đối chiếu nghiên cứu gốc trong ngân sách nguồn này. Trang giá không phải bằng chứng willingness-to-pay.

**INFERENCE:** Free tier của Forest và Freedom, cùng Flora và essentials của one sec, tạo sức ép rõ lên sản phẩm mới thu phí chỉ cho timer hoặc chặn cơ bản. Ngược lại, sự tồn tại của nhiều gói trả phí không chứng minh thị trường đã hết cơ hội; vẫn có thể có phân khúc khác biệt chưa được nghiên cứu.

**HYPOTHESIS — R1-M-16: các hướng khác biệt đáng kiểm chứng, chưa phải khoảng trống đã chứng minh.**

1. **Giảm công sức để bắt đầu và quay lại công việc.** Review Focus Plant gợi ý cần khảo sát thời gian tới phiên đầu tiên và số thao tác ngoài công việc. Giả thuyết bị bác bỏ nếu nhóm mục tiêu thích game hoặc sản phẩm hiện tại đã đủ nhanh.
2. **Đo tiến triển của công việc thay vì chỉ số phút.** Tuy nhiên Focus To-Do, Session và Structured đã tiếp cận phần này. Chỉ có ý nghĩa nếu xác định được một công việc cụ thể mà các workflow hiện có chưa đáp ứng tốt.
3. **Accountability phù hợp một cộng đồng cụ thể.** “Có phòng học/bạn bè” tự nó chưa khác biệt vì Forest và Flora đã có. Cần bằng chứng về việc tham gia đều, phối hợp lịch hoặc quay lại sau bỏ dở; chưa có bằng chứng đó trong vòng này.
4. **Phục vụ một phân khúc Việt Nam có kênh phân phối riêng.** Dịch giao diện sang tiếng Việt chưa đủ: phải chứng minh lợi thế về cách học/làm việc, khả năng chi trả hoặc tiếp cận cộng đồng so với sản phẩm sẵn có.

**UNKNOWN — R1-M-17: thích nghi quốc tế và các lựa chọn thay thế chưa kiểm chứng.**

Quan sát được website Forest có EN/中文; Focus To-Do có English/简体中文; Tide có English/简体中文/繁體中文; Opal có English/French; Structured quảng bá hơn 30 ngôn ngữ. **Không suy ra danh sách ngôn ngữ trong ứng dụng hoặc việc có/không có tiếng Việt từ menu website.** Giá VND, phân phối tại Việt Nam, hành vi mua và kênh địa phương chưa được xác minh. Luật áp dụng, điều kiện xử lý dữ liệu và yêu cầu với người dùng vị thành niên chưa nghiên cứu; chưa có kết luận pháp lý cho việc chuyển mô hình sang Việt Nam.

Các hướng thay thế sau là **lead chưa được kiểm tra bằng nguồn riêng**, không phải competitor records đã xác minh:

- **Native:** Apple Screen Time/Focus, Android Digital Wellbeing, timer và lịch có sẵn.
- **Adjacent:** Focusmate, YPT/Yeolpumta, FLIPD, LifeAt, Habitica, Calm/Headspace và công cụ lịch/to-do hiện dùng.
- **Manual/local:** đồng hồ và giấy, để điện thoại ở phòng khác, thư viện/quán học, nhóm học qua Zalo/Discord/Meet.
- **Dịch vụ con người:** gia sư, coach học tập/năng suất, người điều phối nhóm học. Chưa xác minh nhà cung cấp hay agency cụ thể.
- **Không thay đổi:** giữ công cụ đang dùng, tự điều chỉnh thông báo, hoặc chấp nhận mức xao nhãng hiện tại. Đây là lựa chọn cần đưa vào nghiên cứu nhu cầu, không mặc định người dùng muốn thêm ứng dụng.

Nguồn và cách dừng được ghi để CIO có thể tái sử dụng bằng chứng. **Tất cả nguồn dưới được truy cập ngày 20/11/2026, Asia/Ho_Chi_Minh**. Ngoại trừ thông tin cập nhật/review của Focus Plant, các trang sản phẩm không nêu ngày cập nhật nội dung rõ ràng.

| Source ID | URL chính xác và locator | Loại nguồn / giới hạn |
|---|---|---|
| **M-SRC-01** | https://www.forestapp.cc/ — Features, Plans, FAQ; đã đọc cả phần phân trang | Website Seekrtech; mô tả vendor, chưa kiểm chứng chạy app/giá địa phương. |
| **M-SRC-02** | https://www.focustodo.cn/ — Features, Download | Website sản phẩm; không có giá trong nội dung đọc. |
| **M-SRC-03** | https://play.google.com/store/apps/details?id=com.shikudo.focus.google&hl=en&gl=US — About, Reviews, What’s new | Google Play US, publisher Shikudo; cập nhật app 13/11/2026. Review được hiển thị có thiên lệch lựa chọn. |
| **M-SRC-04** | https://flora.appfinca.com/ — Features, Trees, download | Website AppFinca; bộ đếm cây trích xuất là 0 nên không dùng làm số liệu tác động. |
| **M-SRC-05** | https://tide.fm/en_US/ — Focus, Sleep, Meditation, Product | Website Tide/Moreless; testimonial do vendor chọn, không có giá. |
| **M-SRC-06** | https://www.stayinsession.com/ — workflow, Mac Only, Slack, FAQ | Website Session/Translucent; câu hỏi FAQ không hiện phần trả lời. |
| **M-SRC-07** | https://structured.app/ — features, metrics, Web App | Website Structured; hệ điều hành/gói giá chưa rõ trong bản trích xuất. |
| **M-SRC-08** | Đầu vào https://www.opal.so/ → URL trả về https://opalapp.com/ — features, platforms, footer | Website Opal; thống kê hiệu quả và testimonial là nội dung vendor. |
| **M-SRC-09** | https://freedom.to/ — platforms, workflow, FAQ “Is Freedom free?” | Website Freedom; giá hiện bằng `$`, không hiện mã tiền tệ/vùng. |
| **M-SRC-10** | https://one-sec.app/ — interventions, integrations, FAQ | Website one sec; có dẫn nghiên cứu nhưng nghiên cứu gốc chưa được mở. |
| **M-SRC-11** | https://flora.app/ | Trang WordPress mặc định, **sai đích**; không dùng làm bằng chứng về Flora. Vẫn tính vào trần trang đã đọc. |

Hai lần thử URL khác không tạo được nguồn nội dung: `https://www.shikudo.com/focus-plant` và `https://www.superbyte.site/study-bunny` đều trả **HTTP 404**. Focus Plant sau đó được xác minh qua Google Play; Study Bunny còn bỏ ngỏ.

Đã dùng đúng **3 truy vấn**, nguyên văn:

1. `Focus Plant Shikudo site:apps.apple.com/us/app`
2. `Flora green focus site:apps.apple.com/us/app`
3. `Study Bunny SuperByte site:apps.apple.com/us/app`

Bing RSS trả tổng cộng 29 kết quả không liên quan; không dùng snippet nào làm chứng cứ. Có **13 URL đầu vào được thử, 11 trang trả nội dung và 2 URL lỗi**, tính Opal redirect là cùng một nguồn. Tổng 44 lần gọi tải bao gồm tải lặp và phân trang, không phải 44 nguồn độc lập. Không mở riêng trang giá, nghiên cứu gốc, cửa hàng Việt Nam hoặc nguồn agency vì đã chạm trần nguồn.

Độ tin cậy **HIGH** đối với việc các trang công bố những chức năng nêu trên; **MEDIUM** đối với nhận định chồng lấn cơ chế; **LOW/UNKNOWN** đối với hiệu quả, mức sẵn lòng trả tiền, chi phí chuyển đổi thực tế và cơ hội tại Việt Nam. Đây là findings độc lập gửi CIO; chưa có finding của agent khác để phản hồi và chưa diễn ra vòng tranh luận.

