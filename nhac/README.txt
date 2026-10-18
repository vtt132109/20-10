NHẠC NỀN — HƯỚNG DẪN
========================

Có 3 cách để có nhạc nền. Web tự chọn theo thứ tự ưu tiên:
  ①  YouTube   ②  File trong thư mục này   ③  Nhạc tổng hợp (mặc định)


────────────────────────────────────────────────────────────────
①  CÁCH DÙNG NHẠC THẬT BẰNG YOUTUBE  (nhanh nhất)
────────────────────────────────────────────────────────────────
Mở file index.html, tìm:

    const NHAC = {
      youtube: '',      <-- ĐIỀN MÃ VIDEO VÀO ĐÂY

Lấy mã video từ link YouTube:
    https://www.youtube.com/watch?v=AbCdEfGhIjK
                                    └────────┘
                              11 ký tự này, chính là phần bạn điền vào

Sau khi điền xong, lưu file lại và tải lại trang. Bấm nút loa ở
góc trên bên phải → bài hát đó sẽ phát.

  • Đây là trình phát YouTube chính thức, YouTube tự lo phần bản quyền.
  • Không cần tải bài hát về máy.
  • Cần mạng Internet.
  • Chỉnh âm lượng: sửa  amLuong: 35  trong cùng khối (0–100).


────────────────────────────────────────────────────────────────
②  CÁCH DÙNG FILE NHẠC RIÊNG  (chạy được cả offline)
────────────────────────────────────────────────────────────────
Thả file .mp3 (hoặc .m4a) vào chính thư mục này.

Tên file sẽ được web dò lần lượt — đặt tên đúng một trong các tên sau
là chạy luôn, không cần sửa code:

    think-about-you.mp3      ← đổi tên file thành tên này
    think-about-you.m4a
    nhac.mp3
    bai-hat.mp3
    music.mp3
    audio.mp3
    nhac.m4a

Muốn chỉ định tên khác? Sửa trong index.html:
    const NHAC = {
      file: './nhac/ten-ban-cua-ban.mp3'      <-- điền đường dẫn vào đây


────────────────────────────────────────────────────────────────
③  KHÔNG LÀM GÌ  (mặc định)
────────────────────────────────────────────────────────────────
Nếu để trống cả youtube và file, web tự phát nhạc nền tổng hợp bằng
Web Audio: điệu cực Cmaj7 → Am7 → Fmaj7 → G, có tiếng piano, tiếng
chuông và hồi âm. Không cần file nào, không cần mạng.


────────────────────────────────────────────────────────────────
VỀ PHỤ ĐỀ
────────────────────────────────────────────────────────────────
8 câu phụ đề hiện ở đáy màn hình, tự chia đều theo thời lượng thật
của bài đang phát. Muốn đổi lời, tìm trong index.html:

    const LYRICS = [
      { t: 0,  x: 'Câu thứ nhất' },
      ...

Nếu bài nhạc dài hơn 8 câu, thêm dòng vào mảng LYRICS.


────────────────────────────────────────────────────────────────
⚠  LƯU Ý QUAN TRỌNG VỀ BẢN QUYỀN
────────────────────────────────────────────────────────────────
Cách ① (YouTube) là hợp lệ: bạn không lấy file nhạc về, chỉ nhúng
trình phát chính thức của YouTube.

Nếu muốn dùng cách ②, hãy chỉ dùng nhạc bạn có quyền:

   OK   • Bài bạn MUA được (Apple Music / Spotify có nút tải về)
   OK   • Nhạc royalty-free: Pixabay Music, Free Music Archive,
         Bensound, Incompetech, YouTube Audio Library
   OK   • Nhạc do chính bạn hát hoặc thu âm
   OK   • Nghệ sĩ cho phép tải miễn phí (đọc kỹ điều khoản)

   KHÔNG  • Tải từ YouTube/Spotify/Apple Music rồi nhúng lại vào web
   KHÔNG  • Tải từ mp3.pm, zippyshare, 123kbps… (bản lậu)

Cách mua nhạc có bản quyền hợp lệ nhất cho món quà cá nhân:
  • Mua một bản tải về từ kho nhạc (Apple Music / Spotify)
  • Hoặc liên hệ Kay Chau Anh xin bản mp3 để dùng cho món quà riêng.
    Dùng cá nhân, không phát hành, thường được chấp nhận.

Nếu bạn gửi web cho người khác: nhớ gửi kèm file nhạc trong thư mục
này — người nhận cần file đó mới nghe được (cách ① thì chỉ cần gửi
link trang).