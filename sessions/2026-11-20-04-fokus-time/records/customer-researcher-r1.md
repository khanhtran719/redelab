# customer-researcher — immutable R1

```json
{
  "id": "e1132a6f-29ac-4787-b478-9bc5d412cc4e",
  "agentId": "e1132a6f-29ac-4787-b478-9bc5d412cc4e",
  "sessionId": "7d889320-b711-43ea-9c96-81b3ac60b712",
  "workspace": "/Users/trankhanh/MyFolder/innovation-lab",
  "continuationOf": null,
  "title": "Fokus R1 customer discovery",
  "status": "completed",
  "createdAt": "2026-11-20T10:16:03.149Z",
  "threadId": "01a1f874-bf71-77f1-850e-fc06b598ff8a",
  "archived": false,
  "error": null,
  "attempts": 1,
  "toolsetVersion": 2,
  "startedAt": "2026-11-20T10:16:03.154Z",
  "retryAt": null,
  "warnings": [
    "Tool hub_fetch_url: web_http_403",
    "Tool hub_fetch_url: web_http_404",
    "Tool hub_fetch_url: web_http_403"
  ],
  "endedAt": "2026-11-20T10:19:18.239Z",
  "promptBytes": 3295,
  "outputLength": 18585,
  "offset": 0,
  "nextOffset": null
}
```

Tôi sẽ dùng skill problem-discovery để khảo sát công việc và trở ngại của từng nhóm, giữ độc lập với ý tưởng giải pháp. Tôi sẽ đọc hướng dẫn dự án, dùng tối đa 3 truy vấn và 3 nguồn bên ngoài, rồi trả lại bằng chứng, phản chứng và các khoảng trống cho CIO.

Cả 3 truy vấn đều trả về kết quả lệch chủ đề, nên tôi không dùng chúng làm bằng chứng. Tôi sẽ kiểm tra trực tiếp các nguồn nghiên cứu đã biết; bằng chứng riêng cho sinh viên, freelancer và người dùng Việt Nam có thể vẫn thiếu trong giới hạn khảo sát này.

Hai nguồn cho thấy cần tách “khả năng duy trì chú ý” khỏi “hoàn thành công việc”: nghiên cứu can thiệp báo cáo cải thiện chú ý, còn nghiên cứu lập trình viên ghi nhận việc chuyển tác vụ vẫn có thể đi cùng cảm giác làm việc hiệu quả. Tường thuật về lịch họp cũng gợi ý trở ngại có thể nằm ở quyền kiểm soát lịch, nhưng chưa đủ để khái quát. Chưa có bằng chứng trực tiếp về nhu cầu trả tiền hay sử dụng lặp lại của bốn nhóm.

**Gửi CIO — SES-20261120-04, vòng độc lập Customer Discovery.** Bằng chứng hiện có hỗ trợ việc phân biệt ba vấn đề: khả năng duy trì chú ý, hoàn thành công việc có ý nghĩa, và quyền kiểm soát lịch làm việc. **Chưa đủ bằng chứng để xác định phân khúc cần một ứng dụng focus mới, nhu cầu trả tiền hoặc khả năng dùng lâu dài.**

Web đọc trực tiếp hoạt động, nhưng cả 3 truy vấn tìm kiếm trả về kết quả lệch chủ đề. Tôi không dùng các kết quả đó làm bằng chứng. Đã đọc thành công đúng **3 nguồn bên ngoài**; không phỏng vấn, tiếp cận khách hàng, sửa file hay thực hiện phản biện liên tác nhân.

**1. Sổ nguồn và giới hạn khảo sát**

Tất cả nguồn được truy cập ngày **20/11/2026, Asia/Ho_Chi_Minh**. `VERIFIED` dưới đây nghĩa là đã đọc nguồn hỗ trợ phát biểu hẹp, không phải đã tái kiểm chứng nghiên cứu.

| ID | Nguồn, ngày công bố và URL chính xác | Nội dung thực sự đọc được | Giới hạn |
|---|---|---|---|
| **C-SRC-01** | Castelo và cộng sự, *Blocking mobile internet on smartphones improves sustained attention, mental health, and subjective well-being*, PNAS Nexus; công bố trực tuyến 18/02/2025. https://api.crossref.org/works/10.1093/pnasnexus/pgaf017 | Abstract do nhà xuất bản cung cấp qua Crossref: thử nghiệm ngẫu nhiên kéo dài một tháng, chặn Internet trên smartphone trong hai tuần; vẫn cho phép cuộc gọi, tin nhắn và Internet trên máy tính. Báo cáo cải thiện chú ý đo khách quan cùng các kết quả tâm lý. Locator: `message.abstract`, `message.published-online`. | Chỉ đọc abstract và metadata; toàn văn bị HTTP 403. Chưa kiểm tra cỡ mẫu, địa bàn tuyển mẫu, mức tuân thủ, hao hụt mẫu, độ lớn tác động và phân tích thống kê. Không phải bằng chứng về kết quả học tập, sản lượng công việc hay nhu cầu mua app. |
| **C-SRC-02** | Meyer, Fritz, Murphy, Zimmermann, *Software Developers’ Perceptions of Productivity*, ACM FSE, 11/2014. https://www.microsoft.com/en-us/research/publication/software-developers-perceptions-of-productivity/ | Abstract trên trang nghiên cứu: khảo sát **379 lập trình viên chuyên nghiệp**, nghiên cứu quan sát **11 lập trình viên**; cảm nhận năng suất và việc chuyển tác vụ. Locator: đoạn tóm tắt dưới tên bài. | Chưa đọc toàn văn và cách chọn mẫu; địa lý chưa xác định từ nội dung đọc. Nguồn cách thời điểm khảo sát khoảng 12 năm; không đại diện mặc nhiên cho freelancer, designer hay môi trường remote hiện nay. |
| **C-SRC-03** | Paul Graham, *Maker’s Schedule, Manager’s Schedule*, 07/2009. https://www.paulgraham.com/makersschedule.html | Toàn bài: tường thuật cá nhân về lịch họp, lập trình/viết, gom giờ gặp và chuyển thời gian lập trình sang ban đêm. Locator: các đoạn về “office hours”, “dinner till about 3 am” và ảnh hưởng của cuộc họp đến việc bắt đầu công việc khó. | Một lời kể công khai, không phải mẫu nghiên cứu; bối cảnh founder/lập trình viên tại Silicon Valley, gồm hồi tưởng thập niên 1990. Quyền tự chủ lịch cao; nguồn cũ, không chứng minh mức phổ biến. |

Có bằng chứng nghiên cứu với người thật được báo cáo trong C-SRC-01/02 và một lời kể cá nhân trong C-SRC-03. **Không có dữ liệu khách hàng do Lab trực tiếp thu thập, không có lời kể đã kiểm chứng của người dùng app focus, và không có mẫu Việt Nam/Đông Nam Á.** Không suy địa bàn người tham gia từ địa chỉ cơ quan của tác giả.

**2. Các phát hiện có cơ sở mạnh nhất**

**R1-C-01 — Khả năng duy trì chú ý có thể bị ảnh hưởng bởi việc luôn truy cập được Internet trên điện thoại.**

- **VERIFIED:** C-SRC-01 báo cáo can thiệp chặn Internet di động cải thiện khả năng duy trì chú ý đo khách quan. Đây là kết quả nghiên cứu được trình bày trong abstract, không phải lời quảng cáo sản phẩm.
- **INFERENCE:** Môi trường truy cập có thể là một yếu tố gây khó khăn, bên cạnh ý định hoặc kỷ luật cá nhân. Tuy nhiên, nguồn chưa xác định công việc cụ thể nào trong bốn nhóm bị ảnh hưởng nhiều nhất.
- **Giới hạn/phản chứng đối với diễn giải rộng:** Internet trên máy tính vẫn được phép. Không thể diễn giải thành “chặn mọi Internet giúp làm việc tốt hơn”, hoặc “mọi gián đoạn đến từ điện thoại”. Cải thiện bài đo chú ý chưa chứng minh cải thiện điểm thi, chất lượng thiết kế hoặc hoàn thành dự án.
- **Độ tin cậy:** **MEDIUM** cho kết quả can thiệp được báo cáo, vì chỉ đọc abstract; **LOW** khi áp dụng vào từng phân khúc. Cần toàn văn và quan sát công việc thực tế để nâng mức tin cậy.

**R1-C-02 — Với lập trình viên, kết quả mong muốn gắn với việc hoàn thành tác vụ; số lần chuyển tác vụ không tự nó xác định thất bại.**

- **VERIFIED:** C-SRC-02 cho biết người tham gia cảm thấy ngày làm việc hiệu quả khi hoàn thành nhiều hoặc những tác vụ lớn, ít gián đoạn/chuyển ngữ cảnh đáng kể. Nhưng dữ liệu quan sát cũng ghi nhận nhiều chuyển tác vụ trong khi họ vẫn cảm thấy hiệu quả.
- **INFERENCE — phát biểu vấn đề có giới hạn:** Khi thực hiện công việc lập trình, người làm cần duy trì hoặc khôi phục tiến độ đến một đơn vị công việc hoàn chỉnh. “Giảm mọi lần chuyển tác vụ” chưa phải mô tả đầy đủ nhu cầu.
- **Phản chứng:** Việc chuyển tác vụ có thể cùng tồn tại với cảm giác năng suất. Nguồn chưa chứng minh mọi lần chuyển là có hại, cũng chưa chứng minh cảm giác năng suất tương ứng sản lượng khách quan.
- **Độ tin cậy:** **MEDIUM** cho nhóm lập trình viên được nghiên cứu; **LOW** cho designer/freelancer hoặc hiện trạng năm 2026. Nhật ký công việc hiện tại kèm đầu ra sẽ giúp phân biệt chuyển tác vụ cần thiết và gián đoạn gây thiệt hại.

**R1-C-03 — Một trở ngại có thể nằm ở lịch do người khác chi phối, kể cả trước khi gián đoạn xảy ra.**

- **VERIFIED:** C-SRC-03 mô tả việc một cuộc họp chia nhỏ buổi làm việc và làm tác giả ít muốn bắt đầu công việc tham vọng trước đó. Cách ứng phó được kể lại: gom cuộc hẹn cuối ngày; từng lập trình từ sau bữa tối đến khoảng 3 giờ sáng.
- **INFERENCE — phát biểu vấn đề có giới hạn:** Người làm công việc cần nhiều thời gian thiết lập ngữ cảnh có thể khó bắt đầu và hoàn thành phần việc khó khi lịch bị chia nhỏ. Quyền sắp lịch là một biến cần khảo sát.
- **Phản chứng:** Chính tác giả cho rằng lịch dạng cuộc hẹn phù hợp với công việc quản lý; không phải mọi nghề cần những khối thời gian dài. Gom lịch cũng là một cách ứng phó đã phục vụ được trường hợp này, nên chưa thể kết luận thiếu giải pháp.
- **Độ tin cậy:** **HIGH** rằng bài viết chứa lời kể này; **LOW** về mức phổ biến và mức độ nghiêm trọng trong thị trường. Một mẫu nhân viên ít quyền tự chủ có thể cho kết quả khác hẳn.

**3. Bản đồ phân khúc và đủ 10 câu hỏi khám phá**

Các mục `HYPOTHESIS` là giả thuyết để kiểm tra, không phải hành vi đã quan sát. Những thước đo bên dưới là đề xuất nghiên cứu, chưa phải giá trị sản phẩm đã tạo ra.

**R1-C-04 — Sinh viên đại học/người ôn thi**

**JTBD — HYPOTHESIS:** Khi có bài học hoặc kỳ thi sắp tới, hoàn thành một đơn vị học và nhớ/áp dụng được kiến thức trong quỹ thời gian đã dành, thay vì chỉ tích lũy thời gian ngồi học. Người dùng và người hưởng lợi trực tiếp có thể là người học; người trả tiền có thể là họ hoặc phụ huynh — **UNKNOWN**, chưa có bằng chứng.

| Câu hỏi | Kết quả hiện tại |
|---|---|
| 1. Công việc và tác nhân kích hoạt? | **HYPOTHESIS:** Làm bài tập, đọc tài liệu, luyện đề khi đến lịch học hoặc gần hạn nộp/kỳ thi. Luồng cần quan sát: chọn phần học → học/làm bài → kiểm tra hiểu → chuyển phần tiếp theo. |
| 2. Gián đoạn nào? | **UNKNOWN:** Chưa có nguồn trực tiếp cho nhóm này. Điện thoại là giả thuyết từ R1-C-01; chưa phân biệt với khó hiểu bài, mệt mỏi hoặc môi trường sống. |
| 3. Đang thay thế/ứng phó bằng gì? | **UNKNOWN:** Chưa quan sát được. Cần hỏi về lần học gần nhất trước khi gợi ý các phương pháp như học nhóm, đổi nơi học hoặc cất điện thoại. |
| 4. Vì sao cách hiện tại chưa đủ? | **UNKNOWN:** Không được mặc định phương pháp hiện tại thất bại. Cũng có thể vấn đề là kiến thức nền hoặc kế hoạch học. |
| 5. Tần suất và hậu quả? | **UNKNOWN:** Chưa có số buổi bị ảnh hưởng, thời gian mất hoặc tác động đến điểm. **HYPOTHESIS:** Cường độ thay đổi theo lịch thi. |
| 6. Động lực bắt đầu/tìm công cụ? | **HYPOTHESIS:** Bài tồn đọng hoặc kỳ thi tạo động lực; chưa biết có dẫn đến tìm app hay không. |
| 7. Vì sao bỏ cuộc/bỏ công cụ? | **UNKNOWN:** Chưa có dữ liệu về bỏ phiên học hoặc ngừng dùng công cụ. |
| 8. Giá trị đo được? | **HYPOTHESIS:** Số câu làm đúng, khả năng nhớ sau một khoảng thời gian, phần học hoàn thành; cần kiểm soát độ khó. Thời gian bấm timer chưa đủ. |
| 9. Điều kiện dùng lặp lại? | **UNKNOWN:** Chưa biết nhu cầu quanh kỳ thi hay quanh năm; không có retention. |
| 10. Lý do trả tiền? | **UNKNOWN:** Chưa có chi tiêu, người quyết định mua hoặc WTP được quan sát. |

**Khoảng trống tiềm năng — HYPOTHESIS:** Người học cần Internet/tài liệu trên chính điện thoại có thể gặp xung đột giữa tiếp cận tài nguyên và tránh xao nhãng. Chưa chứng minh đây là phân khúc bị phục vụ thiếu. **Confidence: LOW.**

**R1-C-05 — Developers/designers/freelancers**

**JTBD — INFERENCE cho developer:** Khi đã chọn một tác vụ, đưa công việc đến một mốc hoàn thành có ý nghĩa dù có chuyển tác vụ. Áp dụng sang designer/freelancer vẫn là **HYPOTHESIS**. Quyền lựa chọn công cụ cá nhân, quyền sắp lịch và ngân sách có thể thuộc các bên khác nhau; **UNKNOWN** trong mẫu hiện tại.

| Câu hỏi | Kết quả hiện tại |
|---|---|
| 1. Công việc và tác nhân kích hoạt? | **VERIFIED:** C-SRC-02 gắn cảm nhận năng suất với hoàn thành tác vụ. **HYPOTHESIS:** Luồng cụ thể là nhận yêu cầu → dựng ngữ cảnh → thực hiện → kiểm tra/bàn giao; chưa quan sát trong phiên này. |
| 2. Gián đoạn nào? | **VERIFIED:** Có chuyển tác vụ/hoạt động trong C-SRC-02; cuộc họp trong lời kể C-SRC-03. **UNKNOWN:** Tỷ trọng do điện thoại, đồng nghiệp, công cụ hay tự chuyển. |
| 3. Đang thay thế/ứng phó bằng gì? | **VERIFIED, một trường hợp:** Gom cuộc hẹn cuối ngày và làm việc lập trình ban đêm, C-SRC-03. Chưa xác minh mức sử dụng timer/blocker ở phân khúc. |
| 4. Vì sao cách hiện tại chưa đủ? | **VERIFIED, lời kể:** Từ chối cuộc hẹn có thể gây khó xử; giờ gặp kéo dài vẫn thu hẹp ngày làm việc. **UNKNOWN:** Những người khác có cùng trở ngại không. |
| 5. Tần suất và hậu quả? | **UNKNOWN:** Không có ước lượng thiệt hại có thể khái quát. Không dùng lời kể “mất nửa ngày” làm hệ số năng suất cho ngành. |
| 6. Động lực bắt đầu/tìm công cụ? | **INFERENCE:** Mong hoàn thành việc lớn có ý nghĩa hơn việc đơn thuần giảm số lần chuyển. Tác nhân khiến họ tìm/mua công cụ vẫn **UNKNOWN**. |
| 7. Vì sao bỏ cuộc/bỏ công cụ? | **UNKNOWN:** Chưa có dữ liệu. **HYPOTHESIS:** Một phương pháp cản trở trao đổi cần thiết có thể không phù hợp. |
| 8. Giá trị đo được? | **HYPOTHESIS:** Mốc bàn giao đạt chất lượng, thời gian khôi phục ngữ cảnh và phần việc phải làm lại; không lấy số dòng code hay số phút tập trung làm đại diện duy nhất. |
| 9. Điều kiện dùng lặp lại? | **UNKNOWN:** Tác vụ lặp lại không chứng minh app sẽ được dùng lặp lại. |
| 10. Lý do trả tiền? | **UNKNOWN:** Không có hóa đơn, ngân sách hoặc WTP. **HYPOTHESIS:** Freelancer có thể gắn giá trị với thời gian giao hàng, nhưng chưa quan sát được mối liên hệ. |

**Khoảng trống tiềm năng — HYPOTHESIS:** Người làm tác vụ phức tạp nhưng ít quyền kiểm soát lịch. Chưa có bằng chứng riêng cho designer hoặc freelancer. **Confidence: MEDIUM cho mô tả developer trong C-SRC-02; LOW cho phần mở rộng.**

**R1-C-06 — Nhân viên văn phòng/remote**

**JTBD — HYPOTHESIS:** Hoàn thành phần việc cá nhân đúng chất lượng trong ngày, đồng thời đáp ứng nghĩa vụ phối hợp. Người sử dụng có thể là nhân viên; người kiểm soát lịch/quy định và người mua có thể là quản lý hoặc doanh nghiệp — **UNKNOWN**, chưa xác minh.

| Câu hỏi | Kết quả hiện tại |
|---|---|
| 1. Công việc và tác nhân kích hoạt? | **HYPOTHESIS:** Sau khi nhận đầu việc, chuẩn bị thông tin → xử lý → xin phản hồi → hoàn tất. Mức phụ thuộc phối hợp cần được quan sát. |
| 2. Gián đoạn nào? | **INFERENCE từ C-SRC-03:** Cuộc hẹn có thể chia nhỏ thời gian. Tin nhắn công việc, việc nhà và chăm sóc người thân ở remote đều **UNKNOWN** trong dữ liệu này. |
| 3. Đang thay thế/ứng phó bằng gì? | **UNKNOWN cho phân khúc:** Gom lịch là cách ứng phó có thật ở C-SRC-03, nhưng chưa xác minh nhân viên thông thường có quyền làm vậy. |
| 4. Vì sao cách hiện tại chưa đủ? | **HYPOTHESIS:** Mong đợi phản hồi nhanh có thể xung đột với thời gian làm việc cá nhân. Chưa có bằng chứng về chính sách hoặc áp lực thực tế. |
| 5. Tần suất và hậu quả? | **UNKNOWN:** Chưa biết số lần/ngày, làm thêm giờ, lỗi hoặc thời hạn bị ảnh hưởng. |
| 6. Động lực bắt đầu/tìm công cụ? | **HYPOTHESIS:** Việc cá nhân liên tục bị dời hoặc phải làm ngoài giờ. Chưa biết có kích hoạt tìm công cụ không. |
| 7. Vì sao bỏ cuộc/bỏ công cụ? | **UNKNOWN:** Chưa có dữ liệu sử dụng. Khả năng phương pháp cá nhân không phù hợp nhịp nhóm chỉ là **HYPOTHESIS**. |
| 8. Giá trị đo được? | **HYPOTHESIS:** Hoàn thành đầu việc trong giờ, chất lượng đầu ra và mức đáp ứng nghĩa vụ phối hợp; cần đo cả hai phía. |
| 9. Điều kiện dùng lặp lại? | **UNKNOWN:** Chưa có bằng chứng về thói quen hoặc sự chấp nhận của nhóm/quản lý. |
| 10. Lý do trả tiền? | **UNKNOWN:** Chưa biết nhân viên hay doanh nghiệp mua; không có dữ liệu ngân sách hoặc ý định mua. |

**Phản chứng cần giữ:** C-SRC-03 cho rằng lịch nhiều cuộc hẹn phù hợp với một số loại công việc. Phối hợp có thể chính là đầu ra, không phải trở ngại. **Confidence: LOW.**

**R1-C-07 — Creators/dự án cá nhân**

**JTBD — HYPOTHESIS:** Khi có khoảng thời gian tự chủ, bắt đầu và đưa một phần sáng tạo đến mốc nhìn thấy được. Cá nhân có thể vừa sử dụng vừa quyết định chi tiêu; trường hợp có khách hàng/nhà tài trợ khác cần tách riêng — **UNKNOWN**.

| Câu hỏi | Kết quả hiện tại |
|---|---|
| 1. Công việc và tác nhân kích hoạt? | **HYPOTHESIS:** Viết, dựng, thiết kế hoặc phát triển dự án cá nhân; chọn phần việc → thiết lập ngữ cảnh → tạo bản nháp → sửa → hoàn thành mốc. |
| 2. Gián đoạn nào? | **VERIFIED, lời kể C-SRC-03:** Biết trước có cuộc họp có thể làm tác giả ít muốn bắt đầu công việc tham vọng. Chưa chứng minh điều này phổ biến ở creator. |
| 3. Đang thay thế/ứng phó bằng gì? | **VERIFIED, một trường hợp:** Dành thời gian ít bị làm phiền và gom cuộc hẹn. Chưa có quan sát cộng đồng creator hoặc dự án ngoài giờ. |
| 4. Vì sao cách hiện tại chưa đủ? | **UNKNOWN:** Chưa biết người dùng thiếu thời gian, thiếu bước tiếp theo, thiếu kỹ năng hay bị xao nhãng. Các nguyên nhân này không tương đương. |
| 5. Tần suất và hậu quả? | **UNKNOWN:** Không có số phiên bỏ dở hoặc dự án không hoàn tất. |
| 6. Động lực bắt đầu/tìm công cụ? | **HYPOTHESIS:** Muốn hoàn thành một mốc tự đặt hoặc tận dụng khoảng rảnh. Chưa xác minh động lực tìm app. |
| 7. Vì sao bỏ cuộc/bỏ công cụ? | **UNKNOWN:** Không có lịch sử ngừng dùng. Không thể quy bỏ dự án cho thiếu tập trung. |
| 8. Giá trị đo được? | **HYPOTHESIS:** Bản nháp hoặc mốc hoàn thành theo tiêu chí đặt trước; thời gian bắt đầu lại sau gián đoạn. Chất lượng cần đánh giá riêng. |
| 9. Điều kiện dùng lặp lại? | **UNKNOWN:** Chưa biết nhịp làm dự án đều đặn hay theo đợt; không có retention. |
| 10. Lý do trả tiền? | **UNKNOWN:** Không có bằng chứng người làm dự án cá nhân trả tiền để cải thiện việc tập trung. |

**Khoảng trống tiềm năng — HYPOTHESIS:** Người làm dự án ngoài giờ với những khoảng rảnh ngắn, khó dự đoán. Nguồn hiện có không đại diện cho họ. **Confidence: LOW.**

**4. Bằng chứng còn thiếu và cách nghiên cứu không dẫn dắt**

Chưa thể gọi bất kỳ nhóm nào là “underserved”: chưa có chuỗi bằng chứng về vấn đề lặp lại → cách ứng phó thực tế → thất bại của cách ứng phó → hậu quả đủ lớn. Cũng chưa xác định người mua, khả năng chi trả hay nhu cầu dùng app trên điện thoại.

Đề xuất nghiên cứu tiếp theo, **chưa thực hiện và không có outreach trong phiên này**:

- Lấy mẫu có chủ đích trong bốn nhóm, bao gồm người đang dùng công cụ, đã bỏ và chưa từng dùng; tách VN, quốc gia SEA cụ thể và thị trường quốc tế. Không gộp để suy ra mức phổ biến.
- Dựng lại **một phiên gần nhất**, kể cả phiên thành công: “Bạn định hoàn thành gì? Điều gì xảy ra tiếp theo? Khi dừng hoặc đổi việc, nguyên nhân là gì? Sau đó bạn làm gì?” Chưa nhắc đến app focus.
- Nếu được cho phép trong nghiên cứu sau, đối chiếu lời kể với nhật ký ngắn và đầu ra phù hợp, tránh thu dữ liệu nhạy cảm không cần thiết. Phân biệt tự chuyển tác vụ, gián đoạn bên ngoài và chuyển việc cần thiết.
- Hỏi về công cụ/phương pháp thực sự đã dùng, lần cuối dùng, lần bỏ, khoản chi đã phát sinh và người quyết định. Không dùng câu “Bạn có trả tiền cho app giúp tập trung không?” làm bằng chứng WTP.
- Chủ động tìm trường hợp bác bỏ: người chuyển việc nhiều vẫn hoàn thành tốt; người tập trung được nhưng không hoàn thành vì yêu cầu mơ hồ; người dùng cách miễn phí đã đủ; người có vấn đề nhưng không muốn thêm công cụ.

**5. Nhật ký truy vấn và truy cập**

Ba truy vấn tiếng Anh, ngày 20/11/2026, không giới hạn địa lý:

1. `"blocking mobile internet" sustained attention 2025 adherence study`
2. `developer task interruption productivity study self interruptions external interruptions 2018`
3. `site.reddit.com/r/productivity pomodoro doesn’t work studying creative flow`

Công cụ trả về 30 mục kết quả tổng cộng, đều lệch chủ đề; không mở và không dùng snippet để kết luận. Nguồn đọc trực tiếp gồm Crossref/abstract PNAS Nexus, trang Microsoft Research và bài viết cá nhân Paul Graham; không có thảo luận Reddit được đọc thành công.

**Số lần fetch: 6; thành công: 3; nguồn thực sự kiểm tra: 3.** Các URL không đọc được:

- HTTP 403: https://doi.org/10.1093/pnasnexus/pgaf017
- HTTP 403: https://academic.oup.com/pnasnexus/article/4/2/pgaf017/8016017
- HTTP 404: https://www.microsoft.com/en-us/research/publication/the-work-life-of-developers-activities-switches-and-perceived-productivity/

Dừng ở giới hạn nguồn đã giao. Đây là bản đồ vấn đề và khoảng trống bằng chứng để CIO sử dụng; không xếp hạng thương mại hoặc đề xuất hướng sản phẩm.

