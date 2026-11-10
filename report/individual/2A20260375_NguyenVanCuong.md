# Báo cáo cá nhân — MSSV_HoTen

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Nguyễn Văn Cường
- MSSV: 2A202603750
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: Nhóm E2
- Link repo nhóm: https://github.com/nvcuong96/K5-L3B-Day02-NhomE2-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Tốn thời gian | Khi tôi cần xử lý 1 ticket hỗ trợ từ khách hàng, tôi muốn biết ngay vấn đề này đã từng gặp trước đây chưa và các bước xử lý chuẩn, để giảm thời gian tra cứu, tránh trao đổi lòng vòng và giải quyết sự cố nhanh chóng. | Dev mới (onboarding), Dev trực ca, khách hàng | Đọc và phân tích ticket/email mất 5–10 phút, tìm kiếm tài liệu nội bộ mất ~10 phút, hỏi lại khách hàng và chờ phản hồi mất 30–45 phút; tổng cộng mất 45–50 phút trước khi bắt đầu sửa lỗi thật sự. |
| 2 | Tốn thời gian / Pain từ người khác | Khi phải thực hiện nhiều chỉ định khám và xét nghiệm tại bệnh viện, tôi muốn biết rõ thứ tự thực hiện tối ưu và thời gian chờ dự kiến tại từng phòng, để chủ động sắp xếp di chuyển, tránh đi lòng vòng giữa các khoa phòng và giảm bớt thời gian chờ đợi mệt mỏi. | Bệnh nhân ngoại trú, người nhà đi cùng, điều dưỡng tiếp đón / điều phối phòng khám, bác sĩ | Nghiên cứu tại Bệnh viện Quân y 103 trên 303 bệnh nhân năm 2024 ghi nhận thời gian chờ kết quả sinh hóa trung bình khoảng 98 phút; tổng thời gian khám ngoại trú kéo dài 3–4 tiếng; điều dưỡng liên tục bị ngắt quãng vì người bệnh hỏi thời gian chờ. |
| 3 | Lặp lại (Repetitive) | Khi tiếp nhận dồn dập hàng trăm hóa đơn và chứng từ thanh toán nhiều định dạng mỗi ngày, tôi muốn nhanh chóng đối soát và phát hiện ngay các điểm sai lệch giữa chứng từ với đơn đặt hàng (PO/GRN), để xử lý thanh toán đúng hạn cho nhà cung cấp mà không phải nhập tay lặp đi lặp lại từng dòng hay chịu rủi ro thất thoát số liệu. | Kế toán công nợ phải trả (AP), kế toán trưởng, nhà cung cấp | Theo Ardent Partners (2024), thời gian xử lý thủ công trung bình một hóa đơn AP là 9,15 ngày; mỗi hóa đơn mất 15–30 phút nhập liệu và đối chiếu tay; vào kỳ chốt sổ cuối tháng nhân viên AP thường phải làm thêm giờ 2–3 tiếng/ngày. |
| 4 | Cần đọc, tổng hợp nhiều thông tin | Khi đến hạn chốt báo cáo tiến độ tuần cho nhiều dự án song song, tôi muốn nhanh chóng nắm bắt bức tranh toàn cảnh, tiến độ thực tế các mốc bàn giao và các điểm nghẽn (blocker) phát sinh từ nhiều kênh công việc khác nhau, để kịp thời cảnh báo rủi ro cho ban giám đốc và khách hàng mà không phải mất hàng giờ thu thập, giục giã và gọt giũa dữ liệu thủ công. | Project Manager (PM), Scrum Master, Tech Lead, Ban Giám đốc / Khách hàng | PM quản lý 3–4 dự án mất 3–4 tiếng mỗi thứ Sáu chỉ để rà soát Jira/Git/email/chat, giục dev cập nhật trạng thái và tổng hợp slide báo cáo; 20–30% rủi ro/blocker phát sinh trong tuần bị phát hiện trễ do thông tin nằm rải rác. |
| 5 | Pain từ người khác / Cần đọc, tổng hợp | Khi ứng dụng phát hành bản cập nhật mới nhận về hàng ngàn đánh giá trên App Store và Google Play, tôi muốn nhanh chóng gom nhóm các cụm phản ánh về lỗi kỹ thuật (crash, giật lag, lỗi giao dịch) và mức độ bức xúc của người dùng, để đội ngũ kỹ thuật ưu tiên vá lỗi nghiêm trọng kịp thời mà không phải cuộn đọc thủ công từng nhận xét rời rạc. | Product Owner (PO), Kỹ sư hỗ trợ ứng dụng / QA, người dùng cuối gặp lỗi | Mỗi đợt cập nhật lớn nhận 500–1.000 đánh giá/tuần; PO và QA mất 4–6 tiếng mỗi tuần đọc và phân loại thủ công; thường mất 3–4 ngày mới phát hiện ra luồng lỗi nghiêm trọng ảnh hưởng diện rộng, khiến điểm đánh giá ứng dụng bị kéo tụt từ 4.6 xuống dưới 4.0 sao. |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.



---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Gợi ý thứ tự khám cho bệnh nhân | Pain thật, nhiều người gặp | Liệu có giảm thời gian chờ đợi được nhiều hay không? |
| 2 | Gợi ý xử lý ticket | Giảm thời gian tranfer người cũ cho người mới, giảm thời gian xử lý ticket |  |
| 3 | Đối chiếu, nhập liệu các hóa đơn | quy trình rõ ràng | Đảm bảo AI nhập đúng, chính xác |

### Problem Card #1 — Gợi ý thứ tự khám cho bệnh nhân

| Trường | Nội dung |
|---|---|
| Job Story | Khi phải thực hiện nhiều chỉ định khám và xét nghiệm tại bệnh viện, tôi muốn biết rõ thứ tự thực hiện tối ưu và thời gian chờ dự kiến tại từng phòng, để chủ động sắp xếp di chuyển, tránh đi lòng vòng giữa các khoa phòng và giảm bớt thời gian chờ đợi mệt mỏi |
| Actor | Bệnh nhân đến khám, điều dưỡng / nhân viên tiếp đón, bác sĩ, bệnh viện |
| Thời điểm / bối cảnh | Khi bệnh nhân đăng ký khám tại quầy hoặc qua app, trước khi vào khu chờ; bệnh viện đông bệnh nhân mỗi buổi sáng |
| Quy trình hiện tại (3–7 bước) | 1. Bệnh nhân đến quầy đăng ký lấy số · 2. Ngồi chờ không biết bao lâu · 3. Điều dưỡng gọi theo thứ tự số · 4. Bệnh nhân di chuyển đến phòng khám · 5. Chờ tiếp tại phòng xét nghiệm hoặc chẩn đoán hình ảnh · 6. Nhận kết quả, quay lại bác sĩ · 7. Thanh toán và nhận đơn |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 2 và 5: chờ không có thông tin — thời gian chờ kết quả sinh hóa trung bình ~98 phút (Bệnh viện Quân y 103, 2024, N=303); bệnh nhân không biết thứ tự ưu tiên nên di chuyển sai phòng |
| Impact (nếu không giải thì sao) | Bệnh nhân mất cả buổi sáng cho một lần khám; điều dưỡng liên tục trả lời câu hỏi "còn bao lâu nữa?"; bác sĩ bị gián đoạn; bệnh viện kém hài lòng |
| Success metric (baseline → target) | Thời gian chờ trung bình từ ~98 phút xuống dưới 60 phút; tỉ lệ bệnh nhân đi nhầm phòng giảm ≥ 50%; điểm hài lòng bệnh nhân tăng |
| Phương án không dùng AI | Bảng điện tử hiển thị số thứ tự + thời gian chờ ước tính theo lịch cố định; phân luồng bệnh nhân theo bệnh phổ biến |
| Giả thuyết về AI | AI dự đoán thời gian chờ dựa trên lịch sử lượt khám, loại dịch vụ, số bệnh nhân đang chờ; đề xuất thứ tự phòng khám tối ưu cho từng bệnh nhân → hiển thị qua app hoặc màn hình tại quầy |
| Cảm nhận nhanh | Workflow (các bước dự đoán cố định) có AI ở bước ước tính thời gian |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 7 bước, ~180 phút / lượt khám

[1 Đăng ký lấy số: 5'] → [2 Chờ gọi tên: ???] ← KHÔNG BIẾT BAO LÂU
→ [3 Khám bác sĩ: 10–15'] → [4 Làm xét nghiệm / CĐHA: 10']
→ [5 Chờ kết quả: ~98' trung bình] ← BOTTLENECK CHÍNH
→ [6 Tái khám nhận kết quả: 10'] → [7 Thanh toán + nhận đơn: 10']

Vấn đề: Bệnh nhân không có thông tin thời gian → chờ thụ động,
         di chuyển sai phòng, hỏi điều dưỡng liên tục.
```

### Problem Card #2 — Gợi ý xử lý ticket hỗ trợ khách hàng

| Trường | Nội dung |
|---|---|
| Job Story | Khi tôi nhận một ticket hỗ trợ từ khách hàng, tôi muốn biết ngay liệu vấn đề này đã từng gặp trước đây không và cách xử lý ra sao, để giảm thời gian phân tích, trao đổi và chuyển giao giữa các dev |
| Actor | Dev mới (onboarding), Dev xử lý ticket, khách hàng |
| Thời điểm / bối cảnh | Khi nhận ticket mới qua hệ thống helpdesk; đặc biệt khi dev mới chưa quen hệ thống hoặc khi dev cũ chuyển giao ca trực |
| Quy trình hiện tại (3–7 bước) | 1. Đọc và phân tích nội dung email / ticket (~5–10 phút) · 2. Tìm kiếm trong tài liệu nội bộ / wiki (~10 phút) · 3. Hỏi đồng nghiệp có kinh nghiệm · 4. Hỏi lại khách hàng để làm rõ (~30 phút chờ phản hồi) · 5. Thực hiện xử lý · 6. Ghi lại kết quả (thường bị bỏ qua) |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 2 và 4: tìm tài liệu không có cấu trúc (~10 phút) + hỏi lại khách hàng và chờ phản hồi (~30 phút hoặc hơn); tổng ~45–50 phút trước khi bắt đầu xử lý thật sự |
| Impact (nếu không giải thì sao) | Dev mới mất nhiều thời gian ramp-up; khách hàng chờ lâu; kiến thức xử lý ticket không được tái sử dụng; dev cũ bị làm phiền để trả lời câu hỏi lặp lại |
| Success metric (baseline → target) | Thời gian từ nhận ticket đến bắt đầu xử lý từ ~45 phút xuống dưới 15 phút; tỉ lệ ticket phải hỏi lại khách hàng giảm ≥ 30% |
| Phương án không dùng AI | Chuẩn hóa wiki / runbook theo loại lỗi; template câu hỏi triage; checklist onboarding cho dev mới |
| Giả thuyết về AI | AI phân tích nội dung ticket, tìm kiếm trong lịch sử ticket đã giải quyết, gợi ý các bước xử lý phù hợp và câu hỏi làm rõ cần hỏi khách hàng → Dev review và quyết định trước khi thực hiện |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 6 bước, ~45–50 phút trước khi bắt đầu fix

[1 Đọc ticket: 5–10'] → [2 Tìm tài liệu: 10'] ← KHÔNG CÓ CẤU TRÚC
→ [3 Hỏi đồng nghiệp: ???] → [4 Hỏi lại KH + chờ: ~30'] ← BOTTLENECK
→ [5 Xử lý thật sự] → [6 Ghi kết quả: thường bỏ qua]

Vấn đề: Kiến thức nằm trong đầu dev cũ, không được lưu có hệ thống
         → Dev mới phải hỏi lại từ đầu với mỗi loại ticket.
```

### Problem Card #3 — Đối chiếu và nhập liệu hóa đơn AP tự động

| Trường | Nội dung |
|---|---|
| Job Story | Khi tiếp nhận dồn dập hàng trăm hóa đơn và phiếu thanh toán mỗi ngày, tôi muốn nhanh chóng đối soát và phát hiện ngay các điểm sai lệch giữa chứng từ với đơn đặt hàng (PO/GRN), để giảm nhập liệu thủ công, hạn chế sai sót và rút ngắn thời gian xử lý công nợ |
| Actor | Kế toán công nợ phải trả (AP), trưởng phòng kế toán, nhà cung cấp |
| Thời điểm / bối cảnh | Hằng ngày khi hóa đơn từ nhà cung cấp đổ vào (email, scan, hệ thống ERP); đặc biệt vào cuối tháng khi khối lượng tăng đột biến |
| Quy trình hiện tại (3–7 bước) | 1. Nhận hóa đơn qua email / scan / bản cứng · 2. Đọc và nhập tay từng trường dữ liệu vào ERP · 3. Đối chiếu với đơn đặt hàng (PO) và phiếu nhận hàng (GRN) · 4. Phát hiện sai lệch và hỏi lại nhà cung cấp hoặc bộ phận mua hàng · 5. Trưởng phòng phê duyệt · 6. Thanh toán |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 2 và 3: nhập tay và đối chiếu thủ công — theo Ardent Partners (2024), thời gian xử lý trung bình 1 hóa đơn AP là 9,15 ngày|
| Impact (nếu không giải thì sao) | Trả tiền chậm → mất chiết khấu thanh toán sớm; sai sót nhập liệu → tranh chấp với nhà cung cấp; nhân sự AP bị kéo căng cuối tháng |
| Success metric (baseline → target) | Thời gian xử lý trung bình từ 9,15 ngày xuống dưới 3 ngày; tỉ lệ nhập sai giảm ≥ 80%; tỉ lệ straight-through processing tăng lên ≥ 70% |
| Phương án không dùng AI | Yêu cầu nhà cung cấp gửi hóa đơn điện tử chuẩn (e-invoice XML/EDI); template nhập liệu có validation; kiểm tra chéo 2 người |
| Giả thuyết về AI | AI (OCR + LLM) đọc hóa đơn ở mọi định dạng, trích xuất các trường (số hóa đơn, nhà cung cấp, số tiền, ngày), tự đối chiếu với PO/GRN trong ERP, gắn cờ sai lệch để kế toán xử lý thay vì nhập từ đầu |
| Cảm nhận nhanh | Workflow (OCR → trích xuất → đối chiếu rule → kế toán duyệt exception) |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 6 bước, trung bình 9,15 ngày/hóa đơn

[1 Nhận hóa đơn (email/scan): ~5'] → [2 Nhập tay vào ERP: ~15–30'/HĐ] ← BOTTLENECK
→ [3 Đối chiếu PO + GRN thủ công: ~15'/HĐ] ← BOTTLENECK
→ [4 Xử lý sai lệch + hỏi lại: ???] → [5 Phê duyệt: ~1 ngày]
→ [6 Thanh toán]

Vấn đề: Mỗi hóa đơn có định dạng khác nhau → không thể dùng rule đơn giản;
         sai sót nhập tay tích lũy → khó phát hiện đến cuối tháng.
```

### Card muốn pitch nhất

- Card số: 1 (Gợi ý thứ tự khám cho bệnh nhân tại bệnh viện)
- Vì sao: Nhu cầu và pain point thực tế rất lớn, có số liệu bằng chứng xác thực. Quy trình lặp lại mỗi ngày nhưng người đi khám hoàn toàn không có thông tin thời gian thực để chủ động sắp xếp các bước khám.
- Câu hỏi muốn nhóm phản biện: "Nếu tại một thời điểm có cả 2 phòng khám/xét nghiệm đều đang vắng bệnh nhân, hệ thống dựa vào tiêu chí gì để quyết định ưu tiên điều hướng bệnh nhân vào phòng nào trước?"

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Dự đoán thời gian khám chính xác từng phút là bất khả thi vì phụ thuộc lớn vào các ca cấp cứu đột xuất và tốc độ chẩn đoán của từng bác sĩ; dễ gây phản tác dụng nếu AI báo sai giờ. | Đồng ý | Đổi phạm vi bài toán từ "dự đoán chính xác giờ khám từng phút" thành **"phân luồng và gợi ý thứ tự các phòng khám theo độ dài hàng chờ thực tế"** để tối ưu hóa thời gian chờ song song (ví dụ: làm xét nghiệm máu trước vì mẫu cần thời gian ủ/quay ly tâm). |
| Bệnh nhân cao tuổi hoặc người không dùng smartphone không thể cài app di động để nhận luồng gợi ý. | Đồng ý | Bổ sung phương án hiển thị trực quan số thứ tự và lộ trình phòng khám gợi ý ngay trên màn hình bảng điện tử tại quầy tiếp đón và in kèm mã QR trên phiếu khám giấy. |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Pitch 3 Problem Card cá nhân (Khám bệnh viện, Xử lý ticket dev, Nhập liệu hóa đơn AP). | Đóng góp 3 candidate vào bảng Pitch chung của nhóm (#4, #5, #8); bài Khám bệnh viện và Hóa đơn AP được đưa vào thảo luận sôi nổi. |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt:<br>1. *Hỏi Hải (Bài Hợp đồng thuê nhà):* "Người dùng hoàn toàn có thể tự copy hợp đồng ném vào ChatGPT để hỏi điều khoản bất lợi, vậy giải pháp chuyên biệt của bạn hơn gì ChatGPT?"<br>2. *Hỏi Khôi (Bài Tiếp nhận xe xưởng):* "Khách hàng thường tả tiếng kêu hoặc cảm giác lái rất mơ hồ ('xe kêu lục cục khi qua gờ'), dữ liệu đầu vào không chuẩn hóa như vậy thì AI gợi ý phụ tùng có bị sai lệch lớn không?" | • Giúp Hải nhận ra rủi ro thay thế bởi công cụ phổ thông, thúc đẩy nhóm tư duy về giá trị chuyên sâu của giải pháp.<br>• Giúp Khôi nhận thấy điểm yếu về tính mơ hồ của dữ liệu đầu vào xe điện khi chưa quét OBD-II chuẩn. |
| Nhận phản biện | Câu hỏi tôi nhận được: Khôi hỏi: *"Nếu cả 2 phòng đều vắng thì hệ thống ưu tiên phòng nào trước?"* | Tôi đã sửa gì: Bổ sung quy tắc nghiệp vụ rõ ràng vào quy trình: Ưu tiên bước xét nghiệm có thời gian chạy mẫu lâu nhất (như xét nghiệm máu mất ~90 phút chờ kết quả) làm trước, để trong lúc chờ kết quả sinh hóa bệnh nhân có thể đi khám nội hoặc chụp X-quang. |
| Gom cluster / cây OST | Tham gia phân loại 12 candidate thành 3 nhóm; cùng nhóm nhận diện và gạch bỏ các giải pháp trá hình trong cây OST. | Cùng nhóm gạch bỏ các ý tưởng solution đội lốt opportunity như "Xây app xe buýt", "Dùng AI đọc hợp đồng" để giữ đúng outcome và pain gốc. |
| Chọn candidate problem | Thảo luận bảng chấm điểm shortlist; ban đầu bảo vệ bài Hóa đơn AP (#8) vì quy trình chuẩn. | Sau khi nghe phân tích về rào cản tiếp cận dữ liệu bảo mật kế toán trong thời gian lab, tôi đồng thuận 100% chọn candidate #3 (Đối chiếu khiếu nại tài xế) vì có baseline thời gian thật (22') và vừa sức kiểm chứng. |
| Kiểm chứng / research | Tìm kiếm các bài báo điều tra thực tế của Báo *Tuổi Trẻ*, *Người Quan Sát*, *Thanh Niên* về áp lực đánh giá 1 sao do kẹt xe và tắc đường; rà soát tài liệu ACM của CMU. | Cung cấp bằng chứng thực tế từ báo chí chính quy và các nghiên cứu khoa học cho Mục 3.2 và 3.3 của báo cáo nhóm, làm rõ mâu thuẫn giữa thuật toán hạ sao và quy trình giải trình thủ công. |
| Quy trình nhóm | Cùng nhóm vẽ sơ đồ quy trình 6 bước hiện tại (22 phút) và 4 bước tương lai (5–6 phút). | Xác định chính xác bottleneck nằm ở khâu tra cứu 3 màn hình riêng biệt (18/25 phút); đề xuất phương án quay về (fallback) khi AI không chắc chắn. |
| Problem Statement | Tham gia xây dựng success metric và boundary cho Problem Statement v0 và v1. | Thống nhất ranh giới bắt buộc: AI không bao giờ được tự duyệt gỡ phạt, quyền quyết định cuối cùng phải 100% thuộc về nhân viên vận hành (Human-in-the-loop). |
| Mức can thiệp AI | Thảo luận ma trận độ mơ hồ × độ phức tạp; so sánh 4 mức No AI, Rule, Workflow, Agent. | Lập luận rõ vì sao chọn mức Workflow (kết hợp Rule gom log + LLM đọc hiểu tóm tắt + Ops duyệt) và bác bỏ mức Agent vì rủi ro thất thoát ngân sách thưởng. |
| Quyết định | Tham gia đánh giá 4 rủi ro (*Value, Usability, Feasibility, Viability*) và thiết lập ngưỡng dừng (stop condition). | Thống nhất quyết định Go phạm vi nhỏ (Pilot 50 ticket) và điều kiện dừng: nếu tỷ lệ tra cứu lại > 35% thì quay về tối ưu quy trình No AI. |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Gợi ý thêm các vấn đề thường gặp theo 4 lăng kính nghiệp vụ. | Gợi ý nhanh các khía cạnh công việc tốn thời gian trong lập trình và kế toán. | Gợi ý ý tưởng quá rộng và mơ hồ ("Trợ lý AI quản lý toàn bộ dự án", "AI tối ưu toàn bộ cuộc sống"). | Lọc bỏ toàn bộ các ý tưởng mơ hồ, chỉ giữ lại các vấn đề có quy trình rõ và đo được thời gian thực tế. |
| CP2 Problem Card | Đóng vai người phản biện khó tính (Devil's Advocate) để tìm lỗ hổng của Problem Card #1 (Bệnh viện). | Chỉ ra rằng dự đoán thời gian khám phụ thuộc lớn vào ca cấp cứu đột xuất và tốc độ của bác sĩ. | Gợi ý giải pháp tự động điều phối bác sĩ khám nhanh hơn — điều này vi phạm chuyên môn y khoa. | Nhận định lại ranh giới: AI chỉ gợi ý thứ tự phòng khám cho bệnh nhân theo độ dài hàng chờ, tuyệt đối không can thiệp vào quy trình khám của bác sĩ. |
| CP4 Research | Hỗ trợ tìm kiếm các thuật ngữ chuyên ngành về *Algorithmic management in gig economy* và tóm tắt nhanh tài liệu nghiên cứu. | Giúp tổng hợp nhanh luận điểm chính của bài báo ACM (Lee et al., CMU) và kiến trúc Uber Michelangelo. | Đưa ra một số số liệu chung chung về thị trường gọi xe không có nguồn kiểm chứng; không nắm được thông tin bảo mật nội bộ của VinFast/GSM. | Tự rà soát các bài báo điều tra thực tế từ nguồn uy tín (*Tuổi Trẻ*, *Người Quan Sát*, *Thanh Niên*); nêu rõ lý do hệ thống GSM là bảo mật doanh nghiệp. |
| CP5 Quy trình | Chuyển đổi mô tả quy trình dạng văn bản sang sơ đồ khối ASCII. | Định dạng sơ đồ luồng dữ liệu nhanh, trực quan. | Tự ý gộp bước tra cứu telemetry và đọc tin nhắn chat thành 1 bước tự động trong quy trình hiện tại. | Tách lại thành 2 bước thủ công riêng biệt vì thực tế nhân viên CS phải mở 2 cổng portal riêng biệt, đó chính là nguồn gốc gây ra nút thắt thời gian. |
| CP5–6 Problem Statement | Phản biện tính khả thi và độ chặt chẽ của Problem Statement v0. | Chỉ ra rằng Success Metric ban đầu chỉ đo tốc độ (từ 22' xuống 6') dễ dẫn đến hệ lụy nhân viên duyệt ẩu để chạy KPI. | Đề xuất giải pháp đưa thêm tiêu chuẩn kỹ thuật LLM (BLEU score, ROUGE score) vào metric của người dùng. | Thay thế bằng các metric thực tế trong vận hành: Tỷ lệ nhân viên phải tra lại log gốc (< 20%) và tỷ lệ khiếu nại lại lần 2 (< 40%). |
| CP6 Mức can thiệp / quyết định | So sánh ưu nhược điểm của 4 mức can thiệp AI. | Phân tích rõ sự khác biệt giữa Rule-based và Machine Learning/LLM. | Xu hướng "thần thánh hóa" Agent, gợi ý để Agent tự động nhắn tin giải trình cho tài xế và tự cộng tiền thưởng. | Bác bỏ phương án Agent, khẳng định chọn mức Workflow có con người kiểm duyệt (HITL) để phòng ngừa gian lận và bảo toàn ngân sách. |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**
**Khi nghe Khôi trình bày về bài đối soát khiếu nại tài xế, em thấy rằng vấn đề xuất phát rất thực tế, có thể giải quyết và đo hiệu quả bằng con số thật.

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

Nhóm có xẩy ra tình trạng bị solution first điển hình như khi Hải trình bày về việc xây dựng AI đối chiếu hợp đồng. Hải đã trình bảy giải pháp sử dụng LLM để đọc hợp đồng rồi phân tích các điều khoản bất lợi. Nhóm đã phải biện lại khi hỏi paint thực sự nằm ở đâu, có lớn không.

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**



**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

Điều làm em cảm thấy bất ngờ nhất là khi đọc các bài phóng sự điều tra trên báo Tuổi Trẻ và Người Quan Sát, em mới thấu hiểu nỗi sợ tột cùng của tài xế công nghệ trước một lượt đánh giá 1 sao. Trước đây em chỉ nghĩ 1 sao là phản hồi chất lượng bình thường, nhưng thực tế nó là "án phạt sinh kế" tước đi toàn bộ tiền thưởng tuần và thưởng Tết của tài xế chỉ vì kẹt xe làm giao muộn.

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

Điều khó nhất với em là việc thiết lập Success Metric và Boundary (Ranh giới). Việc lượng hóa thành con số baseline và target đo lường được thì rất khó. Nhóm chỉ dám ước lượng

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

Phản biện mạnh hơn ở việc cách vấn đề được phát hiện, đo mức độ "đau" của người dùng.

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

---

## 7. Tài liệu tham khảo

1. **CURRENT STATUS OF WAITING TIME FOR CONSULTATION AND ROUTINE BLOOD TESTS AMONG OUTPATIENTS AT 103 MILITARY HOSPITAL IN 2024 (2024):  Ho La Quang1, Mai Le Thi Ngoc1, Thanh Nguyen Duy1, Phu Nguyen Van1, Anh Nguyen Thi Lan1**.
2. **Ardent Partners (2024):** Báo cáo tình hình xử lý hóa đơn phải trả (Accounts Payable Metrics Benchmark 2024 - thời gian xử lý trung bình 9,15 ngày/hóa đơn).
