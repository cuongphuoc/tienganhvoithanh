# Web học 1000 từ vựng của Kim Thanh 🌸

Ứng dụng học từ vựng tiếng Anh A1–A2 với **1000 từ**, chạy hoàn toàn trên trình duyệt — không cần cài đặt, không cần build, không phụ thuộc thư viện ngoài.

## Tính năng

### ✨ Today's Learning — 15 từ × 4 dạng bài = 60 câu
Mỗi từ trong buổi học được luyện đủ **4 kỹ năng**, các dạng câu được xen kẽ nhau (không bao giờ có 2 câu liền kề cùng một từ):

| Dạng | Đề bài | Trả lời |
|---|---|---|
| 📝 Trắc nghiệm | từ tiếng Anh | chọn 1 trong 4 nghĩa tiếng Việt |
| ✍️ Ghi nghĩa tiếng Việt | từ tiếng Anh | gõ nghĩa tiếng Việt |
| 🔤 Ghi từ tiếng Anh | nghĩa tiếng Việt | gõ từ tiếng Anh |
| 🎧 Nghe | chỉ phát âm, không hiện chữ | chọn từ tiếng Anh đúng |

### Học tuần tự, không nhảy cóc

Today's Learning đi **lần lượt theo đúng danh sách 1000 từ**, không random:

- Ngày 1 → từ 1–15 · Ngày 2 → từ 16–30 · Ngày 3 → từ 31–45 …
- Mỗi ngày lấy đúng **15 từ mới kế tiếp** (đổi được trong Settings: 5/15/20/30).
- Con trỏ chỉ nhích khi bạn làm **xong cả 60 câu**. Thoát giữa buổi thì lần sau vào lại đúng 15 từ đang học dở — không mất từ nào.
- Trong một buổi, **vị trí các từ được xáo** để khỏi học vẹt theo danh sách, nhưng vẫn đúng bộ 15 từ của ngày đó.
- Học hết 1000 từ (~67 ngày) thì Today's Learning báo hoàn thành; từ cũ chuyển sang ôn ở mục 🔄 Review.

Các từ **đến hạn ôn không trộn vào Today's Learning** — chúng nằm ở mục 🔄 Review.

### 🏁 Đánh dấu cuối buổi
Kết thúc buổi học, toàn bộ từ của buổi được liệt kê kèm điểm `đúng/tổng` để bạn tự đánh dấu **Đã thuộc / Chưa thuộc**. Lựa chọn này ghi đè lịch ôn tập:
- **Đã thuộc** → đẩy lịch ôn xa ra (tối thiểu 7 ngày)
- **Chưa thuộc** → đưa về cấp 0 và hẹn ôn lại sau 5 phút

### 🔄 Review
Cùng 4 dạng bài tập như trên, áp dụng cho các từ đã đến hạn ôn (tối đa 15 từ/buổi). Đây là nơi các từ cũ quay lại — kể cả những từ bạn đánh dấu **Chưa thuộc**.

### 🌱 New Words
Học từ mới theo kiểu flashcard (Again / I Know) — giữ nguyên lối học truyền thống.

### 📚 Vocabulary
Tra cứu và tìm kiếm toàn bộ 1000 từ theo từ tiếng Anh hoặc nghĩa tiếng Việt, lọc theo chủ đề, xem chi tiết từng từ kèm phiên âm và ví dụ.

## Ghi nhớ kiểu spaced repetition

Mỗi từ có 5 cấp độ (0–4), khoảng cách ôn giãn dần: **0 → 1 → 3 → 7 → 14 ngày**.

Điểm của một từ được chốt sau khi làm **đủ 4 câu** của từ đó:
- đúng ≥ 75% → lên 1 cấp
- đúng ≤ 25% → xuống 1 cấp, ôn lại sau 5 phút
- ở giữa → giữ nguyên cấp, chỉ dời lịch ôn

Nhờ vậy một từ không thể nhảy vọt lên cấp cao chỉ vì 4 câu liên tiếp đều đúng.

## Chấm bài gõ

- **Bắt buộc đúng dấu** tiếng Việt.
- Chấp nhận **mọi biến thể nghĩa** trong dữ liệu (phân tách bởi `,` `;`), và bỏ qua nội dung trong ngoặc đơn — nên `anh rể` được chấp nhận cho nghĩa `anh (em) rể, anh (em) vợ`.
- Không phân biệt khoảng trắng thừa và dấu câu.
- Bài gõ từ tiếng Anh so **khớp chính xác** sau chuẩn hoá, nên `sea` không bao giờ bị tính đúng cho `season`.
- Ô nhập có xử lý **IME tiếng Việt** (Telex/VNI), không nộp bài khi đang gõ dở.

## Âm thanh

Dùng **Web Speech API** có sẵn của trình duyệt (giọng `en-US`). Nếu trình duyệt không phát được âm thanh, bài nghe sẽ **tự hiện từ ra** kèm nút "Hiện từ" để bạn không bị tắc ở câu hỏi.

## Cách chạy

Mở trực tiếp file `index.html` bằng trình duyệt (Chrome/Edge khuyến nghị, để có giọng đọc tiếng Anh).

## Cấu trúc

```
index.html    Giao diện: 4 màn hình (Home, Learn, Vocabulary, Word Detail) + modal Settings
script.js     Toàn bộ logic + dữ liệu 1000 từ vựng nhúng sẵn
style.css     Giao diện
```

## Lưu tiến độ

Toàn bộ tiến độ (cấp độ từng từ, XP, chuỗi ngày, mục tiêu) được lưu trong `localStorage` của trình duyệt — **không gửi lên máy chủ nào**.

Vào **⚙️ Settings** để đổi mục tiêu ngày (5/15/20/30 từ), **xuất** tiến độ ra file JSON để sao lưu, **nhập** lại, hoặc xoá toàn bộ để học lại từ đầu.
