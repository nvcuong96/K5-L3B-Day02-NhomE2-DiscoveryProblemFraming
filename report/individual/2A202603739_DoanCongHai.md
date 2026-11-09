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
| 1 | | | |
| 2 | | | |
| 3 | | | |

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi …, tôi muốn …, để … |
| Actor | |
| Thời điểm / bối cảnh | |
| Quy trình hiện tại (3–7 bước) | |
| Bottleneck (bước nào, mất bao nhiêu phút) | |
| Impact (nếu không giải thì sao) | |
| Success metric (baseline → target) | |
| Phương án không dùng AI | |
| Giả thuyết về AI (nếu có) | |
| Cảm nhận nhanh | No AI / Rule / Workflow / Agent / Chưa biết |

Quy trình nháp hiện tại:

```text

```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi …, tôi muốn …, để … |
| Actor | |
| Thời điểm / bối cảnh | |
| Quy trình hiện tại (3–7 bước) | |
| Bottleneck (bước nào, mất bao nhiêu phút) | |
| Impact (nếu không giải thì sao) | |
| Success metric (baseline → target) | |
| Phương án không dùng AI | |
| Giả thuyết về AI (nếu có) | |
| Cảm nhận nhanh | No AI / Rule / Workflow / Agent / Chưa biết |

Quy trình nháp hiện tại:

```text

```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi …, tôi muốn …, để … |
| Actor | |
| Thời điểm / bối cảnh | |
| Quy trình hiện tại (3–7 bước) | |
| Bottleneck (bước nào, mất bao nhiêu phút) | |
| Impact (nếu không giải thì sao) | |
| Success metric (baseline → target) | |
| Phương án không dùng AI | |
| Giả thuyết về AI (nếu có) | |
| Cảm nhận nhanh | No AI / Rule / Workflow / Agent / Chưa biết |

Quy trình nháp hiện tại:

```text

```

### Card muốn pitch nhất

- Card số:
- Vì sao:
- Câu hỏi muốn nhóm phản biện:

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| | | |

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
