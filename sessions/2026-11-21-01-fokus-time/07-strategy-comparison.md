# 07 — Product Strategy Comparison

SES-20261121-01 · 21/11/2026. Áp dụng đủ chín tiêu chí [rubric](../../protocols/scoring-rubric.md). Hai cột là F1-N/F3-N sau peer revision; đây là làn khám phá, không mặc định sản phẩm khả thi thương mại. Điểm phản ánh phán đoán có lý do, không probability hoặc customer evidence. Không chuẩn hóa số thẻ và số buổi của hai job thành cùng một outcome.

Sau actual Red Team/rebuttal/final review, Inventor đã rút endorsement của cả hai app. Scorecard được giữ để đánh giá **hai phương án giả thuyết**, không phục hồi shortlist thương mại. F1-N = IDEA-0013; F3-N = IDEA-0014.

## Scorecard với missingness

| Tiêu chí | Trọng số | F1-N | F3-N | Rationale, evidence class và confidence | Opposing view / plausible interval |
|---|---:|---|---|---|---|
| Customer problem severity | 20% | UNKNOWN | UNKNOWN | CLM002/003 gần pain; không đo độ đau của phone-primary planned pause hoặc uncertainty-with-rubric. LOW cho target | Customer phản đối chuyển evidence lân cận sang segment mới; F3 có tín hiệu gần hơn nhưng chưa đủ score |
| Evidence of demand | 15% | UNKNOWN | UNKNOWN | CLM007, không có đổi công cụ/commitment/transaction target | Lời kể pain hoặc giá vendor không tạo demand score; chưa có khoảng số defensible |
| Meaningful differentiation | 15% | UNKNOWN | UNKNOWN | CLM015/016; khác mô tả cơ chế chưa chứng minh customer advantage trước same-prompt/current-tool | Market/Red Team: notes, worksheet, Anki/RemNote có thể đủ; chưa chứng minh full equivalence nên không chấm thấp như fact |
| Distribution feasibility | 15% | UNKNOWN | UNKNOWN | R2-strategy-03/RT4; chưa có cohort access/CAC/conversion; LOW | Student/community existence không là kênh được sở hữu; không score mặc định5 |
| Small-team technical feasibility | 10% | 7 | 7 | INFERENCE/MEDIUM: T1/T10, TX1/TX3; local text workflow không cần blocker/cloud/scoring; chưa test thiết bị | Technical chỉ đánh giá phạm vi, kỹ năng đội UNKNOWN; interval5–8 nếu phạm vi/năng lực thay đổi |
| Monetization potential | 10% | UNKNOWN | UNKNOWN | CLM007/012, RT3/4; one-time/seasonal subscription đều HYPOTHESIS | User có thể học prompt rồi rời app; chưa có evidence là không ai trả, cũng chưa có bằng chứng mua |
| Legal and data feasibility | 5% | UNKNOWN | UNKNOWN | CLM014: chưa chọn data/age/jurisdiction; no clearance | Local text giảm phạm vi tương đối, không xác nhận tuân thủ hay quyền nội dung |
| Long-term defensibility | 5% | UNKNOWN | UNKNOWN | R1-strategy-04: dễ hình dung copy nhưng lợi thế durable/retention chưa được kiểm | Không có moat xác lập; thiếu evidence không tự là điểm0/1, không giả lợi thế dữ liệu |
| Fit for lean MVP | 5% | 7 | 7 | INFERENCE/MEDIUM: [scope](08-top-proposals.md), TX1/TX3: một vòng nhỏ đủ đặt câu hỏi, không đủ chứng minh sản phẩm riêng | RT5: nếu value chỉ tới khi thêm integrations/tutor thì scope nhỏ không giải job; interval5–8 |
| **Tổng** | **100%** | **NOT RANKED** | **NOT RANKED** | Chỉ **15% trọng số có số**; **15% evidence coverage theo traceable INFERENCE**, chưa có kiểm chứng outcome target | **85% trọng số UNKNOWN**, không renormalize, không xếp theo partial total |

Coverage trên nói nguồn hỗ trợ phán đoán feasibility/MVP ở phạm vi đã giới hạn, không phải15% thị trường được xác nhận hoặc15% xác suất thành công. Không có direct target outcome/transaction evidence cho F1-N/F3-N. Không đưa tổng giả định vì nó sẽ chủ yếu phản ánh cách điền85% còn thiếu.

**Ranking sensitivity:** Không có thứ tự thương mại để kiểm độ bền. Một kết quả same-prompt note/worksheet đạt ngang với ít công hơn có thể loại standalone app dù technical/MVP score cao. Ngược lại hành vi tự chuyển công cụ, có lợi ích ròng và giao dịch lặp có thể thay đổi các tiêu chí demand/difference/distribution. Pháp lý/quyền dữ liệu sống còn không được bù bằng điểm tổng. Bảng này không là approval.

## Mobile-specific assessment bổ sung, không cộng vào điểm gốc

| Trục | F1-N | F3-N |
|---|---|---|
| Mobile-first value | Chỉ có lý do cùng nơi làm việc; surface riêng còn UNKNOWN. Chuyển app trên cùng phone vẫn có cost | Có thể hợp người vốn dùng câu hỏi trên phone; worksheet/flashcards có thể gần job hơn; UNKNOWN |
| UX simplicity | Một active handoff giảm scope; capture/retrieve ròng chưa đo | Commitment–attempt–compare–gap rõ về mô tả; đặt tiêu chí/tự chấm có thể nặng |
| Retention potential | Lặp theo job, có thể học prompt rồi không cần app; UNKNOWN | Lặp/mùa vụ và chuyển practice sang công cụ cũ; UNKNOWN |
| Platform feasibility | Bản text local INFERENCE khả thi hai OS; không cần entitlement | Bản text local INFERENCE khả thi hai OS; không cần camera/scoring |
| Privacy/permission burden | Thấp tương đối nếu local/no-sensitive-permission; text task vẫn có thể nhạy cảm | Thấp tương đối nếu không ảnh/cloud; nội dung học/quyền rubric còn ràng buộc |
| Dependency risk | Host task/note location, navigation và user remembering capture; không có API link đã kiểm | Chất lượng bài/rubric, độ khó, independent oracle nghiên cứu; không tự biến thành tutor |

## Research priority tách khỏi commercial viability

| Revision | Commercial eligibility | Priority / confidence | Câu hỏi đổi quyết định | Evidence/effort/access đề xuất | Dừng khi |
|---|---|---|---|---|---|
| F1-N | Không đủ; NOT RANKED | **Conditional MEDIUM** cho việc làm rõ pain; access UNKNOWN. CIO judgment, không Founder EXPLORE | Có lỗi restart cụ thể lặp mà cùng prompt ngay tại draft không giải không? | Quan sát buổi gần nhất/diary của người phone-primary; quy mô/effort xem [brief](08-top-proposals.md); chưa tuyển cohort | Không có pain/cơ hội lặp, hoặc note tại task đủ; không dựng app để đi tìm pain |
| F3-N | Không đủ; NOT RANKED | **Conditional MEDIUM** cho gap so current study tool; oracle/access UNKNOWN. Không xếp cao hơn F1-N | Khi đã có worksheet/Anki/RemNote, còn lỗi nào đáng trả cho một vòng mới? | Một dạng bài/rubric hợp lệ; quan sát cách ôn thực tế, sau đó mới cân nhắc đối chứng; người chấm chưa có | Current-tool đủ; hoặc chỉ tạo/chấm nội dung mới có ích; không chuyển cơ hội để cứu thương hiệu |

Không hướng nào HIGH mặc định. Customer và Strategist đã phản biện việc ưu tiên F1 vì dễ falsify; Strategist rút ưu tiên mặc định. Inventor vẫn coi phép đo F1 có cấu trúc dễ bác bỏ **nếu** đã có cohort. Đây là bất đồng về trật tự học có điều kiện, không hai bảng xếp hạng thương mại. F3 gần pain người học hơn nhưng Red Team làm tăng duplication concern trong recall subset.

RT6 bổ sung hai outcome hợp lệ cần chọn trước: học tốt hơn với công sức tương đương, hoặc học không kém với tổng công sức thấp hơn. Không đổi thước đo sau khi xem kết quả; một test nhỏ “không khác biệt có ý nghĩa” không xác nhận non-inferiority. Không có outcome study nào đã chạy trong phiên.

Kết luận Red Team và reply thực nằm ở [assessment](06-red-team-assessment.md); trạng thái cuối và recommendation của CIO xem [Founder brief](09-founder-brief.md).
