# Team

> Điền file này trên repo chung do nhóm trưởng fork. Nhóm điền phần **Thông tin nhóm** và **Thành viên**. Mỗi người tự điền phần của mình trong **Cá nhân**. Không copy file này sang repo khác.

## Thông tin nhóm

- Tên nhóm: Nhóm E2
- Candidate problem nhóm chọn (1 câu): Đối chiếu tự động lý do khiếu nại của tài xế với log telemetry GPS và lịch sử chat để hỗ trợ Driver Ops phê duyệt gỡ phạt KPI công bằng trước hạn chốt thưởng tuần.
- Quyết định cuối (Go / Not Yet / No-Go): Go (phạm vi nhỏ / pilot workflow)

## Thành viên

| STT | Họ và tên | MSSV | Vai trò trong nhóm | Tài khoản GitHub |
|---:|---|---|---|---|
| 1 | Nguyễn Văn Cường | 2A202603750 | Phụ trách Problem Card, vẽ quy trình & đồng viết báo cáo | nvcuong96 |
| 2 | Hiếu | (Điền MSSV) | Phụ trách Research giải pháp & tổng hợp dữ liệu | (GitHub) |
| 3 | Hải | (Điền MSSV) | Người phản biện chính, kiểm chứng rủi ro | (GitHub) |
| 4 | Khôi | (Điền MSSV) | Điều phối thời gian, chốt Problem Statement v1 | (GitHub) |

Không ghi email hay số điện thoại vào bảng này, vì repo có thể để public.

Gợi ý vai trò (một người có thể giữ nhiều vai): điều phối thời gian, ghi chép, người phản biện chính, phụ trách kiểm chứng (phỏng vấn/survey), phụ trách research, vẽ quy trình, viết Problem Statement.

## Phân công theo checkpoint

| Checkpoint | Người chính | Người hỗ trợ | Sản phẩm |
|---|---|---|---|
| CP3 — Hội tụ nhóm | Cường | Khôi | Cluster, cây OST, bảng chấm điểm |
| CP4 — Kiểm chứng | Hải | Hiếu | Assumption map, tổng hợp báo chí điều tra & nghiên cứu ACM |
| CP4 — Research | Hiếu | Cường | Bảng research giải pháp có link (Uber, Zendesk) |
| CP5 — Quy trình trước/sau | Cường | Khôi | Quy trình 6 bước → 4 bước + bảng before/after |
| CP5 — Problem Statement v0 | Khôi | Cường | Problem Statement v0 |
| CP6 — Mức can thiệp + Problem Statement v1 | Cường | Hải | Ma trận độ mơ hồ, AI Canvas, 4 tiêu chí eval, Problem Statement v1 |
| CP6 — Quyết định | Khôi | Cả nhóm | 4 rủi ro + quyết định Go phạm vi nhỏ & ngưỡng dừng |

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
- Đặt câu hỏi phản biện sâu cho bài của Hải (*Hơn gì ChatGPT*) và bài của Khôi (*Dữ liệu OBD-II mơ hồ thì AI gợi ý phụ tùng có sai lệch không*).
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
