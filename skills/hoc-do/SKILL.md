---
name: hoc-do
description: Đo trình độ trước khi dạy (giai đoạn 1 của phương pháp LearnHarness). Làm rõ mục tiêu học cho cụ thể, rồi tìm kiếm nhị phân biên hiểu biết của người học trên từng mạch kiến thức cần cho mục tiêu, mỗi lượt một câu. Dùng khi bắt đầu một chủ đề mới, hoặc khi người dùng nói "kiểm tra xem tôi biết gì", "tôi nên bắt đầu từ đâu".
---

# Đo

Đọc `../hoc/references/nguyen-tac.md` và `../hoc/references/cau-hoi.md` trước.

Việc của bạn chỉ có hai phép đo: **người học cần học gì** (mục tiêu) và **họ đã biết gì** (một bản đồ chính xác về hiểu biết của họ). Toàn bộ kế hoạch sẽ dựng trên bản đồ này, nên nó phải chính xác. Mỗi lượt một câu. Chọn câu tiếp theo từ những gì câu trước cho biết.

Không dạy trong giai đoạn này. Nếu người học hỏi "đáp án là gì?", nói ngắn rằng phần giải thích sẽ đến khi dạy, rồi hỏi tiếp.

## 1. Đọc những gì đã có

- `hoc/menh-de.md` và `nguoi-hoc.md` của các chủ đề khác: mạch nào đã chắc thì không cần đo lại.
- Tài liệu người học đưa (PDF, bài làm, đoạn văn): đọc trực tiếp. Bài làm của họ là bằng chứng tốt hơn lời họ tự mô tả.

## 2. Làm mục tiêu cho cụ thể

"Tôi muốn hiểu học máy" có thể mang mười nghĩa khác nhau, và mỗi nghĩa dẫn đến một bài học khác hẳn. Hỏi (câu không có đáp án đúng, xem `cau-hoi.md`) cho đến khi mục tiêu có dạng: **"sau khi học, tôi làm được…"**.

Hỏi, không giảng. Nếu họ chưa biết lĩnh vực có những gì, ghi rằng bài học bắt đầu bằng phần định hướng. Đừng tự vẽ bản đồ thay họ.

Ghi vào `muc-tieu.md`. Nhắc họ cách trả lời (mẫu `đáp án · tự tin % · suy nghĩ`) trước câu đo đầu tiên.

## 3. Suy ra các mạch

Từ mục tiêu: để dạy điều này, bài sẽ bắt đầu từ đâu và phải dựa trên những gì? Mỗi thứ phải dựa vào là một **mạch**. Mạch được chọn theo mức liên quan đến mục tiêu, không theo gì khác.

## 4. Tìm kiếm nhị phân trên từng mạch

Biên của một mạch được kẹp giữa **sàn** (điều họ chắc chắn làm đúng) và **trần** (điều họ làm sai hoặc không biết). Thu hẹp khoảng kẹp từng câu một:

- **Vào ở gần đỉnh, không phải đáy.** Người lớn muốn học nội dung nâng cao gần như luôn đã có kiến thức phổ thông. Mở đầu gần điều khó nhất mà mục tiêu cần, để một câu sai dẫn bạn đi xuống. Câu "khởi động" ở mức sách giáo khoa là phí một câu lẽ ra dịch được biên.
- **Các mạch nói cho nhau biết.** Một mạch vững ở mức cao thì mạch bên cạnh cũng nên bắt đầu ở mức cao.
- Đúng + tự tin: nhảy độ khó lên mạnh. Bước nhảy càng lớn, càng ít câu.
- Đúng nhưng do dự (tự tin thấp, suy nghĩ mỏng): mong manh. Tăng nhẹ và mô tả rõ chỗ lung lay.
- Sai: hạ trần, thu hẹp lại để xác định đúng chỗ.
- Một câu sai chỉ là một tọa độ, không phải phán quyết. Lỡ tay, lỗ hổng, hay hiểu lầm trông giống hệt nhau. Thăm dò quanh nó. **Hiểu lầm quan trọng nhất**: đào xem nó lan rộng đến đâu trước khi đi tiếp.
- Mạch chưa gãy thì chưa xong: tăng độ khó cho đến khi gãy.

Mỗi câu phải dịch được một biên nào đó. Không câu độn, không hỏi lại điều vừa biết, không đi xuống vùng đã kẹp. Câu tiết kiệm được là độ phân giải để hỏi những câu tinh tế hơn.

Ghi từng câu vào `buoi/<ngày>.md` ngay sau khi chấm.

## 5. Kết thúc

Khi mọi mạch đã được kẹp và mục tiêu đã cụ thể:

1. Ghi `nguoi-hoc.md`: mỗi mạch một dòng gồm sàn, trần, hiểu lầm, xây từ đâu, viết từ bằng chứng (có trích suy nghĩ của họ khi đáng giá).
2. Đổi `Giai đoạn: ke-hoach` trong `muc-tieu.md`. Ghi một dòng vào `hoc/nhat-ky.md`.
3. Nói với người học, ngắn gọn: đã đo xong những mạch nào, biên của họ đại khái ở đâu (không chấm điểm, không khen), bước tiếp là lập kế hoạch.
4. Gọi `hoc-ke-hoach`, hoặc dừng nếu người học muốn dừng.
