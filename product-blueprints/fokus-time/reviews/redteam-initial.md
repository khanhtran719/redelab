# Red Team — initial independent specification audit

22/11/2026 · SES-20261121-01 · IDEA0014 · frozen product blueprint **v0.1**. Reviewer thực `/root/ft_define_redteam_sol`, custom remit `red-team-critic`, runtime task requested **gpt-6.1-sol**. Đây là audit tài liệu trong phạm vi Founder đã cho phép, không mở lại selected direction, không chạy DISCOVER/market scan, không đề xuất phát triển. Chỉ reviewer này ghi file này; không sửa normative/shared files và không delegation.

## Kết luận ban đầu

**PARTIAL — hai correction tài liệu cụ thể cần phản hồi; không thấy critical blocker đã được chứng minh trong baseline nghiệp vụ.** Có thể hoàn tất sau một vòng correction và actual proponent response, không cần mở rộng sản phẩm. Chưa ghi READY FOR FOUNDER REVIEW vì mã quyết định chưa nhất quán và cạnh tạo nháp đầu tiên cần chốt trạng thái đã lưu. Đây là mức hoàn thiện specification, không nói sản phẩm đã được kiểm thử hoặc Founder đã duyệt chi tiết.

**VERIFIED, phạm vi tài liệu:** đọc README và 01–10, PD-X4, frozen-draft-v0.1.json và các peer reply liên quan. Đối chiếu nội dung và SHA256 của cả11 normative Markdown files với frozen JSON đều **MATCH** tại lúc audit. Điều này xác nhận đúng revision, không xác nhận phần mềm. Không sửa file normative, không web/source refresh, không chạy sản phẩm/device/usability/learning/security/restore test. Các AC ứng dụng đều **NOT RUN**.

**INFERENCE:** các default independent-only, withdrawal-only, one open record và OS-backup-policy A cùng tồn tại được, với các giới hạn hiện đã công bố. Không có cơ sở ép kết luận BLOCKED chỉ vì Inventor thích alternative hoặc nhu cầu/value chưa có evidence mới. Ngược lại, không có cơ sở nâng logic coherence thành learner comprehension, learning progress, hiệu quả hơn worksheet/Anki/RemNote hoặc willingness-to-pay; các điểm đó **UNKNOWN** ở review này.

## RTD1 — Mã DEC-002 trỏ tới hai quyết định khác nghĩa

- **Severity:** P2, nonblocking correction về authority/traceability; không phải bằng chứng có hành động vượt quyền đã xảy ra.
- **Refs:** 01-product-vision.md, `PROPOSED — DEC-002` ở Product promise; 09-decisions-and-open-questions.md, Decision register `DEC-002 APPROVED`, `DEC-004 PROPOSED`; 10-dev-studio-handoff.md, Authoritative reading order và authority. Global portfolio DEC-0001 không phải lỗi này.
- **Proponent/claim:** bản tổng hợp normative của CIO; không gán cho chuyên gia khác. 01 dùng DEC-002 cho primary segment university student; 09 dùng DEC-002 cho documentation-only authorization, còn primary segment là DEC-004.
- **Scenario/causal impact:** reviewer hoặc PCR dẫn “DEC-002” để nói target student đã/chưa được duyệt. Tùy file họ có thể đọc ra status PROPOSED hoặc APPROVED và một nội dung khác. Handoff yêu cầu IDs ổn định và không tự chọn precedence để chữa contradiction; duplicate semantic ID làm approval evidence mất đơn nghĩa.
- **Evidence/class:** **VERIFIED** hai locator có nội dung khác; hậu quả handoff là **INFERENCE**, chưa có downstream mistake thực tế.
- **Correction tối thiểu:** đổi citation trong01 sang `PROPOSED — DEC-004` cho primary segment, giữ09 là register; kiểm cùng ID không có nghĩa thứ ba. Không tự nâng target segment thành APPROVED và không sửa portfolio human decision.
- **Observable acceptance/falsifier:** tìm DEC-002 trong normative package chỉ được documentation-only authority; DEC-004 luôn primary segment proposal. Nếu có một register có chủ ý định nghĩa namespace riêng cho01 thì concern giảm, nhưng frozen v0.1 không khai namespace như vậy. Không cần thêm namespace hoặc decision mới để sửa lỗi một nhãn.
- **State:** OPEN, chưa có actual CIO/proponent response lúc chốt initial notes.

## RTD2 — Chưa khóa thời điểm New tạo record đã lưu và hậu quả Discard trước lần lưu đầu

- **Severity:** P2, nonblocking product-state ambiguity cần chốt trước khi coi specification complete; không yêu cầu kiến trúc/schema/idempotency mechanism.
- **Refs:** FR001 primary/inputs, FR006 acknowledgment; BR001 one-open including draft; BR004 diagram `[*] → DRAFT: create/save draft`; BR008 explicit durable save boundaries; UX001, UX-S01/S02; AC001/004/022. NFR006 first-save disclosure phụ thuộc ranh giới này.
- **Proponent/claim:** CIO normative synthesis; đây là cạnh còn thiếu của explicit-save/single-slot contract, không phải bác Technical whole-save concern hoặc Strategy four-phase simplification.
- **Scenario:** dataset không có open record. User chọn New, gõ một phần hoặc chưa gõ, rồi Back → Discard edits trước bất kỳ Save/Start acknowledged nào. Họ mở Home hoặc kill/reopen. Frozen draft chưa nói rõ New đã lưu một DRAFT rỗng hay chỉ mở form chưa lưu, nên hai sản phẩm đều có thể diễn giải các đoạn hiện có: (A) không record, slot free; (B) một empty DRAFT chiếm slot. Trường hợp B có thể làm user tưởng Discard bỏ nháp nhưng New lần tới lại route về ghost draft. Nếu New thực sự tự lưu thì first-save disclosure và trạng thái saved phải diễn ra ngay lúc đó; nếu chưa lưu thì không được báo saved hoặc giữ ghost record sau restart.
- **Evidence/class:** **VERIFIED** AC001 bắt đầu từ hành động Save; AC004 bắt đầu từ open record; AC022 bắt đầu từ acknowledged save. Không có scenario cho New→Back/Discard trước first save. **INFERENCE** có hai cách hiểu ranh giới record; không khẳng định đã có lỗi ứng dụng.
- **Correction tối thiểu được khuyến nghị:** New chỉ mở nội dung chuẩn bị chưa lưu khi chưa có record; không tự tạo persisted DRAFT. First successful Save draft hoặc Start tạo/ghi đúng một record với whole-save acknowledgment; Start vẫn một action vào LEARNING, không phải phải Save riêng. Back/Discard trước first acknowledgment không để record/slot mới; failed first Save giữ input trong process, không success. Cách này không thêm phase thứ năm: unsaved form là interaction state, không learning record đã lưu. Với DRAFT đã acknowledged thì Discard chỉ bỏ edits và giữ bản đã lưu. Nếu CIO chọn New tạo saved empty draft thay thế, phải nói rõ first-save notice, Home/Discard/restart và acceptance tương ứng; hai phương án không cùng normative.
- **Observable acceptance/falsifier:** thêm AC cho (1) New→Back khi chưa gõ; (2) New→type→Discard trước save; cả hai không tạo record/slot theo default khuyến nghị; (3) incomplete Save acknowledged→Back/Discard edits→reopen giữ đúng saved draft và slot; (4) first Save/Start thất bại/lost acknowledgment→reopen whole prior hoặc whole new state, không ghost/duplicate; disclosure có trước first actual saved data. Concern được giải nếu correction nêu deterministic behavior đủ để các oracle phân biệt A/B, không cần code/device proof ở bước này.
- **State:** OPEN, chưa có actual CIO/proponent response lúc chốt initial notes.

## Phản hồi thực tới lập luận chuyên gia đã nhận

**Strategy RSP2 / Customer CP-X1, so với Inventor IP3:** tôi chấp nhận lập luận rằng qualifier không biến assisted attempt thành evidence đạt đích tự làm. BR005 + AC013/014/020 đã cho baseline có nghĩa nhất quán: chỉ independent+sufficient comparison+reference mở assessed options; helped/uncertain vẫn lưu facts/gap, không ép fail/retry. Assistance timing đã tách việc xem answer sau attempt khỏi help để solve; đó là hướng dẫn tự khai, không anti-cheat certification. **Before → after:** trước đọc packet còn cần kiểm đây là gate làm mất useful assisted learning; sau đối chiếu unassessed/gap/wording, concern về mất toàn bộ value được giảm. Tôi không có evidence để nói alternative IP3 sai với mọi sản phẩm; preference của Inventor phải còn trong OPEN001.

**Market MP2-R:** phản đối “text reference + đã compare” chưa đủ xác nhận đủ cơ sở là đúng về logic. Frozen v0.1 đã cụ thể hóa NOT_CONFIRMED / DONE_INSUFFICIENT / DONE_SUFFICIENT và yêu cầu cuối cùng, nên scenario người học tự khai comparison không đủ không thể commit assessed verdict. **Before → after:** risk có thể hữu hình trong wording cũ được giải ở frozen v0.1; tôi không lặp lại nó như open issue. Chất lượng/trung thực của tự khai vẫn UNKNOWN, guard không chứng minh rubric thật sự đủ.

**Strategy RSP3 / Customer CP-X3, so với Inventor IP5:** withdrawal-only giải được invariant tối thiểu “đừng tiếp tục hiển thị kết luận mà user đã rút như hiện hành”; mọi surface và optional copied context đều cần qualifier. BR007/AC028–030 có eligibility/no-undo/failure/retry, nên tôi không yêu cầu replacement/undo engine để đủ vòng sản phẩm nhỏ. **Before → after:** original-immutable có thể khiến sai sót bị giữ như đúng nếu chỉ delete-only; withdrawal giải được phần đó. Cost no-undo và inability to edit wrong unassessed notes là trade-off đã nói, không được gọi là user preference đã kiểm chứng. Dissent OPEN008 cần giữ.

**Technical whole-save/backup concern đã relay ở packet:** acknowledgment, old-or-new action, stale retry, goal split và current-dataset delete có contract và AC riêng. BR010 nói rõ stale OS snapshot có thể hồi sinh deleted/withdrawn content và app có thể không nhận biết restore; vì vậy không thể đòi nó đồng thời giữ newest withdrawal trong một older snapshot không có dấu ấy. Tính nhất quán đó giảm concern về false latest-restore claim, không chứng minh OS transfer/restore hoạt động. Tôi giữ UNKNOWN cho device/corruption/storage-full/update/privacy inspection; không thêm cloud/export để giả chữa giới hạn.

## Các góc đã xét và giới hạn nhận định

| Góc audit | Kết quả trên frozen v0.1, chỉ ở mức specification |
|---|---|
| Thiếu comparison/source; comparison không đủ; assistance/uncertainty | Có unassessed path, sufficient-declaration gate rõ; không forced diagnosis |
| Gap chưa biết, thay gate sau chọn verdict | BR005/006 và AC013/014/018/021 có clear/reject/retained-notes; không thấy critical contradiction |
| Partial save vs Close; Back vs return-to-learning | BR004/008/009 phân biệt, cảnh báo saved+unsaved discard, cancel no-op |
| Goal change; immutable commitment; one open slot | Whole old-close/new-draft, retry không duplicate; còn cạnh first-New ở RTD2 |
| Failure/kill/lost acknowledgment/stale UI | Old/new coherent contract có AC023 across mutations; không giả có implementation proof |
| Corruption/reset/delete-one/delete-all | Read error khác empty, reset explicit destructive, scope rõ, no false success |
| History/withdrawal/restore | Không resume closed, original not-current khi withdrawal hiện hữu; OS snapshot limitation rõ |
| Input/Unicode/accessibility | Limits/type/boundary oracle, full VoiceOver/TalkBack/large-text contract có; execution NOT RUN |
| Scope/authority/handoff | Không architecture/code/deployment/Dev Studio activation, separate authorization được giữ; RTD1 sửa reference |
| OS support/performance/legal/value | OPEN explicit và không numerical targets/clearance bịa; không chặn việc Founder xem docs |

Không phát hiện fatal evidenced barrier trong review tĩnh này; không được suy từ đó rằng không còn unknown. Concern về friction/value tự báo cáo, trusted comparison và lợi ích hơn công cụ sẵn có còn là conditional risk, cần real observation nếu được phép nghiên cứu sau; không dùng nó để tự ý đổi Founder direction hoặc thêm sản phẩm.

## Bước tiếp theo trong scope

CIO/proponent trả lời RTD1 và RTD2 bằng concede/revise/rebut có locator, sửa normative docs nếu nhận và gửi revision/diff cùng response thực. Reviewer sẽ ghi final reassessment riêng, giữ nguyên initial record này. Trước response/final review, không ghi hai issue là FIXED và không gọi việc đã gửi là đã RESPONDED. Chưa có Founder approval, implementation authorization hay product test result phát sinh từ review này.
