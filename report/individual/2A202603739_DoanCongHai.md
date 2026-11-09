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
| Pitch Problem Card | | |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: | |
| Nhận phản biện | Câu hỏi tôi nhận được: | Tôi đã sửa gì: |
| Gom cluster / cây OST | | |
| Chọn candidate problem | | |
| Kiểm chứng / research | | |
| Quy trình nhóm | | |
| Problem Statement | | |
| Mức can thiệp AI | | |
| Quyết định | | |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | | | | |
| CP2 Problem Card | | | | |
| CP4 Research | | | | |
| CP5 Quy trình | | | | |
| CP5–6 Problem Statement | | | | |
| CP6 Mức can thiệp / quyết định | | | | |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

---

## 7. Tài liệu tham khảo

-
