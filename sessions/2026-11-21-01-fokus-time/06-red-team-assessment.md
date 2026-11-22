# 06 — Independent Red Team Assessment

SES-20261121-01 · 21/11/2026. Reviewer thật `/root/fokus_redteam_sol`, invocation `gpt-6.1-sol`. [Initial assessment, source/query ledger](records/redteam-r1.md), [Inventor response](records/inventor-r4-redteam-response.md), [Strategy response](records/strategy-r3-redteam-response.md), [final reviewer reply](records/redteam-r2-final.md). CIO dưới đây tóm tắt, không viết lời đáp thay chuyên gia.

**INFERENCE:** Chưa có lý do standalone app đủ bằng chứng. **Không có fatal barrier đã chứng minh**, và chưa có thử nghiệm falsify thực tế. Sau critique, Inventor rút nhãn candidate app cho cả F1-N/F3-N; Strategist không xếp hạng thương mại và chấp nhận dừng nếu baseline không tạo increment. Withdrawal là phán đoán evidence, không Founder REJECT và không proof rằng phương pháp vô ích.

## Phản đối ưu tiên và reply thật

| Objection | Concern / tác động | Evidence hoặc test có thể bác bỏ | Reply thực / còn lại |
|---|---|---|---|
| RT1 — F1 chưa có lỗi note cụ thể | Thu hẹp sang phone-primary/planned pause làm capture dễ hơn nhưng không chứng minh cần surface khác; có thể thêm context switch | C4 không có target field evidence; so same-prompt tại task, tính toàn chu kỳ và mọi lần quên/không thể capture | Inventor không nêu được lỗi còn lại; rút app về pain-first. Cần quan sát lỗi thật trước, không dựng app đi tìm pain |
| RT2 — F3 gần study tools | Recall có thể đã được Anki/RemNote/current tool giải đủ; worksheet-only là baseline thiếu | [Anki](https://docs.ankiweb.net/manual/studying) question/reveal/compare/rating; [RemNote](https://help.remnote.com/en/articles/9101991-preparing-for-an-exam) exam-linked practice; không proof equivalent outcomes | Inventor rút app, không nhảy sang bài dài để né. Strategy screening ví dụ bài nhiều bước chỉ là hypothesis mới, không winner mới |
| RT3 — tuần hai chưa có cầu nối | Người học prompt rồi chuyển về công cụ cũ có thể thành công khách hàng nhưng không cần app | Quan sát tự nguyện ở cơ hội job thật sau hết hướng dẫn; không dùng DAU/streak | Strategy thừa nhận trạng thái mỗi lần có thể cần externalize nhưng notes cũng làm được; one-time utility cũng chưa có lý do mua |
| RT4 — economics/cohort chưa có | Target mới hẹp; vài người hài lòng không chứng minh kênh và chi phí support có thể thu hồi | Cohort có access hợp lệ, khoản chi thật theo job, lựa chọn có đánh đổi và giao dịch thực trong nghiên cứu riêng | Strategy giữ access/payment/CAC UNKNOWN, bỏ hàm ý ưu thế VN/SEA; không bịa kênh đối tác |
| RT5 — scope nhỏ/value mỏng | Nếu chỉ thắng nhờ import/sync/tutor/content thì đã đổi opportunity và dependency | Baseline tạo increment/voluntary repeat không nhờ quyền/nội dung ngoài phạm vi | Cả hai chấp nhận dừng, không tự mở scope để cứu thương hiệu. Local app không bị gán chi phí infra cao vô căn cứ |
| RT6 — tránh loại nhầm utility efficiency | Một utility có thể giữ learning và giảm effort; đòi mọi app tăng điểm có thể sai, tự tick lại quá yếu | Định trước learning-gain hoặc efficiency promise; quality floor và oracle phù hợp; không suy non-inferiority từ tiny null result | Cả hai sửa phương pháp nhưng không coi đó là evidence cứu app; margin/effort benefit chưa biết |

Nguồn Anki/RemNote được Red Team tự mở; các agent khác nhận relay và không giả đã tự kiểm lần nữa. Hai Apple Books guide attempts không đọc được; không có VERIFIED claim bookmark/annotation từ các attempts đó. Không suy absence/uniqueness từ lỗi truy cập.

## Mười câu hỏi cho Founder

| Câu hỏi | Kết luận có giới hạn |
|---|---|
| Vì sao ai đó cài Fokus? | HYPOTHESIS: sau một lỗi restart hoặc một buổi học không biết lỗ hổng. Chưa có install/switching evidence; cũng có thể chỉ cần note/worksheet |
| Vì sao dùng sau tuần đầu? | Chỉ nếu job lặp và có lợi ích ròng vượt prompt/current tool; UNKNOWN. Nhắc nhiều không tạo value |
| Vì sao không timer tích hợp? | Hai hướng nhắm restart/learning diagnosis thay vì phút, nhưng khác outcome chưa chứng minh cần app riêng |
| Vì sao không Screen Time/Digital Wellbeing? | Native giảm interruption, không mặc định thay mọi job mới; vẫn có thể giải distraction đủ cho khách. Không coi native tính năng người lớn là API cấp cho Fokus |
| Vì sao không Forest/app đã có? | Chưa có switching incentive được quan sát. Feature bundle không đủ; đối thủ gần nhất của hai hướng còn là công cụ chứa task và công cụ học |
| Switching incentive mạnh nhất là gì? | HYPOTHESIS: lỗi lặp có chi phí đáng kể mà current tool chưa giải, được giảm ròng; chưa quan sát |
| Giả định yếu nhất? | Delivery mobile riêng vẫn cần thiết khi đặt cùng prompt ở ngay nơi làm/học |
| Tính năng hấp dẫn nhưng ít giá trị? | Album bằng chứng, chart/self-tick, streak, AI recap chưa gắn outcome. R3 bỏ chúng; không đưa lại để tạo engagement |
| Đội nhỏ giữ được gì? | Baseline text local có scope nhẹ tương đối theo Technical; skills/cost/device reliability chưa đo. Điều đó không chứng minh business |
| Vì sao thất bại dù app hoàn hảo? | Job hiếm, current tool sát context hơn, người dùng học prompt rồi rời, không trả hoặc không tiếp cận được bằng nguồn lực hợp lý |

## Điều kiện đủ để khuyến nghị dừng hướng app

Nếu không có lỗi quan trọng lặp lại trong cohort có thể tiếp cận, chưa có lý do ưu tiên nghiên cứu một app. Nếu practice không đem lợi ích ròng, bỏ practice cho target đó. Nếu practice có ích nhưng current tool/same-prompt artifact tương đương hoặc tốt hơn, dừng standalone app; giữ hướng dẫn/template có thể là kết quả hữu ích. Nếu có increment nhưng không có căn cứ kinh tế/kênh đáng kiểm tra theo nguồn lực Founder, không tiếp tục mặc định.

Nếu cả hai hướng rơi vào các điều kiện trên, hội đồng không bảo vệ việc duy trì Fokus dưới dạng mobile app. Điều kiện chưa được thử không được viết thành kết quả thất bại đã quan sát. Mở sang tutor/content/integration là cơ hội khác cần scope mới, không là cách tự hoàn tất nhiệm vụ hiện tại.

## Việc phản biện đã làm được và chưa làm được

Đã thay đổi đối chứng, thu hẹp claim, bỏ hai nhãn candidate app trong recommendation của Inventor, và sửa cách đánh giá utility efficiency. Không có dữ liệu mới về target behavior, willingness-to-pay hay retention. Các reply đồng ý không tạo empirical corroboration.

[Final reply](records/redteam-r2-final.md) đã được nhận: Red Team chấp nhận withdrawal thận trọng, giữ nguyên mọi gap thực nghiệm. Nó sửa chính RT3: nhớ prompt không có nghĩa nhớ trạng thái mới mỗi lần, nhưng app riêng vẫn phải hơn notes/study tools. Nó giữ bất đồng scope: Strategy đề xuất screening bài toán nhiều bước, Inventor không chấp nhận pivot để tránh recall competition; không tổng hợp thành target mới đồng thuận. Không cần vòng debate tiếp khi chưa có evidence mới.
