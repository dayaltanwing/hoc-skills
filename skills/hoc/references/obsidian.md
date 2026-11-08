# Ghi khái niệm vào Obsidian

Khi người học đã **thật sự rõ** một khái niệm, skill tự ghi khái niệm đó thành một ghi chú trong vault Obsidian của họ. Obsidian chỉ là một thư mục chứa file `.md`, nên skill ghi file thẳng vào đó, không cần plugin hay MCP.

## Cấu hình

Đường dẫn vault được lưu trong `hoc/cau-hinh.md` của thư mục học (xem `du-an.md`). Dòng `Obsidian vault:` để trống, hoặc ghi `tắt`, thì bỏ qua mọi bước trong file này.

Thiết lập (`/hoc obsidian`, hoặc lần đầu một khái niệm sắp được ghi mà chưa có cấu hình):
1. Đọc danh sách vault trong `~/Library/Application Support/obsidian/obsidian.json` (macOS), `%APPDATA%\obsidian\obsidian.json` (Windows), hoặc `~/.config/obsidian/obsidian.json` (Linux). Mỗi vault có một `path`.
2. Hỏi người học chọn vault nào (khuyên dùng vault đang mở, `"open": true`), hoặc tắt tính năng. Không tự chọn.
3. Ghi vào `hoc/cau-hinh.md`: đường dẫn vault, thư mục gốc trong vault (mặc định `Học`).

Vault nằm ngoài thư mục học, nên Claude Code sẽ hỏi quyền khi ghi lần đầu. Nói với người học một lần: muốn khỏi bị hỏi thì mở phiên bằng `claude --add-dir "<vault>"`, hoặc thêm vault vào `permissions.additionalDirectories` trong `.claude/settings.json` của thư mục học.

## Khi nào ghi

"Rõ" nghĩa là **đã được kiểm chứng**, không phải "đã được giảng":

| Sự kiện | Việc ghi |
|---|---|
| Câu kiểm tra đầu tiên của một nút trên bản đồ được trả lời **đúng** (đúng thật, không phải đúng với tự tin thấp chưa củng cố) | Tạo ghi chú cho khái niệm đó |
| Một bước tiếp theo của cùng nút được kiểm chứng | Bổ sung mệnh đề vào ghi chú đó |
| Một hiểu lầm được vá xong (kiểm tra lại trên tình huống mới đã đúng) | Thêm vào mục "Hiểu lầm đã vá" |
| `hoc-viet`: bản viết lại đạt | Tạo hoặc bổ sung ghi chú cho kỹ thuật viết đó |
| `hoc-luyen`: cuối buổi | Cập nhật thuộc tính `luyen_gan_nhat` của các khái niệm đã luyện |

Không ghi khi: câu trả lời sai, đúng nhưng tự tin thấp mà chưa củng cố, hoặc chỉ mới giảng xong chưa kiểm tra.

Sau mỗi lần ghi, báo **một dòng** ở cuối tin nhắn, ví dụ `↳ Obsidian: đã thêm [[Thông tin cũ trước thông tin mới]]`. Không xin phép từng lần: người học đã bật tính năng.

## Nơi ghi

```
<vault>/<thư mục gốc>/
├── <Tên chủ đề>.md                 # ghi chú tổng (MOC) của chủ đề
└── <Tên chủ đề>/
    └── <Tên khái niệm>.md          # mỗi khái niệm (mỗi nút trên bản đồ) một ghi chú
```

- Tên file là **tên khái niệm bằng tiếng Việt có dấu**, ngắn, dạng danh từ hoặc mệnh đề ngắn (ví dụ `Danh từ hóa.md`, `Lời nguyền của sự hiểu biết.md`). Bỏ các ký tự Obsidian cấm trong tên: `\ / : * ? " < > | # ^ [ ]`.
- Tên ghi chú được chốt một lần cho mỗi nút. Ghi tên đó vào cột `obsidian` của `ban-do.md` để các lần sau dùng đúng tên ấy, vì link `[[...]]` dựa vào tên.

## Mẫu ghi chú khái niệm

```markdown
---
tags: [hoc, <slug-chu-de>]
chu_de: "[[<Tên chủ đề>]]"
nut: <slug-nút>
ngay_hieu: <yyyy-mm-dd>
luyen_gan_nhat:
nguon: hoc-skills
---

%% hoc:start %%
**<Khái niệm, phát biểu trong một câu khẳng định.>**

## Vì sao
<Con đường khám phá ngắn: vấn đề nào dẫn đến nó, bước nào làm nó hiện ra là hiển nhiên. 2–5 câu.>

## Ví dụ
<Một ví dụ cụ thể. Ưu tiên ví dụ chính người học đã làm đúng trong buổi.>

## Theo lời tôi
> <Câu trả lời đúng của người học, trích nguyên văn hoặc gần nguyên văn.>

## Dựa trên
- [[<khái niệm nền 1>]]
- [[<khái niệm nền 2>]]

## Dẫn đến
- [[<khái niệm kế tiếp>]]

## Hiểu lầm đã vá
- <hiểu lầm> → <điều đúng> (<yyyy-mm-dd>)

## Mệnh đề
- <các mệnh đề từ hoc/menh-de.md thuộc nút này>
%% hoc:end %%
```

- "Dựa trên" và "Dẫn đến" lấy từ các cạnh của `ban-do.md`. Đây là thứ làm cho đồ thị của Obsidian phản ánh đúng cấu trúc kiến thức. Link đến khái niệm chưa có ghi chú cũng được, Obsidian hiện nó như ghi chú chưa tạo.
- Không có nội dung cho một mục (chưa có hiểu lầm, chưa có "Dẫn đến") thì bỏ mục đó.
- Viết ngắn, viết bằng lời của khái niệm, không phải biên bản buổi học. Ghi chú này để người học đọc lại sau vài tháng.

## Ghi chú tổng của chủ đề

````markdown
---
tags: [hoc, moc]
nguon: hoc-skills
---

%% hoc:start %%
Mục tiêu: <câu "sau khi học, tôi làm được…">

```mermaid
<bản đồ từ ban-do.md, giữ nhãn ngắn>
```

## Khái niệm đã rõ
- [[<khái niệm>]] · <ngày>
%% hoc:end %%
````

Tạo cùng lúc với ghi chú khái niệm đầu tiên của chủ đề. Cập nhật danh sách mỗi khi thêm khái niệm. Vẽ lại bản đồ khi `ban-do.md` thay đổi.

## Không bao giờ ghi đè chữ của người học

Người học sẽ tự sửa, tự viết thêm vào các ghi chú này. Vì vậy:

- Skill chỉ sửa phần nằm giữa `%% hoc:start %%` và `%% hoc:end %%` (dòng chú thích của Obsidian, không hiện khi đọc). Mọi thứ ngoài hai dấu này là của người học: không sửa, không xóa.
- Đọc file trước khi sửa. Trong phần của skill, nếu người học đã sửa chữ thì giữ bản của họ và chỉ thêm vào.
- File cùng tên đã tồn tại mà **không** có `nguon: hoc-skills` trong frontmatter: đó là ghi chú của người học. Không đụng vào phần có sẵn. Thêm một mục `## Từ buổi học <yyyy-mm-dd>` ở **cuối** file, có dấu `%% hoc:start %%`/`%% hoc:end %%` bao quanh, và báo người học.
- Không đổi tên, không di chuyển, không xóa file nào trong vault. Muốn đổi tên khái niệm thì hỏi người học.
- Không đụng vào thư mục `.obsidian/`.
