---
name: hoc-ke-hoach
description: Lập kế hoạch học (giai đoạn 2 của phương pháp LearnHarness). Từ kết quả đo và mục tiêu, dựng bản đồ phụ thuộc tối thiểu bằng mermaid, đi từ các sự thật vô điều kiện đến mục tiêu, trình bày cho người học và chờ đồng ý trước khi dạy. Dùng sau hoc-do, hoặc khi người dùng muốn xem, sửa lộ trình học.
---

# Kế hoạch

Đọc `../hoc/references/nguyen-tac.md` trước. Đọc `muc-tieu.md` và `nguoi-hoc.md` của chủ đề.

## Suy nghĩ kỹ ở đây

Đây là bước có đòn bẩy lớn nhất. Đừng vội. Với trình độ và mục tiêu đã có, hãy thật sự suy luận cách tốt nhất để dạy *điều này* cho *người này*:

- Phác lĩnh vực từ hiểu biết của bạn: khái niệm cốt lõi, nguyên lý nền thật sự, cách trình bày chuẩn, bẫy thường gặp. Chỗ nào bức tranh của bạn chưa rõ thì kiểm tra (tài liệu người học, tìm web) ngay lúc này.
- Bài học này dựa trên những **sự thật vô điều kiện** nào? Lĩnh vực có một mệnh đề phổ quát gọn ("mọi X đều thông qua ___") không?
- Người học đã nắm những gì (theo `nguoi-hoc.md`)? Xây từ đó, không thấp hơn, không cao hơn.
- **Cây tối thiểu**: không dạy lại điều họ đã nắm, không dạy điều không nằm trên đường đến mục tiêu dù hay đến đâu, đường suy luận ngắn nhất có thể.
- Con đường khám phá có động cơ từ nền đến mục tiêu là gì? Mỗi bước từ đâu ra, vì sao ai đó lại nghĩ đến nó?
- Mỗi đoạn nên dạy kiểu Socratic (để họ tự suy ra) hay kể giải (bạn dẫn dắt)?

## Kiểm tra gốc trước khi trình bày

Với mỗi nút bạn coi là nền: nó có thật là sự thật vô điều kiện *với người này* không, hay là một định lý trá hình suy ra từ điều đơn giản hơn? Nếu nó suy ra được thì đẩy xuống và mở rộng bản đồ. Một gốc sai làm hỏng mọi thứ treo trên nó.

## Viết bản đồ

Ghi `ban-do.md` theo mẫu trong `../hoc/references/du-an.md`:

- `graph TD`. Nút là **mốc cấu trúc** (sự thật nền ở dưới, các trạm chính, mục tiêu ở cuối), không phải từng lượt dạy. Một nút có thể cần một bước hoặc năm bước suy luận.
- `A --> B`: phải hiểu A trước B.
- Không giới hạn số nút: bản đồ chi tiết bao nhiêu tùy môn học cần. Thứ giữ bản đồ dễ đọc là cấu trúc đúng, không phải nén bớt.
- Nhãn ngắn. Bản đồ là bản đồ, không phải lãnh thổ.

## Trình bày: luôn luôn, trước khi dạy

1. **Cách tiếp cận, bằng văn xuôi** (vài câu): học gì, theo thứ tự nào, và vì sao như vậy, dựa trên biên của họ và điều họ muốn đạt.
2. **Bản đồ**: một khối mermaid (lần duy nhất bạn vẽ nó trong tin nhắn). Nếu môi trường không hiển thị mermaid, kèm danh sách thụt lề ngắn.
3. Hỏi họ có đồng ý không, hoặc muốn đổi gì. **Dừng lượt.** Không dạy trong lượt trình bày.

Họ muốn sửa thì sửa bản đồ và trình bày lại. Khi họ đồng ý: đổi `Giai đoạn: day`, ghi `Nút đang học:` là nút nền đầu tiên, ghi nhật ký, rồi gọi `hoc-day`.

## Bản đồ thay đổi theo người học

Bản đồ là giả thuyết. Dữ liệu thật đến trong lúc dạy. Khi `hoc-day` phát hiện nền bị thiếu, hiểu lầm sâu hơn dự kiến, hoặc người học đã nắm sẵn một đoạn, thì sửa `ban-do.md` (thêm, bỏ, đổi cạnh) và ghi một dòng vào "Lịch sử thay đổi". Các lần sửa giữa chừng không cần trình bày lại, chỉ nói một câu cho họ biết.
