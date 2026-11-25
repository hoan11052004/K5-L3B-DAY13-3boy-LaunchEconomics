# Báo cáo cá nhân — Nguyễn Công Hoàn

## 1. Thông tin thành viên

- Họ tên: Nguyễn Công Hoàn
- MSSV: 2A202603972
- Email: 26ai.hoannc@vinuni.edu.vn
- Vai trong nhóm: Người viết code; gắn nhãn lỗi 2

## 2. Phần việc phụ trách

- Phụ trách CP1 (Nhiệm vụ A): mô hình chi phí mỗi việc thành công.
- Phụ trách CP2 (Nhiệm vụ B): bảng độ nhạy và các kịch bản giới hạn chạy lại.
- Hỗ trợ gắn nhãn độc lập 20 ca lỗi ở CP3 với vai trò người gắn nhãn 2.

## 3. Đóng góp cụ thể

- Hoàn thiện ba hàm A1 trong `src/lab13.py`: số lần chạy kỳ vọng, tỷ lệ thành công và hệ số chi phí mỗi việc thành công; kiểm tra đạt các mốc `1,20 · 1,25 · 1,25`.
- Hoàn thiện `mo_hinh()` để tính tiền token và tool trên mọi lần chạy, tiền xem lại/làm lại từ các cột `_simulated`, tổng chi phí, số việc thành công và CPS.
- Hoàn thiện phần tính A3 theo bốn loại yêu cầu và A4 với chi phí cố định 40 triệu đồng/tháng cho phạm vi `noi_dia + hang_nang`.
- Hoàn thiện CP2: chín kịch bản B1, kịch bản kết hợp B2, ba giới hạn chạy lại ở B3 và xem lại 100% ở B4.
- Điền `report/team/bang_chi_phi.md` bằng kết quả tính từ hai file CSV; ghi nhãn `simulated` cho các số dùng phút nhân viên giả lập.

## 4. Bằng chứng

- Commit hoàn thiện CP1–CP2: [`ba3fc74`](https://github.com/hoan11052004/K5-L3B-DAY13-3boy-LaunchEconomics/commit/ba3fc74d99dad4b70ebb01185450e1aa9e15ff89).
- File code: `src/lab13.py`.
- File báo cáo: `report/team/bang_chi_phi.md`.
- Kết quả đối chiếu chính: A2 có tổng chi phí `4.373.585 đ`, `978` việc thành công và CPS khoảng `4.472 đ`; B2 có CPS khoảng `6.543 đ`; giới hạn 2 lần có chi phí cả hệ thống thấp nhất.
- Khi kiểm tra, ba phép thử A1 in `ĐẠT`; các kịch bản không làm thay đổi hai DataFrame dữ liệu đầu vào.

## 5. Công cụ AI đã dùng

- Dùng ChatGPT/Codex để giải thích công thức CP1–CP2, gợi ý cấu trúc hàm, rà soát lỗi và kiểm tra tính nhất quán của báo cáo.
- Tự kiểm tra bằng cách chạy `src/lab13.py`, đối chiếu các số A1–A4/B1–B4 với tài liệu hướng dẫn, kiểm tra các trường hợp giới hạn chạy lại và xác nhận dữ liệu CSV không bị sửa.
- Không dùng AI để tạo dữ liệu; mọi con số trong báo cáo được tính từ `src/lab13.py` và hai file CSV của bài.

## 6. Tự đánh giá

Tôi hoàn thành phần code và báo cáo CP1–CP2, hiểu cách phân biệt chi phí trợ lý với chi phí toàn hệ thống và lý do phải tính cả lần chạy lỗi. Tôi cũng hiểu rằng CP2 cho thấy chi phí xem lại/làm lại quan trọng hơn giá token, nên pilot cần theo dõi các chỉ số này.
