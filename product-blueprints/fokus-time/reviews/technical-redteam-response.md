# Technical actual response — PD-X5 / RTD1–RTD2

22/11/2026 · SES-20261121-01 / IDEA-0014 · actual respondent `/root/ft_define_technical_sol`, requested `gpt-6.1-sol`. Đã đọc [Red Team initial](redteam-initial.md), [actual CIO response](redteam-cio-response.md), và đối chiếu với TP2/TP3 cùng TXD2/TXD3 của tôi. Không chỉnh normative files, không web/agent/code/Dev Studio. Tất cả correction là **PROPOSED**; đây là review logic tài liệu, mọi device/app/failure/backup/privacy test vẫn **NOT RUN**.

## TRD1 — RTD1: đồng ý sửa reference, không mở authority mới

**Concede:** primary segment proposal phải trỏ DEC004; documentation authority dùng DEC002 trong product namespace. Global DEC0001 giữ nguyên. Đây là correction tổng hợp của CIO; tôi không là proponent lỗi reference. AC: một ID trong normative package không mang hai meaning/status; không nâng segment proposal thành approved. Final reviewer cần xác nhận revision thật, không lấy ý định sửa làm kết quả đã sửa.

## TRD2 — RTD2: accept form chưa lưu, rút cách nói New luôn tạo slot

Lập luận Red Team đúng: TP2/TP3 trước đây bảo vệ một record và whole-save nhưng chưa xác định New có là thao tác lưu hay không. Tôi **concede missing boundary** và accept default CIO: New chỉ mở một transient preparation form khi dataset chưa có open record; đây là interaction state, không phải phase dữ liệu thứ năm. First Save tạo một DRAFT hoàn chỉnh theo nghĩa lưu nguyên vẹn, dù nội dung chưa đủ Start. First Start trực tiếp tạo một LEARNING record với frozen commitment và toàn bộ validation cần thiết; không đòi Save riêng.

**Before → after:** “slot gồm draft” nay chỉ gồm **persisted DRAFT**; một form chưa từng được lưu không chiếm persisted slot. Tuy nhiên form đang mở phải được bảo vệ khỏi thay thế/nhân đôi trên UI. Đây không phá invariant TP2, mà xác định khi nào invariant record bắt đầu áp dụng.

**AC-TRD2:** New → chưa gõ → Back → Home, dataset không đổi; New → gõ → Discard khi chưa có save pending/committed → không có record/slot, nội dung bị bỏ; mở lại app không tạo ghost draft. Repeated New trước khi form bị bỏ quay lại cùng form và giữ edits, không reset/nhân đôi. Sau Discard thành công, lần New tiếp theo là form trống mới, không hồi sinh phần đã bỏ. Process chết trước bất kỳ commit nào có thể mất form; UI không hứa phục hồi phần gõ chưa lưu.

## TRD3 — còn một contradiction cần chỉnh: “trước acknowledgment” không đồng nghĩa “chưa lưu”

**Phản biện chính tới CIO response:** câu “Discard before first acknowledgment leaves dataset unchanged/no ghost slot” quá rộng khi đặt cạnh “lost acknowledgment can recover ... full new record”. Có thể first Save đã commit nhưng acknowledgment mất/chưa tới UI. Tại thời điểm ấy vẫn chưa có acknowledgment, nhưng persisted record thật đã tồn tại. Nếu Discard luôn ép về no-record thì nó đang xóa một record đã lưu mà không có delete confirmation; nếu giữ record thì lại trái câu Discard tuyệt đối.

**Correction nhỏ nhất:** tách ba tình huống ở cấp hành vi, không đòi phase/kiến trúc mới:

- Chưa yêu cầu lưu, hoặc đã biết chắc first save không commit: Discard transient edits không tạo/xóa record.
- Save/Start đang xử lý hoặc chưa biết kết quả: không tuyên bố no-record, không cho New/retry/Discard hành xử như chắc save thất bại. Thao tác tiếp theo phải dựa kết quả được xác định lại từ dữ liệu thực; có thể cho người dùng rời nhưng phải nói trạng thái lưu chưa xác nhận, không gọi là đã bỏ record.
- Save/Start thực sự commit dù ack mất: khi xác định lại, hiển thị đúng một saved DRAFT hoặc LEARNING. “Discard edits” sau đó chỉ bỏ phần sửa chưa lưu; muốn xóa saved record dùng hành động xóa đã xác nhận. Retry cùng thao tác không tạo record thứ hai.

**AC-TRD3:** Save-first commit + UI chưa nhận ack → người dùng Back/Discard/Retry hoặc process chết → reopen thấy đúng một DRAFT, không bị tự xóa và không duplicate. Start-first commit + ack mất → reopen đúng một LEARNING, commitment freeze giữ; không trở transient form và không Start lần hai. First-save thật sự không commit → dataset giữ no-record, input còn khi process sống để retry. Không có nhánh half-record hoặc success giả. Nếu đóng app trong kết quả chưa rõ, “edits since last acknowledged save may be lost” là giới hạn bảo đảm tối thiểu, **không phải lời hứa mọi thay đổi chưa acknowledged chắc chắn bị loại bỏ**.

Cách viết chuẩn đề nghị: **“Discard trước lần lưu đầu chỉ giữ dataset không đổi khi chưa có save đang chờ/chưa rõ kết quả và chưa có commit. Khi lưu chưa xác nhận, app phải xác định lại bản đã lưu trước khi áp dụng hành động tiếp theo; không tự xóa dữ liệu đã commit.”** Underlying mechanism dành cho Dev Studio sau authorization riêng.

## TRD4 — existing draft và mọi entry point phải dùng cùng guard

**Accept:** đã Save DRAFT rồi sửa thêm → Discard bỏ edits mới hơn, giữ bản đã lưu và slot. Không dùng cùng chữ “Bỏ nháp” để vừa discard edits vừa delete persisted draft. First Save cho incomplete contents không kích terminal validation; first Start cần đủ điều kiện.

**Guard bổ sung:** transient form không chiếm persisted slot vẫn không được silently replaced bởi New/history/past-gap. Nếu form có edits và user chọn past-gap/create-from-history, phải cho giữ form hoặc chủ động bỏ trước khi hành động mới lưu draft. Nếu họ chọn Save form hiện có thì saved draft mới đó chiếm slot; không được tiếp tục tạo draft past-gap thứ hai. Đây là hệ quả trực tiếp một-slot, không cần queue/version engine.

**AC-TRD4:** saved DRAFT A + edits B → Discard → reopen A; Delete draft A là hành động khác có confirm. Transient có text A + chọn past gap B → cancel giữ A; confirm bỏ A rồi tạo một saved draft B theo action đã mô tả; save A thay vì bỏ thì trở A và slot bị chiếm, không tự tạo B. Không có pending mutation chưa xác nhận được bypass bằng entry point khác (TRD3).

## TRD5 — privacy phải nằm trước mọi action thật sự ghi, không chỉ nút Save

Accept CIO đưa thông tin local/OS backup trước first Save hoặc Start. Chỉ mở form New không tạo saved-data acknowledgment; không cần giả quyền hệ thống hay pop-up consent ngoài scope. Thông tin phải nhận biết/đọc được, không sau khi dữ liệu đã ghi.

**AC-TRD5:** first Start không đi qua Save vẫn thấy thông tin trước action; first incomplete Save cũng vậy. Các action rõ ràng tạo **saved** draft từ past gap/history phải có copy trước xác nhận cho biết sẽ lưu draft, tuân disclosure policy hiện có; không âm thầm lưu nội dung bằng một navigation vô hại. OS restore theo cơ chế OS không được mô tả như app vừa xin consent hoặc bảo đảm đã hiển thị disclosure trước khi OS restore; thông tin trong app phải đúng về giới hạn này.

Không thay backup policy: allowed theo OS/user, current-dataset deletion, no latest/restore/global-erasure guarantee. Đọc tài liệu OS trước đây không chứng minh privacy copy/cấu hình thực đã khớp.

## TRD6 — goal-new saved draft khác New form là hợp lý nếu action nói rõ

**Đáp RTD2/CIO và TP2/TP3/TXD2:** New form chỉ là mở soạn; “Đổi đích và tạo nháp mới” là explicit whole mutation của một record đã Start. Có thể cùng tồn tại hai contract đó vì trigger/label/hậu quả khác nhau. Không cần mọi draft entry point đều phải transient, nhưng phải nói rõ cái nào đã lưu.

**AC-TRD6:** đổi đích confirmed → old CLOSED-UNASSESSED đúng reason + một saved successor DRAFT; successor không carry attempt/comparison/outcome, chưa Start; hủy trước commit giữ exact prior state/input; failure/lost ack phục hồi toàn bộ trước hoặc toàn bộ sau và retry không duplicate. Back/Discard khi vừa vào successor, chưa sửa gì, chỉ rời màn hình và **giữ saved successor**; muốn bỏ nó phải Delete confirmed. Không gọi Discard là hủy whole goal change sau commit. Privacy/whole-save acknowledgment phải bao cả old và successor, không chỉ việc old đóng.

Optional past-gap tạo saved draft tương tự phải hiển thị là action tạo/lưu, không tự Start và không thay kết luận cũ. Nếu pending result chưa rõ, dùng TRD3; không tự tạo thêm saved draft để chữa mất acknowledgment.

## Kết luận actual response

Ủng hộ correction RTD1 và RTD2, có một **remaining contradiction TRD3** cần đổi wording trước final freeze; các guard TRD4–6 làm acceptance đủ phân biệt hành vi. Không thêm feature hoặc persisted state. Cần CIO sửa normative documents/AC theo hợp đồng rõ rồi independent Red Team kiểm revision thực. Phản hồi này không phải final reviewer verdict, không phải Founder approval hay implementation verification.
