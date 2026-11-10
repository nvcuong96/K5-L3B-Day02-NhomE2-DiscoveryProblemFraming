# Team

> Điền file này trên repo chung do nhóm trưởng fork. Nhóm điền phần **Thông tin nhóm** và **Thành viên**. Mỗi người tự điền phần của mình trong **Cá nhân**. Không copy file này sang repo khác.

## Thông tin nhóm

- Tên nhóm: Nhóm E2
- Candidate problem nhóm chọn (1 câu): Đối chiếu tự động lý do khiếu nại của tài xế với log telemetry GPS và lịch sử chat để hỗ trợ Driver Ops phê duyệt gỡ phạt KPI công bằng trước hạn chốt thưởng tuần.
- Quyết định cuối (Go / Not Yet / No-Go): Go (phạm vi nhỏ / pilot workflow)

## Thành viên

| STT | Họ và tên        | MSSV        | Vai trò trong nhóm                                       | Tài khoản GitHub   |
| --: | ---------------- | ----------- | -------------------------------------------------------- | ------------------ |
|   1 | Nguyễn Văn Cường | 2A202603750 | Phụ trách Problem Card, vẽ quy trình & đồng viết báo cáo | nvcuong96          |
|   2 | Nguyễn Văn Hiếu  | 2A202603746 | Phụ trách Research giải pháp & tổng hợp dữ liệu          | lunaHieu  |
|   3 | Đoàn Công Hải    | 2A202603739 | Người phản biện chính, kiểm chứng rủi ro                 | rawser246  |
|   4 | Lê Nguyễn Anh Khôi | 2A202603755 | Điều phối thời gian, chốt Problem Statement v1          | KN-16              |

Không ghi email hay số điện thoại vào bảng này, vì repo có thể để public.

Gợi ý vai trò (một người có thể giữ nhiều vai): điều phối thời gian, ghi chép, người phản biện chính, phụ trách kiểm chứng (phỏng vấn/survey), phụ trách research, vẽ quy trình, viết Problem Statement.

## Phân công theo checkpoint

| Checkpoint                                 | Người chính | Người hỗ trợ | Sản phẩm                                                           |
| ------------------------------------------ | ----------- | ------------ | ------------------------------------------------------------------ |
| CP3 — Hội tụ nhóm                          | Cường       | Khôi         | Cluster, cây OST, bảng chấm điểm                                   |
| CP4 — Kiểm chứng                           | Hải         | Hiếu         | Assumption map, tổng hợp báo chí điều tra & nghiên cứu ACM         |
| CP4 — Research                             | Hiếu        | Cường        | Bảng research giải pháp có link (Uber, Zendesk)                    |
| CP5 — Quy trình trước/sau                  | Cường       | Khôi         | Quy trình 6 bước → 4 bước + bảng before/after                      |
| CP5 — Problem Statement v0                 | Khôi        | Cường        | Problem Statement v0                                               |
| CP6 — Mức can thiệp + Problem Statement v1 | Cường       | Hải          | Ma trận độ mơ hồ, AI Canvas, 4 tiêu chí eval, Problem Statement v1 |
| CP6 — Quyết định                           | Khôi        | Cả nhóm      | 4 rủi ro + quyết định Go phạm vi nhỏ & ngưỡng dừng                 |

## Cá nhân

Mỗi thành viên thêm một mục theo mẫu dưới đây, tiêu đề là `HoVaTen-MSSV`.

### NguyenVanCuong-2A202603750

**Phần việc phụ trách:**

- Pitch 3 Problem Card cá nhân (Khám bệnh viện, Xử lý ticket dev, Hóa đơn AP).
- Tham gia gom nhóm Cluster, xây dựng cây OST và tham gia thảo luận chấm điểm shortlist chọn candidate #3.
- Xây dựng quy trình trước/sau (6 bước hiện tại → 4 bước tương lai), thiết lập ranh giới boundary và phương án quay về.
- Cùng nhóm hoàn thiện bảng AI Canvas và 4 tiêu chí đánh giá đầu ra AI cho Problem Statement v1.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Đóng góp 3 candidate đầu vào cho nhóm (gồm candidate #4, #5, #8 trong bảng Pitch chung).
- Đặt câu hỏi phản biện sâu cho bài của Hải (_Hơn gì ChatGPT_) và bài của Khôi (_Dữ liệu OBD-II mơ hồ thì AI gợi ý phụ tùng có sai lệch không_).
- Vẽ sơ đồ và tính toán thời gian chi tiết cho quy trình hiện tại (22 phút) và tương lai (5–6 phút) trong Mục 4.
- Đề xuất phương án quay về (Fallback) khi AI thiếu độ tin cậy.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- Bảng Pitch (candidate #4, #5, #8) và câu hỏi phản biện trong Mục 2.1 `group_report.md`.
- Mục 2.2 Cluster và Mục 2.3 Cây OST.
- Mục 4.1, 4.2 và 4.3 trong `group_report.md`.
- File cá nhân: `report/individual/2A20260375_NguyenVanCuong.md`.

**Điều mình học được từ phần nhóm:**

- Hiểu được sự khác biệt cốt lõi giữa "Giải pháp trá hình" (Solution-first) và "Vấn đề/Nhu cầu thật" (Opportunity) khi xây dựng cây OST.
- Nhận ra rằng trong các bài toán vận hành phức tạp, AI không nên thay thế con người hoàn toàn mà cần thiết kế theo hướng Hỗ trợ (Augmentation) với ranh giới con người kiểm duyệt (Human-in-the-loop) để phòng ngừa gian lận.

### NguyenVanHieu-2A202603746

**Phần việc phụ trách:**

- Pitch 3 Problem Card cá nhân (Tối ưu hành trình di chuyển sinh viên 30km buýt vs xe máy, Đọc hiểu bài báo học thuật tiếng Anh, Lọc thông báo nhóm chat).
- Phụ trách chính phần Research giải pháp công nghệ đã có (Uber Michelangelo, Zendesk AI) và tổng hợp bằng chứng khoa học quốc tế (ACM CHI '15).
- Tham gia phân loại Cluster, xây dựng cây OST và thảo luận chấm điểm shortlist chọn candidate #3.
- Cùng nhóm xây dựng 4 tiêu chí đánh giá (eval metrics) cho LLM và xác lập ranh giới (boundary) trong Problem Statement v1.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Đóng góp 3 candidate đầu vào cho nhóm (#1, #9, #12 trong bảng Pitch chung).
- Đặt câu hỏi phản biện sâu về rào cản độ trễ API real-time cho bài của Khôi (#6 Cứu hộ pin xe điện) và ưu thế so với ChatGPT cho bài của Hải (#2 Hợp đồng thuê nhà).
- Tổng hợp và đối chuẩn chuyên sâu 2 giải pháp công nghệ hàng đầu: _Uber Michelangelo Platform_ (học cách đối soát telemetry) và _Zendesk AI_ (chỉ ra khoảng trống không hiểu log GPS).
- Đóng góp luận cứ cho Mục 3.2, 3.3 và Mục 7 trong `group_report.md`.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- Bảng Pitch (candidate #1, #9, #12) và câu hỏi phản biện trong Mục 2.1 `group_report.md`.
- Mục 3.2 (Bằng chứng kiểm chứng ACM) và Mục 3.3 (Bảng Research giải pháp Uber Michelangelo, Zendesk AI).
- Mục 7 (Tiêu chí đánh giá chất lượng đầu ra AI).
- File cá nhân: `report/individual/2A202603746_NguyenVanHieu.md`.

**Điều mình học được từ phần nhóm:**

- Nhận thức sâu sắc rằng bài toán công nghệ phải bắt nguồn từ nỗi đau vận hành có thật và đo lường được (như 22 phút đối soát/ticket trước giờ chốt thưởng), tránh sa vào bẫy "bệnh cầm búa đi tìm đinh" (solution-first).
- Hiểu rõ ranh giới giữa Augmentation (hỗ trợ con người) và Automation (tự động hóa hoàn toàn): trong các bài toán rủi ro cao về tài chính/thưởng phạt, AI chỉ nên đóng vai trò trợ lý tóm tắt bằng chứng, quyền phán quyết cuối cùng phải luôn thuộc về con người (Human-in-the-loop).

### LeNguyenAnhKhoi-2A202603755

**Phần việc phụ trách:**
- Pitch 3 Problem Card cá nhân (Khiếu nại tài xế, Cứu hộ sạc pin khẩn cấp, Tiếp nhận xe xưởng dịch vụ); bảo vệ bài #3 để nhóm chọn làm bài toán chung.
- Điều phối tiến độ thảo luận của nhóm, hỗ trợ Cường gom nhóm Cluster và xây dựng cây Opportunity Solution Tree (OST) rút gọn.
- Phụ trách chính xây dựng Problem Statement v0 và phối hợp hoàn thiện Problem Statement v1 sau khi nhận phản biện.
- Phụ trách chính Mục 8 Quyết định: đánh giá 4 loại rủi ro (Value, Usability, Feasibility, Viability), xây dựng kịch bản thử nghiệm pilot 2 tuần và thiết lập 2 ngưỡng dừng.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):
- Đóng góp candidate được chọn làm đề tài chính của nhóm (#3 — Đối chiếu khiếu nại tài xế với telemetry GPS và chat, đạt điểm cao nhất 32/35 điểm).
- Đặt câu hỏi phản biện cho 4 bài của các thành viên: Hiếu (#1 — *Hơn gì Google Maps*), Cường (#4 — *Phòng khám vắng ưu tiên ai*), Hải (#10 — *Phát hiện gian lận ảnh mờ*), Hiếu (#12 — *Phân biệt tin bài tập chính thức*).
- Tiếp thu phản biện của Hải để bổ sung cơ chế cờ đối chiếu chéo (Cross-check Flag) giữa telemetry GPS và log chat, ngăn chặn gian lận mẫu câu.
- Soạn thảo Problem Statement v0 và nâng cấp lên v1 (bổ sung 2 metric chặn: tỷ lệ xem lại log < 20% và tỷ lệ khiếu nại lần hai giảm ≥ 40%).
- Đánh giá 4 rủi ro, chốt quyết định Go phạm vi nhỏ (pilot 50 ticket) và đưa ra 2 ngưỡng dừng định lượng dứt khoát.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):
- Bảng Pitch (candidate #3, #6, #7) và các câu hỏi phản biện trong Mục 2.1 `group_report.md`.
- Mục 2.4 Bảng chấm điểm shortlist (candidate #3 được chọn).
- Mục 5 Problem Statement v0 và Mục 7 Problem Statement v1 trong `group_report.md`.
- Mục 8.1 và 8.2 (Bốn rủi ro, Quyết định Go, Kịch bản pilot & Ngưỡng dừng) trong `group_report.md`.
- File cá nhân: `report/individual/2A202603755_LeNguyenAnhKhoi.md`.

**Điều mình học được từ phần nhóm:**
- Nhận thức rõ ràng ranh giới giữa một sự bất tiện thoáng qua (minor inconvenience) và một nỗi đau vận hành cấp tính (acute pain) có tác động tài chính trực tiếp đến con người.
- Thấu hiểu sâu sắc tư duy thiết kế AI hỗ trợ (Augmentation) thay vì tự động hóa hoàn toàn (Automation); trong các bài toán đối soát nghiệp vụ có nguy cơ gian lận, con người luôn phải là chốt chặn cuối cùng (Human-in-the-loop) để bảo đảm tính công bằng và an toàn ngân sách.

### DoanCongHai-2A202603739

**Phần việc phụ trách:**
- Pitch 3 Problem Card cá nhân (Hợp đồng thuê nhà, Hoàn trả hàng e-commerce, Phân loại bệnh nhân cấp cứu).
- Đảm nhận vai trò **Người phản biện chính** của nhóm: liên tục chất vấn các lỗ hổng về gian lận, tính khả thi dữ liệu và rủi ro ROI ở các bước thảo luận.
- Đảm nhận vai trò **Người chính CP4 (Kiểm chứng)**: thu thập và phân tích dữ liệu thực tế từ các bài phóng sự điều tra của Báo *Tuổi Trẻ*, *Người Quan Sát* và các nghiên cứu khoa học ACM.
- Hỗ trợ hoàn thiện Problem Statement v1 và rà soát tiêu chí đánh giá đầu ra AI cùng kịch bản pilot ở CP6.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):
- Đóng góp 3 candidate đầu vào cho nhóm (#2, #10, #11 trong Bảng Pitch chung).
- Đặt câu hỏi phản biện then chốt cho đề tài của Khôi (#3): *"Nếu tài xế lợi dụng mẫu câu chuẩn để khai báo gian dối, làm thế nào để workflow AI kết hợp Rule kiểm tra chéo telemetry một cách khách quan mà không để lọt gian lận?"* — làm thay đổi hoàn toàn kiến trúc giải pháp của nhóm sang hướng Workflow có cờ kiểm tra chéo (Cross-check Flag).
- Thu thập bằng chứng thực nghiệm từ 2 bài phóng sự điều tra và 1 công trình khoa học quốc tế (ACM CHI '15) chứng minh áp lực đánh giá 1 sao là nỗi đau sinh kế thật của tài xế.
- Phản biện chỉ số Success Metric trong Problem Statement v0, thúc đẩy nhóm bổ sung 2 metric chặn chất lượng (tỷ lệ mở lại log < 20% và khiếu nại lần 2 giảm ≥ 40%) vào bản v1.
- Tham gia xây dựng 4 tiêu chí đánh giá đầu ra AI và thiết lập 2 ngưỡng dừng định lượng cho đợt thử nghiệm pilot 2 tuần.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):
- Bảng Pitch (candidate #2, #10, #11) và các câu hỏi phản biện trong Mục 2.1 `group_report.md`.
- Mục 3.1 (Assumption Map) và Mục 3.2 (Bằng chứng kiểm chứng Báo Tuổi Trẻ & ACM) trong `group_report.md`.
- Phản biện Success Metric được ghi nhận trong Mục 5 và Mục 7 của `group_report.md`.
- File cá nhân: `report/individual/2A202603739_DoanCongHai.md`.

**Điều mình học được từ phần nhóm:**
- Nhận thức rõ ràng bài học tránh bẫy "solution-first": không bắt đầu từ một công nghệ AI hào nhoáng rồi đi tìm bài toán, mà phải xuất phát từ nỗi đau quy trình nghiệp vụ có nút thắt nhận thức cụ thể.
- Hiểu sâu sắc giá trị của mô hình Human-in-the-loop: trong các bài toán đối soát nghiệp vụ có nguy cơ gian lận và tác động đến tiền bạc, AI chỉ đóng vai trò trợ lý trích xuất và chỉ điểm mâu thuẫn (Augmentation), con người phải luôn là người nắm quyền phán quyết cuối cùng.
