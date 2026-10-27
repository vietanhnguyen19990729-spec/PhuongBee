# PhuongBee — trang giới thiệu bản thân

Trang tĩnh một file (`index.html`). Không cần cài gì, mở bằng trình duyệt là chạy.

## Cấu trúc thư mục

```
C:\Showcase\
  index.html     ← trang web (mọi chữ/ảnh/link sửa trong khối CONFIG đầu thẻ <script>)
  music.mp3      ← nhạc nền (bài Perfect, chép từ C:\VyA\assets\bgm.mp3)
  img\           ← 24 ảnh ĐÃ xử lý (cắt đúng khung, cân sáng, làm nét) — đây là thứ được đăng lên mạng
C:\Showcase-anh-goc\
  Archive (1).zip ← 21 ảnh gốc, để NGOÀI thư mục web nên không bị đăng lên mạng
```

## Ảnh ↔ vị trí trên web

| Tên file | Dùng ở đâu | Cắt theo |
|---|---|---|
| `hero.jpg` / `hero-m.jpg` | Ảnh bìa — máy tính dùng ảnh ngang, điện thoại dùng ảnh dọc | giữ nguyên tỉ lệ |
| `portrait.jpg` | Khung vòm "Về mình" | 4:5 |
| `story-1..3.jpg` | Phần "Câu chuyện" — máy tính: khung dọc bên phải; điện thoại: toàn màn | giữ nguyên (dọc) |
| `reel-1..6.jpg` | Dải ảnh trôi ngang | 3:4 |
| `gal-1,2,3,4,5,7,8.jpg` | Bộ sưu tập (7 ảnh = 12 ô, lưới kín) | theo cỡ ô: lớn / dọc / vuông / ngang |
| `pol-1..4.jpg` | Chồng polaroid | ~4:5 |
| `og.jpg` | Ảnh xem trước khi chia sẻ link (chưa gắn, xem cuối trang) | 1.91:1 |

Ảnh **không dùng**: `IMG_1046` (chụp trên xe cùng 3 người khác — trang công khai nên bỏ, chưa xin phép họ).
`IMG_1052` (chụp màn hình Facebook) đã cắt bỏ phần giao diện, chỉ giữ ảnh.

## Thay / thêm ảnh

Điểm giữ lại khi bị cắt (`pos`, dạng `"x% y%"`) nằm ngay trong `CONFIG` cho ảnh bìa và ảnh "Câu chuyện".
Muốn thay ảnh: ghi đè file cùng tên trong `img\` (giữ tỉ lệ như bảng trên) rồi mở lại trang.
Khi thiếu file, trang hiện tên file ngay tại ô đó để biết cần ảnh nào.

Lưới bộ sưu tập là 4 cột × 3 hàng = 12 ô. Cỡ ô: `big` = 4 ô, `tall` = 2 ô, `wide` = 2 ô, trống = 1 ô.
Nếu đổi số ảnh/cỡ ô thì tổng phải vẫn là 12 (hoặc bội của 4), không thì cuối lưới bị hở.

## Thứ tự các cảnh khi cuộn

| # | Cảnh | Hiệu ứng |
|---|---|---|
| — | Màn "Mở quà" | Bấm để vào → tim nổ + nhạc bắt đầu phát |
| 1 | Hero | Ảnh toàn màn zoom chậm, tên viết tay từng nét, cuộn thì ảnh trôi chậm (parallax) |
| 2 | Lời chào | 안녕하세요 → "Mình là PhuongBee" → 4 thẻ ngắn, tan sương nối nhau theo cuộn |
| 3 | Về mình | Ảnh khung vòm nghiêng 3D theo chuột, huy hiệu "Đang độc thân" xoay, 4 dòng thông tin |
| 3b | Thần tượng | 2 vé concert (Sơn Tùng M-TP / BTS), 3 thẻ tiếng Hàn lật ra nghĩa, dải chữ chạy theo cuộn |
| 4 | Câu chuyện | Ảnh ghim cố định, cuộn tới đâu đổi ảnh + chương tới đó |
| 5 | Lướt cùng mình | Cuộn dọc kéo dải ảnh trôi ngang |
| 6 | Bộ sưu tập | Lưới kiểu tạp chí, ảnh mở dần từ giữa ra |
| 7 | Kỷ niệm | Chồng ảnh polaroid xoè ra theo cuộn |
| 8 | Lời nhắn | Câu trích dẫn + nút "Làm quen trên Facebook" |

Ở mọi nơi đều có tim/bụi vàng bay nền, vệt lấp lánh theo chuột, chạm đâu nổ tim đó. Nút ♡ nhỏ ở chân trang làm mưa tim.
Bấm ảnh (bộ sưu tập, dải ngang) để xem lớn; vuốt trái/phải trên điện thoại, mũi tên/Esc trên máy tính.

## Cần kiểm tra trước khi đăng

1. **Link Facebook**: đã điền `https://www.facebook.com/phuongbee99` trong `CONFIG.facebook`.
2. **Vé concert**: sửa `song` (bài yêu thích) trong `CONFIG.idols` cho đúng gu bạn ấy.
3. **Chữ**: lời chào, bio, bảng thông tin (cung hoàng đạo, thành phố), tên các chương, chú thích ảnh đều nằm trong `CONFIG` — hiện là nội dung mẫu, cần bạn ấy xác nhận.
   - **Không** ghi số điện thoại, địa chỉ nhà, nơi làm việc cụ thể. Trang công khai, ai có link cũng xem được.
4. **Nhạc**: chỉ phát sau khi người xem bấm "Mở quà" (trình duyệt cấm tự phát). Đổi bài = thay `music.mp3`.

## Đăng lên mạng (miễn phí)

**Netlify Drop** (dễ nhất): vào https://app.netlify.com/drop → kéo cả thư mục `C:\Showcase` thả vào → nhận link dạng `ten-ngau-nhien.netlify.app`. Có thể đổi tên link trong Site settings.

Muốn ảnh xem trước đẹp khi gửi link qua Messenger/Zalo: sau khi có link, thêm vào `<head>`:
`<meta property="og:image" content="https://<link-cua-ban>/img/og.jpg">` rồi đăng lại.
