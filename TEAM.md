# Team

## Thông tin nhóm

- Tên nhóm: 3boy
- Lớp: L3B
- Repo nhóm: `K5-L3B-DAY13-3boy-LaunchEconomics` (xem [SUBMISSION.md](SUBMISSION.md))
- URL repo, nhánh nộp, commit chốt: https://github.com/hoan11052004/K5-L3B-DAY13-3boy-LaunchEconomics, nhánh `main` (nhánh làm việc: `AnhQuanHANU`)

## Thành viên

| STT | Họ tên | MSSV | Email | GitHub | Vai trò |
| --: | ------ | ---- | ----- | ------ | ------- |
|   1 | Nguyễn Anh Quân | 2A202603892 | 2A202603892@vinuni.edu.vn | AnhQuanHANU | Người giữ hồ sơ, Phụ trách Kế hoạch Pilot (D) & Hồ sơ Launch v0 (E) |
|   2 | Nguyễn Công Hoàn | (cập nhật) | (cập nhật) | hoan11052004 | Người viết code & Gắn nhãn lỗi 2 (A, B, C) |
|   3 | Nguyễn Phi Hoàng | 2A202603952 | (cập nhật) | phihoang1709 | Người kiểm số & Gắn nhãn lỗi 1 (A, B, C) |

Bốn vai của lab:

- **Người viết code:** viết và chạy `src/lab13.py`.
- **Người kiểm số:** tính tay một con số để đối chiếu, điền bảng.
- **Người gắn nhãn 1:** đọc đề, theo dõi điều kiện "Xong khi"; gắn nhãn 20 ca độc lập ở CP3.
- **Người gắn nhãn 2, kiêm giữ hồ sơ:** điền `report/team/ho_so_launch_v0.md` từ đầu buổi; gắn nhãn 20 ca độc lập ở CP3.

Đổi người viết code sau giờ giải lao, để ít nhất hai người trong nhóm tự tay tính được chi phí.

## Cá nhân

Mỗi thành viên đồng thời tạo một báo cáo riêng trong `report/` theo dạng:

```text
report/team/MSSV_HoTen.md
```

Ví dụ: `report/team/20241234_NguyenVanAn.md`.

Sao chép mục dưới đây cho từng thành viên.

## NguyenAnhQuan-2A202603892

### Phần việc phụ trách

- Phụ trách toàn diện Nhiệm vụ D (Kế hoạch Pilot, cỡ mẫu, luật dừng) và Nhiệm vụ E (Chỉ số, Rủi ro kinh tế, Hồ sơ Launch v0).

### Đóng góp cụ thể

- Tính toán 5 bài toán cỡ mẫu D1 và giải bất phương trình $m \ge 299$, chứng minh tính không khả thi của MDE 5% với 40 nhân viên và đề xuất đánh đổi MDE 6% ($n = 859$).
- Hoàn thiện `report/team/pilot_plan.yaml` với 3 luật dừng chuẩn cú pháp `NẾU – TRONG – THÌ – KHÔNG THÌ`.
- Soạn thảo `report/team/chi_so.md` (3 chỉ số từ dữ liệu, 2 chỉ số đề xuất mới, 10 trace events có `trace_id`, 3 rủi ro kinh tế).
- Đóng gói bản Hồ sơ Launch v0 1 trang tại `report/team/ho_so_launch_v0.md` với đề xuất Go có điều kiện (5 điều kiện cụ thể).

### Bằng chứng

- File `report/team/pilot_plan.yaml`, `report/team/chi_so.md`, `report/team/ho_so_launch_v0.md`, `report/team/2A202603892_NguyenAnhQuan.md`.

## NguyenCongHoan-MSSV (cập nhật)

### Phần việc phụ trách

- Viết và chạy `src/lab13.py` cho CP1–CP2 (ba hàm A1, `mo_hinh`, `tao_bao_cao`); điền `report/team/bang_chi_phi.md`.
- Gắn nhãn độc lập 20 ca lỗi ở CP3 (người gắn nhãn 2).

### Đóng góp cụ thể

- Commit `ba3fc74`: hoàn thiện code và bảng chi phí nhiệm vụ A, B; `python lab13.py` in ba phép thử ĐẠT (1,20 · 1,25 · 1,25).
- Bộ nhãn 20 ca độc lập, trùng 18/20 với người gắn nhãn 1 (đồng thuận 90%).

### Bằng chứng

- https://github.com/hoan11052004/K5-L3B-DAY13-3boy-LaunchEconomics/commit/ba3fc74
- `report/team/bang_loi.md` (cột "Nhãn người 2")

## NguyenPhiHoang-2A202603952

### Phần việc phụ trách

- Kiểm số: chạy xác minh lại CP1–CP2 trên máy cá nhân, tính tay A1 đối chiếu; duyệt chéo số CP4/CP5 sau khi gộp.
- Gắn nhãn độc lập 20 ca lỗi ở CP3 (người gắn nhãn 1); so nhãn, đối chiếu đáp án, hoàn thiện `report/team/bang_loi.md`.

### Đóng góp cụ thể

- Dựng môi trường (venv, pandas/statsmodels) và xác minh ba phép thử + toàn bộ bảng A, B khớp số đã commit (sai số so với hướng dẫn ~0,001%).
- Bộ nhãn 20 ca độc lập; phân xử 2 ca không trùng (ca 4, ca 12); điều chỉnh 5 ca sau đối chiếu bảng tham khảo kèm câu lý do; trích 20 ca đề bài ra `docs/20_ca_loi.md` cho hai người gắn nhãn. Commit `6df3dd6`.

### Bằng chứng

- https://github.com/hoan11052004/K5-L3B-DAY13-3boy-LaunchEconomics/commit/6df3dd6
- `report/team/bang_loi.md` (cột "Nhãn người 1", mục "Điều chỉnh sau đối chiếu đáp án")

*Lưu ý liêm chính: nhóm có dùng trợ lý AI (OpenCode/GLM) để giải thích khái niệm, soát lỗi và nháp định dạng file theo RULES.md cho phép; mọi nhãn lỗi do hai thành viên gắn thật và độc lập, mọi con số do `src/lab13.py` tính ra. Mỗi thành viên ghi chi tiết công cụ AI và cách tự kiểm tra trong báo cáo cá nhân của mình.*
