# Báo cáo cá nhân — 2A202603739_DoanCongHai

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Đoàn Công Hải
- MSSV: 2A202603739
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: Nhóm E2
- Link repo nhóm: https://github.com/nvcuong96/K5-L3B-Day02-NhomE2-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Lặp lại | Khi chuẩn bị họp standup hàng ngày vào 9h sáng, tôi muốn tổng hợp nhanh các task đã hoàn thành hôm qua và việc sẽ làm hôm nay từ commit GitHub và Jira, để cập nhật trôi chảy với team mà không phải lục tìm lại từng tab | Lập trình viên, Scrum Master | Mất 10–15 phút mỗi sáng (5 ngày/tuần); tự bấm giờ trong 2 tuần liên tiếp |
| 2 | Lặp lại | Khi có thành viên mới gia nhập nhóm dự án, tôi muốn cung cấp trọn bộ tài liệu hướng dẫn cài đặt môi trường dev và cấp quyền tài khoản theo chuẩn, để họ tự setup được mà không phải hỏi từng bước qua chat | Thành viên mới, Tech Lead, Mentor | Mỗi tháng 1–2 đợt onboarding, mất 2–3 tiếng giải đáp lỗi lặp lại; lưu vết 15+ tin nhắn hỏi lỗi tương tự trên Slack/Discord |
| 3 | Tốn thời gian | Khi nhận một Pull Request (PR) phức tạp (>500 dòng code hoặc thay đổi trên 10 file), tôi muốn nắm nhanh bản đồ liên kết các thay đổi logic nghiệp vụ, để tập trung review đúng trọng tâm và phát hiện bug tiềm ẩn | Reviewer, người tạo PR, toàn team | Mất 45–60 phút/PR lớn, trung bình 3–4 PR/tuần; PR thường bị nghẽn tồn đọng 2–3 ngày chưa kịp merge |
| 4 | Tốn thời gian | Khi nhận tài liệu đặc tả kỹ thuật (API spec / PRD) mới từ đối tác, tôi muốn trích xuất ngay danh sách các endpoint thay đổi và các điểm breaking changes, để cập nhật code kịp tiến độ release | Backend Developer, Tester | Tốn 60–90 phút đọc tài liệu 15–20 trang; 1–2 lần/tháng; từng có 1 lần release trễ do sót ghi chú thay đổi ở trang 14 |
| 5 | Cần đọc, tổng hợp nhiều thông tin | Khi hệ thống gặp sự cố cảnh báo lỗi trên Staging/Production, tôi muốn đối soát nhanh giữa error trace (Sentry), log server và các commit vừa deploy gần nhất, để xác định đúng commit gây lỗi mà không phải mở 4 dashboard riêng rẽ | Dev on-call, DevOps | Mất 30–45 phút mỗi lần truy vết incident; tần suất 2 lần/tuần; có lịch sử cứu hỏa ghi nhận trong kênh alert |
| 6 | Cần đọc, tổng hợp nhiều thông tin | Khi chuẩn bị thi kết thúc môn hoặc kiểm tra đồ án lớn, tôi muốn tổng hợp các slide bài giảng, ghi chú thảo luận và rubric chấm điểm thành một bản checklist nội dung cốt lõi, để ôn tập trọng tâm mà không bị sót yêu cầu | Sinh viên trong nhóm lớp | Mất 3–4 tiếng trước mỗi đợt nộp/thi; hỏi đáp tài liệu 5–6 lần trong nhóm chat lớp |
| 7 | Pain từ người khác | Khi Product Manager cần làm báo cáo tiến độ tuần vào chiều thứ Sáu, họ muốn có sẵn số lượng issue đã xử lý và rủi ro kỹ thuật từ dev, để gửi tổng kết cho cấp trên đúng hạn mà không phải nhắn tin giục từng dev | PM, Tech Lead, Ban quản lý | PM nhắn tin nhắc nhở trong kênh chung liên tục từ 14h đến 17h thứ Sáu; 3/5 tuần gần nhất báo cáo bị gửi trễ sau 18h |
| 8 | Pain từ người khác | Khi Tester bắt đầu test một tính năng mới, họ muốn biết bug mình vừa phát hiện đã có ai tạo ticket trên Jira chưa, để tránh tạo ticket trùng lặp gây mất thời gian triage cho lập trình viên | Tester, Developer | Sprint vừa rồi có 8/45 ticket bị đánh dấu là 'Duplicate'; tốn khoảng 10–15 phút cho mỗi ticket trùng để xác nhận và đóng lại |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- **Ý AI gợi ý được giữ lại:** *'Khi nhận ticket bug phản ánh từ khách hàng thiếu thông tin tái hiện, tôi muốn có bộ câu hỏi làm rõ chuẩn hóa ngay lập tức, để gửi khách hàng phản hồi chỉ trong 1 lần tương tác.'* (Giữ lại vì đây là vấn đề rất thực tế của đội Support/Dev, giảm thời gian email qua lại nhiều vòng).
- **Ý AI gợi ý bị loại bỏ:** *'Trợ lý AI tự động quản lý toàn bộ task dự án và tự phân công cho lập trình viên.'* (Loại bỏ vì đây là giải pháp viển vông, bắt đầu từ mong muốn dùng AI chứ không đi từ một nỗi đau quy trình cụ thể có người chịu trách nhiệm, phạm vi quá rộng và thiếu tính khả thi).

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Review Pull Request (PR) lớn (>500 dòng / nhiều file) | Quy trình rõ, tốn nhiều thời gian nhất (~58 phút/PR), ảnh hưởng trực tiếp đến tốc độ merge và release của toàn team | Liệu AI tóm tắt diff có nắm đúng logic nghiệp vụ sâu của hệ thống hay chỉ tóm tắt bề mặt? |
| 2 | Đối soát incident từ logs, Sentry và commit deploy | Nỗi đau lớn khi có sự cố, MTTR kéo dài gây rủi ro uptime cao | Quyền truy cập và tính bảo mật của dữ liệu log production khi đưa qua AI |
| 3 | Báo cáo tiến độ tuần và sprint metric cho PM | Quy trình lặp lại hàng tuần, tốn thời gian tổng hợp thủ công từ Jira/GitHub | Một số team chỉ cần dashboard số liệu thô chứ không bắt buộc narrative chi tiết |

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi nhận một Pull Request (PR) phức tạp (>500 dòng code hoặc thay đổi trên 10 file), tôi muốn nắm nhanh bản đồ liên kết các thay đổi logic nghiệp vụ, để tập trung review đúng trọng tâm và phát hiện bug tiềm ẩn |
| Actor | Reviewer (Senior Dev / Peer Dev) chịu trách nhiệm duyệt chất lượng code trước khi merge |
| Thời điểm / bối cảnh | Trong giờ làm việc khi nhận được mention/notif yêu cầu review PR trước thềm sprint freeze hoặc release |
| Quy trình hiện tại (3–7 bước) | 1. Mở GitHub PR & đọc mô tả task (3')<br>2. Lướt danh sách files changed để hình dung phạm vi (5')<br>3. Đọc chi tiết từng file code diff & lần theo trace luồng gọi hàm giữa các file (35')<br>4. Kiểm tra test cases và CI status (10')<br>5. Viết comment nhận xét và bấm Approve / Request Changes (5') |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3: Đọc chi tiết từng file diff và liên kết ngữ cảnh giữa các module (mất ~35 phút, hay bị quá tải nhận thức khi PR lớn) |
| Impact (nếu không giải thì sao) | PR tồn đọng 2–3 ngày làm chậm chu kỳ release; reviewer dễ duyệt ẩu do mệt mỏi dẫn đến lọt bug logic lên Staging/Production |
| Success metric (baseline → target) | Baseline: 58 phút/PR lớn → Target: dưới 25 phút/PR; tỷ lệ phát hiện các lỗi kiến trúc/logic không giảm |
| Phương án không dùng AI | Đặt rule bắt buộc chia nhỏ PR (mỗi PR < 200 dòng code); bắt buộc dùng PR template có visual flow do tác giả tự vẽ; checklist review chuẩn hóa |
| Giả thuyết về AI (nếu có) | AI phân tích toàn bộ git diff, tự động tạo bản tóm tắt luồng dữ liệu (data flow) thay đổi giữa các file và highlight 3–5 điểm logic trọng yếu cần reviewer chú ý |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 58 phút/PR lớn

[1 Mở PR & đọc mô tả: 3'] 
→ [2 Lướt danh sách file changed: 5'] 
→ [3 Đọc diff & lần trace luồng hàm giữa các file: 35'] ← BOTTLENECK
→ [4 Kiểm tra test cases & CI: 10'] 
→ [5 Comment & Approve/Request changes: 5']
```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi hệ thống gặp sự cố cảnh báo lỗi trên Staging/Production, tôi muốn đối soát nhanh giữa error trace (Sentry), log server và các commit vừa deploy gần nhất, để xác định đúng commit gây lỗi mà không phải mở 4 dashboard riêng rẽ |
| Actor | On-call Developer / DevOps Engineer chịu trách nhiệm xử lý sự cố khẩn cấp |
| Thời điểm / bối cảnh | Khi nhận alert thông báo lỗi 5xx hoặc crash tăng đột biến trong kênh chat #dev-alerts |
| Quy trình hiện tại (3–7 bước) | 1. Đọc tin nhắn cảnh báo trên Slack/Discord (2')<br>2. Mở dashboard Sentry đọc stack trace và thông điệp lỗi (8')<br>3. Mở log server (CloudWatch/Kibana) tra cứu ngữ cảnh kèm theo request ID (12')<br>4. Mở lịch sử deploy trên GitHub đối chiếu các commit mới nhất (8')<br>5. Xác định commit khả nghi và báo cho dev sở hữu commit (5') |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3: Tra cứu và chắp nối ngữ cảnh từ hàng nghìn dòng log server phân tán (12 phút) |
| Impact (nếu không giải thì sao) | MTTR (Mean Time to Resolution) kéo dài trung bình >35 phút/lần; gián đoạn trải nghiệm người dùng; kỹ sư on-call bị áp lực lớn |
| Success metric (baseline → target) | Baseline: 35 phút để tìm ra nguyên nhân ban đầu → Target: dưới 12 phút; độ chính xác khoanh vùng đúng commit >80% |
| Phương án không dùng AI | Cấu hình log centralization chuẩn với correlation-id / trace-id xuyên suốt; gắn thẻ Release version tự động vào Sentry để biết ngay commit deploy |
| Giả thuyết về AI (nếu có) | AI gom stack trace từ Sentry + sample logs liên quan và so khớp với git diff của bản release gần nhất để đưa ra nhận định commit nghi vấn cao nhất |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 35 phút/lần incident triage

[1 Đọc alert Slack: 2'] 
→ [2 Mở Sentry xem stack trace: 8'] 
→ [3 Tra cứu server logs phân tán: 12'] ← BOTTLENECK
→ [4 Đối chiếu git commit deploy gần nhất: 8'] 
→ [5 Khoanh vùng thủ phạm & báo dev: 5']
```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi Product Manager cần làm báo cáo tiến độ tuần vào chiều thứ Sáu, họ muốn có sẵn số lượng issue đã xử lý và rủi ro kỹ thuật từ dev, để gửi tổng kết cho cấp trên đúng hạn mà không phải nhắn tin giục từng dev |
| Actor | Junior Product Manager / Scrum Master phụ trách báo cáo tiến độ sprint |
| Thời điểm / bối cảnh | Chiều thứ Sáu hàng tuần trước buổi họp giao ban tuần với ban giám đốc |
| Quy trình hiện tại (3–7 bước) | 1. Export số liệu Jira sprint (velocity, ticket done/in progress/bug) (10')<br>2. Kiểm tra các PR đã merge trên GitHub (10')<br>3. Nhắn tin hỏi dev về các blocker và lý do task trễ (20')<br>4. Viết narrative nhận định tình hình, rủi ro và kế hoạch tuần tới vào Google Docs (20')<br>5. Format và gửi email/Slack cho ban quản lý (5') |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3: Phải liên lạc phân tán hỏi từng dev để lấy thông tin blocker (20 phút) và bước 4 viết narrative (20 phút) |
| Impact (nếu không giải thì sao) | Tốn 65 phút/tuần; báo cáo thường xuyên gửi trễ (3/5 tuần gửi sau 18h); thiếu thông tin rủi ro cốt lõi do dev bận không kịp trả lời |
| Success metric (baseline → target) | Baseline: 65 phút/báo cáo → Target: dưới 20 phút; 100% báo cáo nộp đúng hạn trước 17h thứ Sáu |
| Phương án không dùng AI | Template Jira tự động hóa dashboard; quy định bắt buộc dev ghi blocker vào trường cố định trên Jira trước 12h thứ Sáu |
| Giả thuyết về AI (nếu có) | AI tự động tổng hợp thông tin status từ Jira và commit messages trên GitHub, nháp sẵn khung narrative nhận định để PM rà soát |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 65 phút/tuần

[1 Export số liệu Jira: 10'] 
→ [2 Kiểm tra PR GitHub: 10'] 
→ [3 Nhắn tin hỏi blocker từ từng dev: 20'] ← BOTTLENECK 1
→ [4 Viết narrative nhận định vào Docs: 20'] ← BOTTLENECK 2
→ [5 Format & Gửi báo cáo: 5']
```

### Card muốn pitch nhất

- Card số: Card #1 (Review Pull Request lớn)
- Vì sao: Đây là nỗi đau thực tế diễn ra hàng ngày của đội ngũ kỹ thuật phần mềm; quy trình các bước rất rõ ràng; có baseline thời gian đo lường cụ thể (~58 phút); ranh giới giữa việc AI hỗ trợ đọc hiểu ngữ cảnh và con người ra quyết định approve/reject rất tách bạch.
- Câu hỏi muốn nhóm phản biện: "Nếu áp dụng chính sách bắt buộc dev tách nhỏ PR dưới 200 dòng (No AI / Rule), liệu có giải quyết triệt để được vấn đề mà không cần đến AI không? Khi nào một PR thực sự không thể tách nhỏ?"

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Baseline 58 phút/PR có phải chỉ là cảm tính cá nhân? | Đồng ý | Bấm giờ thật 3 lần review PR lớn gần nhất: 52 phút, 65 phút và 55 phút (trung bình ~57.3 phút) |
| AI đọc code dễ bị ảo giác (hallucination), khen chê vu vơ hoặc sót lỗi bảo mật nghiêm trọng | Đồng ý | Đã chỉnh rõ boundary: AI tuyệt đối không thay thế con người bấm Approve hay tự động merge; AI chỉ làm nhiệm vụ tóm tắt luồng dữ liệu (data flow) và chỉ điểm các đoạn code nhạy cảm để con người review nhanh hơn |
| Giải pháp Rule (ép dev tách PR < 200 dòng) có thể đã đủ, không cần AI | Đồng ý một phần | Làm rõ bối cảnh: Có những PR liên quan đến refactor schema database, thay đổi cấu trúc config toàn hệ thống hoặc nâng cấp thư viện lớn bắt buộc phải đi cùng nhau trong 1 commit/PR nguyên khối, không thể chia nhỏ được |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Pitch 3 Problem Card cá nhân (#2 Hợp đồng thuê nhà, #10 Hoàn trả hàng e-commerce, #11 Phân loại cấp cứu trong bảng chung). | Đóng góp 3 candidate đa dạng góc nhìn vào bảng thảo luận chung; bài Hợp đồng thuê nhà và Phân loại cấp cứu được nhóm đưa vào cây OST rút gọn. |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt:<br>1. *Hỏi Hiếu (#1 Đi lại):* "Xử lý độ trễ thế nào khi dữ liệu giao thông thay đổi liên tục từng phút?"<br>2. *Hỏi Khôi (#3 Khiếu nại tài xế):* "Nếu tài xế lợi dụng mẫu câu chuẩn để khai báo gian dối (ví dụ đổ lỗi do tắc đường hoặc lỗi app), làm thế nào để workflow AI kết hợp Rule kiểm tra chéo telemetry một cách khách quan mà không để lọt gian lận?"<br>3. *Hỏi Khôi (#6 Cứu hộ pin):* "Nếu xe hết pin nằm trong hầm sâu xe sạc không vào được, AI dựa vào đâu để biết mà không điều xe đến vô ích?"<br>4. *Hỏi Khôi (#7 Xưởng xe):* "Kỹ thuật viên cứng nhìn mã OBD-II là biết khoang, đầu tư AI bước này có thực sự mang lại ROI?" | Câu hỏi đặt cho bài #3 đã giúp Khôi và nhóm nhận diện lỗ hổng gian lận nghiêm trọng, dẫn đến việc thiết kế bổ sung cơ chế cờ đối chiếu chéo (Cross-check Flag) giữa telemetry GPS và log chat, đồng thời chuyển tư duy thiết kế từ tự động duyệt sang AI hỗ trợ (Augment) có con người duyệt (HITL). |
| Nhận phản biện | Câu hỏi tôi nhận được:<br>1. *Cường hỏi bài #2 (Hợp đồng thuê nhà):* "Người dùng hoàn toàn có thể tự copy hợp đồng ném vào ChatGPT để hỏi điều khoản bất lợi, vậy giải pháp chuyên biệt của bạn hơn gì ChatGPT?"<br>2. *Khôi hỏi bài #10 (Hoàn hàng):* "Nếu khách cố tình chụp ảnh góc mờ để lừa hệ thống, AI dựa vào đâu phát hiện?"<br>3. *Hiếu hỏi bài #11 (Cấp cứu):* "Nếu bệnh nhân có bệnh lý ẩn nguy hiểm mà giấy chuyển viện không ghi rõ, AI dựa vào đâu không xếp nhầm ưu tiên thấp?" | Tôi đã sửa gì:<br>• Nhận ra bài #2 bị lỗi solution-first và dễ bị thay thế bởi công cụ phổ thông.<br>• Thấy được bài #10 và #11 có rủi ro biên quá lớn và khó tiếp cận dữ liệu thật.<br>• Quyết định cùng nhóm rút gọn OST và đồng thuận dồn lực cho bài toán Khiếu nại tài xế (#3). |
| Gom cluster / cây OST | Cùng nhóm phân loại 12 candidate thành 3 Cluster (A: Điều hướng real-time, B: Rà soát đối chiếu văn bản, C: Tóm tắt lọc thông tin); bóc tách các ý tưởng solution trá hình. | Xác định rõ Outcome chung và đưa bài #3 vào Cluster B (Rà soát & đối chiếu văn bản/bằng chứng phức tạp). |
| Chọn candidate problem | Tham gia thảo luận và chấm điểm ma trận 7 tiêu chí; thẳng thắn phản biện tính bất khả thi về mặt dữ liệu của bài Hóa đơn AP (#8) và Y tế cấp cứu (#11). | Thống nhất chọn candidate #3 (32/35 điểm) vì có quy trình chuẩn, đo lường được baseline (20-25 phút) và vừa sức kiểm chứng trong buổi lab. |
| Kiểm chứng / research | Đảm nhận vai trò **Người chính CP4**: Rà soát các phóng sự điều tra của Báo *Tuổi Trẻ*, *Người Quan Sát*; tổng hợp tài liệu quy chế Xanh SM / Grab và nghiên cứu học thuật ACM (Rosenblat & Stark, 2016). | Cung cấp bằng chứng thực nghiệm xác thực cho Assumption #1, #2; chứng minh đánh giá 1 sao là "án phạt sinh kế" tước đoạt tiền thưởng của tài xế và chỉ ra lỗ hổng tài xế gian lận cớ tắc đường. |
| Quy trình nhóm | Phản biện quy trình 6 bước hiện tại và 4 bước tương lai; yêu cầu làm rõ cơ chế Fallback và Boundary. | Bổ sung phương án Fallback quay về tra cứu thủ công khi dữ liệu telemetry GPS khuyết thiếu hoặc độ tin cậy AI < 80%; chốt ranh giới AI không được tự duyệt. |
| Problem Statement | Phản biện Problem Statement v0: chỉ ra lỗ hổng nếu chỉ đo tốc độ (từ 22' xuống 6') thì nhân viên sẽ duyệt ẩu để chạy KPI. | Nhóm tiếp thu và bổ sung vào v1 hai metric chất lượng: tỷ lệ Ops phải tra lại log gốc < 20% và tỷ lệ khiếu nại lại lần 2 giảm ≥ 40%, kèm 4 tiêu chí đánh giá đầu ra AI khắt khe. |
| Mức can thiệp AI | Thảo luận ma trận độ mơ hồ × độ phức tạp; phân tích và phản biện các mức No AI, Rule, Workflow, Agent. | Khẳng định mức Workflow là tối ưu nhất: dùng Rule gom data cứng, LLM đọc hiểu ngữ cảnh và chỉ điểm mâu thuẫn, con người giữ quyền quyết định; kiên quyết loại bỏ mức Agent. |
| Quyết định | Tham gia đánh giá 4 loại rủi ro (Value, Usability, Feasibility, Viability); thiết lập 2 ngưỡng dừng đo lường được. | Đồng thuận quyết định **Go phạm vi nhỏ (Pilot 50 ticket cũ trong 2 tuần)**; thiết lập ngưỡng dừng: dừng ngay nếu tỷ lệ mở lại log > 35% hoặc có ≥ 2 ca bỏ lọt gian lận. |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Brainstorm thêm các vấn đề thường gặp theo 4 lăng kính trong quy trình vận hành và đời sống sinh viên. | Gợi ý góc nhìn về việc trích xuất thông tin bug report từ khách hàng (được giữ lại ở mục 2). | Gợi ý ý tưởng viển vông, mang tính solution-first: "Trợ lý AI tự động quản lý toàn bộ task dự án và tự phân công cho dev". | Loại bỏ ý tưởng viển vông; tự viết lại các Job Story dựa trên trải nghiệm và quan sát thực tế có số liệu đo lường cụ thể. |
| CP2 Problem Card | Đóng vai người phản biện (Devil's Advocate) để tìm điểm yếu của Problem Card #1 (Review PR lớn). | Chỉ ra rủi ro AI bị ảo giác và chất vấn baseline 58 phút có phải do cảm tính. | Gợi ý giải pháp Rule (ép dev chia PR < 200 dòng) một cách máy móc mà không hiểu tính chất của việc refactor lớn. | Tự bấm giờ 3 lần review PR thật (52', 65', 55'); bổ sung lập luận giải thích vì sao có những PR nguyên khối không thể tách nhỏ và xác định boundary AI chỉ tóm tắt luồng dữ liệu chứ không duyệt code. |
| CP4 Research | Tra cứu các bài báo khoa học và case study quốc tế về quản trị thuật toán tài xế công nghệ (Uber, Grab). | Tóm tắt nhanh luận điểm của nghiên cứu Rosenblat & Stark (2016) trên ACM về thiên kiến đánh giá của khách hàng. | Tự bịa (hallucinate) ra các API mở của GSM/Xanh SM vốn là hệ thống nội bộ đóng kín. | Xác định rõ hệ thống GSM là đóng bảo mật; chuyển hướng kiểm chứng thực nghiệm qua tuyến bài điều tra của Báo *Tuổi Trẻ*, *Người Quan Sát* và quy chế ứng xử chính thức của hãng. |
| CP5 Quy trình | Hỗ trợ mô hình hóa luồng dữ liệu giữa các bên (Driver, CS, GPS System) sang định dạng sơ đồ ASCII. | Tạo khung sơ đồ trực quan nhanh, tiết kiệm thời gian vẽ hình. | AI tự động thiết kế để AI tự cập nhật kết quả gỡ phạt vào hệ thống mà không cần con người xác nhận. | Chỉnh sửa lại sơ đồ: bổ sung bước Driver Ops kiểm tra cờ cảnh báo và ra quyết định phê duyệt (Human-in-the-loop); thiết lập phương án fallback về tra cứu thủ công. |
| CP5–6 Problem Statement | Rà soát câu chữ của Problem Statement v0 để tìm sơ hở về mặt logic và đo lường. | Gợi ý tách bạch giữa AI intervention point và các bước xử lý dữ liệu của Rule. | Metric do AI gợi ý chỉ tập trung vào tốc độ xử lý nhanh, không lường trước hành vi nhân viên bấm duyệt bừa để chạy KPI. | Đề xuất nhóm bổ sung các metric chặn: tỷ lệ phải tra lại log gốc < 20%, tỷ lệ khiếu nại vòng 2 giảm ≥ 40% và xây dựng 4 tiêu chí đánh giá đầu ra khắt khe. |
| CP6 Mức can thiệp / quyết định | So sánh ưu nhược điểm giữa Rule-based, Workflow và Autonomous Agent trong bài toán gian lận. | Phân tích rõ chi phí tính toán và rủi ro pháp lý của từng phương án công nghệ. | Đề xuất ngưỡng dừng rất mơ hồ ("Dừng lại nếu người dùng không hài lòng hoặc độ chính xác không cao"). | Thiết lập 2 ngưỡng dừng định lượng tuyệt đối: tỷ lệ mở lại log vượt quá 35% hoặc phát hiện ≥ 2 trường hợp bỏ lọt gian lận thì dừng ngay đợt pilot. |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

Khi lắng nghe phần trình bày top 3 problems của các thành viên trong nhóm, bài học lớn nhất mà tôi nhận được là sự phân biệt rõ ràng giữa một "nỗi đau bề mặt" (sự phiền toái nhỏ nhặt) và một "nỗi đau vận hành có chi phí thực sự" (acute operational pain). Ban đầu, những ý tưởng như so sánh phương tiện xe buýt/xe máy của Hiếu hay lọc tin nhắn nhóm học tập nghe rất gần gũi, nhưng khi đặt lên bàn cân phân tích thì người dùng hoàn toàn có thể tự giải quyết bằng các thao tác thông thường hoặc công cụ miễn phí có sẵn mà không cần đầu tư giải pháp AI chuyên biệt. Ngược lại, bài toán đối soát khiếu nại 1 sao của Khôi hay quy trình review PR lớn của cá nhân tôi lại có đối tượng chịu trách nhiệm rất cụ thể (Driver Ops, Tech Lead), có áp lực thời gian dồn dập (hạn chốt thưởng tuần, lịch release) và có hậu quả đo đếm được bằng tiền bạc hoặc sự trì trệ của cả hệ thống. Tôi hiểu rằng muốn giải quyết bài toán AI hiệu quả, điều kiện tiên quyết không phải là công nghệ phức tạp mà là phải tìm đúng nút thắt nhận thức lặp đi lặp lại trong một quy trình tác nghiệp thực tế.

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

Nhóm tôi đã bị rơi vào cái bẫy "solution-first" rất điển hình ở giai đoạn đầu CP3, và người mắc phải chính là tôi với đề tài rà soát hợp đồng thuê nhà cho sinh viên (#2). Khi chuẩn bị bài, tôi đã quá hào hứng với ý tưởng xây dựng một ứng dụng AI dùng mô hình LLM để tự động đọc toàn bộ hợp đồng và highlight các điều khoản rủi ro. Tuy nhiên, ngay khi tôi vừa pitch xong, Cường đã đặt một câu hỏi phản biện rất thẳng thắn: *"Người dùng hoàn toàn có thể tự copy hợp đồng ném vào ChatGPT để hỏi điều khoản bất lợi, vậy giải pháp chuyên biệt của bạn hơn gì ChatGPT?"*. Câu hỏi này khiến tôi sững lại và nhận ra mình đang say mê giải pháp công nghệ hơn là thấu hiểu bối cảnh người dùng. Nỗi đau thật sự của sinh viên là sự thiếu tự tin về mặt pháp lý và tâm lý sợ bị chủ nhà làm khó khi đàm phán, chứ không đơn thuần là việc không có công cụ đọc văn bản. Cả nhóm đã dừng lại để mổ xẻ và nhận thấy bài toán này thiếu một quy trình nghiệp vụ rõ ràng, không có tần suất lặp lại thường xuyên và rất dễ bị thay thế bởi các công cụ AI phổ thông. Nhóm đã quyết định loại bỏ ý tưởng này để tập trung vào bài toán đối soát khiếu nại tài xế, nơi quy trình và dữ liệu gắn chặt chẽ với nhau.

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

Tôi đã hoàn toàn đổi ý trong quá trình thảo luận về giải pháp kiểm soát gian lận cho bài toán của nhóm ở CP3 và CP4. Ban đầu, khi Khôi trình bày bài toán đối soát khiếu nại, tôi từng giữ quan điểm rất khắt khe và hoài nghi: tôi cho rằng các tài xế hoàn toàn có thể học thuộc các mẫu văn bản giải trình "chuẩn kịch bản kẹt xe" hoặc bắt tay nhau tạo cớ để lừa AI, do đó việc áp dụng AI vào đây là vô nghĩa và chỉ làm tăng nguy cơ thất thoát tiền thưởng của nền tảng. Tôi thậm chí đã đề xuất chỉ nên dùng Rule cứng: nếu GPS không ghi nhận vận tốc bằng 0 đúng 20 phút thì từ chối thẳng thừng mọi khiếu nại. Tuy nhiên, sau khi Khôi và nhóm phân tích lại thực tế giao thông qua các bài phóng sự điều tra của Báo Tuổi Trẻ (xe di chuyển nhích từng mét với vận tốc 2–5 km/h thì Rule vận tốc = 0 sẽ hoàn toàn bất lực và xử oan cho tài xế), tôi đã thay đổi nhận định. Tôi nhận ra rằng từ chối AI một cách cực đoan là sai lầm; thay vào đó, giải pháp đúng đắn là kết hợp sức mạnh của cả hai: dùng Rule để tính toán số liệu vật lý thô (vận tốc trung bình, độ dài dừng đỗ) và dùng AI để đối chiếu ngữ cảnh giữa lời kể với mốc thời gian chat, đồng thời giữ nguyên chốt chặn con người (Driver Ops) kiểm duyệt cuối cùng.

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

Khi trực tiếp phụ trách khâu kiểm chứng tài liệu và phóng sự điều tra ở CP4, điều làm tôi bàng hoàng và bất ngờ nhất chính là mức độ khốc liệt của chỉ số "đánh giá 1 sao" đối với đời sống của người tài xế công nghệ. Trước đây, ở góc độ người dùng thông thường, tôi chỉ nghĩ đánh giá sao là một phản hồi dịch vụ đơn giản. Nhưng qua các phóng sự điều tra chuyên sâu của Báo *Tuổi Trẻ* và *Người Quan Sát*, tôi mới thấu hiểu đánh giá 1 sao thực sự là một "án phạt sinh kế" tàn nhẫn: một tài xế bị khách đánh 1 sao trả đũa (chỉ vì không dám vượt đèn đỏ hoặc kẹt xe giờ cao điểm) sẽ bị tụt điểm sao trung bình xuống dưới 4.85, đồng nghĩa với việc bị tước sạch toàn bộ tiền thưởng tuần và thưởng Tết lên đến hàng triệu đồng—được ví như "mất Tết". Nghịch lý lớn nhất là thuật toán phạt trừ điểm của ứng dụng diễn ra tự động và tàn nhẫn trong tích tắc, nhưng quy trình khiếu nại minh oan lại cực kỳ nhiêu khê, mất 3–5 ngày do nhân viên CS phải mở 3 màn hình đối soát thủ công, khiến tài xế vẫn phải chịu thiệt thòi trước chu kỳ chốt thưởng. Điều này củng cố niềm tin tuyệt đối của tôi vào giá trị xã hội và ROI thực tế của bài toán nhóm đã chọn.

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

Điều khó nhất khi cùng nhóm hoàn thiện Problem Statement (đặc biệt là bước chuyển từ v0 sang v1) chính là việc thiết lập **Success Metric** và **Boundary (Ranh giới)** sao cho không tạo ra hệ quả tiêu cực ngoài ý muốn (perverse incentives). Ở bản v0, nhóm chỉ đặt mục tiêu đơn giản là "rút ngắn thời gian xử lý từ 22 phút xuống dưới 6 phút/ticket". Tôi đã nhận ra ngay lỗ hổng chết người của chỉ số này: nếu chỉ đo thời gian, nhân viên CS sẽ có xu hướng đọc lướt qua loa bản tóm tắt của AI rồi bấm phê duyệt hàng loạt để hoàn thành chỉ tiêu KPI về tốc độ, dẫn đến việc bỏ sót hàng loạt tài xế gian lận. Cái khó là làm sao vừa giải phóng sức lao động cho nhân viên, vừa duy trì tính nghiêm minh của quy trình. Tôi đã thúc đẩy nhóm bổ sung thêm hai metric chặn chất lượng: Tỷ lệ nhân viên phải mở lại log gốc tra cứu phải nhỏ hơn 20% (đo lường độ đầy đủ của tóm tắt) và Tỷ lệ tài xế khiếu nại lại lần 2 phải giảm tối thiểu 40% (đo lường tính công bằng của quyết định). Việc cân bằng giữa hiệu suất và chất lượng chính là bài toán hóc búa nhất.

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

Nếu có cơ hội làm lại từ đầu, điều tôi muốn thay đổi nhất là chủ động xây dựng một bộ dữ liệu giả lập (mock telemetry log dataset) chuẩn hóa gồm tọa độ GPS, thời gian dừng đỗ và đoạn chat ngay từ Checkpoint 2. Việc thiếu dữ liệu mẫu cụ thể ở giai đoạn đầu đã khiến nhóm tốn nhiều thời gian tranh cãi mang tính giả định về khả năng của AI. Ngoài ra, tôi sẽ phản biện nhóm quyết liệt hơn ở khâu chấm điểm shortlist CP3: tôi sẽ yêu cầu nhóm loại bỏ sớm hơn các đề tài thuộc lĩnh vực chuyên môn quá hẹp hoặc dữ liệu bí mật như Kế toán AP (#8) hay Phân loại bệnh nhân cấp cứu (#11). Việc nhóm dành gần một tiếng đồng hồ để cân nhắc giữa bài toán Kế toán và bài toán Tài xế là không cần thiết, bởi nhóm hoàn toàn không có thành viên nào am hiểu sâu về chuẩn mực kiểm toán 3-way matching để kiểm chứng giả định. Nếu tiết kiệm được thời gian đó, nhóm đã có thể tiến hành thử nghiệm prompt chi tiết hơn trên tập dữ liệu mẫu.

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

Bài toán của nhóm giải quyết tình trạng nhân viên Driver Ops mất 20–25 phút đối soát thủ công qua 3 màn hình riêng biệt (ticket, telemetry GPS, chat) để xử lý khiếu nại đánh giá 1 sao của tài xế trước hạn chốt thưởng tuần. Quy trình mới tinh gọn từ 6 bước thủ công thành 4 bước tích hợp: Rule tự động gom log telemetry và đoạn chat theo mã cuốc xe, AI đọc hiểu ngữ cảnh để tạo Bản tóm tắt bằng chứng 150 từ kèm cờ cảnh báo nghi vấn, Driver Ops đọc duyệt và Rule cập nhật hệ thống. Metric đo lường gồm rút ngắn thời gian xử lý xuống ≤ 6 phút/ticket, đạt tỷ lệ hoàn thành đúng hạn ≥ 98%, đồng thời kiểm soát chất lượng với tỷ lệ mở lại log gốc < 20% và tỷ lệ khiếu nại lần 2 giảm ≥ 40%. Boundary tuyệt đối là AI không bao giờ được tự động phê duyệt gỡ phạt hay can thiệp điểm thưởng, quyền quyết định hoàn toàn thuộc về con người (Human-in-the-loop). Nhóm lựa chọn mức can thiệp là **Workflow** vì quy trình mang tính tuần tự cố định, kết hợp Rule xử lý số liệu cứng và AI xử lý ngôn ngữ tự nhiên để hỗ trợ nhận thức (Augment). Quyết định cuối cùng là **Go phạm vi nhỏ (Pilot 50 ticket cũ trong 2 tuần)**, đi kèm 2 ngưỡng dừng nghiêm ngặt: dừng ngay lập tức nếu tỷ lệ mở lại log gốc vượt quá 35% hoặc phát hiện từ 2 trường hợp bỏ sót gian lận trở lên.

---

## 7. Tài liệu tham khảo

1. **Báo Tuổi Trẻ Online:** *"Tài xế thời kẹt xe: Đơn nhiều, giao chẳng được bao nhiêu"* — [`https://tuoitre.vn/tai-xe-thoi-ket-xe-don-nhieu-giao-chang-duoc-bao-nhieu-20250114115250949.htm`](https://tuoitre.vn/tai-xe-thoi-ket-xe-don-nhieu-giao-chang-duoc-bao-nhieu-20250114115250949.htm)
2. **Báo Người Quan Sát:** *"Tài xế xe ôm công nghệ: Chấp nhận khách đánh giá 1 sao, còn hơn ‘mất Tết’"* — [`https://nguoiquansat.vn/tai-xe-xe-om-cong-nghe-chap-nhan-khach-danh-gia-1-sao-con-hon-mat-tet-192562.html`](https://nguoiquansat.vn/tai-xe-xe-om-cong-nghe-chap-nhan-khach-danh-gia-1-sao-con-hon-mat-tet-192562.html)
3. **ACM Digital Library:** Lee, M. K., Kusbit, D., Metsky, E., & Dabbish, L. (2015). *"Working with Machines: The Impact of Algorithmic Management on Gig Workers"*. Proceedings of the 33rd Annual ACM Conference on Human Factors in Computing Systems (CHI '15) — [`https://dl.acm.org/doi/10.1145/2702123.2702548`](https://dl.acm.org/doi/10.1145/2702123.2702548)
4. **Google People + AI Guidebook (PAIR):** *"Human-Centered AI Design: Augmentation vs Automation & Handling Errors"* — [`https://pair.withgoogle.com/guidebook/`](https://pair.withgoogle.com/guidebook/)
