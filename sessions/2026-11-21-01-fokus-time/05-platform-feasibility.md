# 05 — Technical & Platform Feasibility

SES-20261121-01 · 21/11/2026 · [Technical R1: nguồn sơ cấp, T1–T10 và giới hạn](records/technical-r1.md). Đây là tư vấn khả thi, không phải thiết kế kiến trúc hoặc bằng chứng app đã hoạt động. Chưa cài app, thử thiết bị, xin entitlement hay nộp store.

| Khả năng | Phân loại | Căn cứ và điều kiện làm thay đổi lựa chọn |
|---|---|---|
| Ý định, trạng thái phiên, ghi kết quả/lịch sử cục bộ | **Feasible on both, INFERENCE/MEDIUM** | T1: vòng tự nhập không cần quan sát app khác; độ nhanh/UX chưa kiểm |
| Timer hiển thị đúng khi mở lại | **Feasible on both, INFERENCE** | T5: thời lượng phải dựa trạng thái/thời điểm đã lưu; không dựa giả định app chạy nền liên tục. Kill/reboot/đổi giờ còn cần kiểm |
| Báo kết thúc đúng giây, mọi trạng thái | **Conditional; absolute promise unrealistic** | T6/T7: quyền, Doze, Focus/notification settings và reboot có thể ảnh hưởng. Lưu thời lượng đúng không bảo đảm người dùng nhận báo |
| iOS shielding tự quản lý | **Platform-specific/conditional** | T2: [individual authorization](https://developer.apple.com/videos/play/wwdc2022/110336/) có hỗ trợ; [entitlement phân phối](https://developer.apple.com/documentation/bundleresources/entitlements/com.apple.developer.family-controls) riêng. Người dùng có thể thu hồi; quyền tài khoản Fokus UNKNOWN |
| Android đo usage | **Conditional observation, not verified blocking** | T3: [UsageStatsManager](https://developer.android.com/reference/android/app/usage/UsageStatsManager) không chứng minh quyền ép khóa |
| Android blocking dùng Accessibility | **Conditional/unverified for Fokus** | T4: [Play policy](https://support.google.com/googleplay/android-developer/answer/10964491?hl=en) yêu cầu khai báo/consent/approval theo use case; không kết luận mọi blocker bị cấm hoặc chắc được duyệt |
| Không thể vượt qua, chống gỡ app, parity mọi máy | **Not realistic for self-managed MVP** | T8: revocation và quyền người dùng là ranh giới thật. Không xây lời hứa dựa trên né ranh giới đó |
| Camera/voice/widget/shortcut tích hợp | **Unverified conveniences here** | Không là điều kiện sống còn của vòng tự nhập; permission/latency/accessibility riêng chưa kiểm |
| Tự biết người dùng đang học tốt/làm việc thật | **Unsupported** | Usage/minutes/upload không chứng minh output hay học; không dùng AI để giả một oracle chưa có |
| Đồng bộ/nhóm/nhắc khẩn đáng tin cậy | **Additional dependency, unverified SLA** | Không cần cho ba workflow cá nhân nhỏ; F2 không được dựa push làm kênh khẩn duy nhất |

## Những ranh giới mobile cần giữ

**Offline:** Có thể đề xuất hoàn tất vòng ghi tay/xem lại ngay cả khi không mạng; đây là feasibility inference, chưa là kiểm tra. Không hứa backup/sync. Mất máy/xóa app có thể mất lịch sử; cần nói rõ nếu sau này phát triển.

**Background và pin:** Không cần chạy countdown hoặc theo dõi usage liên tục để tạo vòng giá trị cá nhân. Đây là cách giảm dependency, chưa có số đo pin. [Alarm docs](https://developer.android.com/develop/background-work/services/alarms), [Doze](https://developer.android.com/training/monitoring-device-state/doze-standby) và [notification permission](https://developer.android.com/develop/ui/compose/notifications/notification-permission) cho thấy cần kiểm trạng thái máy/quyền riêng. Nguồn local notification Apple đã đọc là archive2018: không đủ xác nhận toàn bộ hành vi iOS hiện hành.

**Quyền riêng tư và bảo mật:** Tên task có thể chứa thông tin khách hàng; ảnh bài tập có thể chứa tên/trường/người khác. Phạm vi nhỏ nên chỉ giữ dữ liệu cần cho một vòng, cho sửa/xóa và không mặc định đưa nội dung lên cloud/AI hoặc màn khóa. Baseline text-only tự chọn giúp giảm nhu cầu camera/mic. Đây là khuyến nghị giới hạn dữ liệu, chưa phải audit bảo mật hoặc xác nhận tuân thủ pháp luật.

**Accessibility:** Cần dùng được bằng VoiceOver/TalkBack, chữ lớn, giảm chuyển động, trạng thái không chỉ dựa màu và lối thoát dễ hiểu; chưa có UI để kiểm. Quyền Accessibility dùng để block khác chất lượng trợ năng của giao diện.

**Thiết bị:** OS minimum, OEM battery management, work profiles và độ phủ thiết bị đúng cohort VN/SEA đều UNKNOWN. Không lấy một thiết bị thành công làm parity. Những giới hạn này đặc biệt quan trọng nếu giá trị phụ thuộc báo thức hoặc blocking.

**Stores và dữ liệu theo vùng:** Chưa kiểm approval của use case cụ thể, entitlement của tài khoản hay yêu cầu riêng từng thị trường/trẻ vị thành niên. Không tuyên bố legal clearance. Giá/phí tài khoản store chưa kiểm trong phiên; không điền số quen thuộc từ trí nhớ.

## Khối lượng tương đối và vận hành

| Phạm vi tư vấn | Mức tương đối, không phải báo giá | Chi phí duy trì chính |
|---|---|---|
| Một vòng cá nhân text-only, offline, không account | LOW–MEDIUM | Hai OS, phục hồi trạng thái, dữ liệu cục bộ, trợ năng, support; đội có kỹ năng gì còn UNKNOWN |
| Camera/voice/widget/sync tùy chọn | MEDIUM, tùy lựa chọn | Quyền và lỗi nhập, storage/privacy, matrix thiết bị và thay đổi OS |
| Blocker parity hoặc social realtime | HIGH/conditional | Hai hệ quyền, review/entitlement, reliability, support, multi-user và an toàn cộng đồng |
| AI chấm học, học liệu, mạng xã hội công khai | Ngoài MVP của các brief | Nội dung/quyền dữ liệu/đánh giá chất lượng và vận hành chưa có căn cứ nhỏ gọn |

Local-only không cần API tính tiền theo phút tập trung; vẫn có công bảo trì, store/account, thiết bị kiểm thử và hỗ trợ. Không có cơ sở ước tính số tuần hay tổng tiền khi chưa biết năng lực đội và phạm vi chất lượng. Đơn vị học nên theo dõi: thiết bị × OS × trạng thái quyền, công xử lý ticket/100 người dùng và giờ phục hồi sau thay đổi OS; không coi đây là chi phí đã đo.

## Những kiểm tra chưa chạy

Device/background/kill/reboot/clock-change/offline/battery, entitlement/account access, store submission, pin, assistive technology và security/privacy review đều **NOT RUN**. Khi Founder muốn thử kỹ thuật, cần phạm vi riêng; phiên này chỉ đọc nguồn công khai. [Technical R2](records/technical-r2.md) ghi các phản biện cụ thể gửi Strategist và không thay thế kiểm thử.
