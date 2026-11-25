# Báo cáo nhóm

Báo cáo ngắn, tối đa 2 trang. Số liệu chi tiết nằm trong các file hồ sơ; ở đây chỉ dẫn lại con số chính.

## 1. Thông tin nhóm

- Tên nhóm: **3boy** · Lớp: **L3B**
- Thành viên: xem `TEAM.md` (nhóm 3 người, gộp bốn vai của lab)

## 2. Mục tiêu và cách tiếp cận

Trả lời bốn câu hỏi của Gate 2a: chi phí mỗi việc thành công có đáng không, nhân viên có dùng không, hỏng thì sao, pilot có ra được quyết định không. Cách tiếp cận: một người giữ chuỗi code tuần tự A1 → `mo_hinh()` → độ nhạy → cỡ mẫu (vì B, D dùng lại cùng một hàm); hai người còn lại gắn nhãn lỗi và lo phần chữ song song; mọi số trong hồ sơ lấy trực tiếp từ output `src/lab13.py`, số từ cột `_simulated` đều ghi nhãn.

## 3. Giải pháp

- **A · Mô hình chi phí** ([bang_chi_phi.md](team/bang_chi_phi.md)): ba hàm A1 đạt đáp án biết trước (1,20 · 1,25 · 1,25); `mo_hinh()` cộng token/tool trên mọi lần chạy kể cả lỗi, mẫu số chỉ đếm việc thành công; tách theo `loai` và cộng chi phí cố định 40 triệu đ/tháng cho phạm vi `noi_dia` + `hang_nang`.
- **B · Độ nhạy** ([bang_chi_phi.md](team/bang_chi_phi.md)): gọi lại `mo_hinh()` cho 9 kịch bản; kiểm tra tuyến tính bằng assert ngay trong code.
- **C · Bảng lỗi** ([bang_loi.md](team/bang_loi.md)): hai bộ nhãn độc lập 20 ca, đồng thuận 90%, quy tắc phân biệt cho 2 ca không trùng, đối chiếu đáp án và điều chỉnh 5 ca kèm lý do; bảng khắc phục đủ năm loại, mỗi dòng có event đo được và một vai trò phụ trách.
- **D · Pilot plan** ([pilot_plan.yaml](team/pilot_plan.yaml)): chia theo nhân viên (20 cụm mỗi nhóm), đánh đổi MDE 6 điểm với cỡ mẫu 859/nhóm (m ≥ 299 yêu cầu/người, DE = 6,96), random có phân tầng theo depot, 3 luật dừng đủ bốn vế NẾU–TRONG–THÌ–KHÔNG THÌ, người có quyền dừng là Giám đốc vận hành.
- **E · Chỉ số, rủi ro, hồ sơ launch v0** ([chi_so.md](team/chi_so.md), [ho_so_launch_v0.md](team/ho_so_launch_v0.md)): 3 chỉ số tính thử từ dữ liệu (82,83% · 27,12% · 4,25%) + 2 chỉ số tự đề xuất, 10 event có `trace_id`, 3 dòng rủi ro lấy số từ bảng độ nhạy; hồ sơ 7 mục, đề xuất **Go có điều kiện** kèm 5 điều kiện có người phụ trách và ngày kiểm tra.

## 4. Kết quả

- Chi phí mỗi việc thành công: **4.472 đ (simulated)**, gấp 16,3 lần hóa đơn token mỗi yêu cầu, nhưng chỉ **0,37×** mức 12.000 đ khi nhân viên tự làm (CPS + cố định, khối lượng 45.000 yêu cầu/tháng, simulated). Nhiệm vụ A.
- Ba yếu tố nhạy nhất (simulated): **số ca làm lại (+51,8%) · tỉ lệ xem lại (+40,7%) · lương nhân viên (+23,1%)**. Nhiệm vụ B.
- Quốc tế (`quoc_te`) không đáng xử lý: CPS 22.515 đ (simulated), 1,88× mức tự làm → phạm vi đề xuất `noi_dia` + `hang_nang`. Nhiệm vụ A.
- Xem lại 100% cho phạm vi đề xuất: CPS lên **11.743–12.415 đ (0,98–1,03×, simulated)** — gần hòa/đắt hơn nhân viên tự làm → pilot phải học được tỉ lệ xem lại giảm an toàn tới đâu. Nhiệm vụ B.
- Lỗi: đồng thuận gắn nhãn **90%**, khớp đáp án **20/20** sau đối chiếu; năm loại đều có cách phát hiện đo được. Nhiệm vụ C.
- Lỗi: đồng thuận gắn nhãn **90%**, khớp đáp án **20/20** sau đối chiếu; năm loại đều có cách phát hiện đo được. Nhiệm vụ C.
- Pilot: chia theo nhân viên, chỉ phát hiện được mức chênh **≥ 6 điểm** với power 0,8 (859 yêu cầu/nhóm, DE = 6,96, m ≥ 299/người); nếu hiệu quả thật chỉ 5 điểm, power giảm còn **0,64** — đánh đổi đã ghi rõ trong file. Tỉ lệ mở lại trong 7 ngày hiện tại **4,25%**; luật an toàn dừng nếu vượt trần 6% hoặc cao hơn đối chứng ≥ 2 điểm. Nhiệm vụ D.
- Chỉ số trong đợt chạy thử (simulated): chính **82,83%** · bỏ qua gợi ý **27,12%** · lỗi lọt đến khách **4,25%**. Đề xuất cuối: **Go có điều kiện** (5 điều kiện, mỗi điều kiện có vai trò phụ trách và ngày kiểm tra). Nhiệm vụ E.

## 5. Khó khăn và cách xử lý

- **Môi trường Windows:** không có `py -3` (lệnh trong `src/README.md`), Python hệ thống thiếu pandas → dựng `.venv` bằng `python -m venv` rồi `pip install -r requirements.txt`; thêm `sys.stdout.reconfigure(encoding='utf-8')` để in tiếng Việt không lỗi mã hoá. Bằng chứng: lệnh đã chạy và output lưu trong buổi.
- **Nhóm 3 người so với 4 vai của lab:** gộp vai (người kiểm số kiêm gắn nhãn 1, người gắn nhãn 2 kiêm giữ hồ sơ); hai bộ nhãn CP3 vẫn gắn độc lập đúng luật.
- **Đề bài 20 ca nằm trong file docx khó đọc khi gắn nhãn song song:** trích 20 ca ra `docs/20_ca_loi.md` cho hai người gắn nhãn dùng chung; không sửa hai file CSV dữ liệu.

## 6. Tổng hợp đóng góp

Chi tiết đóng góp của từng thành viên nằm trong `TEAM.md`.

## 7. Hạn chế và hướng cải thiện

- Đợt chạy thử không có nhóm đối chứng nên chỉ được viết "chỉ số trong đợt chạy thử là…", chưa kết luận nâng chỉ số; mọi số phút nhân viên là **simulated** từ hai cột `_simulated`.
- Bảng khắc phục mới dừng ở năm ca đại diện; pilot cần đo đủ 10 event (đặc biệt `input_validation_failed`, `handoff_to_staff`, đối soát sổ cái) mới tin được các ngưỡng.
- Pilot chỉ phát hiện được mức chênh từ 6 điểm trở lên; nếu trợ lý chỉ nâng 5 điểm, xác suất phát hiện giảm còn 0,64 — đã ghi rõ trong phần đánh đổi của `pilot_plan.yaml`.
- Số phút xem lại/làm lại hiện là **simulated**; hồ sơ launch v0 đã đặt điều kiện đo thật (đồng hồ CSKH) ngay tuần đầu của bước rollout 0.10 trước khi thay thế.

## 8. Tài liệu tham khảo

- Erol và cộng sự, *Cost-of-Pass: An Economic Framework for Evaluating Language Models*, [arxiv.org/abs/2504.13359](https://arxiv.org/abs/2504.13359)
- Google PAIR, *People + AI Guidebook*, chương "Errors + Graceful Failure", [pair.withgoogle.com](https://pair.withgoogle.com)
- Tài liệu statsmodels, lớp `NormalIndPower` (mục `stats.power`)
