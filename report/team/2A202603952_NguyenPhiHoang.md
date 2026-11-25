# Báo cáo cá nhân — Nguyễn Phi Hoàng

## 1. Thông tin thành viên

- Họ tên: Nguyễn Phi Hoàng
- MSSV: 2A202603952
- Email: [... điền email vinuni.edu.vn]
- Vai trong nhóm: **Người kiểm số** kiêm **Người gắn nhãn 1**

## 2. Phần việc phụ trách

- Kiểm số cho nhiệm vụ A, B: dựng môi trường trên máy cá nhân, chạy lại `src/lab13.py`, đối chiếu ba phép thử A1 và toàn bộ bảng A2–B4 với số đã commit và với số tham khảo trong tài liệu.
- Gắn nhãn 1 ở nhiệm vụ C: gắn nhãn độc lập 20 ca lỗi, không trao đổi với người gắn nhãn 2.
- So nhãn, phân xử 2 ca không trùng, đối chiếu bảng nhãn tham khảo, điều chỉnh 5 ca kèm lý do; hoàn thiện `report/team/bang_loi.md`.
- Trích 20 ca lỗi từ file đề docx ra `docs/20_ca_loi.md` cho hai người gắn nhãn dùng chung.
- Hỗ trợ phần hành chính: đồng đóng góp chi tiết vào `TEAM.md`, `report/team/group_report.md`.

## 3. Đóng góp cụ thể

- **Kiểm số CP1–CP2:** máy không có `py -3` như hướng dẫn cài đặt → dựng `.venv` bằng `python -m venv`, cài `requirements.txt`. Chạy `python lab13.py`: ba phép thử ĐẠT (1,20 · 1,25 · 1,25); bảng A2/B khớp từng con số với `report/team/bang_chi_phi.md` đã commit; B4 là 12.415 đ so với số tham khảo 12.414 đ trong hướng dẫn (lệch 0,001%, do hướng dẫn cắt phần thập phân của 12.414,8) — cùng kết luận 1,03×.
- **Tính tay đối chiếu:** A1 tính tay theo công thức (1 − (1 − p)^k) ÷ p với p = 0,8: k=2 → 1,20; k=None → 1,25; hệ số chi phí k=3 → 1,25 — trùng code.
- **Gắn nhãn 20 ca độc lập** trong 8 phút, tách chỗ, không trao đổi; kết quả trùng người gắn nhãn 2 ở 18/20 ca (đồng thuận 90%).
- **Phân xử 2 ca không trùng:** ca 4 → Giới hạn hệ thống (trợ lý làm đúng thiết kế, gốc là LogiX không có dữ liệu); ca 12 → Ngầm (không có đầu vào của khách sai, "sai" là chi phí gấp 3 lần 3 tuần không ai thấy).
- **Đối chiếu đáp án và điều chỉnh 5 ca** (5→Ngầm, 6→Do người dùng, 13→Giới hạn, 16→Ngữ cảnh, 20→Hệ thống), mỗi ca ghi một câu lý do vào mục "Điều chỉnh sau đối chiếu đáp án".

## 4. Bằng chứng

- Commit `6df3dd6` "feat: complete CP3 error labels and remediation table" (push lên main): https://github.com/hoan11052004/K5-L3B-DAY13-3boy-LaunchEconomics/commit/6df3dd6
- `report/team/bang_loi.md`: cột "Nhãn người 1", mục "Quy tắc phân biệt cho các ca không trùng", mục "Điều chỉnh sau đối chiếu đáp án".
- `docs/20_ca_loi.md`: phiếu 20 ca tôi trích từ đề bài cho hai người gắn nhãn.
- Output `python lab13.py` trên máy cá nhân (venv) in "Ba phép thử đáp án biết trước: ĐẠT".

## 5. Công cụ AI đã dùng

- Công cụ: trợ lý AI (OpenCode/GLM) trong phiên làm việc nhóm.
- Dùng vào: giải thích khái niệm (công thức cỡ mẫu cụm, hệ số thiết kế), soát lỗi cài đặt (lỗi `py -3` không có, thiếu pandas), nháp định dạng file báo cáo (`bang_loi.md`, `group_report.md`, phiếu `20_ca_loi.md`), và gợi ý cấu trúc bộ câu hỏi duyệt chéo.
- **Tự kiểm tra:** mọi nhãn lỗi do tôi gắn thật, độc lập với người gắn nhãn 2, và bộ nhãn của tôi đã chốt trước khi xem bảng nhãn tham khảo trong tài liệu; mọi con số tôi đều chạy lại từ `src/lab13.py` trên máy mình và tính tay lại A1; sau khi AI nháp file, tôi đọc duyệt từng dòng và chỉnh trước khi commit. Không dùng AI để bịa nhãn hay bịa số.

## 6. Tự đánh giá

- Điểm mạnh: kiểm soát được luồng làm bài theo 5 checkpoint; số liệu CP1–CP3 được xác minh độc lập trên máy thứ hai nên nhóm chắc chắn số đúng trước khi làm tiếp; phần CP3 làm đúng quy trình hai bộ nhãn độc lập.
- Cần cải thiện: phần D (statsmodels) do thành viên khác phụ trách nên tôi mới đọc hiểu ở mức đối chiếu kết quả, chưa tự viết code D1; muốn tự tay chạy lại phần cỡ mẫu để bảo vệ trọn vẹn khi hội đồng hỏi sâu.
