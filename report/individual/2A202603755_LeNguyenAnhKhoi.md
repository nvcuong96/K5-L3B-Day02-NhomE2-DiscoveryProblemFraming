# Báo cáo cá nhân — 2A202603755_LeNguyenAnhKhoi

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Lê Nguyễn Anh Khôi
- MSSV: 2A202603755
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: E2
- Link repo nhóm: https://github.com/nvcuong96/K5-L3B-Day02-NhomE2-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Lặp lại | Khi tài xế khiếu nại đánh giá 1 sao do nguyên nhân khách quan (hỏng app, khách hủy phút chót), tôi muốn tự động đối chiếu logs chuyến đi để gỡ phạt KPI ngay, nhằm đảm bảo quyền lợi công bằng cho tài xế | Điều phối viên CSKH, Tài xế GSM | 35–45 phút/khiếu nại; trung bình 60–80 ca/ngày trên hệ thống; tồn đọng vé khiếu nại cuối tuần |
| 2 | Cần đọc, tổng hợp nhiều thông tin | Khi xe báo lỗi pin khẩn cấp (< 5%) trên đường, tôi muốn lập tức tra cứu vị trí xe sạc lưu động gần nhất và tình trạng trạm sạc khả dụng, để điều phối cứu hộ trong 15 phút | Điều phối viên tổng đài cứu hộ, Tài xế | Thao tác trên 3 hệ thống rời rạc (telematics, bản đồ sạc, danh sách xe cứu hộ); trung bình mất 12–18 phút chỉ để chốt phương án điều xe |
| 3 | Tốn thời gian | Khi khách hàng đưa xe vào xưởng dịch vụ với mô tả lỗi mơ hồ, tôi muốn phân loại sơ bộ mã lỗi OBD-II và linh kiện thay thế dự kiến, để phân làn kỹ thuật viên chính xác ngay từ đầu | Cố vấn dịch vụ (Service Advisor), Kỹ thuật viên xưởng | 25 phút tiếp nhận và tra cứu cẩm nang kỹ thuật/xe; 20% ca sửa chữa bị chuyển nhầm khoang dịch vụ |
| 4 | Pain từ người khác | Khi tài xế đối mặt với khách say xỉn hoặc quấy rối trên xe và ấn nút SOS, bộ phận an toàn muốn trích xuất ngay 30 giây ngữ cảnh âm thanh/vị trí trước đó, để đưa ra hỗ trợ khẩn cấp chuẩn quy trình | Nhân viên giám sát an toàn (Safety Team), Tài xế | 8–10 phút để tải log, mở camera/audio stream thủ công; tài xế hoang mang khi tín hiệu SOS phản hồi chậm |
| 5 | Lặp lại | Khi kết thúc ca trực, điều phối viên muốn tổng hợp số lượng xe hết pin trên đường và thời gian phản hồi trung bình theo khu vực, để gửi báo cáo vận hành sáng hôm sau | Trưởng ca điều phối (Ops Lead) | Mỗi ngày 40 phút tổng hợp thủ công từ Excel và tin nhắn nhóm Zalo/Telegram nội bộ |
| 6 | Cần đọc, tổng hợp nhiều thông tin | Khi tài xế nộp yêu cầu hoàn tiền phí cầu đường phát sinh ngoài app do khách đổi lộ trình, tôi muốn đối chiếu tự động hóa đơn ePass/VETC với tọa độ GPS trạm thu phí và thời gian cuốc xe, để duyệt hoàn tiền ngay trong ngày thay vì chờ đối soát cuối tháng | Nhân viên kế toán thanh toán đội xe (Driver Payout Ops), Tài xế | 12–15 phút/hồ sơ để tra cứu chéo lịch sử trừ tiền thẻ thu phí và log cuốc; tồn đọng 150–200 đơn/ngày vào cao điểm lễ/Tết; tài xế bị giam tiền túi 2–3 tuần |
| 7 | Tốn thời gian | Khi nhận cảnh báo xe điện bị sụt pin bất thường (pin tụt dốc nhanh dù tải nhẹ), tôi muốn trích xuất và phân tích nhanh chu kỳ sạc-xả cùng độ lệch điện áp/nhiệt độ cell pin từ telemetry, để xác định xe cần cân bằng pack pin hay thay cell trước khi lập lịch triệu hồi | Kỹ sư phân tích dữ liệu pin (Battery Fleet Engineer), Quản lý đội xe | Mất 35–45 phút tải, làm sạch và vẽ biểu đồ thủ công từ file log CSV thô cho mỗi xe; 15–20 ca nghi vấn/tuần; xe nằm bãi chờ chẩn đoán gây giảm tỷ lệ xe sẵn sàng hoạt động (fleet availability) |
| 8 | Pain từ người khác | Khi tài xế mới gặp sự cố trụ sạc không nhận súng hoặc báo lỗi giao tiếp CCS2 giữa đêm, tôi muốn hệ thống tự động đọc mã lỗi từ trụ và hướng dẫn quy trình reset/cắm lại chuẩn, để tài xế tự xử lý được trong 3 phút mà không phải gọi giục đội kỹ thuật trực đêm | Tài xế mới nhận xe, Kỹ sư trực hỗ trợ hạ tầng trạm sạc (Charging Support) | 15–20 cuộc gọi/đêm vào tổng đài hỗ trợ; tài xế chờ máy 10–15 phút trong trạng thái sốt ruột, xe cạn pin không kịp nạp cho ca đón khách sáng hôm sau |
| 9 | Lặp lại | Khi phát hiện xe taxi điện bật điều hòa đứng im quá 45 phút tại bãi đỗ công cộng, tôi muốn tự động kiểm tra trạng thái cuốc xe và gửi tin nhắn cảnh báo nhắc nhở tài xế tắt máy hoặc di chuyển đón khách, để hạn chế tiêu hao dung lượng pin vô ích và phòng ngừa rủi ro ngủ quên | Giám sát viên vận hành đội xe (Fleet Controller), Tài xế | Soi bản đồ và lọc thủ công từng xe dừng > 30 phút mất 90–120 phút mỗi ca trực; trung bình 50–70 lượt cảnh báo/ngày; lãng phí 3–5% dung lượng pin cao áp/xe/ca |
| 10 | Cần đọc, tổng hợp nhiều thông tin | Khi xảy ra sự cố va quẹt trên đường, tôi muốn gom tự động dữ liệu tốc độ xe trước va chạm (từ CAN bus), đoạn video camera hành trình tương ứng và tường trình ban đầu, để lập hồ sơ giám định bảo hiểm sơ bộ trong 30 phút thay vì chờ thu thập hiện trường nhiều ngày | Chuyên viên xử lý bảo hiểm & tai nạn (Insurance & Claims Specialist), Tài xế | Mất 2–3 ngày gom thủ công thẻ nhớ camera, trích xuất log tốc độ từ server và đơn viết tay; 20–30 vụ va chạm/tuần khiến xe phải lưu bãi chờ duyệt sửa chữa bình quân 5 ngày |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- **Ý AI gợi ý được giữ lại:** Thêm ý #2 (Cứu hộ sạc khẩn cấp khi pin < 5%) và mở rộng điều kiện ràng buộc ở ý #1 (đối chiếu log hành trình tự động). Lý do giữ: Đây là bài toán đặc thù của xe điện, có quy trình nghiệp vụ rõ ràng, dữ liệu telematics có sẵn và đo đếm được thời gian trễ thực tế.
- **Ý AI gợi ý bị loại bỏ:** AI gợi ý *"Trợ lý ảo AI tự động điều phối toàn bộ tài xế nhận cuốc theo thời gian thực để tối ưu doanh thu"*. Loại bỏ vì: Bài toán dispatch tổng thể thuộc về thuật toán tối ưu hóa vận trù học (Operations Research), phạm vi quá rộng, độ phức tạp hệ thống cực lớn, không xác định được bottleneck bước đơn lẻ và không phù hợp với phạm vi triển khai của một bài toán AI tập trung.

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Tự động phân loại và gỡ phạt đánh giá 1 sao oan cho tài xế (#1) | Quy trình xử lý khiếu nại rõ ràng; dữ liệu text phản hồi và telemetry có sẵn; tác động trực tiếp đến thu nhập tài xế và tỷ lệ rời bỏ nền tảng (churn rate) | Dữ liệu giải trình của tài xế và nhận xét của khách có đủ chi tiết để phân biệt lý do chủ quan hay khách quan không |
| 2 | Phân luồng điều phối cứu hộ sạc pin khẩn cấp cho xe < 5% (#2) | Pain point sống còn của xe điện; chi phí kéo xe cứu hộ vật lý rất cao; bottleneck nằm ở khâu tổng hợp dữ liệu 3 màn hình | Tính sẵn sàng của API xe sạc lưu động theo thời gian thực |
| 3 | Sơ loại mã lỗi và phân làn tiếp nhận dịch vụ xưởng (Service Triage) (#3) | Tiết kiệm thời gian cố vấn dịch vụ; giảm thời gian chờ đợi của khách; quy trình 7 bước chuẩn hóa | Mức độ phức tạp của các triệu chứng phi cấu trúc khi khách mô tả bằng lời nói |

---

### Problem Card #1: Tự động phân loại và gỡ phạt đánh giá 1 sao oan cho tài xế

| Trường | Nội dung |
|---|---|
| Job Story | Khi tài xế gửi khiếu nại về cuốc xe bị đánh giá 1 sao do nguyên nhân khách quan (hỏng app, kẹt xe đột xuất, khách giận vì lý do ngoài kiểm soát), tôi muốn tự động đối chiếu lý do khiếu nại với log chuyến đi và lịch sử chat/tổng đài, để phê duyệt gỡ phạt KPI công bằng trước chu kỳ chốt thưởng tuần |
| Actor | Nhân viên vận hành hỗ trợ tài xế (Driver Ops / CS Tier 2) |
| Thời điểm / bối cảnh | Hằng ngày, đặc biệt dồn tải vào thứ Bảy và Chủ Nhật trước kỳ đối soát thưởng tuần |
| Quy trình hiện tại (3–7 bước) | 1. Mở ticket khiếu nại từ app tài xế · 2. Tra cứu mã chuyến đi trên hệ thống quản lý cuốc xe · 3. Đọc phản hồi của khách hàng và lý do khiếu nại của tài xế · 4. Mở hệ thống viễn thông kiểm tra log GPS và thời gian chờ thực tế · 5. Đánh giá nguyên nhân lỗi (Chủ quan hay Khách quan) · 6. Cập nhật trạng thái miễn trừ phạt trên portal · 7. Gửi thông báo kết quả cho tài xế |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3 & Bước 5: Đọc, đối soát chéo văn bản khiếu nại với dữ liệu telemetry mất 20–25 phút/ticket do thông tin rời rạc |
| Impact (nếu không giải thì sao) | Tài xế bị trừ điểm thưởng tuần oan dẫn đến bức xúc, đình công hoặc chuyển sang nền tảng đối thủ; đội Ops tốn 40 giờ công/tuần cho việc duyệt thủ công |
| Success metric (baseline → target) | Thời gian xử lý 1 ticket giảm từ 35 phút xuống dưới 5 phút; Tỷ lệ tài xế khiếu nại lần 2 giảm từ 18% xuống dưới 5% |
| Phương án không dùng AI | Biểu mẫu Google Form/Jira chuẩn hóa bắt buộc đính kèm bằng chứng + Rule tự động gỡ phạt cho các cuốc hủy do khách (chỉ xử lý được các trường hợp có mã lỗi hệ thống rõ ràng, không đọc hiểu được nội dung chat hay lý do ngữ cảnh) |
| Giả thuyết về AI (nếu có) | AI (LLM trích xuất ngữ cảnh) đọc nội dung phản hồi của khách và giải trình của tài xế, đối chiếu với các trường dữ liệu GPS/thời gian chờ được trích xuất bằng Rule, sau đó đưa ra bản tóm tắt nguyên nhân và đề xuất [Gỡ phạt / Giữ nguyên / Cần người duyệt] |
| Cảm nhận nhanh | Workflow (Kết hợp Rule lấy dữ liệu + AI phân loại ngữ cảnh + Người duyệt xác nhận) |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 35 phút/ticket (7/7 bước thủ công)

[1 Mở ticket: 2'] → [2 Tra mã chuyến: 3'] 
→ [3 Đọc feedback & giải trình: 10'] 
→ [4 Mở hệ thống GPS check log: 10'] 
→ [5 Đối soát & ra quyết định: 5'] ← BOTTLENECK
→ [6 Cập nhật miễn trừ: 3'] → [7 Gửi thông báo: 2']
```

---

### Problem Card #2: Phân luồng điều phối cứu hộ sạc pin khẩn cấp cho xe < 5%

| Trường | Nội dung |
|---|---|
| Job Story | Khi xe điện báo động pin dưới 5% tại điểm chết trạm sạc, tôi muốn xác định ngay giải pháp tối ưu (điều hướng trụ sạc gần nhất hay điều xe sạc lưu động), để cứu hộ xe trước khi pin cạn về 0% làm hỏng cell pin |
| Actor | Điều phối viên tổng đài khẩn cấp (Emergency Dispatcher) |
| Thời điểm / bối cảnh | Bất kể thời điểm trong ngày khi nhận tín hiệu cảnh báo pin đỏ từ hệ thống quản lý đội xe |
| Quy trình hiện tại (3–7 bước) | 1. Nhận cảnh báo pin đỏ (< 5%) trên hệ thống quản lý đội xe · 2. Gọi điện xác nhận tình trạng xe với tài xế · 3. Mở bản đồ trạm sạc kiểm tra trụ trống trong bán kính 3km · 4. Kiểm tra vị trí và tình trạng sẵn sàng của xe cứu hộ sạc lưu động · 5. So sánh thời gian di chuyển giữa 2 phương án · 6. Điều xe cứu hộ hoặc hướng dẫn tài xế tới trụ · 7. Theo dõi hành trình cứu hộ |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3, 4 & 5: Tổng hợp dữ liệu từ 3 màn hình riêng biệt (vị trí xe, bản đồ trụ sạc, vị trí xe cứu hộ) mất 8–12 phút |
| Impact (nếu không giải thì sao) | Xe bị cạn kiệt pin giữa đường gây tắc đường, tài xế phải gọi xe cẩu kéo vật lý tốn 1.200.000 VNĐ/lần thay vì dùng sạc lưu động (300.000 VNĐ), tăng nguy cơ hỏng cụm pin cao áp |
| Success metric (baseline → target) | Thời gian ra quyết định điều phối giảm từ 15 phút xuống dưới 3 phút; Tỷ lệ cứu hộ thành công trước khi xe sập nguồn tăng từ 75% lên 95% |
| Phương án không dùng AI | Tích hợp bản đồ GPS hợp nhất hiển thị cả 3 thực thể trên 1 màn hình; xây dựng Rule cứng (nếu khoảng cách tới trụ trống < 1.5km thì tự gửi tọa độ trụ) |
| Giả thuyết về AI (nếu có) | AI tổng hợp dữ liệu giao thông thời gian thực, dung lượng pin còn lại, độ nghiêng quãng đường để đưa ra payload điều phối [dispatch_mobile_charger] hoặc [reroute_station] dạng JSON nháp cho điều phối viên ấn xác nhận |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 16 phút/ca cứu hộ

[1 Nhận alert pin đỏ: 1'] → [2 Gọi điện xác nhận: 3'] 
→ [3 Check trạm sạc: 4'] → [4 Check xe cứu hộ: 4'] 
→ [5 So sánh & chọn phương án: 3'] ← BOTTLENECK
→ [6 Phát lệnh điều phối: 1']
```

---

### Problem Card #3: Sơ loại mã lỗi và phân làn tiếp nhận dịch vụ xưởng (VinFast Service Triage)

| Trường | Nội dung |
|---|---|
| Job Story | Khi khách hàng mang xe điện đến bảo dưỡng/sửa chữa với mô tả lỗi kỹ thuật phức tạp, tôi muốn phân loại sơ bộ hệ thống lỗi và dự trù phụ tùng cần kiểm tra, để chỉ định đúng khoang kỹ thuật và chuẩn bị vật tư trước khi đưa xe lên cầu nâng |
| Actor | Cố vấn dịch vụ xưởng (Service Advisor) |
| Thời điểm / bối cảnh | Đầu giờ sáng (8h00–9h30) khi khách tập trung bàn giao xe tại xưởng |
| Quy trình hiện tại (3–7 bước) | 1. Tiếp nhận xe và nghe khách hàng mô tả hiện tượng · 2. Cắm máy chẩn đoán quét mã lỗi OBD-II · 3. Đọc kết quả quét và tra cứu cẩm nang kỹ thuật xưởng · 4. Phỏng vấn lại khách hàng về các dấu hiệu cảnh báo trên màn hình · 5. Lập phiếu dịch vụ và chỉ định khoang sửa chữa · 6. Bàn giao lệnh sửa chữa cho Tổ trưởng kỹ thuật |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3 & 4: Tra cứu tài liệu kỹ thuật và đối chiếu mã lỗi với mô tả triệu chứng của khách mất 15–20 phút |
| Impact (nếu không giải thì sao) | Khách chờ đợi lâu gây phàn nàn; điều phối nhầm sang khoang sửa chữa thông thường trong khi xe bị lỗi hệ thống truyền động điện cao áp (HV Battery/Inverter) dẫn đến ùn tắc xưởng |
| Success metric (baseline → target) | Thời gian lập phiếu tiếp nhận giảm từ 25 phút xuống dưới 10 phút/xe; Tỷ lệ chỉ định sai khoang kỹ thuật giảm từ 20% xuống dưới 3% |
| Phương án không dùng AI | Bảng tra cứu nhanh mã lỗi OBD-II phổ biến in sẵn tại bàn tiếp nhận + Biểu mẫu check-list cứng phân loại xe cơ bản |
| Giả thuyết về AI (nếu có) | AI phân tích mô tả hiện tượng dạng văn bản phi cấu trúc kết hợp với danh sách mã lỗi quét được, sinh phiếu tóm tắt đề xuất [Lỗi dự kiến, Phụ tùng cần kiểm tra, Khoang dịch vụ phù hợp] |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 25 phút/lượt tiếp nhận

[1 Nghe khách tả lỗi: 5'] → [2 Quét OBD-II: 3'] 
→ [3 Tra cứu cẩm nang kỹ thuật: 10'] ← BOTTLENECK
→ [4 Hỏi sâu triệu chứng: 4'] 
→ [5 Lập phiếu & xếp khoang: 3']
```

---

### Card muốn pitch nhất

- **Card số:** Card #1 — Tự động phân loại và gỡ phạt đánh giá 1 sao oan cho tài xế.
- **Vì sao:**
  1. Đây là bài toán có dữ liệu đầu vào dạng văn bản phi cấu trúc (khiếu nại của tài xế, bình luận của khách hàng) kết hợp số liệu định lượng (telemetry GPS, thời gian dừng đón), rất phù hợp với thế mạnh xử lý ngôn ngữ tự nhiên của LLM.
  2. Đo lường được ngay lập tức (thời gian xử lý vé khiếu nại, số lượng khiếu nại tồn đọng, tỷ lệ duyệt sai).
  3. Phạm vi can thiệp vừa sức cho bài toán lab: Thiết kế một workflow có sự kiểm duyệt của con người (Human-in-the-loop), không cần can thiệp sâu vào tầng điều khiển xe hay tính toán an toàn mạng cấp bách.
- **Câu hỏi muốn nhóm phản biện:** *"Nếu tài xế lợi dụng mẫu câu chuẩn để khai báo gian dối (ví dụ đổ lỗi do tắc đường hoặc lỗi app), làm thế nào để workflow AI kết hợp Rule kiểm tra chéo telemetry một cách khách quan mà không để lọt gian lận?"*

---

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Đề xuất để AI tự động bấm gỡ phạt trên portal mà không qua con người là quá mạo hiểm đối với chính sách thưởng | **Đồng ý** | Chuyển vai trò của AI thành **Augment**: AI chỉ trích xuất dữ liệu, tổng hợp đối chiếu và đề xuất gắn nhãn `[DRAFT_APPROVAL]`. Quyết định gỡ phạt cuối cùng thuộc về nhân viên Ops |
| Baseline 35 phút/ticket chỉ là con số ước chừng, chưa có bằng chứng số liệu | **Đồng ý một phần** | Bổ sung căn cứ vận hành thực tế: 1 ticket cần đối soát qua 3 màn hình nghiệp vụ (quản lý chuyến, telematics GPS, lịch sử tin nhắn), thời gian đọc và kiểm tra chéo trung bình ghi nhận thực tế từ ca trực là 20–25 phút |
| Không phải mọi cuốc 1 sao đều do lỗi khách quan, nếu dữ liệu văn bản quá ngắn (ví dụ khách chỉ chấm 1 sao không để lại bình luận) thì AI không thể suy luận | **Đồng ý** | Thêm điều kiện biên (Boundary): Nếu cuốc xe không có bình luận của khách và telemetry không phát hiện điểm bất thường (như app crash, xe dừng bất khả kháng), case đó được chuyển thẳng về luồng điều tra tiêu chuẩn, không đưa qua AI suy diễn |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Pitch 3 Problem Card cá nhân (#3, #6, #7 trong bảng chung); chủ động thuyết minh chọn bài #3 (Khiếu nại tài xế). | Bài #3 được nhóm đánh giá cao nhất về tính khả thi và được chọn làm Candidate Problem chung của nhóm (32/35 điểm). |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt:<br>- Hỏi Hiếu (#1 Tuyến đi lại): *"Hơn gì Google Maps?"*<br>- Hỏi Cường (#4 Khám bệnh): *"Nếu cả 2 phòng đều vắng thì ưu tiên phòng nào?"*<br>- Hỏi Hải (#10 Hoàn hàng): *"Nếu khách chụp ảnh sản phẩm khác hoặc góc mờ, AI dựa vào đâu phát hiện?"*<br>- Hỏi Hiếu (#12 Nhóm chat): *"Làm sao phân biệt thông báo chính thức với thảo luận bài tập?"* | Giúp các bạn nhìn ra các lỗ hổng biên (edge cases) và bẫy "No AI": nhận ra bài #1 và #12 có thể giải quyết tốt bằng Rule hoặc tính năng có sẵn; bài #10 thiếu bằng chứng xác thực. |
| Nhận phản biện | Câu hỏi tôi nhận được từ Hải:<br>*"Nếu tài xế lợi dụng mẫu câu chuẩn để khai báo gian dối (ví dụ đổ lỗi do tắc đường hoặc lỗi app), làm thế nào để workflow AI kết hợp Rule kiểm tra chéo telemetry một cách khách quan mà không để lọt gian lận?"* | Tôi đã sửa:<br>Bổ sung cơ chế đối chiếu chéo bắt buộc (Cross-check Flag): AI không chỉ đọc text khiếu nại mà phải yêu cầu Rule đối soát đồng thời vận tốc thực tế của telemetry GPS và mốc thời gian chat với khách trước khi tóm tắt. |
| Gom cluster / cây OST | Hỗ trợ Cường gom 12 candidate thành 3 cụm (Cluster A, B, C); tham gia bóc tách các ý tưởng solution-first trong cây OST rút gọn. | Tách bạch được pain point thực sự (vấn đề đọc/đối soát văn bản đa nguồn) ra khỏi các giải pháp công nghệ; xếp bài #3 vào Cluster B. |
| Chọn candidate problem | Phân tích ma trận chấm điểm 7 tiêu chí; bảo vệ tính khả thi của bài toán vận hành xe công nghệ trước bài AP Invoice (#8) và Cấp cứu (#11). | Thuyết phục cả nhóm chọn bài đối soát khiếu nại tài xế (#3) với điểm cao nhất (32 điểm) vì domain vừa sức lab, có dữ liệu telemetry rõ ràng và đo được ROI cụ thể. |
| Kiểm chứng / research | Hỗ trợ nhóm tìm kiếm và đối soát các bài phóng sự điều tra thực tế từ Báo Tuổi Trẻ, Người Quan Sát; tra cứu tài liệu quy chế Xanh SM / Grab và bài báo khoa học ACM (Rosenblat & Stark). | Cung cấp bằng chứng thực nghiệm và cơ sở học thuật vững chắc cho Assumption #1, #2; làm rõ nghịch lý "mất Tết vì 1 sao oan" của tài xế xe công nghệ. |
| Quy trình nhóm | Hỗ trợ Cường định lượng thời gian từng bước trong quy trình trước (6 bước, 20–25') và sau (4 bước, 5–6'); xác lập cơ chế Fallback. | Xác định chính xác 2 điểm nghẽn (Bước 3 & 4: mở 3 màn hình đối soát); thiết lập phương án fallback về tra cứu thủ công khi dữ liệu khuyết thiếu hoặc độ tin cậy < 80%. |
| Problem Statement | Là **người phụ trách chính Problem Statement v0**; sau đó phối hợp chốt Problem Statement v1 dựa trên góp ý phản biện. | Đưa ra bản v0 chuẩn hóa; tiếp thu phản biện của Hải để bổ sung 2 metric đo lường chất lượng phán quyết vào v1 (tỷ lệ tra lại log gốc < 20%, tỷ lệ khiếu nại lần 2 giảm ≥ 40%). |
| Mức can thiệp AI | Thảo luận cùng Cường và Hải trên ma trận Độ mơ hồ × Độ phức tạp; phân tích vì sao không chọn No AI, Rule hay Agent. | Thống nhất chọn mức **Workflow**: Rule gom và tính toán số liệu thô -> AI đọc hiểu ngữ cảnh & tóm tắt đối soát -> Con người (Driver Ops) giữ quyền quyết định cuối cùng (Human-in-the-loop). |
| Quyết định | Là **người phụ trách chính phần Quyết định CP6**: đánh giá 4 loại rủi ro (Value, Usability, Feasibility, Viability); thiết lập kế hoạch pilot 2 tuần và điều kiện dừng (Stop condition). | Đưa ra quyết định cuối cùng: **Go (phạm vi nhỏ / pilot workflow 50 ticket)** kèm 2 ngưỡng dừng nghiêm ngặt nếu tỷ lệ mở lại log > 35% hoặc xuất hiện ≥ 2 ca bỏ sót gian lận. |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Prompt AI brainstorm thêm các góc nhìn pain point đặc thù trong vận hành xe điện và quản lý tài xế công nghệ. | Gợi ý được bài toán khẩn cấp về pin xe điện (< 5%) và hướng đối chiếu chéo dữ liệu hành trình khiếu nại. | Gợi ý ý tưởng viển vông: *"Hệ thống AI tự động dispatch toàn bộ tài xế theo thời gian thực"*, mang tính giải pháp vĩ mô, không có điểm nghẽn cụ thể. | Loại bỏ ngay ý tưởng dispatch vĩ mô; chọn lọc và tinh chỉnh lại 5 Job Stories tập trung vào các mắt xích tác nghiệp cụ thể có đo lường được thời gian trễ. |
| CP2 Problem Card | Nhờ AI đóng vai trò phản biện (Devil's Advocate) để bóc tách rủi ro trong Problem Card #1. | Chỉ ra ngay rủi ro chí mạng: nếu để AI tự động bấm nút gỡ phạt trên portal thì rủi ro thất thoát ngân sách thưởng là cực lớn. | Ước lượng baseline thời gian xử lý thủ công rất hời hợt (cho rằng chỉ mất 3–5 phút đọc lướt text). | Bổ sung thực tế vận hành: nhân viên phải mở 3 màn hình (Helpdesk, Telematics GPS, Lịch sử Chat), mỗi ticket mất thực tế 20–25 phút; chuyển vai trò AI sang Augmentation (Human-in-the-loop). |
| CP4 Research | Dùng AI tra cứu cấu trúc giải pháp của Uber Michelangelo và Zendesk AI để so sánh mô hình xử lý. | Tóm tắt nhanh kiến trúc phát hiện gian lận của Uber và cơ chế ticket triage của Zendesk, tiết kiệm thời gian đọc tài liệu tiếng Anh. | Không nắm được thực tế bảo mật của hệ thống nội bộ GSM/Xanh SM; tự bịa (hallucinate) ra các API mở của Xanh SM vốn không có thật ngoài đời. | Ghi chú rõ hệ thống GSM là hệ thống đóng nội bộ; chuyển hướng kiểm chứng bằng phóng sự điều tra báo chí chính quy (Tuổi Trẻ, Người Quan Sát) và nghiên cứu học thuật của ACM. |
| CP5 Quy trình | Nhờ AI sinh sơ đồ dạng text (ASCII art) cho quy trình trước/sau 6 bước → 4 bước. | Tạo khung sơ đồ trực quan nhanh, phân định rõ ràng giữa các khối xử lý. | AI tự động gộp luôn bước số 3 (Ops duyệt) vào AI, biến thành quy trình tự động hoàn toàn mà không có con người kiểm duyệt. | Tách riêng bước 3 thành nhiệm vụ bắt buộc của Driver Ops; viết rõ ranh giới Boundary (AI không được bấm duyệt) và cơ chế Fallback khi độ tin cậy < 80%. |
| CP5–6 Problem Statement | Sử dụng AI để rà soát câu chữ của Problem Statement v0 xem đã chuẩn cấu trúc và ngữ nghĩa chưa. | Gợi ý làm rõ việc AI nhận dữ liệu GPS thô hay dữ liệu đã qua tiền xử lý, giúp định hình rõ vai trò của Rule. | Success metric ban đầu do AI gợi ý chỉ tập trung vào tốc độ (giảm từ 22' xuống 6'), vô tình tạo kẽ hở cho việc nhân viên duyệt ẩu để chạy KPI. | Viết lại bảng Problem Statement v1: bổ sung metric kiểm soát chất lượng (tỷ lệ tra lại log gốc < 20%, tỷ lệ khiếu nại lần 2 giảm ≥ 40%) và bổ sung 4 tiêu chí đánh giá đầu ra khắt khe. |
| CP6 Mức can thiệp / quyết định | Tham khảo AI về các tiêu chí đánh giá rủi ro (Risk Assessment Framework) và thiết kế kịch bản pilot. | Gợi ý cấu trúc 4 loại rủi ro (Value, Usability, Feasibility, Viability) và cách xây dựng kịch bản thử nghiệm đối chứng (A/B testing trên 50 ticket cũ). | Ngưỡng dừng (Stop condition) AI đề xuất rất chung chung: *"Dừng lại nếu người dùng không hài lòng"*, không thể định lượng để ra quyết định. | Tự thiết lập 2 ngưỡng dừng định lượng tuyệt đối: tỷ lệ mở lại log vượt quá 35% hoặc phát hiện ≥ 2 trường hợp bỏ sót gian lận thì lập tức dừng pilot. |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

Khi lắng nghe phần trình bày top 3 problems của các bạn trong nhóm, bài học lớn nhất mà tôi rút ra được là ranh giới rất mong manh giữa một "vấn đề gây khó chịu thực sự" (real acute pain) và một "sự bất tiện thoáng qua" (minor inconvenience). Ban đầu, khi nghe Hiếu trình bày ý tưởng so sánh phương tiện xe máy và xe buýt đến trường (#1) hay bot lọc tin nhắn nhóm lớp (#12), tôi thấy những bài toán này rất gần gũi với đời sống sinh viên hằng ngày. Tuy nhiên, khi đào sâu phân tích theo lăng kính vận hành, tôi nhận ra mức độ "đau" của chúng chưa đủ sâu: người dùng hoàn toàn có thể bỏ ra thêm 1–2 phút bật Google Maps hoặc dùng tính năng ghim tin nhắn của Zalo/Telegram là đã giải quyết được cơ bản vấn đề. Đối với bài toán của Cường về xếp hàng khám bệnh viện (#4) hay bài toán của Hải về rà soát hợp đồng thuê nhà (#2), tính cấp thiết cao hơn. Tuy nhiên, bài của Cường lại vướng vào điểm nghẽn phân luồng phụ thuộc hoàn toàn vào quy trình vật lý và quyền chỉ định chuyên môn của bác sĩ tiếp nhận, điều mà AI từ bên ngoài không thể can thiệp được. Từ đó, tôi nhận thức sâu sắc rằng một bài toán AI tiềm năng không chỉ cần sự xuất hiện của dữ liệu hay công nghệ hiện đại, mà quan trọng nhất là phải có một quy trình nghiệp vụ lặp đi lặp lại đủ nhiều, có người gánh chịu hậu quả tài chính hoặc áp lực công việc trực tiếp (như tài xế mất tiền thưởng, nhân viên CS trực ca đêm kiệt sức), và có một nút thắt cổ chai nhận thức (cognitive bottleneck) mà các công cụ thông thường không thể tự động hóa được.

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

Nhóm tôi gặp phải tình trạng "solution-first" khá rõ nét ngay trong buổi thảo luận CP3 khi các thành viên bắt đầu pitch ý tưởng cá nhân, điển hình nhất là trường hợp của Hải với đề tài rà soát hợp đồng thuê nhà cho sinh viên. Khi bước lên trình bày, thay vì phân tích cặn kẽ hành vi và rào cản tâm lý của người đi thuê trọ, Hải lại dành phần lớn thời gian say sưa mô tả giải pháp kỹ thuật: bạn dự định ứng dụng một mô hình ngôn ngữ lớn (LLM) để tự động đọc toàn bộ file hợp đồng, trích xuất các điều khoản bất lợi và đưa ra cảnh báo rủi ro pháp lý cho sinh viên. Nghe qua thì thấy công nghệ rất tân tiến, nhưng lúc đó Cường đã lập tức ngắt lời và đặt một câu hỏi phản biện rất thẳng thắn: "Giải pháp này hơn gì việc người dùng tự copy văn bản ném vào ChatGPT?".Câu hỏi đó như một gáo nước lạnh khiến cả nhóm sững lại. Chúng tôi cùng ngồi lại chất vấn chéo: Nỗi đau thật sự của sinh viên nằm ở đâu? Có nghiêm trọng đến mức họ phải cần một công cụ chuyên biệt hay không? Nhóm nhận ra mình đang mắc bẫy kinh điển: nghĩ ra một giải pháp công nghệ hào nhoáng trước rồi mới đi tìm bài toán để gán ghép vào. Bản thân tôi cũng thấy đề xuất này thiếu một quy trình nghiệp vụ cố định và chưa rõ ranh giới can thiệp của AI. Sau khi nhận diện sự lệch hướng, nhóm đã yêu cầu Hải tạm gác lại ý tưởng về "công cụ AI" để quay về bóc tách đúng bản chất vấn đề: sinh viên thiếu kiến thức pháp lý và thường bị quá tải tâm lý khi phải tự đọc dò các điều khoản phạt cọc ẩn trong hợp đồng. Việc này đã giúp chúng tôi có cái nhìn tỉnh táo hơn để sau đó hội tụ vào một bài toán vận hành có nút thắt thực tế rõ ràng hơn.


**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

Tôi đã hoàn toàn đổi ý sau khi nhận được câu hỏi phản biện rất sắc bén từ Hải ở CP2 và CP3. Ban đầu, tôi khá tự tin với ý tưởng tự động hóa mạnh mẽ: tôi kỳ vọng AI có thể đọc giải trình của tài xế, nếu thấy hợp lý thì hệ thống sẽ tự động gỡ phạt đánh giá 1 sao ngay trên cổng portal để giải phóng 100% sức lao động cho nhân viên CS. Tuy nhiên, Hải đã đặt một câu hỏi làm tôi khựng lại: *"Nếu tài xế nắm được kịch bản kiểm tra của AI rồi dùng mẫu câu chuẩn để khai báo gian dối (ví dụ đổ lỗi do kẹt xe hoặc mạng yếu), làm thế nào để workflow AI kết hợp Rule kiểm tra chéo telemetry một cách khách quan mà không để lọt gian lận?"*. Câu hỏi này đã đánh trúng "tử huyệt" trong thiết kế ban đầu của tôi. Tôi nhận ra mình đã quá ngây thơ khi tin vào sự trung thực tuyệt đối của văn bản giải trình. Trong thực tế vận hành nền tảng gọi xe, có những tài xế cố tình tắt ứng dụng, tấp vào quán nước nghỉ ngơi hoặc chạy đơn ngoài cho nền tảng đối thủ, sau đó khiếu nại đổ lỗi cho kẹt xe để xin gỡ sao nhằm ăn trọn tiền thưởng tuần. Nếu trao quyền duyệt tự động cho AI, doanh nghiệp sẽ đối mặt với nguy cơ thất thoát ngân sách thưởng rất lớn và tạo ra sự bất công nghiêm trọng cho những tài xế trung thực. Sau phản biện của Hải, tôi đã thay đổi hoàn toàn tư duy thiết kế: kiên quyết chuyển bài toán từ "Automate" (Tự động hóa hoàn toàn) sang "Augment" (Hỗ trợ ra quyết định), thiết lập ranh giới Boundary cấm AI bấm duyệt, và bắt buộc bổ sung cơ chế Rule tiền xử lý để so khớp vận tốc thực tế của GPS với thời gian gửi tin nhắn trước khi cấp dữ liệu cho LLM tổng hợp.

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

Quá trình kiểm chứng ở CP4 mang lại cho tôi hai sự bất ngờ rất lớn, làm thay đổi góc nhìn lý thuyết sách vở của tôi về thực tế vận hành. Điều bất ngờ đầu tiên là mức độ nghiêm trọng và sự khắc nghiệt của đánh giá 1 sao đối với đời sống tài xế công nghệ khi tôi đọc các bài phóng sự điều tra chuyên sâu của Báo Tuổi Trẻ và Người Quan Sát. Trước đây, tôi chỉ nghĩ 1 sao là một chỉ số phản ánh dịch vụ thông thường, bị trừ một chút điểm thì chạy bù cuốc khác là xong. Nhưng thực tế điều tra cho thấy, chỉ vì một đánh giá 1 sao do khách trút giận (kẹt xe đường dài, tài xế không chịu leo lề hay vượt đèn đỏ theo ý khách), điểm đánh giá trung bình của tài xế bị tụt xuống dưới ngưỡng 4.85, khiến họ bị cắt sạch toàn bộ tiền thưởng tuần và thưởng Tết lên đến hàng triệu đồng - được phóng sự ví như "mất Tết". Nghịch lý ở chỗ: thuật toán phạt trừ điểm của hệ thống diễn ra tự động và tàn nhẫn trong tích tắc, nhưng quy trình khiếu nại để minh oan cho tài xế lại quá chậm chạp, kéo dài từ 3 đến 5 ngày khiến họ phải chịu phạt oan trước kỳ chốt sổ. Điều bất ngờ thứ hai là rào cản kỹ thuật thực tế: toàn bộ dữ liệu telemetry và hệ thống quản lý điều hành của các hãng như Xanh SM (GSM) hay Grab đều là hệ thống đóng bảo mật cao, không hề có các API mở sẵn có để AI cắm vào tùy tiện như tôi tưởng tượng lúc đầu. Điều này buộc nhóm phải điều chỉnh phạm vi giải pháp: thiết kế mô hình dưới dạng một add-on workflow nội bộ trích xuất dữ liệu gián tiếp, chứ không thể mơ mộng can thiệp trực tiếp vào mã nguồn hay hệ thống core của hãng xe.

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

Điều khó nhất và khiến tôi cùng nhóm phải tranh luận, chỉnh sửa nhiều lần nhất khi viết Problem Statement chính là việc định nghĩa các **Success Metrics** và thiết lập **Boundary (Ranh giới)** sao cho không tạo ra hệ quả tiêu cực ngoài ý muốn (perverse incentives). Ở bản thảo Problem Statement v0, tôi viết metric rất đơn giản theo thói quen: "Giảm thời gian xử lý khiếu nại trung bình từ 22 phút xuống dưới 6 phút/ticket". Nghe qua thì thấy rất thuyết phục về mặt năng suất. Nhưng sau khi thảo luận kỹ, chúng tôi nhận ra chỉ số này cực kỳ nguy hiểm: nếu chỉ đo tốc độ, nhân viên CS sẵn sàng lướt thật nhanh qua bản tóm tắt của AI rồi bấm phê duyệt bừa bãi để đạt KPI về thời gian của ca trực, dẫn đến việc bỏ lọt hàng loạt tài xế gian lận. Cái khó là làm sao cân bằng được giữa "tốc độ xử lý" và "chất lượng phán quyết". Chúng tôi đã phải viết lại bản v1, bổ sung thêm các chỉ số chặn: Tỷ lệ nhân viên CS phải mở lại log thô tra cứu thủ công phải nhỏ hơn 20% (để đảm bảo AI tóm tắt đủ bằng chứng tin cậy) và Tỷ lệ tài xế khiếu nại lại lần 2 phải giảm tối thiểu 40% (chứng minh quyết định đưa ra là chính xác, không gây oan ức kéo dài). Thêm vào đó, việc vạch rõ ranh giới: AI chỉ được trích xuất dữ liệu thực tế (Facts), không được suy diễn lý do chủ quan nằm ngoài log, là một thách thức lớn trong việc đóng khung phạm vi trách nhiệm của mô hình ngôn ngữ lớn.

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

Nếu có cơ hội thực hiện lại dự án từ đầu, điều đầu tiên tôi muốn thay đổi là chủ động chuẩn bị sớm một bộ dữ liệu giả lập (mock telemetry dataset) chuẩn hóa ngay từ Checkpoint 2. Việc thiếu một tập log dữ liệu thực tế có cấu trúc (gồm tọa độ GPS, thời gian dừng đỗ, tin nhắn chat và nội dung khiếu nại) ở các bước đầu đã khiến nhóm mất khá nhiều thời gian tranh cãi trừu tượng về việc AI có thể làm được gì và không làm được gì. Nếu có ngay tập dữ liệu mẫu trong tay, chúng tôi có thể đưa thẳng vào LLM để kiểm chứng tính xác thực ngay từ đầu mà không cần phải đoán mò. Điểm thứ hai là tôi sẽ phản biện nhóm mạnh mẽ và quyết liệt hơn ở giai đoạn CP3 khi chấm điểm shortlist: tôi sẽ kiên quyết yêu cầu nhóm loại bỏ ngay từ đầu các đề xuất giải pháp thiếu dữ liệu kiểm chứng độc lập hoặc quá nhạy cảm về rủi ro đạo đức/pháp lý (như bài toán phân loại bệnh nhân cấp cứu #11 hay hóa đơn kế toán doanh nghiệp #8). Nhóm đã tốn mất gần 45 phút tranh luận giằng co giữa bài toán kế toán AP và bài toán khiếu nại tài xế, trong khi rõ ràng không có thành viên nào trong nhóm có nghiệp vụ kế toán chuyên sâu để thẩm định tính khả thi của quy trình 3-way matching. Nếu tôi phản biện dứt khoát hơn dựa trên tiêu chí Domain hiểu biết của nhóm, chúng tôi đã có thể dồn trọn vẹn thời gian đó để tối ưu hóa quy trình tương lai và thiết kế kịch bản pilot chi tiết hơn cho bài toán tài xế.

**6.7. Hiểu bài:**

Nhóm giải quyết vấn đề nhân viên Driver Ops mất 20–25 phút đối soát thủ công qua 3 màn hình rời rạc để xử lý khiếu nại 1 sao của tài xế trước hạn chốt thưởng tuần. Quy trình mới chuyển đổi từ 6 bước thủ công thành 4 bước tích hợp: Rule tự động gom dữ liệu log GPS và đoạn chat theo mã chuyến, AI đọc hiểu ngữ cảnh để sinh Bản tóm tắt bằng chứng 150 từ và gắn cờ nghi vấn, sau đó Driver Ops đọc duyệt và Rule tự động cập nhật hệ thống. Metric thành công cốt lõi là rút ngắn thời gian xử lý xuống dưới 6 phút/ticket, đảm bảo tỷ lệ hoàn thành đúng hạn đạt ≥ 98%, đồng thời tỷ lệ phải mở lại log gốc < 20% và tỷ lệ khiếu nại lần 2 giảm ≥ 40%. Boundary tuyệt đối là AI không bao giờ được tự ý bấm duyệt gỡ phạt hay chỉnh sửa điểm thưởng, quyền quyết định 100% thuộc về con người (Human-in-the-loop). Nhóm chọn mức can thiệp là **Workflow** vì quy trình nghiệp vụ mang tính cố định, AI đóng vai trò hỗ trợ nhận thức (Augment) để xử lý ngôn ngữ tự nhiên còn Rule xử lý số liệu cứng. Quyết định cuối cùng là **Go với phạm vi pilot nhỏ (50 ticket trong 2 tuần)**, kèm ngưỡng dừng nghiêm ngặt nếu tỷ lệ mở lại log gốc vượt quá 35% hoặc phát hiện ≥ 2 trường hợp bỏ lọt gian lận thì lập tức dừng để quay về phương án No AI cải tiến giao diện.

---

## 7. Tài liệu tham khảo

1. **Báo Tuổi Trẻ Online:** *"Tài xế thời kẹt xe: Đơn nhiều, giao chẳng được bao nhiêu"* — [`https://tuoitre.vn/tai-xe-thoi-ket-xe-don-nhieu-giao-chang-duoc-bao-nhieu-20250114115250949.htm`](https://tuoitre.vn/tai-xe-thoi-ket-xe-don-nhieu-giao-chang-duoc-bao-nhieu-20250114115250949.htm)
2. **Báo Người Quan Sát:** *"Tài xế xe ôm công nghệ: Chấp nhận khách đánh giá 1 sao, còn hơn ‘mất Tết’"* — [`https://nguoiquansat.vn/tai-xe-xe-om-cong-nghe-chap-nhan-khach-danh-gia-1-sao-con-hon-mat-tet-192562.html`](https://nguoiquansat.vn/tai-xe-xe-om-cong-nghe-chap-nhan-khach-danh-gia-1-sao-con-hon-mat-tet-192562.html)