# R2 product challenges demand

State SENT, awaiting response.
Tool mcp__agent_hub__agent_followup

```json
{
  "id": "0b7c9806-f929-49fe-902c-12c72787f5df",
  "agentId": "063b5d09-c493-4fdf-ad91-609f138689d5",
  "sessionId": "7d889320-b711-43ea-9c96-81b3ac60b712",
  "workspace": "/Users/trankhanh/MyFolder/innovation-lab",
  "continuationOf": "063b5d09-c493-4fdf-ad91-609f138689d5",
  "title": "Fokus R2 product challenges demand",
  "status": "starting",
  "createdAt": "2026-11-20T10:25:14.359Z",
  "threadId": "01a1f87a-7551-78b3-a137-2cbe7291a942",
  "archived": false,
  "error": null,
  "attempts": 1,
  "toolsetVersion": 2,
  "startedAt": "2026-11-20T10:25:14.362Z",
  "retryAt": null,
  "promptBytes": 69814,
  "outputLength": 0
}
```

## Exact packet

R2-P: Respond to customer R1-C findings by ID: does available pain support a sustainable product? Formulate explicit critique/question back to customer. Assess seven inventor directions, propose at most 3 competing strategies for research, distinguish monetization, distribution, healthy retention, MVP must/should/could/out. Respond also to technical R1-T constraints in packet. No new browsing. <=1600 words, 3 minutes. These are recommendations, no Founder selection.

Actual peer customer-researcher runtime e1132a6f-29ac-4787-b478-9bc5d412cc4e:
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

Actual inventor 5d264061-98c1-4906-bc66-d5fb0d3b6648:
Tôi sẽ dùng skill creative-ideation để phát triển các hướng độc lập cho Fokus Time, phân biệt theo cơ chế thay đổi công việc và hành vi. Tôi sẽ chỉ đọc hướng dẫn được chỉ định, không xem ý tưởng của phiên khác hay tra cứu web; mọi đề xuất sẽ được gắn nhãn HYPOTHESIS.


Tôi đã tách được bảy cơ chế: thu hẹp đầu ra, giữ ngữ cảnh khi bị ngắt, đổi ca bảo vệ thời gian, ghép việc với hoàn cảnh, giới hạn mục đích tra cứu, kiểm chứng kết quả học và cam kết bằng tiền đặt cọc. Các hướng phụ thuộc vào người cùng tham gia, quyền của hệ điều hành hoặc xử lý tiền sẽ được nêu rõ giới hạn; chưa có bằng chứng về nhu cầu hay tính mới.


**Bàn giao CIO — SES-20261120-04, vòng ý tưởng độc lập R1, ngày 20/11/2026.** Bảy hướng dưới đây là bảy giả thuyết sản phẩm riêng, không phải danh sách tính năng để ghép thành một ứng dụng.

Toàn bộ nhận định về khách hàng, vấn đề, cách xoay xở hiện tại, lợi ích, khác biệt và thương mại đều là **HYPOTHESIS; độ tin cậy LOW** vì chưa có bằng chứng thực địa. Chưa xác định thị trường địa lý. Không giả định hiệu quả lâm sàng, không khẳng định tính mới và không chọn ý tưởng thay Founder.

**F-A — “Đủ để giao” · R1-I-01 / CLM-I-01**

- **Ai, việc gì, lúc nào:** Người làm nội dung hoặc freelancer chuẩn bị một đầu ra nhỏ như đề cương, bản nháp hay báo giá. Kích hoạt khi biết phải làm gì nhưng chưa biết làm đến đâu thì đủ. Giả thuyết vấn đề: phạm vi mơ hồ khiến họ tiếp tục nghiên cứu, chỉnh sửa hoặc trì hoãn. Cách xoay xở giả định: checklist, tự đặt deadline, nhờ người khác nhắc dừng.
- **Lời hứa và cơ chế:** “Chốt được thứ có thể giao trước khi bắt đầu.” Người dùng chọn đầu ra nhỏ nhất có ích, tối đa ba dấu hiệu hoàn thành và một phần chủ động bỏ khỏi lượt này. Cơ chế là **loại bỏ công việc không cần thiết**, thay vì kéo dài khả năng tập trung. Phương pháp: first principles và SCAMPER–eliminate. Khác biệt giả thuyết nằm ở quyết định phạm vi và điểm dừng.
- **Hành trình mobile:** Khi nhận việc, mở app → ghi đầu ra và người sẽ dùng nó → xác định tiêu chí “đủ” cùng phần để sau → chuyển sang nơi làm việc, có thể là máy tính → khi muốn mở rộng phạm vi, ghi phần phát sinh vào lượt kế tiếp → trở lại đối chiếu sản phẩm với tiêu chí → kết thúc hoặc sửa đúng điểm chưa đạt. Khi yêu cầu thật sự thay đổi, sửa thỏa thuận và lưu lý do; không coi đó là thất bại.
- **Nhận dùng / bỏ dùng:** Có thể bắt đầu với một việc đang mắc, không cần nhập toàn bộ dự án. Có thể bỏ nếu bước xác định tiêu chí tốn công hơn chính công việc hoặc tạo cảm giác phải lập kế hoạch hai lần.
- **Giả định, độ khó và thương mại:** Người dùng có quyền điều chỉnh phạm vi; tiêu chí đủ rõ và không làm giảm chất lượng cần thiết. Độ phức tạp sản phẩm dự kiến thấp–vừa. Khó thương mại: dễ thay bằng mẫu ghi chú; khả năng bán gói theo nghề hoặc mua một lần chỉ là giả thuyết, chưa có căn cứ cho thuê bao.
- **Lợi ích và phép bác bỏ:** Đo thời gian đến bản có thể giao, số lần mở rộng phạm vi và số lần bị yêu cầu làm lại. Bước học rẻ nhất được đề xuất: cùng một người áp dụng thỏa thuận phạm vi vào một số việc tương đương với cách làm thường lệ, rồi nhờ người nhận đánh giá đầu ra theo cùng tiêu chí. Bác bỏ nếu nhanh hơn chủ yếu do bỏ sót yêu cầu, hoặc chi phí lập thỏa thuận xóa hết thời gian tiết kiệm.

**F-B — “Vé quay lại” · R1-I-02 / CLM-I-02**

- **Ai, việc gì, lúc nào:** Người viết, học hoặc xử lý hồ sơ thường bị ngắt giữa chừng bởi việc gia đình hoặc yêu cầu đột xuất. Kích hoạt ngay trước khi rời việc. Giả thuyết vấn đề: trở lại nhưng phải đọc lại, nhớ lại và quyết định lại. Cách xoay xở giả định: để nguyên tab, ghi chú rời hoặc trông cậy vào trí nhớ.
- **Lời hứa và cơ chế:** “Quay lại đúng bước còn dang dở.” Lưu một gói ngữ cảnh gồm vị trí, điều đang mắc và hành động tiếp theo đủ cụ thể. Cơ chế là **chuyển chi phí tái dựng ngữ cảnh sang lúc ngữ cảnh còn rõ**. Phương pháp: chuyển giao kiến thức từ quy trình bàn giao ca. Khác biệt giả thuyết nằm ở phục hồi công việc sau gián đoạn.
- **Hành trình mobile:** Người dùng chủ động mở thao tác lưu nhanh → nói hoặc gõ “đang ở đâu; bước tới là gì” → thêm liên kết hoặc ảnh nếu cần → rời việc → khi quay lại chọn vé đang chờ → đọc bước tiếp theo và mở tài liệu bằng cách phù hợp → đánh dấu đã tiếp tục hoặc cập nhật điều kiện mới → lưu trữ vé khi xong. Nếu bị ngắt quá bất ngờ, có thể tạo vé thiếu thông tin sau đó; sản phẩm không hứa tự nhận biết mọi gián đoạn.
- **Nhận dùng / bỏ dùng:** Một lần quay lại thuận lợi có thể tạo giá trị sớm. Dễ bỏ nếu quên ghi vé, có quá nhiều vé cũ hoặc phải chuyển sang điện thoại chỉ để lưu việc đang làm trên máy tính.
- **Giả định, độ khó và thương mại:** Cần một khoảng ngắn trước khi rời việc; người dùng phải chấp nhận lưu nội dung công việc. Độ phức tạp thấp–vừa nếu ghi thủ công; quyền truy cập sâu giữa các ứng dụng là UNKNOWN. Giả thuyết thu tiền: tiện ích cá nhân trả phí. Khó thương mại: ghi chú và công cụ công việc hiện tại có thể đã đáp ứng đủ.
- **Lợi ích và phép bác bỏ:** Đo thời gian từ lúc quay lại đến hành động có ích đầu tiên, số lần đọc lại và thời gian tạo vé. Bước học rẻ nhất: thử nghi thức bàn giao bằng công cụ ghi chú sẵn có, so với các lần gián đoạn tương tự. Bác bỏ nếu không nhớ dùng ở đúng thời điểm hoặc thời gian tiết kiệm không bù công ghi lại.

**F-C — “Đổi ca tập trung” · R1-I-03 / CLM-I-03**

- **Ai, việc gì, lúc nào:** Hai người trưởng thành cùng chia sẻ việc nhà hoặc trách nhiệm chăm sóc, mỗi người đều cần khoảng thời gian làm việc riêng. Kích hoạt khi cả hai có việc quan trọng và cùng có nguy cơ bị gọi xử lý việc chung. Cách xoay xở giả định: thương lượng miệng, nhắn tin hoặc âm thầm gánh thay nhau.
- **Lời hứa và cơ chế:** “Có người nhận phần gián đoạn để bạn làm xong một việc.” Hai bên trao đổi những ca có phạm vi và điều kiện rõ ràng. Cơ chế là **phân bổ lại trách nhiệm**, dùng nguyên lý đổi ca và có đi có lại. Khác biệt giả thuyết: giải quyết nguồn gián đoạn nằm ngoài cá nhân.
- **Hành trình mobile:** Một người đề xuất khoảng cần tập trung, đầu ra và trách nhiệm cần người kia nhận → người kia xem rồi chấp nhận hoặc điều chỉnh → cùng xác định trường hợp vẫn phải ngắt ca → bắt đầu → nếu cần thay đổi, chủ động kết thúc hoặc thương lượng lại → cuối ca ghi đã nhận được bao nhiêu thời gian sử dụng được → đề nghị lượt đổi lại. Việc mời, chấp thuận và trao đổi này chỉ là hành trình dự kiến, chưa được thực hiện.
- **Nhận dùng / bỏ dùng:** Giá trị chỉ xuất hiện khi người thứ hai tham gia; lịch sử đổi ca có thể giúp thấy sự công bằng. Có thể bỏ vì một bên thiếu thời gian để đổi lại, cảm thấy bị tính công hoặc không muốn thêm ứng dụng cho quan hệ cá nhân.
- **Giả định, độ khó và thương mại:** Có lòng tin và khả năng bàn giao trách nhiệm thật sự; ứng dụng không thay thế việc đánh giá khả năng chăm sóc hoặc xử lý khẩn cấp. Độ phức tạp vừa về sản phẩm, cao về duy trì phối hợp. Giả thuyết doanh thu: gói hộ gia đình. Khó thương mại: thói quen của hai người và sự sẵn lòng trả tiền đều chưa biết.
- **Lợi ích và phép bác bỏ:** Đo thời gian liên tục thực sự sử dụng được của **cả hai**, công thương lượng và số ca bị phá vỡ. Bước học rẻ nhất: đề xuất thử thỏa thuận đổi ca bằng lịch đang dùng, không tạo tài khoản mới. Bác bỏ nếu tổng thời gian hữu ích không tăng hoặc lợi ích của một người đến từ gánh nặng không được đồng thuận của người còn lại.

**F-D — “Việc vừa với lúc này” · R1-I-04 / CLM-I-04**

- **Ai, việc gì, lúc nào:** Người học hoặc làm việc linh hoạt có những khoảng rảnh khó đoán: đang chờ, thiếu bàn, mạng yếu hoặc chỉ có điện thoại. Kích hoạt khi có khoảng trống nhưng không đủ điều kiện cho việc ưu tiên lớn. Cách xoay xở giả định: mở danh sách dài, chọn đại hoặc lướt nội dung.
- **Lời hứa và cơ chế:** “Hoàn thành một phần việc hợp với điều kiện hiện có.” Trước đó, người dùng tách việc thành đơn vị có đầu ra và ghi điều kiện cần. Lúc rảnh, chọn việc theo điều kiện thực tế. Cơ chế là **đổi thứ tự công việc theo khả năng thực hiện**, lấy phép tương tự từ điều phối sản xuất; không mặc định mọi khoảng trống đều phải được tận dụng.
- **Hành trình mobile:** Khi chuẩn bị việc, ghi một hành động có thể hoàn thành và điều kiện của nó → lúc rảnh chọn thời gian, mức yên tĩnh, kết nối và khả năng đọc/gõ → nhận một số ít lựa chọn phù hợp → chọn một việc và mở tài liệu cần thiết → lưu đầu ra → đánh dấu hoàn thành. Nếu hoàn cảnh kết thúc sớm, ghi điểm dừng; nếu không có việc phù hợp, kết thúc phiên mà không thúc ép làm thêm.
- **Nhận dùng / bỏ dùng:** Có thể bắt đầu bằng vài việc thật. Dễ bỏ vì phải chia nhỏ và gắn điều kiện trước, hoặc vì đề xuất “vừa lúc” dẫn đến né mãi công việc khó nhưng quan trọng.
- **Giả định, độ khó và thương mại:** Việc có thể chia nhỏ mà vẫn giữ ý nghĩa; thời gian ước lượng đủ hữu ích. Độ phức tạp vừa, có thể xét điều kiện người dùng nhập mà không cần giả định quyền truy cập cảm biến. Giả thuyết doanh thu: gói theo hoạt động cụ thể như học ngoại ngữ hoặc xử lý công việc hành chính. Khó thương mại: lợi ích dễ bị xem là một chức năng của danh sách việc.
- **Lợi ích và phép bác bỏ:** Đo số đầu ra có ích hoàn thành, thời gian chọn việc, thời gian chuẩn bị và tiến độ của việc ưu tiên lớn. Bước học rẻ nhất: đối chiếu nhật ký khoảng rảnh với công việc thực tế, rồi thử cách chọn này bằng danh sách hiện có. Bác bỏ nếu chỉ tăng số việc vụn hoặc việc chuẩn bị tốn nhiều hơn giá trị thu được.

**F-E — “Phiếu tra cứu” · R1-I-05 / CLM-I-05**

- **Ai, việc gì, lúc nào:** Người đang viết, học hoặc mua sắm có chủ đích, cần mở điện thoại để trả lời một câu hỏi nhưng dễ đi sang nội dung khác. Kích hoạt ngay trước lượt tra cứu. Cách xoay xở giả định: tự nhắc mục tiêu, đặt giới hạn thời gian hoặc chặn cả ứng dụng dù vẫn cần dùng.
- **Lời hứa và cơ chế:** “Lấy được câu trả lời rồi quay về việc chính.” Trước khi mở nguồn, người dùng xác định câu hỏi và điều kiện kết thúc; ý muốn tìm thêm được ghi riêng. Cơ chế là **giữ mục đích của lần truy cập và tạo điểm thoát rõ ràng**. Phương pháp: đảo ngược vấn đề — cho phép lượt truy cập cần thiết nhưng buộc xác định nó dùng để làm gì.
- **Hành trình mobile:** Ghi câu hỏi ngắn → chọn loại kết quả đủ dùng, chẳng hạn một con số hoặc một nguồn đáng tin → mở nguồn tra cứu → quay lại ghi kết quả và nguồn → chọn “đã đủ”, “chưa tìm được” hoặc “cần đổi câu hỏi” → đóng phiếu và trở về việc ban đầu. Nội dung hấp dẫn nhưng ngoài mục đích được để cho lần khác. Bản giả thuyết cơ bản dựa trên hành động chủ động, không hứa tự giám sát hay đóng ứng dụng khác.
- **Nhận dùng / bỏ dùng:** Có thể thử ngay trong một lượt tra cứu. Dễ bỏ nếu phải gõ nhiều, quên quay lại hoặc phần lớn công việc mang tính khám phá, chưa thể biết trước câu hỏi.
- **Giả định, độ khó và thương mại:** Một phần đáng kể lượt tra cứu có đích đến hữu hạn. Độ phức tạp thấp–vừa ở cơ chế thủ công; khả năng can thiệp giữa các ứng dụng là UNKNOWN. Giả thuyết thu tiền: tiện ích mua một lần. Khó thương mại: ý định tốt có thể không đủ tạo thói quen hoặc nhu cầu trả phí.
- **Lợi ích và phép bác bỏ:** Đo tỷ lệ lượt tra cứu kết thúc với câu trả lời dùng được, thời gian đi lệch mục tiêu và chi phí tạo phiếu. Bước học rẻ nhất: dùng câu hỏi viết trước trong các lượt tra cứu thực tế và tự ghi lại kết quả; phải nêu rõ sai lệch của tự báo cáo. Bác bỏ nếu người dùng vẫn đi lệch như cũ hoặc câu hỏi định trước làm mất những khám phá có giá trị.

**F-F — “Mốc hiểu thật” · R1-I-06 / CLM-I-06**

- **Ai, việc gì, lúc nào:** Người trưởng thành tự học kiến thức có đáp án hoặc bài tập kiểm tra được. Kích hoạt trước và sau một phần học. Giả thuyết vấn đề: thời gian ngồi học và số trang đã đọc không phản ánh việc có sử dụng được kiến thức hay chưa. Cách xoay xở giả định: ghi giờ học, tô sáng và đọc lại.
- **Lời hứa và cơ chế:** “Biết phần nào đã làm được và phần nào cần học tiếp.” Người dùng thử trả lời hoặc giải một nhiệm vụ trước khi xem lại tài liệu, rồi đối chiếu với nguồn kiểm tra đã chọn. Cơ chế là **chuyển kiểm chứng vào trung tâm vòng làm việc**, lấy nhiệm vụ chứng minh hiểu làm đơn vị tiến bộ. Khác biệt giả thuyết nằm ở việc định hướng phiên học tiếp theo theo lỗi thực tế.
- **Hành trình mobile:** Chọn một mục tiêu học và câu hỏi có cách kiểm tra → thử trả lời để biết điểm xuất phát → học từ tài liệu đang có → quay lại trả lời khi không nhìn tài liệu → mở đáp án hoặc lời giải để đối chiếu → ghi sai ở đâu → chọn học tiếp đúng phần đó hoặc kết thúc khi đạt tiêu chí. Nếu không có nguồn đối chiếu đáng tin, kết quả chỉ được lưu là chưa kiểm chứng. Không cần giả định AI chấm đúng.
- **Nhận dùng / bỏ dùng:** Có thể hấp dẫn người muốn thấy tiến bộ cụ thể. Có thể bỏ vì chuẩn bị câu hỏi tốn công, cảm giác bị kiểm tra liên tục hoặc nội dung học khó đánh giá bằng câu trả lời ngắn.
- **Giả định, độ khó và thương mại:** Có nguồn kiểm tra phù hợp và câu hỏi đại diện cho năng lực cần học. Độ phức tạp vừa nếu dùng tài liệu người học đã có; gánh nặng tăng khi sản phẩm tự cung cấp nội dung. Giả thuyết doanh thu: gói cho một lĩnh vực học cụ thể. Khó thương mại: có thể trùng nhiều công cụ học hiện hữu; chưa tra cứu nên mức trùng lặp UNKNOWN.
- **Lợi ích và phép bác bỏ:** Đo khả năng làm một bài tương đương sau khoảng trì hoãn đã định trước, thời gian chuẩn bị và mức duy trì sử dụng. Bước học rẻ nhất: dùng bài tập có lời giải sẵn để so hai cách tổ chức học với nội dung tương đương. Bác bỏ nếu chỉ cải thiện câu đã luyện, không chuyển sang bài tương đương, hoặc người dùng bỏ vì công kiểm tra quá lớn.

**F-G — “Cam kết có giá” · R1-I-07 / CLM-I-07**

- **Ai, việc gì, lúc nào:** Người có một đầu việc cá nhân rõ ràng, tự kiểm soát được nhưng liên tục trì hoãn dù đã có lịch nhắc. Kích hoạt khi người dùng chủ động muốn tạo hậu quả cho lần không thực hiện. Cách xoay xở giả định: nhờ bạn nhắc, công khai deadline hoặc tự hứa phần thưởng.
- **Lời hứa và cơ chế:** “Biến lời hẹn với bản thân thành một cam kết có chi phí rõ ràng.” Người dùng tự chọn một khoản đặt cọc nhỏ, tiêu chí hoàn thành và người xác nhận đồng thuận. Cơ chế là **thay đổi động lực bằng cam kết tài chính**, khác với giảm phân tâm hay sắp việc. Đây không phải khẳng định con người sẽ làm tốt hơn khi có nguy cơ mất tiền.
- **Hành trình mobile:** Chọn đầu ra có thể kiểm chứng → đọc và chấp nhận điều kiện hoàn, mất cọc, hủy trước khi bắt đầu và xử lý bất đồng → chọn người xác nhận, chờ họ đồng ý → kích hoạt cam kết → làm việc ngoài app → nộp bằng chứng tối thiểu → nhận xác nhận hoặc yêu cầu làm rõ → xem kết quả và quyết định có dùng tiếp. Khi có tranh chấp, không tự suy ra gian lận từ việc thiếu bằng chứng. Đây chỉ là hành trình giả định, chưa kiểm tra khả năng xử lý tiền.
- **Nhận dùng / bỏ dùng:** Có thể hấp dẫn người chủ động tìm mức cam kết mạnh hơn. Có thể bỏ ngay vì không tin cơ chế giữ tiền, không tìm được người xác nhận hoặc trải nghiệm mất cọc gây phản ứng tiêu cực.
- **Giả định, độ khó và thương mại:** Tiêu chí khó lách nhưng dễ xác nhận; rủi ro tiền bạc được người dùng hiểu và tự nguyện chọn. Độ phức tạp cao vì thanh toán, hoàn tiền, tranh chấp và hỗ trợ. Điều kiện pháp lý, chính sách cửa hàng ứng dụng và nhà cung cấp thanh toán đều UNKNOWN. Giả thuyết doanh thu: phí dịch vụ cố định, tách khỏi tiền phạt để giảm xung đột lợi ích; khả năng trả phí chưa biết.
- **Lợi ích và phép bác bỏ:** Đo tỷ lệ hoàn thành đúng tiêu chí, chất lượng đầu ra, số tranh chấp và mức sẵn lòng sử dụng lại sau cả thành công lẫn thất bại. Bước học rẻ nhất: đề xuất nghiên cứu những cam kết tự nguyện người dùng đã thực hiện, gồm bằng chứng hành vi và trải nghiệm mất tiền; không thu hay giữ tiền trong bước này. Bác bỏ nếu nhu cầu biến mất khi trình bày đầy đủ điều kiện, hoặc chi phí xác minh và tranh chấp lớn hơn giá trị. Bước nghiên cứu đầu chỉ kiểm tra mức chấp nhận, chưa chứng minh tác động nhân quả.

**Giới hạn bằng chứng và nhật ký nguồn**

- **VERIFIED — CLM-I-00:** Ba tài liệu hướng dẫn dưới đây đã được đọc thành công. Chúng hỗ trợ cách làm và cách gắn nhãn, không chứng minh bất kỳ nhu cầu khách hàng nào.
- **UNKNOWN:** Quy mô và tần suất vấn đề, đối thủ, mức khác biệt thực tế, khả năng trả tiền, hiệu quả sử dụng, quyền tích hợp và các điều kiện vận hành. Chưa có phản chứng thực địa; các phép bác bỏ bên trên là đề xuất tìm phản chứng.
- **Độc lập:** Không đọc backlog, kết quả phiên khác hoặc phương án của agent khác. Đây là bản gốc R1; chưa có phản biện chéo hay đồng thuận chuyên gia để báo cáo.
- **Tra cứu:** 0 truy vấn web; 0 nguồn web; 0 URL ngoài; 3 tệp hướng dẫn nội bộ; 0 nguồn khách hàng hoặc thị trường. Không kiểm tra khả dụng của web vì nhiệm vụ yêu cầu không sử dụng web.
- **Thực thi:** Không chỉnh sửa tệp, tạo prototype, liên hệ người dùng, lập tài khoản, xử lý tiền hoặc chạy thí nghiệm. Mọi bước học đều là đề xuất tư vấn.

| Mã nguồn | Đường dẫn chính xác và vị trí | Nội dung áp dụng | Giới hạn |
|---|---|---|---|
| SRC-I-001 | [AGENTS.md](/Users/trankhanh/MyFolder/innovation-lab/AGENTS.md), “Mission and authority”, “Evidence and decisions” | Phạm vi tư vấn; phân loại bằng chứng; Founder quyết định | Hướng dẫn nội bộ, không phải dữ liệu thị trường |
| SRC-I-002 | [creative-ideation/SKILL.md](/Users/trankhanh/MyFolder/innovation-lab/.agents/skills/creative-ideation/SKILL.md), “Procedure”, “Evidence requirements” | Đa dạng cơ chế; độc lập ban đầu; giả thuyết có thể bác bỏ | Không xác nhận tính mới hoặc nhu cầu |
| SRC-I-003 | [evidence-policy.md](/Users/trankhanh/MyFolder/innovation-lab/protocols/evidence-policy.md), “Claim classes”, “Source and claim ledger” | Nhãn claim, nguồn, độ tin cậy và giới hạn | Quy tắc ghi nhận, không phải bằng chứng hiệu quả |

Ngày truy cập cả ba nguồn: **20/11/2026, Asia/Ho_Chi_Minh**. Ngày xuất bản không có trong nội dung đã đọc. Bản bàn giao giữ nguyên bảy hướng để CIO đối chiếu với nghiên cứu thực tế; chưa đề nghị SELECT. Quyết định của Founder, kể cả SELECT, không cấp quyền phát triển sản phẩm.

Actual technical peer 10d78682-5049-4af6-ab38-d882a7fb7e1e:
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

Market R1 record and current CIO supplement are in sessions/2026-11-20-04-fokus-time/records; read as needed, no new sources. Research only, no edits/delegation/outreach/implementation.

