# Red Team R1 — F1-N / F3-N, không phải broad timer

SES-20261121-01 · 2026-11-21 · runtime `/root/fokus_redteam_sol`, remit Independent Red Team Critic; model được CIO chỉ định gpt-6.1-sol. Không tạo agent khác. Exclusive notes này là initial judgment; không sửa shared ledger/backlog hoặc quyết định Founder.

Đã đọc frozen `red-team-input.md`, toàn bộ Inventor R3, Customer R2/R3, Market R2, Technical R2, Strategy R1, initial mechanisms Inventor R1 và evidence-ledger. Nguồn customer/market/technical cũ dưới đây là **peer-relayed evidence**, không gọi là tự kiểm tra web lại. Đã đọc adversarial-review, evidence policy, debate rules và AGENTS.md. Strategy R2 không nằm trong frozen input; không suy đã nhận hoặc đồng ý. Mọi phép thử dưới đây là **đề xuất chưa thực hiện**, không là yêu cầu build/outreach.

## Phán đoán độc lập ban đầu

**INFERENCE / MEDIUM:** Revision R3 cải thiện tính trung thực và khả năng duy trì: bỏ camera, blocker, sync, AI và lời hứa cứu mọi interruption. Nó đồng thời làm lý do tồn tại của app riêng mỏng hơn. F1-N hiện là một quy tắc bàn giao đặt cạnh công việc; F3-N là một chu trình đối chiếu việc học với tiêu chí có sẵn. Một kỹ thuật hữu ích có thể được tiếp thu rồi dùng trong công cụ khác. Hiện chưa có căn cứ nâng hai hướng từ câu hỏi nghiên cứu sang cơ hội sản phẩm mobile có demand.

**Không thấy fatal barrier đã được chứng minh.** Những rủi ro dưới có thể giết từng hướng nếu điều kiện xảy ra; chưa có quan sát target chứng minh chúng đã xảy ra. Tôi không bác bỏ vì crowded market hoặc vì app nhỏ. Tôi cũng không chấp nhận việc thu hẹp segment như bằng chứng có người thật trong segment.

## RT1 — F1-N có thể đã thu hẹp vào nhóm ít cần sản phẩm nhất

- **Concern / INFERENCE, confidence MEDIUM về causal logic, LOW về prevalence:** người phone-primary có điểm rời tự chọn đã loại được hai tổn thất lớn của F1 gốc: bị cắt ngang bất ngờ và đổi thiết bị. Nhưng người đó đang ở ngay tài liệu/draft; thêm một dòng next action tại đó có thể loại nhu cầu mở surface thứ hai. Thu hẹp làm capture dễ hơn không chứng minh chi phí dựng lại đủ lớn. Trường hợp đọc có thể chỉ cần vị trí đang đọc; trường hợp viết có thể cần ghi chú ngay draft. Reader/bookmark là đối chứng thật, không chỉ Forest.
- **Evidence/unknown:** D3-F1 thừa nhận chưa có mobile increment; CX1/C4 không có field evidence target. Tôi đã tìm Apple Books nhưng không đọc được trang, nên **không xác minh** bookmark/save-place của vendor trong vòng này; e-reader là category substitute cần kiểm tra, không equivalence fact.
- **Impact:** dù handoff giảm restart cost so với không ghi gì, standalone app có thể không có giá trị tăng thêm và thêm switching overhead.
- **Falsifier/giảm lo ngại:** ở cùng task, same-prompt note tại nơi đang làm so với một surface riêng, tính toàn bộ capture→retrieval→resume, chất lượng và lần quên dùng. Lo ngại giảm khi có lỗi tái dựng lặp lại mà note ngay tại task chưa giải được và người dùng tự chọn surface riêng qua các cơ hội tương tự. Chỉ mô tả hành trình không đo được performance mobile.
- **Câu hỏi bắt buộc Inventor:** sau R3, hãy nêu **một lỗi cụ thể còn lại** của note tại draft/reader mà surface riêng xử lý bằng cơ chế đã giữ. Nếu hiện chưa nêu được, anh có ghi F1-N là câu hỏi khám phá pain trước, thay vì tiếp tục gọi nó là candidate app không?
- **Counterevidence:** một active handoff có thể giảm nhiễu của kho notes lớn; đó là lợi thế HYPOTHESIS cần so với một note/prompt duy nhất ngay tại task, không so với toàn bộ notes lộn xộn.

## RT2 — F3-N tiến gần flashcard/study workflow hơn khi bỏ tự chứng nhận

- **Concern / INFERENCE, MEDIUM:** target đã có bộ recall/đáp án là target có thể dùng công cụ luyện recall đang có. Thêm chu trình dự báo–làm–đối chiếu–chọn phần ôn tiếp có thể là lớp thao tác quanh công cụ học, không giải quyết thiếu công cụ. Đối chứng chỉ worksheet chưa đủ nếu người đó hiện dùng flashcards.
- **VERIFIED hẹp, tự đọc RT-S1:** Anki hiển thị câu hỏi trước, rồi đáp án để người học so với câu trả lời đã nghĩ; các nút Again/Hard/Good/Easy biểu thị sai/khó/đúng/dễ và thời điểm ôn tiếp. Nguồn không chứng minh Anki bằng F3-N, có rubric học thuật, hay cải thiện learning trong target.
- **VERIFIED hẹp, tự đọc RT-S2:** RemNote mô tả đặt ngày thi cho document/folder, điều chỉnh lịch luyện flashcard và có lựa chọn cần hai câu đúng liên tiếp trước khi tính mastered. Đây là vendor capability claim, không phải bằng chứng mastery hay retention thật.
- **Impact:** tập con recall ngắn cạnh tranh trực tiếp hơn với study tools; bài tập mở/dài có thể ít phù hợp flashcard hơn nhưng khi đó rubric/độ khó và thao tác điều phối lại khó hơn. Không được chuyển sang tutor/content engine để bảo vệ differentiator.
- **Falsifier/giảm lo ngại:** đối chứng phải là workflow thực sự của learner gồm flashcards khi họ dùng, cộng same-prompt worksheet; cùng nội dung/độ khó, delayed independent performance và tổng thời gian. Lo ngại giảm nếu chỉ ra task kiểm tra có tiêu chí rõ nhưng công cụ hiện tại bỏ sót một lỗi lặp, và cơ chế F3-N giải lỗi đó ròng.
- **Câu hỏi bắt buộc Inventor:** với bằng chứng RT-S1/2, hãy chỉ rõ F3-N giữ khác biệt nào ngoài dự báo trước và ghi lỗ hổng. Nếu phần mới chỉ là prompt tự dùng được trong công cụ học, anh có rút standalone app? Không cần chứng minh novelty, cần chứng minh increment.
- **Counterevidence:** flashcards không mặc nhiên thay thế bài luận, bài toán nhiều bước hoặc tiêu chí về phương pháp. Không có inspected source xác minh full equivalence; kết luận là duplication risk tăng trong recall subset, không phải duplicate toàn bộ.

## RT3 — cài tuần đầu và quay lại tuần hai là hai quyết định chưa có cầu nối

- **Concern / HYPOTHESIS:** một thất bại gần đây có thể đủ để thử kỹ thuật, nhưng giá trị của app phải thắng việc tự ghi next action hoặc tự đối chiếu bài. Sau học prompt, người dùng có thể không còn cần app. Đây có thể là thành công khách hàng và thất bại retention/subscription cùng lúc.
- **Evidence:** Customer R3 tách practice/product/business, Strategy R1 thừa nhận healthy exit. Demand, voluntary repeat và payment trong F1-N/F3-N đều **UNKNOWN**; không có uninstall/cohort evidence.
- **Impact:** app hoàn hảo vẫn thất bại nếu job ít lặp, người dùng nhớ được quy tắc sau vài lần, hoặc tự chuyển kỹ thuật về nơi đang làm. Daily active ép lại sẽ che vấn đề thay vì chữa nó.
- **Falsifier/giảm lo ngại:** sau giai đoạn có hướng dẫn, quan sát **cơ hội có job thật ở tuần hai**, lựa chọn tự nguyện giữa current tool/same-prompt artifact/app khi có nghiên cứu performance được cho phép; ghi lý do không dùng, không chỉ opens. Lo ngại giảm khi người dùng chủ động quay lại vì lợi ích quan sát được mà prompt họ đã nhớ không thay được. Không yêu cầu mọi ngày mở app.
- **Câu hỏi bắt buộc Strategy:** giả thuyết cụ thể nào khiến người đã thuộc prompt vẫn cần sản phẩm ở tuần hai? Nếu câu trả lời là họ không cần nữa, hướng có thể là utility mua một lần hay tài liệu; anh còn lý do bảo vệ business mobile nào và bằng chứng gì còn thiếu?
- **Counterevidence:** nhu cầu lặp đủ đau có thể duy trì utility rất nhỏ; thiếu evidence retention không chứng minh retention thấp.

## RT4 — lợi ích nhỏ và phân khúc mới có thể không chịu được acquisition/support

- **Concern / HYPOTHESIS:** target F1-N mới không còn là mọi freelancer; target F3-N có rubric và có pain đối chiếu cũng không phải mọi sinh viên. Kênh chung “productivity/student communities” có thể tiếp cận người thích timer nhưng không tiếp cận job mới. Giá trị tiết kiệm một thao tác nhỏ có thể khó giải thích và khó thu tiền hơn công sức hỗ trợ.
- **Evidence:** R1-strategy-01/-04/-05 và CLM-007/-012 ghi payment/channel/CAC UNKNOWN. Việc vendor niêm yết giá không bù khoảng trống này. Không có dữ liệu VN/SEA/international để chọn địa lý.
- **Impact:** perfect app, happy few users vẫn không tạo business nếu chi phí tìm/giải thích/hỗ trợ vượt tổng thu; không thể giải bằng thêm feature để justify giá khi chưa có value core.
- **Falsifier/giảm lo ngại:** cần một cohort cụ thể có thể tiếp cận hợp lệ, hành vi chi tiền gần nhất cho chính job và lựa chọn có đánh đổi thật khi nghiên cứu thương mại riêng được phép. Lo ngại giảm nhờ repeat tự nguyện + giao dịch thật + chi phí tiếp cận/phục vụ có dấu vết. Không đặt price/CAC target giả trong session này.
- **Câu hỏi bắt buộc Strategy:** hãy chọn **một** user/job hẹp để mô tả kênh giả thuyết có thể tìm đúng người; nếu chưa có access hoặc payment evidence, anh có giữ opportunity UNKNOWN và bỏ mọi hàm ý lợi thế thương mại VN/SEA không?
- **Counterevidence:** một utility nhỏ có thể bán bằng chi phí thấp; không có căn cứ kết luận acquisition đắt hay sinh viên không trả tiền.

## RT5 — đơn giản kỹ thuật chưa bảo đảm đơn giản sản phẩm và maintainability

- **Concern / INFERENCE, MEDIUM:** F1-N local text và F3-N tự đối chiếu nhẹ hơn blocker/social. Nhưng nếu muốn thắng substitution phải thêm import/context links/sync/content/scoring/notification đúng lúc, đội nhỏ có thể rơi vào cuộc đua compatibility, riêng tư, quyền nội dung và support. Khi bỏ chúng, lý do app riêng vẫn UNKNOWN. Đây là tension cần chấp nhận, không phải yêu cầu thêm feature.
- **Evidence:** TX0/TX1/TX3 giảm API concern cho baseline nhưng giữ team skills/interaction/outcome UNKNOWN. D3-F1/F3 đã bỏ phần lớn phần mở rộng. Không có device test. Không phát hiện legal barrier đã chứng minh; jurisdiction/age/data flow chưa chọn nên legal/data review **UNKNOWN**, không là clearance.
- **Impact:** scope dễ duy trì có thể quá ít value; scope cứu value có thể đổi sang opportunity khác. Nếu phải thêm engine chấm/học liệu để thắng, chưa còn là validation Fokus hiện tại.
- **Falsifier/giảm lo ngại:** lợi ích tăng thêm và voluntary repeat tồn tại trong baseline được giới hạn; lỗi cốt lõi không đòi quyền đọc mọi app/nội dung không có quyền/tutor engine. Khi cần phần mở rộng, đánh giá lại như hypothesis mới trước quyết định đầu tư.
- **Câu hỏi bắt buộc Inventor/Strategy:** nếu baseline không thắng note/worksheet, hai anh chấp nhận dừng app hay sẽ cứu bằng import/sync/AI? Nếu chọn phần mở rộng, phải ghi đây là cơ hội mới chưa được packet này chứng minh.
- **Counterevidence:** không có lý do gán chi phí infrastructure cao cho app local. Rủi ro chủ yếu hiện tại là incremental value và scope creep, không phải feasibility tuyệt đối.

## RT6 — hiệu quả học và giá trị app không phải hai gate cùng một thước đo

- **Concern / INFERENCE, MEDIUM:** F3-N có thể hữu ích về giảm thời gian tổ chức/giúp phát hiện lỗ hổng dù delayed score ngang practice mạnh. Ngược lại delayed learning hơn baseline không chứng minh app hơn same-prompt worksheet. Đòi cả learning tăng và app thắng bằng cùng score có thể loại một efficiency utility tốt; chỉ đo self-ticks có thể giữ app rỗng.
- **Evidence:** D3-F3 và CX3/R3 đã đúng khi tách oracle học khỏi self-tick. Chưa có hiệu quả thực nào; tôi challenge cách diễn giải, không thay oracle bằng engagement.
- **Impact:** false positive khi quy lợi ích practice cho delivery; false negative nếu learning tương đương nhưng tổng chi phí giảm đáng kể và người dùng coi trọng. Cả hai làm chọn sai hướng.
- **Falsifier/giảm lo ngại:** định trước lời hứa: learning cao hơn với chi phí tương đương, hoặc learning không kém với chi phí thấp hơn; hai giả thuyết khác nhau. Luôn giữ quality floor và đối chứng cùng prompt. Lo ngại giảm nếu outcome khách hàng chọn và oracle độc lập không mâu thuẫn.
- **Câu hỏi bắt buộc Inventor/Strategy:** các anh có chấp nhận một phiên bản chỉ tăng hiệu suất điều phối với learning không kém, hay bắt buộc claim learning tốt hơn? Nếu chấp nhận efficiency, hãy ghi sửa promise và không nói nghiên cứu trước đã xác minh nó.
- **Counterevidence:** đang giữ learning oracle mạnh là tốt; không nên hạ yêu cầu chỉ để cứu candidate khi kết quả không đẹp.

## Trả lời thẳng các câu hỏi quyết định

| Câu hỏi | Phán đoán hiện tại |
|---|---|
| Vì sao cài? | HYPOTHESIS: vừa thất bại dựng lại task phone-primary (F1-N), hoặc vừa học xong mà không xác định được lỗ hổng từ tập bài có rubric (F3-N). Chưa có bằng chứng trigger dẫn tới install hay đổi công cụ. |
| Vì sao quay lại sau tuần 1? | Chỉ nếu cùng job lặp và app giữ lợi ích ròng hơn prompt đã học/current tool. UNKNOWN; “nhắc/streak cho quay lại” không giải thích value. |
| Vì sao không native timer/Screen Time/Digital Wellbeing/Forest? | Các công cụ điều phối thời gian/gián đoạn không mặc nhiên tái dựng context hoặc kiểm bài. F1-N/F3-N đổi outcome nên không bị bác chỉ bằng feature matching. Nhưng chúng cũng chưa chứng minh người dùng cần đổi; notes/reader/worksheet/flashcards là đối thủ gần hơn. Native capability cũ là evidence peer relay; không kiểm tra lại hôm nay. |
| Switching incentive mạnh nhất? | HYPOTHESIS: nhiều lần lỗi restart hoặc bỏ sót lỗ hổng có chi phí đủ lớn, được giảm ròng mà current tool không xử lý. “UI sạch hơn”, “khác timer”, không đủ. |
| Giả định yếu nhất? | Một surface mobile riêng có giá trị bền hơn cùng prompt tại nơi công việc/học đã tồn tại. Nó hiện UNKNOWN và cả hai shortlist cùng phụ thuộc. |
| Tính năng hấp dẫn nhưng ít value? | Album ảnh bằng chứng, streak/phút, biểu đồ “đã tiếp tục”, AI recap không chứng minh tăng outcome; đây là nguy cơ giả thuyết, chưa có data feature usage. R3 bỏ camera/streak là điểm mạnh, không đề nghị đưa lại. |
| Maintainable small-team? | Baseline hẹp có lợi thế tương đối (TX0/1/3); không có ước lượng chi phí hoặc device evidence. Chấp nhận dừng nếu value chỉ xuất hiện sau một hệ nội dung/integration khác. |
| Thất bại dù app hoàn hảo? | Job quá hiếm; current tool gần context hơn; người dùng học prompt rồi bỏ app; đúng job nhưng không trả/không tiếp cận được bằng chi phí hợp lý; perfect implementation không giải được các trường hợp này. |
| Khi nào bỏ Fokus hoàn toàn? | Nếu cả F1-N và F3-N không có lợi ích tăng thêm trước same-prompt/current-tool, hoặc có value practice nhưng người dùng không cần delivery riêng; nếu không có cohort có pain lặp và đường kinh tế đáng kiểm tra; hoặc chỉ cứu được bằng đổi sang tutor/content/integration opportunity khác. Đây là điều kiện advisory chưa xảy ra, không Founder REJECT. Có thể giữ worksheet/template như kết quả hữu ích và dừng thương hiệu/app Fokus. |

## Nguồn mới và search receipt

Ngày truy cập **2026-11-21**. Ngôn ngữ English; tìm capability quốc tế, không claim đại diện VN/SEA. **3 search queries**, **4 URL open attempts**, **2 trang đọc thành công**, **2 thất bại**, không reopen, không app install/test. Dừng đúng budget; không search thêm cho broad timer. Search snippets chỉ là leads, không VERIFIED. Không kiểm tra full market, không kết luận uniqueness.

| ID | Nguồn / exact URL / publication | Quan sát hẹp và giới hạn |
|---|---|---|
| RT-S1 | Anki Docs, Studying: https://docs.ankiweb.net/studying.html → redirect https://docs.ankiweb.net/manual/studying ; publication date **UNKNOWN**; accessed 2026-11-21, lines31–41 | Official documentation; sequence question→reveal→compare→rating/next review. Không field study, không proof F3-N equivalence, không proof learning/WTP. |
| RT-S2 | RemNote Help Center, Preparing for an Exam, Soren Bjornstad: https://help.remnote.com/en/articles/9101991-preparing-for-an-exam ; date shown **2026-08-21**; accessed 2026-11-21, lines40–68,81–98 | Official vendor help; exam-linked study and optional mastery criterion. Không xác minh performance/mastery claim, actual use, sales hoặc payment Fokus. |
| RT-X1 | https://support.apple.com/en-ca/guide/iphone/iphc1af7c57/ios ; publication UNKNOWN | Open failed429. Search lead về reading place/bookmark không nâng VERIFIED. |
| RT-X2 | https://support.apple.com/guide/iphone/annotate-books-iphb60ffb8c/ios ; publication UNKNOWN | Direct URL probe failed/inaccessible. Không evidence note/bookmark capability; không source ID VERIFIED. |

Exact queries: `site.support.apple.com guide books bookmark notes reading iPhone resume reading`; `site.docs.ankiweb.net studying answer buttons Again Hard Good Easy show answer`; `site.help.remnote.com exam scheduler confidence practice feedback flashcards`. Search surfaced irrelevant third-party/news results; không sử dụng chúng cho facts.

## Trạng thái tranh luận

Initial assessment: không có candidate đã chứng minh mobile increment; learning value LOW/UNKNOWN, commercial value UNKNOWN. Sau targeted scan: lo duplication **tăng cho recall subset F3-N**; không suy toàn bộ F3 là bản sao. Lo API/ops giảm theo R3 scope; lo app necessity không giảm. Không có fatal barrier chứng minh, không có điểm số hay winner.

RT1–RT2 và RT5–RT6 cần Inventor trả lời thật; RT3–RT4 và RT5–RT6 cần Strategy trả lời thật. Tài liệu này mới là objection packet, **chưa có rebuttal hoặc consensus**. CIO có thể relay theo finding IDs. Sẽ append assessment change sau khi nhận actual responses; không tự viết phản hồi thay peer.
