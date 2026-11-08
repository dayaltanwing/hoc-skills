# hoc-skills: học bất cứ thứ gì, theo phương pháp LearnHarness

**Đo biên hiểu biết, lập bản đồ, dạy từng bước suy luận, luyện cho đến khi tự bật ra.**

Bộ skill cho Claude Code, trao đổi bằng tiếng Việt. Nó đưa phương pháp dạy của [LearnHarness](https://github.com/amosblomqvist/learnharness) vào một phiên chat bình thường, không cần cài app. Kèm theo một skill học viết dựa trên *The Sense of Style* của Steven Pinker.

6 skill · 1 thư mục trạng thái `hoc/` · không cần Python, không cần API key

Cài vào một thư mục học (không ảnh hưởng dự án khác):

```bash
curl -fsSL https://raw.githubusercontent.com/dayaltanwing/hoc-skills/main/get.sh | bash
```

## Phương pháp

| Giai đoạn | Skill | Việc làm |
|---|---|---|
| Đo | `/hoc-do` | Làm mục tiêu cho cụ thể ("sau khi học tôi làm được…"). Tìm kiếm nhị phân biên hiểu biết trên từng mạch kiến thức, mỗi lượt một câu, đọc cả độ tự tin và suy nghĩ của bạn. |
| Kế hoạch | `/hoc-ke-hoach` | Bản đồ phụ thuộc tối thiểu (mermaid), từ các sự thật vô điều kiện đến mục tiêu. Bạn đồng ý rồi mới dạy. |
| Dạy | `/hoc-day` | Một bước suy luận mỗi lượt: **đoán → dạy → kiểm tra**. Bước chưa được kiểm chứng thì không xây gì lên trên. |
| Luyện | `/hoc-luyen` | Bài tập xen kẽ, kiến thức cần dùng không được gọi tên trước, gợi ý theo thang G0–G5. Bài sai được làm lại trên bề mặt mới. |
| Viết | `/hoc-viet` | Chấm đoạn văn của bạn theo 5 nhóm kỹ thuật của Pinker, chọn lỗi gốc, dạy sửa. **Bạn tự viết lại**, skill chấm. |

Cửa trước: `/hoc` đọc trạng thái, chọn đúng giai đoạn và gọi đúng skill. Không biết bắt đầu từ đâu thì gõ lệnh này.

Hai nguyên lý xuyên suốt (diễn đạt lại từ LearnHarness):
1. **Sự thật vô điều kiện trước.** Bắt đầu từ điều bạn chấp nhận được nguyên như vậy, không kèm điều kiện. Não chỉ "chốt" một điều khi nó an toàn, không sợ bị lật lại.
2. **"Làm sao tôi có thể tự khám phá ra điều này?"** Mỗi bước có động cơ, để điều mới hiện ra như được khám phá, không phải bị áp đặt.

## Cách bạn trả lời

```
B · 60% · tôi nghĩ là B vì…, nhưng phân vân với C
```

**Đáp án · độ tự tin · suy nghĩ.** Phần suy nghĩ quan trọng hơn đáp án. "Sai mà tự tin 90%" là tín hiệu mạnh nhất: một hiểu lầm đã cắm rễ. Không biết thì ghi `không biết`, đừng đoán bừa.

Giọng của skill: không khen, không làm mềm. Sai thì nói thẳng là sai.

## Bắt đầu

Mở Claude Code trong thư mục học:

```
/hoc thống kê hồi quy cho đề tài NCKH   # bắt đầu chủ đề mới: đo → kế hoạch → dạy
/hoc tiep                               # học tiếp chỗ đang dở
/hoc luyen                              # luyện trộn các chủ đề đã học
/hoc viet                               # dán một đoạn văn để chấm và học viết
/hoc                                    # tôi đang học gì, đến đâu rồi?
```

## Thư mục học trông như thế nào

```
thu-muc-hoc/
└── hoc/
    ├── nhat-ky.md          mỗi buổi một dòng
    ├── menh-de.md          mệnh đề và chuỗi suy luận đã học (đồ thị kiến thức)
    └── chu-de/<slug>/
        ├── muc-tieu.md     mục tiêu, giai đoạn, nút đang học
        ├── nguoi-hoc.md    biên hiểu biết từng mạch, hiểu lầm
        ├── ban-do.md       bản đồ mermaid
        └── buoi/           biên bản từng buổi
```

Trạng thái nằm trong file, không nằm trong trí nhớ của phiên chat. Mở phiên mới hôm sau, gõ `/hoc tiep` là học tiếp đúng chỗ.

## Cài vào một thư mục

Bộ skill **chỉ được cài vào từng thư mục** (`<thư mục>/.claude/skills/`). Các dự án Claude Code khác của bạn không bị ảnh hưởng.

**Cách nhanh nhất.** Mở Terminal trong thư mục học và chạy:

```bash
curl -fsSL https://raw.githubusercontent.com/dayaltanwing/hoc-skills/main/get.sh | bash
```

**Cập nhật** lên bản mới nhất: chạy lại đúng lệnh trên.

**Gỡ:**

```bash
curl -fsSL https://raw.githubusercontent.com/dayaltanwing/hoc-skills/main/get.sh | bash -s -- --go
```

**Từ bản clone của repo:**
- `./install.sh` cài vào thư mục hiện tại; `./install.sh "<thư mục>"` cài vào thư mục khác.
- `./install.sh --go` để gỡ.
- `./install.sh --link "<thư mục>"`: sửa skill ở bản clone là thư mục học thấy ngay.
- `--global` cài cho mọi dự án. Chỉ dùng khi bạn thật sự muốn.
- Script từ chối cài khi bạn đang ở thư mục home, vì cài ở đó cũng là cài cho mọi dự án.

**Dạng plugin** (Claude Code chạy trong Terminal). Trong thư mục học, chạy lần lượt:

```bash
claude plugin marketplace add dayaltanwing/hoc-skills --scope project
```

```bash
claude plugin install hoc@hoc-skills --scope project
```

Ở dạng plugin, tên skill có thêm tiền tố: `/hoc:hoc`, `/hoc:hoc-day`…

## Giới hạn cần biết

- Claude có thể sai về kiến thức của một lĩnh vực. Đưa tài liệu gốc (PDF, giáo trình) vào thì skill dựa vào tài liệu đó trước.
- Không có giao diện trắc nghiệm, sơ đồ trực tiếp hay đọc chính tả như app LearnHarness. Mọi thứ diễn ra bằng chữ trong phiên chat.
- `hoc-viet` không chứa nội dung sách. Nếu có bản sách, ghi đường dẫn vào `muc-tieu.md` để skill đọc khi cần.

## Nguồn và giấy phép

Phương pháp được diễn đạt lại từ các system prompt của [LearnHarness](https://github.com/amosblomqvist/learnharness) (Amos Blomqvist, AGPL-3.0). Bộ skill này vì vậy cũng phát hành theo [AGPL-3.0](LICENSE). Đây không phải sản phẩm chính thức của LearnHarness.

Bảng kiểm trong `hoc-viet` tóm lược ý tưởng của *The Sense of Style* (Steven Pinker, 2014) bằng lời của bộ skill, không trích sách.
