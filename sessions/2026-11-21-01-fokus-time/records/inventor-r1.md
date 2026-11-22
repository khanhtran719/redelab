# SES-20261121-01 — Inventor R1: các cơ chế độc lập cho Fokus Time

- Người thực hiện: subagent `/root/fokus_inventor_sol`, Creative Product Inventor; model runtime do CIO chỉ định: gpt-6.1-sol. Ngày: 2026-11-21.
- Phạm vi: ý tưởng ứng dụng mobile iOS/Android cho Việt Nam/SEA/quốc tế; không thiết kế kiến trúc hoặc tạo prototype.
- Tính độc lập: đã đọc AGENTS.md, creative-ideation/SKILL.md và evidence-policy.md; **chưa đọc lời giải của agent khác hay session Fokus trước khi lưu R1 này**. Đề bài không có ứng viên sẵn.
- Nguồn: không dùng web, không có phỏng vấn/quan sát người dùng. **Toàn bộ nhu cầu, workaround, hành vi, giá trị và ý tưởng dưới đây là HYPOTHESIS**, chưa phải sự thật về thị trường. Khả năng hệ điều hành và willingness-to-pay là UNKNOWN. Các con số thử nghiệm là ngưỡng quyết định đề xuất, không phải kết quả.

## Kết quả cần đạt và các ràng buộc

Giả thuyết JTBD gốc: người dùng muốn chuyển một việc có ý nghĩa sang trạng thái tiến triển/hoàn tất mà không bị chi phí bắt đầu, gián đoạn hoặc lựa chọn lấn át. “Số phút tập trung” chỉ có thể là một tín hiệu phụ. Không coi timer, streak, chatbot, AI tự động hay giao diện mới là cơ chế cốt lõi.

Ràng buộc: solo/small team có thể học trước khi làm sản phẩm; mobile phải có vai trò hợp lý; không mặc định được đọc/chặn mọi ứng dụng, phát hiện gián đoạn chính xác, tự động gửi tin nhắn hoặc đo năng suất khách quan. Không giả định ADHD hay hiệu quả điều trị.

## F1 — Trở lại đúng chỗ: thẻ bàn giao cho chính mình

**Khách hàng/job.** Freelancer làm việc tri thức một mình và thường phải ngắt việc vì cuộc gọi/việc nhà; muốn quay lại phần đang dở mà không đọc lại từ đầu.

**Vấn đề và workaround — HYPOTHESIS.** Chi phí chính nằm ở việc dựng lại ngữ cảnh sau gián đoạn. Workaround có thể là tab để mở, ghi chú rời hoặc giữ mọi thứ trong đầu; chưa xác minh.

**Cơ chế.** Chuyển ghi nhớ từ “lúc bắt đầu lại” sang “ngay trước khi rời việc”: để lại một thẻ cực ngắn gồm trạng thái hiện tại, hành động tiếp theo và vướng mắc. Lúc trở lại, app chỉ đưa một hành động tiếp tục. Đơn vị giá trị là lần nối lại thành công, không phải phiên dài.

**Hành trình mobile.** Chọn một việc → trước khi rời, chạm “để lại chỗ” rồi nhập/nói một câu hoặc ảnh → khi quay lại mở thẻ → đánh dấu “đã tiếp tục” sau hành động đầu tiên. Không cần tự nhận diện app ngoài; nhắc thủ công là baseline.

**Lời hứa đo được.** Giảm trung vị thời gian từ quay lại đến hành động đầu tiên, đồng thời không tăng tổng thời gian ghi thẻ quá lợi ích thu được. Đo thêm tỷ lệ thẻ thật sự được dùng lại.

**Khác biệt giả thuyết.** Fokus sở hữu việc bàn giao ngữ cảnh qua một lần gián đoạn, thay vì sở hữu toàn bộ task manager. Chưa có bằng chứng đây là khoảng trống cạnh tranh.

**Áp dụng/bỏ dùng.** Tín hiệu bắt đầu rõ: vừa mất vài phút tìm lại chỗ dở. Dễ bỏ nếu thẻ đòi viết dài hoặc người dùng bị cắt ngang đột ngột không thể ghi. Nếu sticky note đáp ứng tương đương, app riêng thiếu lý do tồn tại.

**Giả định kỹ thuật/thương mại — UNKNOWN.** Ghi và gọi lại thẻ phải đủ nhanh trên cả hai OS; lockscreen/shortcut chỉ là giả định cần kiểm tra. Người dùng có thể không trả tiền cho một công cụ ngắn, dùng không đều.

**Phương pháp và học rẻ.** Chuyển giao ca trực + inversion: tối ưu nối lại thay vì cấm ngắt. Đề xuất bài kiểm tra crossover trên giấy với 6–8 người, mỗi người vài lần gián đoạn có/không thẻ. Bác bỏ nếu thời gian nối lại không giảm hoặc hơn nửa lần không chịu ghi thẻ. Chưa thực hiện.

## F2 — Cửa nhận gián đoạn: thỏa thuận giữa hai người

**Khách hàng/job.** Người làm việc/học ở nhà cùng một người thân có những yêu cầu nhỏ không khẩn cấp; muốn có khoảng yên mà vẫn giữ đường liên lạc cho chuyện cần thật.

**Vấn đề và workaround — HYPOTHESIS.** Người kia không biết lúc nào nên hỏi; “đừng làm phiền” quá mơ hồ. Có thể dùng tai nghe, giấy dán cửa hoặc nhắn lại sau; chưa xác minh.

**Cơ chế.** Chuyển từ trách nhiệm tự kiểm soát cá nhân sang hợp đồng phối hợp ngắn giữa hai người: hẹn mốc trả lời tiếp theo, có một hàng đợi yêu cầu không khẩn cấp và lối “cần ngay”. Không đánh giá mức khẩn bằng AI hoặc cấm người dùng phá phiên.

**Hành trình mobile.** Người A mở cửa sổ làm việc và nêu mốc trả lời → người B tự nguyện dùng liên kết/màn hình chung để gửi yêu cầu hoặc chọn cần ngay → A xử lý hàng đợi tại mốc hẹn → cả hai xác nhận thỏa thuận có hữu ích không. Cần nghiên cứu phương án không bắt B cài app; không giả định được tự tích hợp kênh chat.

**Lời hứa đo được.** Giảm số lần gián đoạn không khẩn trong một buổi; không làm tăng thời gian phản hồi cho sự việc mà đôi bên cùng coi là cần ngay. Đo cả gánh nặng với B và xung đột do thỏa thuận gây ra.

**Khác biệt giả thuyết.** Sản phẩm tổ chức quyền yêu cầu và thời điểm phản hồi giữa một cặp, không chỉ chặn thông báo trên máy A. Không tuyên bố mới.

**Áp dụng/bỏ dùng.** Một cặp có thể thử ngay khi đang có xung đột nhắc việc lặp lại. Bỏ nếu B phải học thêm công cụ, mốc trả lời không được giữ hoặc quyền “cần ngay” bị lạm dụng. Nguy cơ biến quan hệ thân thuộc thành quy trình khó chịu.

**Giả định kỹ thuật/thương mại — UNKNOWN.** Chia sẻ trạng thái qua link/thiết bị và độ tin cậy thông báo phải được kiểm tra. Nhu cầu hai bên và người trả tiền chưa biết; có thể chỉ phù hợp như tiện ích miễn phí thay vì công ty độc lập.

**Phương pháp và học rẻ.** Chuyển mô hình giờ tiếp khách/đường cấp cứu sang cặp tại nhà. Đề xuất 5 cặp dùng thẻ giấy “mốc trả lời” và danh sách yêu cầu trong 5 ngày; bác bỏ nếu người còn lại không tự nguyện duy trì hoặc thời gian gián đoạn chỉ chuyển sang xung đột. Chưa thực hiện, không có outreach được ủy quyền.

## F3 — Một bằng chứng hoàn thành: phiên kết thúc bằng sản phẩm nhỏ

**Khách hàng/job.** Sinh viên tự học môn có bài tập cụ thể; muốn biết buổi học đã tạo tiến bộ hữu ích thay vì chỉ “ngồi đủ lâu”.

**Vấn đề và workaround — HYPOTHESIS.** Có thể dùng thời gian/streak làm thay thế cho học được gì, rồi không biết nên dừng hay tiếp. Workaround có thể là checklist chương hoặc số trang, chưa xác minh.

**Cơ chế.** Chuyển tiêu chí kết thúc từ thời gian sang một vật chứng do người học tự đặt trước: giải một bài không nhìn mẫu, tự viết lại một khái niệm hoặc nêu câu hỏi còn thiếu. Bắt đầu bằng chọn điều kiện chứng minh đủ nhỏ; kết thúc bằng đối chiếu lời hứa với vật chứng. Không chấm hiểu biết tự động và không tuyên bố cải thiện điểm số.

**Hành trình mobile.** Chọn một trong vài hình thức bằng chứng → viết đích cụ thể → cất máy học → chụp/nhập kết quả → chọn đạt/chưa đạt và ghi điều thiếu → dừng hoặc thu nhỏ đích tiếp theo. Không cần hồ sơ môn học lớn.

**Lời hứa đo được.** Tăng tỷ lệ buổi học kết thúc với một đầu ra đạt tiêu chí đã định; đồng thời không tăng thời gian thao tác/khuyến khích chọn đích quá dễ. Bằng chứng độc lập nên là bài recall ngắn sau đó, không chỉ tự tick hoàn thành.

**Khác biệt giả thuyết.** Chu trình dự báo–làm–đối chiếu cụ thể; không phải task checklist đổi tên. Dễ bị sao chép bằng ghi chú, nên khác biệt thương mại chưa rõ.

**Áp dụng/bỏ dùng.** Hợp lúc ôn bài thi có dạng bài rõ; dễ bỏ khi nội dung quá mở, việc chụp bài phiền hoặc người học cảm thấy bị kiểm tra. Bỏ nếu thủ tục tạo vật chứng lấn át học.

**Giả định kỹ thuật/thương mại — UNKNOWN.** Chụp/lưu riêng tư là giả định nhẹ hơn tích hợp sâu; cần kiểm tra quyền dữ liệu và lợi ích đủ để trả tiền. Không mặc định B2B trường học hoặc phụ huynh giám sát.

**Phương pháp và học rẻ.** Chuyển acceptance criteria sang học cá nhân. Đề xuất 8 người dùng mẫu giấy trong 1 tuần và so với checklist hiện tại; bác bỏ nếu chất lượng recall không đổi và gánh nặng thao tác cao hơn. Chưa thực hiện.

## F4 — Hàng đợi tò mò: giữ ý định, hoãn lần mở

**Khách hàng/job.** Người viết/thiết kế bị các ý nghĩ “phải tra/mua/xem ngay” tự phát kéo khỏi việc đang làm; muốn không đánh mất ý nghĩ nhưng cũng không mở một chuỗi duyệt dài.

**Vấn đề và workaround — HYPOTHESIS.** Một phần thôi thúc chuyển ứng dụng có thể là sợ quên điều muốn xem. Có thể ghi sổ, mở tab chờ hoặc tự ép nhịn; chưa biết tỷ lệ nguyên nhân này so với buồn chán/né việc.

**Cơ chế.** Tách việc giữ ý định khỏi việc thực hiện: ghi một dòng vào khay tò mò, cam kết mốc xem lại ngắn đã chọn; tại mốc đó quyết định xóa, xử lý hoặc hoãn. Không thưởng số lần chống cám dỗ; tạo kết thúc rõ cho những ý định đã mất giá trị.

**Hành trình mobile.** Khi muốn chuyển việc, mở thao tác nhập nhanh → để lại ý định và quay lại việc → lúc nghỉ app trình một mục một lần → chạm xử lý/xóa/để sau → nếu xử lý, kết thúc rõ rồi quay lại. Không giả định có thể bắt mọi lần mở app ngoài hay ép quay về.

**Lời hứa đo được.** Giảm số lần chuyển ứng dụng tự phát dẫn tới hơn 5 phút lệch việc; ghi nhận tổng phút của thao tác khay để tránh “đổi kiểu phân tâm”. Ngưỡng 5 phút là định nghĩa thử nghiệm đề xuất.

**Khác biệt giả thuyết.** Điều phối lại thời điểm hành động bằng quyền được nhớ và xem lại, thay vì chỉ hạn chế truy cập. Tuy nhiên có thể chỉ là biến thể inbox/read-it-later; cần market critique trước khi shortlist.

**Áp dụng/bỏ dùng.** Dễ thử khi đã nhận ra thói quen mở tab. Bỏ nếu quên dọn khay, thao tác nhập gây thêm lệch việc hoặc thôi thúc do né tránh nhiệm vụ chứ không do sợ quên.

**Giả định kỹ thuật/thương mại — UNKNOWN.** Nhập đủ nhanh và nhắc đúng lúc trên iOS/Android cần kiểm chứng; sự sẵn lòng trả tiền thấp có thể làm hướng này chỉ phù hợp như cơ chế trong sản phẩm khác.

**Phương pháp và học rẻ.** SCAMPER: thay lượt xem tức thì bằng hàng đợi có quyền hủy. Đề xuất 1 tuần crossover bằng giấy đặt cạnh bàn; bác bỏ nếu ghi khay không giảm hành động chuyển việc hoặc khay thành backlog gây áp lực. Chưa thực hiện.

## F5 — Quyền dừng đã định trước: chống kéo dài buổi tối

**Khách hàng/job.** Người đi làm có dự án cá nhân buổi tối và ít quỹ thời gian; muốn tiến đều mà biết lúc nào được nghỉ, không mặc định kéo dài một buổi “đang có hứng”.

**Vấn đề và workaround — HYPOTHESIS.** “Làm đến khi xong” có thể làm công việc mở rộng và khiến buổi sau khó bắt đầu. Workaround có thể là alarm, checklist hoặc bỏ hẳn dự án vài ngày; chưa xác minh. Không đưa ra nhận định y khoa về mệt mỏi.

**Cơ chế.** Đặt trước một hợp đồng đủ: đầu ra tối thiểu + giới hạn nỗ lực/tối đa + bước bàn giao. Khi chạm một trong hai điều kiện thì đóng việc có ý thức; nếu chưa xong ghi phần còn lại để lần sau không phải thương lượng lại. Tối ưu chuỗi buổi có thể duy trì, không tối đa hóa phút hôm nay.

**Hành trình mobile.** Trước buổi chọn “đủ cho tối nay” và mốc phải dừng → làm → khi đạt đích hoặc hết biên, xác nhận đóng → để lại bước tiếp theo → lần sau bắt đầu từ phần đã chốt. App phải cho đổi ý; không khóa cứng hoặc trừng phạt.

**Lời hứa đo được.** Tăng số buổi đã định mà người dùng thực sự bắt đầu trong 2 tuần, giữ hoặc tăng tổng đầu ra được xác nhận; đo tỷ lệ vượt biên và cảm nhận hối tiếc ngày hôm sau. Không dùng số buổi riêng lẻ để giả làm kết quả sức khỏe.

**Khác biệt giả thuyết.** Sản phẩm cấp quyền hoàn tất một ngày dựa trên thỏa thuận trước, không khuyến khích kéo streak hoặc nối timer. F1 lưu ngữ cảnh sau gián đoạn; F5 thay quy tắc phân bổ nỗ lực qua nhiều ngày. Có thể hợp thành một hướng nhưng chưa nên đếm như khác biệt đã được chứng minh.

**Áp dụng/bỏ dùng.** Vào ở thời điểm hay thức muộn làm dự án. Bỏ nếu deadline ngoài kiểm soát, người dùng thích cường độ bùng nổ hoặc “đủ” chỉ là lời tự nhủ không thay đổi hành vi. Có thể reminder thông thường đã đủ.

**Giả định kỹ thuật/thương mại — UNKNOWN.** Không cần đo nỗ lực bằng cảm biến, nhưng nhắc và đóng phiên phải dễ dùng. Người dùng trả tiền để làm ít hơn mỗi tối là giả thuyết khó; cần chứng minh tiến độ toàn kỳ trước.

**Phương pháp và học rẻ.** Inversion + ngân sách hữu hạn: bảo vệ lần làm kế tiếp. Đề xuất nhật ký 14 ngày có tuần baseline và tuần hợp đồng giấy; bác bỏ nếu tổng tiến độ giảm mà tỷ lệ quay lại không tăng. Chưa thực hiện; thứ tự tuần có bias, không coi là thử nghiệm nhân quả hoàn chỉnh.

## F6 — Chuẩn bị gói việc cho khe thời gian: quyết định trước lúc rảnh

**Khách hàng/job.** Người đi làm học thêm kỹ năng có những khoảng chờ ngắn và không đều; muốn tận dụng một vài khoảng có ích mà không tốn cả khoảng để chọn việc.

**Vấn đề và workaround — HYPOTHESIS.** Khi chỉ rảnh vài phút, tìm tài liệu và quyết định việc phù hợp có thể đắt hơn thực hiện. Workaround có thể là bookmark, flashcard hoặc một danh sách chung; chưa xác minh. Không mặc định mọi phút nghỉ đều nên được dùng để làm việc.

**Cơ chế.** Tách công đoạn chuẩn bị khỏi công đoạn tiêu thụ: trong một lần có ngữ cảnh đầy đủ, người dùng tạo gói nhỏ có đủ dữ liệu và một hành động độc lập; khi rảnh chỉ chọn điều kiện “được nghe/được nhìn/có thể gõ” và mở một gói phù hợp. Có lựa chọn nghỉ như trạng thái hợp lệ.

**Hành trình mobile.** Chuẩn bị một vài gói từ tài liệu thuộc quyền sử dụng, tự đặt đầu ra nhỏ và điều kiện dùng → lúc chờ chọn điều kiện thực tế → app đưa một gói → làm hoặc bỏ qua → gói hoàn tất chuyển về việc lớn. Không bắt nhập toàn bộ dự án và không giả định tự đọc tài liệu bên ngoài.

**Lời hứa đo được.** Tăng số đầu ra nhỏ hoàn tất trên một tuần; **trừ toàn bộ thời gian chuẩn bị gói** khi tính giá trị. Đo tỷ lệ gói bị bỏ vì thiếu ngữ cảnh hoặc điều kiện không phù hợp.

**Khác biệt giả thuyết.** Chuẩn bị trước đơn vị việc tự chứa theo điều kiện sử dụng, không đơn giản gắn nhãn phút cho task. Nguy cơ trùng flashcard/offline reading/task lists rất lớn và phải được market challenge.

**Áp dụng/bỏ dùng.** Có thể vào với một tài liệu học đã dùng. Bỏ nếu chi phí chuẩn bị cao, gói nhỏ không đóng góp đáng kể cho mục tiêu hoặc người dùng cần thời gian nghỉ. Chỉ phù hợp tập con công việc tách được.

**Giả định kỹ thuật/thương mại — UNKNOWN.** Offline/import/quyền nội dung và khả năng tác vụ tự chứa cần kiểm tra. Không lấy AI tạo gói làm lời giải cho chi phí chuẩn bị khi chưa chứng minh chất lượng. Retention và trả tiền chưa biết.

**Phương pháp và học rẻ.** Analogy mise-en-place: chuẩn bị sẵn nguyên liệu trước giờ thực hiện. Đề xuất tự soạn 6 gói trên giấy/file có sẵn cho 5 người, ghi cả thời gian chuẩn bị; bác bỏ nếu chi phí chuẩn bị lớn hơn phần thời gian lựa chọn được tiết kiệm hoặc đa số gói không hoàn tất. Chưa thực hiện.

## Sổ claim và giới hạn R1

| Finding ID | Claim phạm vi | Loại | Nguồn | Confidence | Điều làm thay đổi đánh giá |
|---|---|---|---|---|---|
| R1-inventor-01 | F1 có thể giảm chi phí dựng lại ngữ cảnh sau gián đoạn với freelancer | HYPOTHESIS | Không có; cơ chế đề xuất | LOW; chưa quan sát nhu cầu | Ghi thẻ đủ dùng và thời gian nối lại giảm sau khi trừ thao tác |
| R1-inventor-02 | F2 có thể giảm gián đoạn nhờ thỏa thuận giữa một cặp tại nhà | HYPOTHESIS | Không có; analogical invention | LOW; cần cả hai cùng tham gia | Người nhận yêu cầu tự duy trì và lối cần ngay không bị lạm dụng |
| R1-inventor-03 | F3 có thể chuyển một buổi học thành đầu ra kiểm tra được | HYPOTHESIS | Không có; cơ chế đề xuất | LOW; thao tác có thể thừa | Đầu ra và recall độc lập tốt hơn, không chỉ tự tick |
| R1-inventor-04 | F4 có thể giảm hành vi chuyển việc vì sợ quên điều muốn xem | HYPOTHESIS | Không có; cơ chế đề xuất | LOW; nguyên nhân thôi thúc chưa biết | Ý định được hoãn rồi xử lý/xóa mà không tạo thêm backlog |
| R1-inventor-05 | F5 có thể tăng khả năng quay lại dự án qua quy tắc đủ và dừng | HYPOTHESIS | Không có; inversion | LOW; có thể là reminder thông thường | Tiến độ cả kỳ không giảm và tỷ lệ quay lại tăng |
| R1-inventor-06 | F6 có thể làm khoảng chờ hữu ích sau khi trừ chi phí chuẩn bị | HYPOTHESIS | Không có; analogy | LOW; tổng chi phí chưa biết | Giá trị ròng dương và gói không thiếu ngữ cảnh |

Không có claim VERIFIED về khách hàng, cạnh tranh, quy mô, giá, OS API hoặc thương mại. Không đưa ra “độc nhất thị trường”. Chưa xếp hạng theo sức hấp dẫn thương mại trước khi nhận evidence và phản biện. Nếu cần ưu tiên **câu hỏi học**, F1 có điểm thất bại đo được rõ nhất; F2 thay đổi cơ chế phối hợp nhiều nhất nhưng phụ thuộc người thứ hai; F4/F6 có nguy cơ chỉ là tính năng mạnh nhất. Đây là nhận xét cấu trúc giả thuyết, không phải kết quả thẩm định thị trường.

R1 dừng ở catalog độc lập. Chưa có đánh giá của chuyên gia khác và chưa có Founder decision.
