# Phiếu chấm hội đồng Gate 2a

Nhóm số n chấm nhóm số n + 1; nhóm cuối chấm nhóm 1. Chấm theo bằng chứng trong hồ sơ, không theo cách trình bày: một đề xuất No-go có lý do bằng số được điểm cao hơn một đề xuất Go bỏ qua con số bất lợi.

- Nhóm chấm (hội đồng):  MintTea 
- Nhóm được chấm: 3boy

> **Bản chấm giả định:** lập từ hồ sơ 3boy theo kịch bản MintTea làm hội đồng; không phải kết quả duyệt chéo thực tế hoặc xác nhận của MintTea.

| Tiêu chí | 0 điểm | 5 điểm | 10 điểm | Điểm | Lý do (có số) |
| --- | --- | --- | --- | ---: | --- |
| Đề xuất khớp bằng chứng | Mâu thuẫn với số của chính nhóm | Khớp nhưng bỏ qua một con số bất lợi | Khớp, nêu cả con số bất lợi và cách xử lý | 10 | Go có điều kiện nêu rủi ro xem lại 100% có CPS 11.743–12.414 đ (simulated), và yêu cầu đo thời gian thực, giảm xem lại theo điều kiện. |
| Số giả lập và phạm vi | Không nhãn; phạm vi "mọi yêu cầu" | Có nhãn hoặc có thu hẹp phạm vi | Nhãn ở mọi số giả lập; phạm vi thu hẹp có lý do bằng số | 10 | Hồ sơ đánh dấu các mục chi phí là giả lập; phạm vi chỉ `noi_dia` và `hang_nang`, loại `quoc_te` có CPS 1,88 lần 12.000 đ (simulated). |
| Pilot ra được quyết định | Không đối chứng hoặc thiếu cỡ mẫu | Đủ cỡ mẫu, luật dừng chung chung | Tách được tác động, đủ mẫu, luật dừng có ngưỡng, thời hạn, người có quyền dừng | 5 | Có đối chứng ngẫu nhiên 20 nhân viên/nhóm, 3 luật dừng và mục tiêu ≥ 299 yêu cầu/người; chưa chứng minh đạt khối lượng này trong thời gian đo sau rollout. Điểm 5 là đánh giá thận trọng, cần nhóm làm rõ tính khả thi. |
| **Tổng** | | | | **25 / 30** | Chấm giả định theo hồ sơ hiện có. |

**Quyết định giả định:** Go có điều kiện cho kế hoạch pilot.

**Lý do:** CPS 4.472 đ (simulated) chưa gồm toàn bộ chi phí xử lý các ca thất bại; rủi ro xem lại 100% có thể đưa CPS lên khoảng 12.414 đ (simulated). Cần xác nhận đủ mẫu và thời gian theo dõi, đo phút nhân viên thực tế và hoàn thành cơ chế chống hoàn trùng trước khi chạy pilot.

**Một câu hỏi cho đội trình:** Sau ba bước , nhóm có bao nhiêu tuần và bao nhiêu yêu cầu đủ điều kiện mỗi nhân viên để đạt ít nhất 299 yêu cầu/người, đồng thời theo dõi mở lại đủ 7 ngày trước ngày quyết định 05/01/2027?

**Câu trả lời mẫu của đội trình**: Trước khi chạy pilot, nhóm sẽ ước tính lượng yêu cầu đủ điều kiện theo từng nhân viên, chốt thời gian thu mẫu và dời ngày quyết định nếu cần; nếu không đủ mẫu, nhóm sẽ báo cáo kết quả là chưa đủ bằng chứng thay vì kết luận tác động.
