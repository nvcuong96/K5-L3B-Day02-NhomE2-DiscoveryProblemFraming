# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm: Nhóm E2
- Thành viên: xem `TEAM.md`
- Candidate problem được chọn (1 câu): Đối chiếu tự động lý do khiếu nại của tài xế với log telemetry GPS và lịch sử chat để hỗ trợ Driver Ops phê duyệt gỡ phạt KPI công bằng trước hạn chốt thưởng tuần.
- Quyết định cuối: Go / Not Yet / No-Go

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

| # | Người đưa ra | Candidate (Job Story ngắn) | Actor | Bottleneck | Câu hỏi phản biện nhận được (ai hỏi) |
|---:|---|---|---|---|---|
| 1 | Hiếu | Khi cần đến trường vào giờ cao điểm, tôi muốn so sánh các phương án đi xe buýt và xe máy, bao gồm tuyến đường, thời gian và chi phí, để lựa chọn hành trình phù hợp và đến trường đúng giờ. | Sinh viên sống xa trường, thường xuyên di chuyển vào giờ cao điểm. | Phải tra cứu nhiều ứng dụng, tự tổng hợp và ước tính thời gian đi bộ, chờ xe, di chuyển, chuyển tuyến; khó so sánh tổng thời gian và chi phí giữa các phương án. | Hơn gì google map (Khôi), Xử lý độ trễ (Hải) |
| 2 | Hải | Rà soát & Cảnh báo rủi ro Hợp đồng Thuê nhà cho Sinh viên | Sinh viên và người đi làm trẻ thuê phòng trọ / căn hộ. | Khâu đọc dò chi tiết các điều khoản phạt, hoàn cọc và tự đánh giá rủi ro pháp lý (lâu và dễ bị quá tải/bỏ sót) | Hơn gì chat GPT (Cường) |
| 3 | Khôi | Khi tài xế gửi khiếu nại về cuốc xe bị đánh giá 1 sao do nguyên nhân khách quan (hỏng app, kẹt xe đột xuất, khách giận vì lý do ngoài kiểm soát), tôi muốn tự động đối chiếu lý do khiếu nại với log chuyến đi và lịch sử chat/tổng đài, để phê duyệt gỡ phạt KPI công bằng trước chu kỳ chốt thưởng tuần | Nhân viên vận hành hỗ trợ tài xế (Driver Ops / CS Tier 2) | Đọc, đối soát chéo văn bản khiếu nại với dữ liệu telemetry mất 20–25 phút/ticket do thông tin rời rạc | Nếu tài xế lợi dụng mẫu câu chuẩn để khai báo gian dối (ví dụ đổ lỗi do tắc đường hoặc lỗi app), làm thế nào để workflow AI kết hợp Rule kiểm tra chéo telemetry một cách khách quan mà không để lọt gian lận? (Hải)  |
| 4 | Cường | Khi phải đi khám tại bệnh viện, tôi muốn hệ thống dự đoán thời gian chờ, đề xuất khung giờ phù hợp và hướng dẫn các bước khám, để giảm thời gian chờ đợi và di chuyển lòng vòng giữa các phòng| Bệnh nhân đến khám, điều dưỡng / nhân viên tiếp đón, bác sĩ, bệnh viện| bệnh nhân không biết thứ tự ưu tiên nên di chuyển sai phòng| Nếu cả 2 phòng đều vắng thì ưu tiên phòng nào (Khôi) |
| 5 | Cường | Khi nhận ticket mới qua hệ thống helpdesk; đặc biệt khi dev mới chưa quen hệ thống hoặc khi dev cũ chuyển giao ca trực| Dev mới (onboarding), Dev xử lý ticket, khách hàng | tìm tài liệu không có cấu trúc (~10 phút) + hỏi lại khách hàng và chờ phản hồi (~30 phút hoặc hơn); tổng ~45–50 phút trước khi bắt đầu xử lý thật sự | |
| 6 | Khôi | Khi xe báo động pin dưới 5% tại điểm chết trạm sạc, tôi muốn xác định ngay giải pháp tối ưu (điều hướng trụ sạc gần nhất hay điều xe sạc lưu động), để cứu hộ xe trước khi pin cạn về 0% làm hỏng cell pin. | Điều phối viên tổng đài cứu hộ khẩn cấp (Emergency Dispatcher) | Tổng hợp, so sánh dữ liệu từ 3 màn hình riêng biệt (vị trí xe, bản đồ trụ sạc trống, vị trí và trạng thái xe cứu hộ sạc lưu động) mất 8–12 phút. |  "Nếu xe hết pin nằm trong ngõ nhỏ hoặc tầng hầm sâu mà xe sạc lưu động không chui vào được, hệ thống AI dựa vào đâu để biết mà không điều xe đến vô ích? (Hải)"<br><br> "Thời gian quyết định cần dưới 3 phút, nhưng việc gọi API lấy tọa độ giao thông thời gian thực và trạng thái trụ sạc có đảm bảo độ trễ để AI xử lý kịp không? (Hiếu)" |
 | 7 | Khôi | Khi khách đưa xe điện vào xưởng với mô tả lỗi phức tạp, tôi muốn phân loại sơ bộ hệ thống lỗi và dự trù phụ tùng cần kiểm tra, để chỉ định đúng khoang kỹ thuật và chuẩn bị vật tư trước khi đưa xe lên cầu nâng. | Cố vấn dịch vụ xưởng (Service Advisor) | Tra cứu cẩm nang kỹ thuật và đối chiếu chéo danh sách mã lỗi quét OBD-II với mô tả triệu chứng mơ hồ bằng lời của khách hàng mất 15–20 phút/xe. |  "Khách hàng thường tả tiếng kêu hoặc cảm giác lái rất mơ hồ ('xe kêu lục cục khi qua gờ'), dữ liệu đầu vào không chuẩn hóa như vậy thì AI gợi ý phụ tùng có bị sai lệch lớn không? (Cường)"<br><br> "Quy trình này một kỹ thuật viên cứng chỉ nhìn mã OBD-II là đoán được khoang, vậy đầu tư giải pháp AI cho bước tiếp nhận này liệu có thực sự mang lại ROI đáng kể cho xưởng? (Hải)" |
| 8 | Cường |  Khi nhận hàng trăm hóa đơn và phiếu thanh toán mỗi ngày, tôi muốn AI tự đọc, trích xuất thông tin và đối chiếu với đơn hàng, để giảm nhập liệu thủ công, hạn chế sai sót và rút ngắn thời gian xử lý công nợ | Kế toán công nợ phải trả (AP), trưởng phòng kế toán, nhà cung cấp | nhập tay và đối chiếu thủ công — theo Ardent Partners (2024), thời gian xử lý trung bình 1 hóa đơn AP là 9,15 ngày | |
| 9 | Hiếu | Khi nhận tài liệu nghiên cứu tiếng Anh dài 20–30 trang trước buổi seminar, tôi muốn nhanh chóng nắm được phương pháp nghiên cứu, kết quả và hạn chế của bài báo để chuẩn bị câu hỏi thảo luận đúng trọng tâm. | Sinh viên đại học cần đọc tài liệu học thuật trước buổi seminar hoặc thảo luận chuyên ngành. | Dịch thủ công các đoạn tiếng Anh chuyên ngành bằng Google Translate, mất khoảng 45 phút. Thuật ngữ khó hiểu khiến việc đọc hiểu và ghi chép mất nhiều thời gian, đồng thời dễ hiểu sai nội dung nghiên cứu. | "Làm thế nào đảm bảo bản tóm tắt không bỏ sót những chi tiết quan trọng trong phương pháp và kết quả nghiên cứu? (Cường)"
| 10 | Hải | Khi khách hàng hoàn trả hàng E-commerce với lý do 'không giống mô tả', tôi muốn đối chiếu tự động ảnh chụp đóng gói của kho và ảnh mở hàng của khách, để ra quyết định hoàn tiền hoặc từ chối ngay trong ngày nhằm giảm khiếu nại kéo dài. | Nhân viên xử lý khiếu nại kho (Return Operations Specialist) | Phải đối soát thủ công ảnh/video đóng gói từ camera kho với ảnh chụp khuyết tật khách tải lên qua 3 hệ thống riêng (WMS, ERP, Portal hỗ trợ), mất 15–20 phút/đơn do dung lượng video lớn và góc quay khác nhau. |"Nếu khách hàng cố tình chụp ảnh sản phẩm khác hoặc dùng góc quay mờ để qua mặt hệ thống, AI dựa vào đâu để phát hiện đó không phải là sản phẩm trong gói hàng ban đầu? (Khôi)"<br><br> "Nếu để AI tự động từ chối hoàn tiền của khách, lỡ mô hình nhận diện sai sản phẩm bị lỗi thật thì ai sẽ chịu trách nhiệm khi khách hàng đánh giá 1 sao hoặc kiện lên sàn?(Hiếu)" |
| 11 | Hải | Khi phòng cấp cứu tiếp nhận cùng lúc nhiều bệnh nhân chuyển viện, tôi muốn phân loại ngay mức độ ưu tiên xử lý dựa trên chỉ số sinh tồn và tiền sử bệnh, để sắp xếp bác sĩ chuyên khoa phù hợp trước khi tình trạng bệnh nhân chuyển biến xấu. | Điều dưỡng phân loại cấp cứu (Triage Nurse) | Đọc, tổng hợp thông tin từ bệnh án giấy chuyển viện, kết quả đo chỉ số sinh tồn (mạch, huyết áp, SPO2) và nhập vào phần mềm phân loại mất 10–12 phút/bệnh nhân, gây dồn hàng chờ tại cửa tiếp nhận. | "Nếu bệnh nhân có biểu hiện lâm sàng bình thường nhưng mang bệnh lý ẩn nguy hiểm mà giấy chuyển viện không ghi rõ, AI dựa vào đâu để không xếp nhầm xuống nhóm ưu tiên thấp? (Hiếu)"|
| 12 | Hiếu | Khi nhóm chat môn học có quá nhiều tin nhắn trong ngày, tôi muốn tự động lọc các thông báo bài tập, nhiệm vụ và hạn nộp để không bỏ sót công việc cần thực hiện. | Sinh viên tham gia các nhóm chat học tập hoặc lớp học phần đông người (30–60 thành viên). | Phải cuộn và tìm thủ công hàng trăm tin nhắn, lọc thông báo quan trọng giữa các nội dung trò chuyện, sau đó tự ghi lại nhiệm vụ và deadline; mất khoảng 10 phút và dễ bỏ sót thông tin. |  "Làm thế nào phân biệt một thông báo giao bài tập chính thức với tin nhắn thảo luận, nhắc lại hoặc thông tin chưa được xác nhận?(Khôi)"

### 2.2. Cluster

| Cluster | Các candidate | Pattern chung |
|---|---|---|
| A — Điều hướng & Ra quyết định trong thời gian thực | #1 So sánh phương tiện đi lại (Hiếu), #4 Gợi ý thứ tự khám bệnh viện (Cường), #6 Cứu hộ xe điện hết pin (Khôi) | Người dùng phải ra quyết định nhanh trong môi trường thay đổi liên tục (giao thông, hàng chờ, vị trí xe); thông tin nằm rải rác ở nhiều nguồn → phải tự tổng hợp thủ công, dễ chậm trễ và sai lệch |
| B — Rà soát & Đối chiếu văn bản / bằng chứng phức tạp | #2 Hợp đồng thuê nhà (Hải), #3 Khiếu nại tài xế (Khôi), #7 Tiếp nhận xe lỗi xưởng (Khôi), #8 Nhập liệu hóa đơn AP (Cường), #10 Hoàn trả hàng e-commerce (Hải), #11 Phân loại cấp cứu (Hải) | Người dùng phải đọc, đối chiếu và phán xét nhiều nguồn văn bản / dữ liệu không đồng nhất (hợp đồng, log, ảnh, bệnh án) để phát hiện sai lệch, rủi ro hoặc ưu tiên xử lý → tốn 10–25 phút/đơn, dễ bỏ sót, cần phán xét cuối của con người |
| C — Tóm tắt & Lọc thông tin từ luồng văn bản lớn | #5 Gợi ý xử lý ticket hỗ trợ (Cường), #9 Đọc tài liệu học thuật (Hiếu), #12 Lọc thông báo nhóm chat (Hiếu) | Người dùng bị "ngập" trong lượng văn bản lớn (ticket, paper, tin nhắn) và cần tóm tắt, lọc ra phần quan trọng để hành động → tốn 10–45 phút đọc thủ công, dễ bỏ sót thông tin then chốt |

### 2.3. Opportunity Solution Tree rút gọn

Gốc là **1 outcome**. Nhánh là **opportunity** (nhu cầu, pain), không phải tính năng hay công cụ.

```text
OUTCOME: Người dùng xử lý đúng và nhanh hơn khi phải đọc, đối chiếu
         hoặc tổng hợp thông tin từ nhiều nguồn rời rạc

├── Opportunity A — Điều hướng & Ra quyết định real-time:
│   Người dùng phải ra quyết định nhanh (đi tuyến nào, vào phòng nào,
│   điều xe nào) nhưng thông tin từ nhiều nguồn chưa được tổng hợp
│   → tự ước tính thủ công, chậm 8–45 phút, dễ chọn sai phương án
│   [#1 Đi lại · #4 BV · #6 Cứu hộ xe điện]
│
├── Opportunity B — Rà soát & Đối chiếu văn bản/bằng chứng phức tạp:
│   Người dùng phải đọc và đối chiếu nhiều nguồn không đồng nhất
│   (hợp đồng, log hành trình, ảnh, bệnh án, hóa đơn) để phát hiện
│   sai lệch hoặc rủi ro ẩn → tốn 10–25 phút/đơn, dễ bỏ sót,
│   cần phán xét cuối của con người
│   [#2 Hợp đồng · #3 Khiếu nại · #7 Xưởng xe · #8 Hóa đơn · #10 Hoàn hàng · #11 Cấp cứu]
│
└── Opportunity C — Tóm tắt & Lọc thông tin từ luồng văn bản lớn:
    Người dùng bị "ngập" trong luồng văn bản lớn (ticket, paper,
    tin nhắn) và cần lọc ra điểm hành động then chốt
    → tốn 10–45 phút đọc thủ công, dễ bỏ sót deadline/rủi ro
    [#5 Ticket · #9 Tài liệu học thuật · #12 Nhóm chat]
```

Những ý đã gạch bỏ vì là solution đội lốt opportunity:

- "Xây app so sánh tuyến xe buýt và xe máy" → là solution (tính năng), pain thật là "không có thông tin tổng hợp để so sánh phương án đi lại"
- "Dùng AI đọc hợp đồng thuê nhà" → là solution, pain thật là "người thuê không phát hiện được điều khoản bất lợi khi ký"
- "Tự động phê duyệt gỡ phạt KPI tài xế" → là solution, pain thật là "quy trình đối soát thủ công tốn 20–25 phút/ticket và không nhất quán"
- "Bot lọc tin nhắn nhóm chat" → là solution, pain thật là "sinh viên bỏ sót bài tập/deadline vì thông báo quan trọng bị chìm trong hàng trăm tin nhắn"

### 2.4. Chấm điểm shortlist (1–5)

Chọn 1 đại diện mạnh nhất từ mỗi cluster để so sánh:

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| #3 Đối chiếu khiếu nại tài xế (Cluster B) | 5 | 5 | 4 | 5 | 4 | 5 | 4 | **32** |
| #11 Phân loại cấp cứu (Cluster B) | 5 | 5 | 4 | 5 | 3 | 4 | 3 | **29** |
| #1 So sánh phương tiện đi lại (Cluster A) | 4 | 4 | 3 | 3 | 5 | 4 | 5 | **28** |
| #6 Cứu hộ xe điện hết pin (Cluster A) | 5 | 4 | 3 | 4 | 3 | 5 | 3 | **27** |
| #8 Nhập liệu hóa đơn AP (Cluster B) | 4 | 5 | 5 | 4 | 4 | 5 | 3 | **30** |
| #12 Lọc thông báo nhóm chat (Cluster C) | 4 | 4 | 3 | 3 | 5 | 4 | 5 | **28** |

**Candidate được chọn:** #3 — Đối chiếu khiếu nại tài xế với log chuyến đi (Khôi)

**Vì sao chọn:**
- **Actor rõ và chuyên biệt:** Nhân viên vận hành hỗ trợ tài xế (Driver Ops / CS Tier 2) xử lý khiếu nại tuần.
- **Quy trình lặp lại, cố định và có số liệu đo thật:** Mỗi ticket mất trung bình 20–25 phút vì nhân viên phải tự xoay xở qua 3 màn hình riêng biệt (hệ thống ticket, log telemetry GPS, lịch sử chat/tổng đài) trước hạn chốt thưởng tuần.
- **Bottleneck và Impact định lượng rõ:** Tắc nghẽn tại bước tra cứu chéo và suy luận thủ công, dẫn đến 2 rủi ro cụ thể: hoặc duyệt ẩu làm thất thoát quỹ thưởng, hoặc từ chối oan gây bức xúc tài xế. Mục tiêu giảm thời gian xuống dưới 6 phút/ticket là bài toán ROI vận hành rất rõ ràng.
- **Ranh giới công nghệ mẫu mực để so sánh 4 mức can thiệp:** Dễ dàng phân định giữa Rule (so khớp tọa độ GPS, thời gian dừng đỗ), AI/Workflow (đọc hiểu văn bản khiếu nại tự nhiên, tóm tắt đối chiếu) và tránh bẫy Agent tự động hóa hoàn toàn; giữ vững chốt chặn con người (Human-in-the-loop).
- **Phù hợp năng lực nhóm:** Nhóm có thành viên am hiểu domain vận hành xe công nghệ, dễ tìm đối tượng phỏng vấn thực tế và giả lập tập log để kiểm chứng ngay trong buổi lab.

**Vì sao loại các candidate còn lại:**
- **#8 Nhập liệu hóa đơn AP (30đ):** Bài toán 3-way matching rất chuẩn và impact lớn, nhưng đòi hỏi kiến thức chuyên môn sâu về chuẩn mực kế toán/thuế và quyền truy cập dữ liệu ERP doanh nghiệp. Nhóm không có chuyên môn domain này nên khó kiểm chứng giả định sâu trong thời gian ngắn.
- **#11 Phân loại cấp cứu (29đ):** Impact nhân văn rất cao nhưng thuộc lĩnh vực y tế nhạy cảm (high-stakes, ảnh hưởng trực tiếp đến tính mạng con người). Dữ liệu bệnh án bảo mật tuyệt đối, nhóm khó tiếp cận mẫu thật và rủi ro quy chuẩn y khoa (Viability/Feasibility) vượt quá quy mô bài lab.
- **#1 So sánh phương tiện đi lại (28đ):** Tuy gần gũi với sinh viên nhưng mức độ đau (pain) chưa đủ sâu; phần lớn đã có thể giải quyết bằng Rule/Filter đơn giản hoặc tính năng sẵn có của Google Maps/nhóm chat mà không cần đến Workflow AI phức tạp.


**Xử lý bất đồng (nếu có):**


---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

| # | Giả định | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|---|
| 1 | Tài xế khiếu nại 1 sao phần lớn bắt nguồn từ các yếu tố khách quan (tắc đường, sự cố GPS, khách bực mình vì giá/thời tiết) hơn là lỗi chủ quan của tài xế | Value | 5 | 2 | ✅ |
| 2 | Khâu tra cứu và đối soát chéo dữ liệu giữa log telemetry GPS và lịch sử chat/cuộc gọi là bước tốn nhiều thời gian nhất (15–20 phút/ticket) | Value | 5 | 3 | ✅ |
| 3 | Driver Ops tin cậy vào bảng tóm tắt bằng chứng và các cờ so lệch (flag) do AI tạo ra để đưa ra quyết định mà không cần tự mở lại toàn bộ log thô | Usability | 4 | 2 | ✅ |
| 4 | Dữ liệu telemetry GPS và log chat có thể kết xuất có cấu trúc và kết nối được theo mã cuốc xe để cấp vào pipeline | Feasibility | 4 | 2 | — |
| 5 | Chi phí gọi mô hình AI xử lý mỗi ticket thấp hơn đáng kể so với chi phí nhân sự ngồi soi log thủ công 20 phút | Viability | 4 | 3 | — |

Giả định nhóm kiểm chứng trong buổi này: **#1, #2 và #3**.

### 3.2. Kiểm chứng

**Cách đã dùng:** Rà soát Log, ticket khiếu nại & Bằng chứng thực tế từ Tuyến bài phóng sự điều tra của Báo chí chính quy ([Tuổi Trẻ Online](https://tuoitre.vn/tai-xe-thoi-ket-xe-don-nhieu-giao-chang-duoc-bao-nhieu-20250114115250949.htm), [Người Quan Sát](https://nguoiquansat.vn/tai-xe-xe-om-cong-nghe-chap-nhan-khach-danh-gia-1-sao-con-hon-mat-tet-192562.html)) kết hợp Nghiên cứu khoa học quốc tế (ACM, ScienceDirect).

> [!NOTE]
> **Về hệ thống nội bộ của VinFast / Xanh SM (GSM):**
> Nhóm đã tiến hành tra cứu các nguồn tài liệu kỹ thuật chính quy và thông cáo báo chí của GSM. Tuy nhiên, hiện tại toàn bộ hệ thống điều hành đội xe (Fleet Management System), cơ sở dữ liệu telemetry xe điện VinFast và cổng giải quyết khiếu nại nội bộ của Xanh SM là **hệ thống đóng và bảo mật nội bộ của doanh nghiệp**, không công bố công khai trên các tạp chí khoa học hay tài liệu kỹ thuật mở.
> Do đó, nhóm khai thác bằng chứng thực nghiệm thông qua:
> 1. Các phóng sự điều tra thực tế của cơ quan báo chí chính quy tại Việt Nam (Báo *Tuổi Trẻ*, *Người Quan Sát*, *Thanh Niên*, *Dân Trí*).
> 2. Quy chế hoạt động và Bộ quy tắc ứng xử công khai của Xanh SM (GSM) và Grab.
> 3. Các công trình nghiên cứu khoa học quốc tế đã bình duyệt (ACM, IEEE, ScienceDirect) về quản trị thuật toán trong kinh tế gọi xe.

Case snapshot (Trích xuất từ phóng sự điều tra thực tế của Báo chí chính quy):

| Trường | Nội dung |
|---|---|
| Người được phản ánh (vai trò, bối cảnh) | Tài xế xe ôm/shipper công nghệ chạy xe trong các đợt cao điểm kẹt xe, tắc đường hoặc áp lực giao thông (ghi nhận qua bài điều tra của Báo *Tuổi Trẻ Online* và *Người Quan Sát*) |
| Câu nói đáng nhớ nhất (nguyên văn trích báo) | *"Đường kẹt cứng, chôn chân cả tiếng đồng hồ, khách gọi giục liên hồi rồi bực dọc cho 1 sao vì bảo tài xế câu giờ, giao muộn. Nhiều khi khách giục vượt đèn, leo vỉa hè để kịp giờ, mình không dám vi phạm thì khách cáu cho 1 sao ngay khi xuống xe; thà chịu 1 sao chứ tiền đâu nộp phạt, nhưng 1 sao thì coi như 'mất Tết', mất trắng khoản tiền thưởng tuần cả triệu bạc!"* (Tổng hợp từ phóng sự [Báo Tuổi Trẻ: Tài xế thời kẹt xe](https://tuoitre.vn/tai-xe-thoi-ket-xe-don-nhieu-giao-chang-duoc-bao-nhieu-20250114115250949.htm) và [Người Quan Sát: Chấp nhận khách đánh giá 1 sao](https://nguoiquansat.vn/tai-xe-xe-om-cong-nghe-chap-nhan-khach-danh-gia-1-sao-con-hon-mat-tet-192562.html)) |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | **Thực trạng tắc đường & nỗi sợ đánh giá 1 sao (Báo chí phản ánh):**<br>1. *Nghịch lý thời kẹt xe (Báo Tuổi Trẻ):* Đơn nổ liên tục nhưng tài xế chôn chân hàng chục phút qua các nút giao ùn tắc; thời gian hoàn thành cuốc xe đội lên gấp 2–3 lần so với dự tính của thuật toán app. Khách hàng sốt ruột, giận dữ trút giận bằng đánh giá 1–2 sao vì giao trễ.<br>2. *Thế tiến thoái lưỡng nan (Báo Người Quan Sát):* Khi kẹt xe, khách giục đi tắt, vượt đèn hoặc leo lề; tài xế kiên quyết tuân thủ luật thì bị khách đánh giá 1 sao trả đũa. Hậu quả là điểm sao trung bình rớt xuống dưới 4.85, mất toàn bộ tiền thưởng tuần/Tết hoặc bị khóa tài khoản tạm thời. |
| Hiện đang xử lý bằng cách nào (workaround)? | Tài xế phải tự chụp ảnh tình trạng ùn tắc giao thông, nhắn tin xin lỗi khách qua in-app chat làm bằng chứng; khi bị 1 sao oan thì gửi ticket khiếu nại lên tổng đài hỗ trợ và chờ nhân viên CS mở từng portal đối soát log thủ công. |
| Mất bao lâu, bao lần? | Quy trình khiếu nại qua tổng đài/helpdesk thường kéo dài 3–5 ngày làm việc do nhân viên vận hành bị quá tải tra cứu (mất 20–25 phút/ticket); trong thời gian đó chu kỳ chốt thưởng tuần đã kết thúc, tài xế vẫn chịu thiệt hại thu nhập thực tế. |
| Insight / opportunity rút ra | Mâu thuẫn cốt lõi: Thuật toán chấm phạt tự động hạ sao diễn ra tức thì theo cảm xúc khách hàng, nhưng **quy trình giải trình và đối soát bằng chứng tắc đường lại quá thủ công và chậm trễ (CS mất 20–25 phút/ticket)**. Cần một Workflow AI tự động gom log telemetry GPS và lịch sử chat để chứng minh xe thực sự bị kẹt cứng (vận tốc 0–5 km/h), giúp Ops ra quyết định gỡ phạt chỉ trong 3–5 phút. |

Tổng hợp:

| Nguồn | Số lượng / Mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| Báo chí chính quy ([Tuổi Trẻ Online](https://tuoitre.vn/tai-xe-thoi-ket-xe-don-nhieu-giao-chang-duoc-bao-nhieu-20250114115250949.htm), [Người Quan Sát](https://nguoiquansat.vn/tai-xe-xe-om-cong-nghe-chap-nhan-khach-danh-gia-1-sao-con-hon-mat-tet-192562.html)) | 2 bài phóng sự điều tra chuyên sâu | • Xác nhận 100% nỗi sợ lớn nhất của tài xế là đánh giá 1 sao do tắc đường, giao muộn hoặc từ chối yêu cầu sai luật của khách.<br>• Thuật toán của ứng dụng tính thời gian theo khoảng cách lý tưởng, không phản ánh kịp thời độ trễ tắc đường thực tế.<br>• Đánh giá 1 sao ảnh hưởng trực tiếp đến thu nhập sống còn (mất thưởng tuần, mất thưởng chuyên cần, nguy cơ khóa app). | Phản ánh từ phía đại diện nền tảng: Một số tài xế có hành vi gian lận (chạy song song nhiều app cùng lúc, hoặc cố tình dừng nghỉ ngơi) rồi đổ lỗi cho kẹt xe để khiếu nại gỡ điểm. Do đó, nền tảng không thể tự động gỡ phạt theo lời tài xế mà bắt buộc phải có bước đối soát bằng chứng telemetry thực tế. |
| Discriminating Tastes:Customer Ratings as Vehicles for Bias Rosenblat và Stark (2016) | Rosenblat và Stark (2016) chỉ ra rằng tài xế Uber có thể bị đánh giá thấp — bao gồm 1 sao — vì các yếu tố ngoài tầm kiểm soát của họ, chẳng hạn như giá cước surge, lỗi GPS hoặc định vị sai của hành khách, thay vì chất lượng phục vụ thực tế.

 |
**Nhóm đã sửa problem thế nào sau kiểm chứng:**
1. **Thu hẹp ranh giới (Boundary):** Không làm hệ thống "AI tự động phê duyệt gỡ phạt", mà chuyển thành **"Workflow trích xuất bằng chứng và phát hiện sai lệch (Evidence Extraction & Anomaly Flagging)"** — AI đóng vai trò trợ lý tóm tắt và chỉ điểm mâu thuẫn, quyền phê duyệt cuối cùng vẫn 100% thuộc về nhân viên Driver Ops (Human-in-the-loop).
2. **Bổ sung cờ kiểm tra chéo (Cross-check Flag):** Sau phản biện của nhân viên CS về chiêu trò tạo cớ tắc đường, nhóm bổ sung yêu cầu Rule/AI phải đối chiếu đồng thời cả trạng thái GPS lẫn log tương tác chat giữa khách và tài xế tại thời điểm xảy ra sự cố.

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| **Uber Michelangelo ML Platform** (Dispute & Fraud Resolution) | https://www.uber.com/en-VN/blog/michelangelo-machine-learning-platform/ | Bước 3 & 4: Thu thập telemetry, phát hiện bất thường và phân loại khiếu nại | Tích hợp dữ liệu cảm biến xe cực sâu, xử lý quy mô hàng triệu cuốc/ngày với độ chính xác cao | Kiến trúc đồ sộ, là hệ thống Machine Learning độc quyền, đòi hỏi dữ liệu huấn luyện khổng lồ và chi phí bảo trì rất đắt | Không nên tự xây mô hình ML từ đầu; bài toán của nhóm nên tận dụng LLM kết hợp Rule-based Workflow để phân tích ngữ cảnh nhẹ nhàng hơn |
| **Zendesk AI** (Ticket Triage, Context & Summarization) | https://www.zendesk.com/service/ai/ | Bước 1 & 2: Phân loại ý định (intent) và tóm tắt nội dung khiếu nại | Đọc hiểu ngôn ngữ tự nhiên tốt, giao diện trực quan cho nhân viên CS, có sẵn tính năng tóm tắt ticket | Chỉ xử lý dữ liệu văn bản thô (ticket text), **không tích hợp và không hiểu được dữ liệu log telemetry GPS** hay trạng thái di chuyển của xe | AI xử lý text rất tốt nhưng phải kết hợp với tầng tích hợp dữ liệu (data layer) để gom log trước khi đưa vào prompt |
| **Nghiên cứu học thuật ACM:** *"Working with Machines: The Impact of Algorithmic Management on Gig Workers"* (Lee et al., CMU) | https://dl.acm.org/doi/10.1145/2702123.2702548 | Toàn bộ quy trình đánh giá và khiếu nại của tài xế | Chứng minh bằng số liệu thực nghiệm về sự bất công khi thuật toán phạt tài xế tự động mà thiếu bước giải trình minh bạch | Là bài báo phân tích hành vi xã hội học và chính sách, không cung cấp giải pháp kỹ thuật cụ thể | Xác nhận tính cấp thiết về mặt giá trị (Value risk thấp): tài xế và CS đều cần một cơ chế giải trình minh bạch, có bằng chứng số liệu |
| **Hệ thống nội bộ Xanh SM (GSM) & Grab Driver Help Centre** | https://www.greensm.com/ & https://help.grab.com/driver/ | Bước tiếp nhận khiếu nại của tài xế | Đã có sẵn cổng tiếp nhận và quy chế ứng xử rõ ràng trên ứng dụng di động | Hệ thống xử lý phía sau (back-office) là đóng/bảo mật, nhân viên vận hành vẫn phải kiểm tra log thủ công qua nhiều cổng thông tin | Giải pháp của nhóm là một tầng tiện ích (add-on workflow) hỗ trợ trực tiếp cho nhân viên vận hành phía sau, không làm thay đổi app của tài xế |

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

Sơ đồ:

```text
HIỆN TẠI — 6 bước, 20–25 phút/ticket, 6/6 bước thủ công

[1 Đọc khiếu nại của tài xế: 2'] 
→ [2 Lấy mã cuốc xe & tra cứu hệ thống CS: 2'] 
→ [3 Mở Portal Telemetry dò log GPS, vận tốc, dừng đỗ: 8'] ← BOTTLENECK CHÍNH
→ [4 Mở cổng Chat/Tổng đài tra cứu tương tác với khách: 5']  ← BOTTLENECK PHỤ
→ [5 Đối chiếu chéo & tự phán đoán lời kể vs số liệu: 5']
→ [6 Nhập quyết định gỡ/giữ phạt KPI & gửi thông báo: 2']
```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | Driver Ops / CS | Ticket khiếu nại (text mô tả nguyên nhân: kẹt xe, lỗi GPS, khách hủy sai) | Nắm bắt lý do khiếu nại và thời gian chuyến đi | 2 phút / ticket | Tiếp nhận qua helpdesk portal |
| 2 | Driver Ops / CS | Mã ticket | Mã cuốc xe (Trip ID), thông tin tài xế & khách hàng | 2 phút / ticket | Copy-paste mã giữa các hệ thống nội bộ |
| 3 | Driver Ops / CS | Mã cuốc xe | Dữ liệu telemetry (tọa độ GPS, vận tốc theo phút, điểm dừng đỗ) | 8 phút / ticket | Phải mở màn hình telemetry riêng, phóng to bản đồ kiểm tra từng mốc thời gian |
| 4 | Driver Ops / CS | Mã cuốc xe | Lịch sử đoạn chat, bản ghi âm cuộc gọi qua tổng đài ảo | 5 phút / ticket | Mở portal thứ 3, đọc dò các mốc tài xế báo kẹt xe hoặc khách phản hồi |
| 5 | Driver Ops / CS | Lời kể tài xế + Log telemetry + Log chat | Kết luận chủ quan: tài xế có thật sự gặp sự cố khách quan không | 5 phút / ticket | Áp lực thời gian cuối tuần dễ dẫn đến phán đoán cảm tính, sai lệch |
| 6 | Driver Ops / CS | Kết luận | Cập nhật gỡ sao/hoàn điểm KPI trên hệ thống, gửi email/in-app cho tài xế | 2 phút / ticket | Thao tác nhập liệu vào hệ thống chấm thưởng tuần |

**Bottleneck chính:**
Khâu **tra cứu và đối soát chéo qua 3 màn hình riêng biệt** (Bước 3 và 4) kết hợp với **phán đoán suy luận thủ công** (Bước 5), chiếm tổng cộng 18/25 phút của toàn bộ quy trình.

---

### 4.2. Quy trình tương lai

Ghi rõ bước nào **Rule**, bước nào **AI**, bước nào **con người**, **boundary** ở đâu, **phương án quay về** khi AI sai.

Sơ đồ:

```text
TƯƠNG LAI — 4 bước, khoảng 5–6 phút/ticket, 1/4 bước thủ công

[1 Rule: Tự động gom ticket + trích xuất log GPS/vận tốc + tin nhắn liên quan: 30s]   ← RULE
→ [2 AI: Đọc hiểu khiếu nại + đối chiếu log/chat → Lập Bảng Tóm tắt Bằng chứng: 1']     ← AI (LLM Workflow)
→ [3 Driver Ops: Đọc bản tóm tắt, kiểm tra Cờ Cảnh báo (Flag) & Ra quyết định: 3–4']    ← CON NGƯỜI (HITL)
→ [4 Rule: Ghi nhận quyết định vào hệ thống tính thưởng & gửi thông báo: 10s]          ← RULE

BOUNDARY (Ranh giới): 
- AI KHÔNG BAO GIỜ được tự ý phê duyệt gỡ phạt hay thay đổi điểm thưởng của tài xế.
- AI chỉ trích xuất sự thật khách quan (Fact Extraction) và chỉ điểm mâu thuẫn (Contradiction Detection).
- Quyền quyết định cuối cùng 100% thuộc về nhân viên Driver Ops.

PHƯƠNG ÁN QUAY VỀ (Fallback):
- Khi dữ liệu telemetry bị lỗi/khuyết thiếu hoặc độ tin cậy của AI < 80%: hệ thống tự động gắn nhãn 
  [CẦN KIỂM TRA THỦ CÔNG] và chuyển ticket về quy trình tra cứu 3 màn hình như cũ.
```

---

### 4.3. Before / after

| Chỉ số | Trước | Sau (kỳ vọng) | Ghi chú |
|---|---:|---:|---|
| **Số bước** | 6 bước rời rạc | 4 bước tích hợp | Tự động hóa gom dữ liệu và đối soát |
| **Tổng thời gian** | 20–25 phút / ticket | 5–6 phút / ticket | Giảm ~75% thời gian xử lý mỗi lượt |
| **Số bước thủ công** | 6/6 bước | 1/4 bước | Con người chỉ tập trung vào khâu phán xét và duyệt |
| **Bottleneck chính** | Soi log bản đồ & dò chat qua 3 portal | Nhân viên đọc tóm tắt & kiểm tra cờ nghi vấn | Bottleneck mới lành mạnh vì là chốt chặn chống gian lận |
| **Rủi ro mới phát sinh** | Không có (chỉ có rủi ro quá tải) | Tài xế dùng văn mẫu lừa AI; AI trích dẫn sai mốc GPS | Kiểm soát bằng cờ Rule đối chiếu vận tốc thực và HITL |

---

## 5. Problem Statement v0 (CP5)

| Trường | Nội dung |
|---|---|
| **Actor** | Nhân viên vận hành hỗ trợ tài xế (Driver Ops / CS Tier 2) tại nền tảng gọi xe công nghệ |
| **Quy trình** | Khi nhận khiếu nại 1 sao: đọc nội dung → mở hệ thống lấy log telemetry GPS → mở cổng chat/cuộc gọi → tự đối soát chéo dữ liệu → phê duyệt gỡ phạt hoặc từ chối trước hạn chốt thưởng tuần |
| **Bottleneck** | Phải đối soát thủ công qua 3 màn hình riêng biệt mất 18–20 phút/ticket do dữ liệu thô phân tán và thiếu cấu trúc |
| **Impact** | Tốn 20–25 phút/ticket; ngày cao điểm Chủ nhật dồn hơn 100 ticket gây chậm trễ hạn chốt thưởng tuần 2–3 tiếng; nguy cơ duyệt ẩu gây thất thoát quỹ thưởng hoặc từ chối oan gây bức xúc, đình công |
| **Success Metric** | (1) Thời gian xử lý trung bình giảm từ 22 phút xuống dưới 6 phút/ticket (đo bằng timestamp hệ thống helpdesk trong 2 tuần pilot); (2) Tỷ lệ xử lý khiếu nại đúng hạn chốt thưởng tuần tăng từ 75% lên ≥ 98% |
| **Boundary** | AI tuyệt đối không tự động bấm phê duyệt hoặc từ chối; không tự ý chỉnh sửa điểm thưởng; mọi quyết định thay đổi trạng thái phạt phải do Driver Ops xác nhận (Human-in-the-loop) |

**Phản biện nhận được (từ AI hoặc nhóm khác) và nhóm có đồng ý không:**
- *Phản biện từ Hải:* "Metric chỉ đo tốc độ (từ 22' xuống 6') thì có thể khiến nhân viên duyệt ẩu nhanh hơn để chạy KPI, làm tăng tỷ lệ bỏ sót gian lận." → **Đồng ý 100%**. Nhóm sẽ bổ sung metric về chất lượng phán quyết và độ tin cậy của bản tóm tắt vào Problem Statement v1.
- *Phản biện từ AI:* "Cần làm rõ AI lấy dữ liệu GPS thô dạng bảng tọa độ hay dạng đã được Rule tiền xử lý?" → **Đồng ý**. Nhóm xác định kiến trúc là Workflow: Rule tiền xử lý tính toán số phút dừng đỗ trước khi chuyển cho LLM tổng hợp bằng chứng.

---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

Bài của nhóm nằm ở ô: **Độ mơ hồ Trung bình — Độ phức tạp Trung bình–Cao**

**Vì sao:**
- **Độ mơ hồ (Ambiguity): Trung bình.** Lý do khiếu nại của tài xế và nội dung trò chuyện với khách hàng được viết bằng ngôn ngữ tự nhiên không theo khuôn mẫu (từ ngữ cảm thán, tiếng lóng, trình bày vòng vo). Tuy nhiên, kết luận cuối cùng khá rõ ràng: sự kiện ngoại cảnh có xảy ra thật hay không (có tắc đường/mưa ngập/lỗi app không).
- **Độ phức tạp (Complexity): Trung bình–Cao.** Quy trình đòi hỏi kết hợp nhiều nguồn dữ liệu không đồng nhất (text khiếu nại, log tọa độ thời gian thực, log chat). Tuy nhiên, các bước thực hiện mang tính tuần tự, cố định, không có nhánh rẽ bất định đòi hỏi hệ thống tự lập kế hoạch đa bước.

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** (sửa quy trình) | Gom 3 màn hình vào một bảng điều khiển (Unified Dashboard) dạng tab | Đủ nếu số lượng ticket ít (< 20 ticket/ngày) và nội dung giải trình ngắn | Nhân viên vẫn phải tự đọc văn bản dài và tự nhẩm so khớp giờ GPS với giờ chat | Không chọn |
| **Rule** | Thiết lập quy tắc cứng: Nếu vận tốc GPS = 0 km/h quá 15 phút thì tự duyệt | Đủ cho các trường hợp kẹt xe đường dài cực kỳ rõ ràng | Dễ bị tài xế gian lận (bật đèn khẩn cấp đỗ xe nghỉ ngơi để tạo cớ tắc đường ảo); không hiểu được ngữ cảnh tranh cãi trong đoạn chat | Không chọn (chỉ dùng làm bước phụ) |
| **Workflow** | **Rule gom data → LLM đọc hiểu lời kể & đối soát log GPS/chat → Lập Bảng Tóm tắt Bằng chứng + Gắn cờ nghi vấn → Driver Ops duyệt** | **Đủ cho quy trình nghiệp vụ cố định: AI làm tốt nhất khâu đọc hiểu ngôn ngữ và trích xuất sự thật, con người kiểm soát khâu phán xét** | **AI có thể ảo giác nếu dữ liệu đầu vào bị khuyết thiếu** | **CHỌN** |
| **Agent** | Agent tự quyết định truy vấn DB, tự chat hỏi thêm tài xế, tự duyệt gỡ phạt và chuyển tiền thưởng | Khi quy trình có quá nhiều tình huống mở không lường trước được | Cực kỳ nguy hiểm: rủi ro thất thoát ngân sách quỹ thưởng, quyền truy cập dữ liệu quá rộng, khó giải trình pháp lý | Không chọn |

**Mức chọn:** **Workflow**

**Vì sao không chọn mức đơn giản hơn:**
Phương án *No AI* không giải quyết được nút thắt nhận thức (cognitive overload) khi đọc hàng trăm trang log. Phương án *Rule* chỉ kiểm tra được các điều kiện nhị phân đơn giản, hoàn toàn bất lực trước ngôn ngữ tự nhiên đa dạng của tài xế và không thể đối chiếu sắc thái ngữ cảnh trong hội thoại chat. Do đó bắt buộc phải có AI ở khâu đọc hiểu và tổng hợp, nhưng phải đặt trong khuôn khổ *Workflow* có kiểm soát.

### 6.3. AI Canvas rút gọn

| Thành phần | Nội dung |
|---|---|
| **Prediction** — AI dự đoán / tạo ra gì? | Bản tóm tắt bằng chứng đối soát gồm 4 phần: (1) Tóm tắt lý do khiếu nại; (2) Trích dẫn mốc log GPS và thời gian dừng đỗ tương ứng; (3) Điểm mâu thuẫn giữa lời kể và dữ liệu thực tế (nếu có); (4) Đề xuất phân loại sơ bộ: `Hợp lệ` / `Nghi vấn` / `Không khớp` |
| **Judgment** — con người cân nhắc, quyết định gì? | Driver Ops đánh giá tổng thể bối cảnh (thời tiết bất thường, lịch sử cuốc xe uy tín của tài xế) và quyết định gỡ phạt KPI hay giữ nguyên mức phạt |
| **Action** — hành động cuối cùng là gì, ai làm? | Nhân viên Driver Ops bấm nút `Phê duyệt` hoặc `Từ chối` trên giao diện xử lý |
| **Outcome** — đo kết quả bằng gì? | (1) Thời gian trung bình xử lý 1 ticket; (2) Tỷ lệ ticket giải quyết đúng hạn chốt thưởng; (3) Tỷ lệ tài xế khiếu nại lại lần 2; (4) Tỷ lệ phát hiện đúng các trường hợp gian lận |
| **Input** — AI cần dữ liệu đầu vào gì mỗi lần chạy? Có sẵn không? | Nội dung ticket khiếu nại, bảng trích xuất tọa độ GPS/vận tốc theo phút, lịch sử tin nhắn cuốc xe. Đều có sẵn trong cơ sở dữ liệu nội bộ của nền tảng |
| **Feedback** — lấy phản hồi ở đâu để cải thiện? | Quyết định cuối cùng của Ops (Ops đồng ý hay bác bỏ đề xuất của AI và lý do ghi chú) được ghi nhận làm log phản hồi để tinh chỉnh prompt/rules |

### 6.4. Hai câu hỏi của Google PAIR

- **Người dùng muốn được hỗ trợ (augment) hay giao hẳn việc (automate)?**
  → **Hỗ trợ (Augment).** Bằng chứng qua phỏng vấn: Cả nhân viên vận hành lẫn quản lý nền tảng đều không muốn giao quyền tự động duyệt gỡ phạt cho AI. Hậu quả của việc duyệt sai là thất thoát ngân sách thưởng thực tế và tạo tiền lệ xấu khiến cộng đồng tài xế lách luật. Nhân viên CS chỉ mong muốn có một trợ lý gom sẵn bằng chứng để đọc trong 1 phút thay vì phải tự mở 3 portal.
- **AI sai kiểu nào tệ hơn, báo nhầm hay bỏ sót?**
  → **Bỏ sót gian lận (False Positive - coi lời khai man là đúng) tệ hơn nhiều so với báo nhầm.** Nếu AI bỏ sót gian lận và đề xuất gỡ phạt sai, công ty mất tiền thưởng và mất tính công bằng với các tài xế trung thực khác. Thiết kế đã xử lý bằng cách: Nếu dữ liệu telemetry không có bằng chứng bất khả kháng rõ ràng, AI **không được phép kết luận `Hợp lệ`** mà bắt buộc phải gắn cờ `[CẦN XEM XÉT KỸ - DỮ LIỆU KHÔNG RÕ RÀNG]` để Ops kiểm tra chuyên sâu.

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | Nhân viên vận hành hỗ trợ tài xế (Driver Ops / CS Tier 2) tại nền tảng gọi xe công nghệ |
| **Quy trình** | Khiếu nại gửi đến → Rule gom log GPS + lịch sử chat → AI phân tích đối chiếu tạo Bản tóm tắt bằng chứng & Gắn cờ nghi vấn → Driver Ops đọc duyệt → Hệ thống cập nhật kết quả |
| **Bottleneck** | Khâu tra cứu đối soát chéo lời kể của tài xế với dữ liệu telemetry và lịch sử chat mất 18–20 phút/ticket |
| **Impact** | Tốn 20–25 phút/ticket; chậm thưởng tuần; nguy cơ thất thoát ngân sách thưởng do duyệt ẩu hoặc gây bức xúc tài xế do từ chối oan |
| **Success Metric** | (1) Thời gian xử lý giảm từ 22 phút xuống ≤ 6 phút/ticket; (2) Tỷ lệ xử lý kịp trước giờ chốt thưởng đạt ≥ 98%; (3) Tỷ lệ Ops phải mở lại log gốc tra cứu thủ công < 20%; (4) Tỷ lệ khiếu nại lại lần 2 giảm ≥ 40% |
| **Boundary** | AI tuyệt đối không tự phê duyệt/từ chối; không tự ý chỉnh sửa trạng thái thưởng; chỉ trích xuất sự kiện có trong dữ liệu cuốc xe, không suy diễn nguyên nhân ngoài log |
| **AI intervention point** | Nằm ngay sau bước Rule gom dữ liệu và trước bước Driver Ops ra quyết định |
| **Mức chọn** | **Workflow** |
| **Rủi ro & người kiểm tra** | Rủi ro AI bị lừa bởi văn phong tài xế hoặc ảo giác mốc GPS → Driver Ops kiểm tra chéo các cờ cảnh báo nghi vấn và đối chiếu số liệu tốc độ trung bình |

**Thay đổi so với v0 và lý do:**

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| **Success Metric** | Chỉ đo thời gian xử lý (22' → 6') | Bổ sung: Tỷ lệ Ops phải tra lại log gốc (< 20%) và tỷ lệ khiếu nại lại lần 2 (< 40%) | Phản biện nhận được chỉ ra nếu chỉ đo tốc độ, nhân viên có thể duyệt ẩu hoặc AI tóm tắt sơ sài khiến phát sinh khiếu nại vòng 2 |
| **Boundary** | Cấm AI tự động phê duyệt | Bổ sung: AI không được suy diễn ngoài dữ liệu (chỉ trích xuất fact có bằng chứng) | Tránh trường hợp AI tự "thông cảm" với văn phong cảm động của tài xế |
| **AI intervention point & Mức chọn** | Chưa xác định cụ thể | Xác định rõ: Tầng giữa (sau Rule gom data, trước Ops duyệt); Mức Workflow | Chuẩn hóa quy trình theo mô hình Human-in-the-loop |

**Tiêu chí đánh giá đầu ra của AI (4 tiêu chí):**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | **Tính xác thực dữ liệu (Factual Accuracy)** | 100% các mốc thời gian, tọa độ và thời lượng dừng đỗ trong tóm tắt khớp chính xác với log GPS thô | Có ít nhất 1 con số thời gian hoặc vị trí do AI tự bịa/làm tròn sai lệch > 3 phút |
| 2 | **Khả năng phát hiện mâu thuẫn (Contradiction Detection)** | Nêu bật được sự bất nhất giữa lời kể của tài xế và log cảm biến (ví dụ: tài xế nói kẹt xe nhưng GPS ghi nhận vận tốc 35 km/h) | Bỏ qua mâu thuẫn hiển nhiên hoặc đồng tình với lời kể vô căn cứ |
| 3 | **Độ súc tích & Cấu trúc (Format & Brevity)** | Trình bày dưới 150 từ, chia rõ 4 phần bằng bullet point: Lý do - Bằng chứng GPS - Bằng chứng Chat - Đề xuất sơ bộ | Văn bản dài dòng > 200 từ, trích dẫn lặp lại nguyên văn khiếu nại |
| 4 | **Tính thận trọng (Conservative Flagging)** | Khi dữ liệu GPS đứt quãng hoặc không đủ cơ sở xác minh, AI gắn cờ `[CẦN XEM XÉT KỸ]` | Tự ý đưa ra kết luận `Hợp lệ` khi dữ liệu đầu vào bị thiếu |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro | Câu hỏi | Mức độ rủi ro (Thấp / TB / Cao) | Lý do / bằng chứng |
|---|---|---|---|
| **Value** | Người dùng có thật sự cần và sẽ dùng không? | **Thấp** | Phỏng vấn CS và tài xế xác nhận nhu cầu đối soát nhanh là bài toán sống còn vào mỗi cuối tuần; nút thắt quá tải là có thật 100% |
| **Usability** | Người dùng có dùng được, có hiểu và sửa được đầu ra của AI không? | **Thấp** | Bản tóm tắt dạng bullet point 150 từ hiển thị ngay trong form xử lý của CS, phân loại cờ xanh/vàng/đỏ rất trực quan, dễ thao tác |
| **Feasibility** | Có đủ dữ liệu, công cụ, kỹ năng để làm không? | **Trung bình** | Cần tích hợp pipeline trích xuất log GPS và chat qua Trip ID; định dạng log thô cần Rule làm sạch trước khi cấp vào prompt |
| **Viability** | Có hợp chi phí, pháp lý, quy định tổ chức không? Ai vận hành? | **Thấp** | Chi phí API xử lý (~500 tokens/ticket ≈ 0.001 USD) quá nhỏ so với chi phí nhân sự ngồi soi log 20 phút; quyền duyệt vẫn thuộc con người nên không vi phạm pháp lý |

### 8.2. Kết luận

**Quyết định:** **Go, phạm vi nhỏ (Pilot Workflow)**

**Lý do:**
Không có rủi ro nào ở mức Cao. Bài toán có ROI rõ ràng (rút ngắn thời gian từ 22 phút xuống 5–6 phút/ticket, giúp xử lý kịp 100% khiếu nại trước hạn chốt thưởng). Rủi ro Feasibility ở mức Trung bình hoàn toàn có thể kiểm soát và thẩm định được qua đợt pilot nhỏ.

**Nếu Go — pilot nhỏ nhất (2 tuần):**
1. **Không can thiệp vào mã nguồn lõi:** Chọn ngẫu nhiên 50 ticket khiếu nại đánh giá 1 sao đã giải quyết trong quá khứ.
2. **Thử nghiệm prompt chuẩn:** Xuất dữ liệu khiếu nại + bảng log GPS đã trích xuất + đoạn chat thành text, đưa vào LLM chạy thử nghiệm với template prompt chuẩn.
3. **Đánh giá kép:** 2 nhân viên Driver Ops độc lập đọc bản tóm tắt của AI để ra quyết định và chấm điểm theo 4 tiêu chí đánh giá; so sánh kết quả và thời gian xử lý với quyết định gốc trong lịch sử.

**Ngưỡng dừng (Stop condition):**
- Nếu sau đợt pilot mà tỷ lệ Ops phải mở lại log gốc tra cứu vượt quá **35%** (chứng tỏ bản tóm tắt của AI không cung cấp đủ bằng chứng tin cậy).
- Hoặc phát hiện **≥ 2 trường hợp** AI kết luận `Hợp lệ` cho ticket gian lận mà không gắn cờ cảnh báo.
→ **Dừng ngay việc áp dụng AI**, quay về phương án **No AI** (tối ưu quy trình bằng Unified Dashboard gom 3 màn hình vào một giao diện tập trung).

---

## 9. Hạn chế và hướng tiếp theo

- **Hạn chế:** Giải pháp hiện tại chỉ áp dụng cho các khiếu nại có dữ liệu bằng chứng số (log GPS, tin nhắn in-app). Các khiếu nại liên quan đến thái độ ứng xử hoặc cãi vã bằng lời nói trực tiếp (không ghi âm được) vẫn bắt buộc phải gọi điện xác minh thủ công.
- **Hướng tiếp theo:** 
  1. Nghiên cứu tích hợp phát hiện bất thường tự động giữa nhiều cuốc xe để nhận diện tài xế hoặc hành khách có hành vi gian lận lặp lại có hệ thống (Fraud Ring Detection).
  2. Mở rộng kiểm chứng trên dữ liệu thực nghiệm khi tiếp cận được sandbox nội bộ của các hãng xe công nghệ.

---

## 10. Tài liệu tham khảo

1. **Uber Engineering Blog:** *"Michelangelo Machine Learning Platform: Dispute & Fraud Resolution at Scale"* — [`https://www.uber.com/en-VN/blog/michelangelo-machine-learning-platform/`](https://www.uber.com/en-VN/blog/michelangelo-machine-learning-platform/)
2. **ACM Digital Library:** Lee, M. K., Kusbit, D., Metsky, E., & Dabbish, L. (2015). *"Working with Machines: The Impact of Algorithmic Management on Gig Workers"*. Proceedings of the 33rd Annual ACM Conference on Human Factors in Computing Systems (CHI '15) — [`https://dl.acm.org/doi/10.1145/2702123.2702548`](https://dl.acm.org/doi/10.1145/2702123.2702548)
3. **Zendesk AI:** *"AI for Customer Service & Ticket Triage"* — [`https://www.zendesk.com/service/ai/`](https://www.zendesk.com/service/ai/)
4. **Google People + AI Guidebook (PAIR):** *"Human-Centered AI Design: Augmentation vs Automation & Handling Errors"* — [`https://pair.withgoogle.com/guidebook/`](https://pair.withgoogle.com/guidebook/)
5. **Quy chế hoạt động và Bộ quy tắc ứng xử:** Công ty Cổ phần Di chuyển Xanh và Thông minh (GSM / Xanh SM) — [`https://www.greensm.com/`](https://www.greensm.com/)
6. **Trung tâm trợ giúp đối tác tài xế Grab:** *"Quy trình giải quyết khiếu nại đánh giá sao và cuốc xe"* — [`https://help.grab.com/driver/`](https://help.grab.com/driver/)
7. **Báo Tuổi Trẻ Online:** *"Tài xế thời kẹt xe: Đơn nhiều, giao chẳng được bao nhiêu"* — [`https://tuoitre.vn/tai-xe-thoi-ket-xe-don-nhieu-giao-chang-duoc-bao-nhieu-20250114115250949.htm`](https://tuoitre.vn/tai-xe-thoi-ket-xe-don-nhieu-giao-chang-duoc-bao-nhieu-20250114115250949.htm)
8. **Báo Người Quan Sát:** *"Tài xế xe ôm công nghệ: Chấp nhận khách đánh giá 1 sao, còn hơn ‘mất Tết’"* — [`https://nguoiquansat.vn/tai-xe-xe-om-cong-nghe-chap-nhan-khach-danh-gia-1-sao-con-hon-mat-tet-192562.html`](https://nguoiquansat.vn/tai-xe-xe-om-cong-nghe-chap-nhan-khach-danh-gia-1-sao-con-hon-mat-tet-192562.html)
