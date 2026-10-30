# 🌟 HƯỚNG DẪN CÀI ĐẶT & SỬ DỤNG THIẾT BỊ TINYTOUCH

Chào mừng bạn đến với **tinyTouch** — Thiết bị xác thực cảm biến vân tay cao cấp mở khóa 1 chạm siêu tốc dành cho hệ điều hành **macOS** (MacBook, Mac mini, Mac Studio, iMac).

Link mua  https://s.shopee.vn/6Akenn3gQu

Hỗ trợ kỹ thuật https://m.me/100194225154263

---

## 🎯 TÍNH NĂNG NỔI BẬT (FIRMWARE v1.1.1)
* 🛡️ **Khóa bảo mật sinh trắc học FIDO2 Passkeys (Chuẩn quốc tế):** Tích hợp phần cứng FIDO2 / CTAP2.1 & WebAuthn cao cấp (tương đương YubiKey Bio). Đăng nhập không cần mật khẩu (Passwordless) siêu tốc và an toàn tuyệt đối cho Google, Microsoft, Apple ID, GitHub, Binance, X (Twitter), Bitwarden... Chống tấn công lừa đảo (Phishing-resistant) 100% nhờ xác thực trực tiếp qua cảm biến vân tay phần cứng.
* ⚡ **Mở khóa máy tính 1 chạm siêu tốc:** Chạm nhẹ ngón tay để tự động mở khóa màn hình ngay tức thì trên cả **macOS, Windows và Linux**.
* 🌙 **Tự động đánh thức USB Remote Wakeup:** Chạm ngón tay khi máy tính đang ngủ sâu (Deep Sleep) — thiết bị tự động gửi tín hiệu đánh thức màn hình và gõ chuẩn xác toàn bộ mật khẩu, không bị mất ký tự.
* 🛡️ **Chống dính phím cứng (Shift/Cmd/Alt):** Tự động phát hiện khi tay bạn vô tình tì vào phím Shift, Command hoặc Option trên bàn phím Mac và đợi bạn nhả ra mới gõ pass, chống gõ sai mật khẩu 100%.
* 👁️ **Tự kiểm tra kết quả mở khóa:** App tự động đối soát cửa sổ màn hình khóa sau 2.0 giây để ghi nhận và cảnh báo nếu có sự cố lỡ nhịp.
* 🌐 **Chế độ kép thông minh (Dual-Mode HID + FIDO2):** Hoạt động song song vừa là bàn phím tự gõ mật khẩu thông minh, vừa là USB Security Key FIDO2 mà không cần chuyển đổi phức tạp.
* 🔑 **Tự động điền mật khẩu mọi nơi:** Hỗ trợ đăng nhập linh hoạt vào Apple Passwords, Keychain, Safari, Chrome, 1Password, Bitwarden, ô đăng nhập Admin hệ thống hoặc lệnh `sudo` trong Terminal.
* 🖐️ **Đa tài khoản (5 Ngón tay — 5 Mật khẩu độc lập):** Biến 5 ngón tay thành 5 "chìa khóa" mở 5 tài khoản hoặc dịch vụ khác nhau (Ngón trỏ mở máy, ngón giữa mở Master Password, ngón áp út mở Email/VPN...).
* ⌨️ **Tùy biến phím kết thúc & độ trễ linh hoạt:** Tự do cấu hình phím tự bấm sau khi gõ pass (`Enter`, `Tab`, `None`, hoặc tổ hợp phím kép `enter,space`, `tab,enter`) kèm thời gian chờ tinh chỉnh từ 0 đến 5000ms.
* 💻 **Quản lý trực quan 100% qua Web (Web Controller):** Quản lý vân tay, đổi mật khẩu các slot, xem và xóa danh sách Passkeys FIDO2 đã lưu, nâng cấp firmware 1 chạm trực tiếp trên trình duyệt Chrome/Edge qua WebUSB mà **không cần cài đặt bất kỳ phần mềm nào**.
* 🔒 **Bảo mật phần cứng độc lập cấp quân sự:** Toàn bộ dữ liệu mật khẩu và chứng chỉ FIDO2 được mã hóa phần cứng **XTS-AES 256-bit** trong Flash của chip ESP32-S3, chống trích xuất dữ liệu và khóa 2 lớp chống tráo cảm biến. 
* 🔌 **100% Cắm là chạy (Plug & Play):** Không chạy bất kỳ tiến trình hay dịch vụ chạy ngầm nào trên máy tính, không ngốn RAM/CPU, không lo xung đột phần mềm.
* 🌑 **Thiết kế Stealth Mode:** Đèn LED thông minh chỉ sáng khi quét vân tay và tự động tắt hoàn toàn khi ở chế độ chờ (không chói mắt, tiết kiệm điện năng tối đa).

---

## 🍎 CÁCH 1: SỬ DỤNG ỨNG DỤNG MENU BAR TRÊN MACOS (KHUYÊN DÙNG CHO MAC)
*(Ứng dụng đồ họa chạy nền trên thanh Menu Bar, hỗ trợ mở khóa màn hình kể cả khi Sleep, xác thực sudo và bảo vệ chống lộ mật khẩu)*

> ⚠️ **LƯU Ý QUAN TRỌNG:**  
> Thiết bị tinyTouch xuất xưởng chưa có dữ liệu vân tay. Bạn **BẮT BUỘC phải đăng ký vân tay trên Web trước (Bước 1)** thì thiết bị mới có vân tay chính chủ để chạm xác thực khi ghép đôi với ứng dụng macOS!

### 📌 Bước 1: Đăng ký vân tay trên Web Controller (Bắt buộc làm trước)
1. Cắm thiết bị **tinyTouch** vào cổng USB máy Mac.
2. Mở trình duyệt web (**Google Chrome**, **Microsoft Edge**, **Cốc Cốc** hoặc **Opera**) và truy cập:  
   👉 **[https://touch.mrold.xyz/](https://touch.mrold.xyz/)**
3. Bấm nút **"Kết nối thiết bị"** ở góc trên cùng bên phải $\rightarrow$ Chọn dòng **`tinyTouch`** $\rightarrow$ Bấm **Connect**.
4. **Đăng ký vân tay (Slot 1):**
   * Bấm nút **"👆 Quét ngón"** tại Slot 1 (hoặc ngón bạn muốn dùng).
   * Đặt ngón tay lên cảm biến $\rightarrow$ Nhấc ngón tay ra $\rightarrow$ Đặt lại theo hướng dẫn trên màn hình cho đến khi báo `✓ Đã quét vân tay`.
   *(💡 **Lưu ý:** Bạn chỉ cần quét vân tay trên Web, **KHÔNG CẦN đặt mật khẩu trên Web**, vì mật khẩu mở máy Mac sẽ được ứng dụng tinyTouch lưu an toàn vào macOS Keychain ở các bước sau).*
5. Sau khi quét vân tay thành công, **đóng tab web** để giải phóng cổng kết nối cho ứng dụng macOS.

### 📌 Bước 2: Cài đặt ứng dụng từ file `.dmg`
1. Tải về file [**tinyTouch-macOS.dmg (Bản mới nhất)**](https://github.com/mr-old-youtube/MrOld-touch/releases/latest/download/tinyTouch-macOS.dmg).
2. Nhấp đúp mở file `.dmg` $\rightarrow$ Kéo biểu tượng **`tinyTouch.app`** thả vào thư mục **`Applications`**.

### 📌 Bước 3: Mở ứng dụng và Cấp quyền Trợ năng (Accessibility)
1. Vào thư mục **Applications**, nhấp phải vào `tinyTouch` $\rightarrow$ chọn **Open** $\rightarrow$ chọn **Open** (để macOS cho phép ứng dụng mở lần đầu).
2. Khi mở lên, icon **vòng tròn sinh trắc vân tay** sẽ xuất hiện trên thanh **Menu Bar** (góc trên bên phải màn hình).
3. **Cấp quyền Trợ năng (Bắt buộc để gõ pass vào màn hình khóa):**
   * Vào **Cài đặt hệ thống (System Settings)** $\rightarrow$ **Quyền riêng tư & Bảo mật (Privacy & Security)** $\rightarrow$ **Trợ năng (Accessibility)**.
   * Tìm ứng dụng **tinyTouch** và gạt công tắc sang **BẬT (ON)**.

### 📌 Bước 4: Thiết lập mật khẩu & Ghép đôi an toàn
1. Cắm thiết bị **tinyTouch** vào cổng USB máy Mac.
2. Bấm vào icon tinyTouch trên Menu Bar $\rightarrow$ chọn **"Cài đặt & Mật khẩu..."** (hoặc nhấn phím tắt `⌘,`).
3. **Tại cửa sổ Cài đặt:**
   * **Mục 2 (Mật khẩu mở máy Mac):** Nhập mật khẩu tài khoản macOS của máy Mac hiện tại $\rightarrow$ Bấm **"Lưu Pass"**.
   * **Mục 3 (Ghép đôi bảo mật):** Bấm nút **"⚡ Tạo Mã & Ghép Đôi Tự Động"** $\rightarrow$ Hệ thống tự sinh mã khóa 64 ký tự hex ngẫu nhiên an toàn và hiển thị *"⏳ Đang yêu cầu xác thực vân tay trên tinyTouch..."*.
   * **Chạm vân tay:** Đặt **ngón tay đã đăng ký trên Web ở Bước 1** vào cảm biến tinyTouch để xác nhận quyền chủ nhân và lưu mã khóa vào chip.
4. 🎉 **Hoàn tất!** Giờ đây mỗi khi bạn khóa máy (`Cmd + Ctrl + Q`) hoặc máy đang ngủ (Sleep), chỉ cần chạm vân tay là máy tự sáng màn hình và mở khóa ngay lập tức!

### 📌 Các tính năng mở rộng trên Menu Bar:
* **Xác thực lệnh `sudo` bằng vân tay:** Khi bạn gõ `sudo ...` trong Terminal, app sẽ lắng nghe và bạn chỉ cần chạm vân tay vào tinyTouch là lệnh chạy ngay mà không cần gõ mật khẩu.
* **Bộ lọc ngữ cảnh an toàn (Context Filter):** Tự động phát hiện màn hình khóa hoặc ô mật khẩu an toàn. Nếu bạn chạm vân tay ngoài màn hình Desktop bình thường, app sẽ chặn không gõ ra để chống lộ mật khẩu.
* **Quản lý ghép đôi:** Cho phép xem danh sách máy Mac đã ghép đôi và xóa quyền các máy cũ trực tiếp từ giao diện.

---

## 🌐 CÁCH 2: KHỞI TẠO QUA TRÌNH DUYỆT WEB (CHO WINDOWS, LINUX & CHẾ ĐỘ THUẦN HID)
*(⚡ 100% Không cần cài phần mềm — Khuyên dùng cho Windows & người dùng chỉ thích tự gõ mật khẩu)*

Nếu bạn sử dụng **Windows**, **Linux** hoặc trên Mac chỉ muốn dùng chế độ **Tự gõ mật khẩu (HID)**:

### 📌 Bước 1: Cắm tinyTouch vào cổng USB máy tính
* Windows 10/11, macOS và Linux sẽ tự động nhận diện thiết bị ngay lập tức (không cần cài thêm driver).

### 📌 Bước 2: Mở Web Controller
* Mở trình duyệt (Google Chrome, Microsoft Edge, Opera, Cốc Cốc) và truy cập:
  👉 **[https://touch.mrold.xyz/](https://touch.mrold.xyz/)**

### 📌 Bước 3: Bấm kết nối thiết bị
1. Bấm nút **"Kết nối thiết bị"** ở góc trên cùng bên phải.
2. Trên cửa sổ popup của trình duyệt, chọn dòng **`tinyTouch`** (hoặc `USB Serial Device / COM...`) $\rightarrow$ Bấm **Connect**.
3. *Giao diện sẽ chuyển sang màu xanh lá báo "Đã kết nối tinyTouch" và hiển thị trạng thái thiết bị.*

### 📌 Bước 4: Đăng ký vân tay & Cài mật khẩu mở máy
1. **Quét vân tay chính (Slot 1):**
   * Bấm nút **"👆 Quét ngón"** tại Slot 1.
   * Đặt ngón tay lên cảm biến lần 1 $\rightarrow$ Nhấc ngón tay ra $\rightarrow$ Đặt lại lần 2 $\rightarrow$ Báo `✓ Đã quét vân tay`.
2. **Cài mật khẩu mở máy:**
   * Bấm nút **"🔑 Đặt pass"** tại Slot 1.
   * Nhập mã PIN hoặc mật khẩu mở máy tính của bạn $\rightarrow$ Bấm **"Lưu mật khẩu"**.
   * Chạm nhẹ vân tay vào cảm biến để xác nhận lưu an toàn trực tiếp vào chip.
3. **Kiểm tra chế độ:**
   * Mặc định thiết bị xuất xưởng đã ở sẵn **🟢 HID Keyboard**. Nếu đang ở PIV, bạn chỉ cần bấm nút **"Chuyển sang HID"**.

🎉 **HOÀN TẤT!** Bây giờ mỗi khi khóa màn hình (`Win + L` trên Windows hoặc `Cmd + Ctrl + Q` trên Mac), bạn chỉ cần **chạm nhẹ vân tay vào cảm biến** là thiết bị tự động gõ mật khẩu và nhấn Enter mở máy tức thì!

---

## 💻 CÁCH 3: CÀI ĐẶT BẰNG CÔNG CỤ DÒNG LỆNH CLI CHO MACOS
*(Dành cho lập trình viên hoặc người dùng thích thao tác chuyên nghiệp qua Terminal)*

### 📌 Bước 1: Tải về và giải nén
* 👉 **Link tải bản mới nhất:** [**Tải tinytouch-macos.zip (Bản mới nhất)**](https://github.com/mr-old-youtube/MrOld-touch/releases/latest/download/tinytouch-macos.zip)
* Sau khi tải về, bạn chỉ cần nhấp đúp vào file `tinytouch-macos.zip` để giải nén.

> ⚡ **Cách tải nhanh qua Terminal (Luôn lấy bản mới nhất):**
> ```bash
> curl -LO https://github.com/mr-old-youtube/MrOld-touch/releases/latest/download/tinytouch-macos.zip && unzip -o tinytouch-macos.zip
> ```

---

### 📌 Bước 2: Mở Terminal tại thư mục vừa giải nén
1. Mở ứng dụng **Terminal** trên Mac (nhấn `Command + Space` $\rightarrow$ gõ `Terminal` $\rightarrow$ `Enter`).
2. Gõ chữ `cd ` (có dấu cách ở cuối) rồi **kéo thả thư mục vừa giải nén vào cửa sổ Terminal** $\rightarrow$ nhấn **Enter**.

---

### 📌 Bước 3: Cấp quyền chạy lần đầu (Nếu macOS hiển thị cảnh báo)
Do phần mềm tải từ Internet, bạn dán lệnh sau vào Terminal để mở khóa bảo mật macOS:
```bash
xattr -d com.apple.quarantine ./tinytouch 2>/dev/null || true
chmod +x ./tinytouch
```

---

### 📌 Bước 4: Chạy cài đặt tự động
Cắm thiết bị tinyTouch vào cổng USB và chạy lệnh:
```bash
./tinytouch setup
```
> 💡 **Trình cài đặt sẽ tự động hướng dẫn bạn:**
> 1. Nhận diện kết nối thiết bị tinyTouch.
> 2. Chọn chế độ hoạt động (**HID** - Khuyên dùng hoặc **PIV**).
> 3. Hướng dẫn chạm ngón tay để quét vân tay (Chạm lần 1 $\rightarrow$ Nhấc ra $\rightarrow$ Chạm lần 2).
> 4. Nhập mật khẩu máy Mac để lưu trực tiếp vào chip bảo mật $\rightarrow$ **Xong ngay!**

*(Sau khi cài đặt xong, bạn có thể thoải mái xóa file tải về, thiết bị vẫn hoạt động vĩnh viễn trên máy Mac!)*

---

## 💡 CÁCH SỬ DỤNG HÀNG NGÀY

Bất cứ khi nào máy Mac của bạn hiển thị ô nhập mật khẩu:
1. Đặt ngón tay đã đăng ký lên cảm biến **tinyTouch**.
2. **Tín hiệu đèn LED:**
   * 🟢 **Đèn nháy Xanh lá:** Nhận diện đúng vân tay $\rightarrow$ Tự động điền mật khẩu và ấn Enter mở khóa ngay lập tức!
   * 🔴 **Đèn nháy Đỏ:** Vân tay không khớp hoặc đặt sai ngón $\rightarrow$ Đặt lại đúng ngón tay vào giữa cảm biến.
   * 🌑 **Đèn tắt hoàn toàn:** Trạng thái nghỉ sẵn sàng (không tốn điện, không gây chói mắt).

---

## 🛡️ HƯỚNG DẪN SỬ DỤNG TÍNH NĂNG FIDO2 PASSKEYS (MỚI TRÊN v1.0.6)

Từ phiên bản Firmware **v1.0.6**, tinyTouch đóng vai trò như một **Khóa bảo mật sinh trắc học FIDO2 cao cấp** (chuẩn CTAP2.1 / WebAuthn, tương tự YubiKey Bio). Bạn có thể đăng nhập vào hàng ngàn dịch vụ lớn (Google, Apple ID, Microsoft, GitHub, Binance, X/Twitter, Bitwarden...) hoàn toàn không cần mật khẩu (Passwordless) và miễn nhiễm với các cuộc tấn công lừa đảo đánh cắp tài khoản (Phishing).

### 1. Đăng ký Passkey cho tài khoản:
1. Đăng nhập vào website hỗ trợ Passkey (ví dụ: Google Account, Microsoft, GitHub, Binance, Bitwarden...).
2. Vào mục **Cài đặt bảo mật (Security Settings)** $\rightarrow$ Tìm mục **"Khóa bảo mật" (Security Key)** hoặc **"Tạo Passkey" (Create Passkey)**.
3. Khi trình duyệt hiển thị hộp thoại yêu cầu xác thực khóa bảo mật $\rightarrow$ **Chạm ngón tay đã đăng ký vào cảm biến tinyTouch**.
4. Đèn LED nháy Xanh lá $\rightarrow$ Trang web báo đã tạo và liên kết Passkey thành công!

### 2. Đăng nhập bằng Passkey (Không cần nhớ hay gõ mật khẩu):
1. Tại trang đăng nhập của website, chọn tùy chọn **"Đăng nhập bằng Passkey"** (Sign in with a Passkey).
2. Khi trình duyệt hiển thị yêu cầu $\rightarrow$ **Chạm ngón tay vào cảm biến tinyTouch**.
3. Thiết bị đối soát vân tay và thực hiện ký số bảo mật phần cứng $\rightarrow$ Bạn được đăng nhập tức thì mà không cần nhập mật khẩu hay mã xác thực 2 bước (2FA OTP)!

### 3. Quản lý Passkeys đã lưu trên thiết bị:
* Truy cập Web Controller tại **[https://touch.mrold.xyz/](https://touch.mrold.xyz/)** bằng Chrome hoặc Edge.
* Bấm **Kết nối thiết bị** $\rightarrow$ Cuộn xuống mục **"Quản Lý Passkeys Đã Lưu (FIDO2)"**.
* Tại đây, bạn có thể:
  * Xem tổng số Passkey đã lưu trữ trên chip.
  * Xem tên miền dịch vụ (Domain/RP ID), tên tài khoản (Username) và số lần đăng nhập (Sign Counter).
  * Xóa từng Passkey riêng lẻ hoặc xóa toàn bộ chỉ với 1 click (yêu cầu chạm vân tay để xác nhận quyền bảo mật).

---

## 🖐️ TÍNH NĂNG ĐẶC BIỆT: GÁN MỖI NGÓN TAY MỘT MẬT KHẨU KHÁC NHAU

Ở chế độ **HID Mode**, tinyTouch cho phép bạn biến 5 ngón tay thành 5 "chìa khóa" mở 5 tài khoản khác nhau:

### 🌟 Ví dụ cách dùng:
* 👆 **Ngón trỏ (Slot 1):** Mật khẩu máy Mac (đăng nhập máy).
* 🖕 **Ngón giữa (Slot 2):** Master Password của 1Password / Bitwarden / Apple Passwords.
* 💍 **Ngón áp út (Slot 3):** Mật khẩu tài khoản Email / Công ty / VPN.
* 🤙 **Ngón cái (Slot 4):** Mật khẩu Server / SSH / GitHub token.
* 🖐️ **Ngón út (Slot 5):** Mật khẩu ví tiền điện tử (Crypto) hoặc ghi chú bảo mật.

### ⚙️ Các lệnh thiết lập:
1. **Xem danh sách 5 khe vân tay:**
   ```bash
   ./tinytouch slots
   ```
2. **Đăng ký vân tay cho ngón mới (ví dụ ngón 2):**
   ```bash
   ./tinytouch enroll 2
   ```
3. **Cài mật khẩu riêng cho từng ngón:**
   ```bash
   ./tinytouch set-password 2    # Cài mật khẩu riêng cho ngón 2
   ./tinytouch set-password 3    # Cài mật khẩu riêng cho ngón 3
   ```
4. **Xóa mật khẩu riêng của 1 ngón (quay về mật khẩu mặc định):**
   ```bash
   ./tinytouch clear-password 2
   ```

---

## 🔄 HƯỚNG DẪN CHUYỂN ĐỔI CHẾ ĐỘ (HID vs PIV)

tinyTouch hỗ trợ 2 chế độ hoạt động linh hoạt, bạn có thể chuyển đổi bất cứ lúc nào:

### 1. Chế độ HID (Bàn phím tự động gõ — ⭐ Khuyên Dùng)
* **Ưu điểm:** Tự động điền mật khẩu ở **mọi nơi 100%** (Màn hình khóa, Apple Passwords, Cài đặt ứng dụng Admin, Keychain, Safari, Terminal...).
* **Cách chuyển:**
  ```bash
  ./tinytouch mode hid
  ```

### 2. Chế độ PIV (Smart Card chuẩn Apple)
* **Ưu điểm:** Máy Mac nhận diện tinyTouch là Thẻ thông minh SmartCard bảo mật, xác thực qua chứng chỉ mã hóa phần cứng.
* **Hạn chế:** Chỉ hỗ trợ mở khóa màn hình Mac và lệnh `sudo` trong Terminal.
* **Cách chuyển:**
  ```bash
  ./tinytouch mode piv
  ```

---

## ⌨️ TÙY BIẾN PHÍM BẤM KẾT THÚC & ĐỘ TRỄ (POST-KEY & DELAY)

Sau khi gõ xong mật khẩu, tinyTouch có thể tự động gõ thêm phím bấm hoặc chuỗi phím theo ý bạn:

1. **Xem cấu hình phím kết thúc hiện tại:**
   ```bash
   ./tinytouch post-key
   ```
2. **Đổi phím kết thúc (Enter, Tab, Space hoặc Không bấm phím nào):**
   ```bash
   ./tinytouch post-key enter          # Mặc định: Gõ Enter để đăng nhập ngay
   ./tinytouch post-key tab            # Nhấn Tab (chuyển sang ô tiếp theo)
   ./tinytouch post-key none           # Chỉ gõ mật khẩu, không bấm thêm phím nào
   ```
3. **Gõ chuỗi nhiều phím liên tiếp (Tùy biến cao cấp):**
   ```bash
   ./tinytouch post-key enter,space    # Gõ Enter rồi gõ tiếp phím Space
   ./tinytouch post-key tab,enter      # Nhấn Tab chuyển nút rồi nhấn Enter
   ```
4. **Tinh chỉnh thời gian chờ giữa các phím (từ 0 đến 5000 mili-giây):**
   ```bash
   ./tinytouch post-key --delay 200    # Đặt độ trễ giữa các phím là 200ms
   ```

---

## 💻 HƯỚNG DẪN DÙNG TINYTOUCH TRÊN NHIỀU MÁY TÍNH KHÁC NHAU

Bạn có thể dùng **1 chiếc tinyTouch** duy nhất để mở khóa và làm việc trên **nhiều máy tính khác nhau**:

### 🛡️ 1. Khi ở chế độ PIV (Dùng trên nhiều máy Mac):
Do chuẩn bảo mật của Apple, mỗi máy Mac mới cần được cấp quyền ghép đôi (Pair) **đúng 1 lần đầu tiên**:
1. Cắm tinyTouch vào máy Mac mới.
2. Tải và giải nén `tinytouch-macos.zip` trên máy Mac mới.
3. Mở Terminal tại thư mục vừa giải nén và chạy lệnh:
   ```bash
   ./tinytouch add-computer
   ```
   *(Hoặc `./tinytouch pair`)*.
4. Nhập mật khẩu máy Mac mới khi được hỏi để xác nhận cấp quyền.
5. 👉 **Xong!** Từ lần sau cắm vào máy Mac đó, chỉ cần chạm vân tay là máy nhận diện SmartCard và tự động đăng nhập ngay lập tức.
6. **Quản lý danh sách máy tính đã ghép nối:**
   ```bash
   ./tinytouch computers               # Liệt kê hoặc xóa bớt máy Mac đã ghép nối
   ```

### 🔑 2. Tự động xoay chứng chỉ bảo mật (PIV Key Rotation):
* Bạn có thể làm mới cặp khóa mã hóa RSA-2048 trên thiết bị bất cứ lúc nào mà **không cần cài lại firmware**:
  ```bash
  ./tinytouch keys
  ```

### ⌨️ 3. Khi ở chế độ HID (Cắm là dùng trên Mac, Windows, Linux):
* **100% Cắm là nhận (Plug & Play)**: Không cần cài đặt phần mềm hay gõ bất kỳ lệnh nào trên máy tính mới.
* Cắm tinyTouch vào bất kỳ máy Mac, laptop Windows hay PC nào $\rightarrow$ Chạm ngón tay là thiết bị tự động gõ mật khẩu mở máy ngay!

---

## 🔄 HƯỚNG DẪN CẬP NHẬT PHIÊN BẢN MỚI

Khi có bản cập nhật mới, bạn có thể nâng cấp nhanh chóng bằng 1 trong 2 cách sau:

### ⚡ Cách 1: Nâng cấp trực tiếp bằng câu lệnh (Khuyên dùng — 2 giây)
Mở Terminal và gõ:
```bash
tinytouch update
```
Phần mềm sẽ tự động tải bản mới nhất từ GitHub Releases và cài đặt vào máy của bạn.

### 🌐 Cách 2: Cập nhật bằng 1 dòng lệnh Terminal duy nhất (Không cần tải file)
```bash
curl -sL https://github.com/mr-old-youtube/MrOld-touch/releases/latest/download/tinytouch-macos.zip -o /tmp/tinytouch.zip && unzip -qo /tmp/tinytouch.zip -d /tmp/tinytouch_update && /tmp/tinytouch_update/tinytouch --version
```

---

## 📖 BẢNG TRA CỨU CÁC LỆNH QUẢN LÝ THƯỜNG DÙNG

| Thao tác | Câu lệnh trong Terminal (Lưu ý có dấu `./` ở đầu) |
| :--- | :--- |
| **Kiểm tra phiên bản CLI** | `./tinytouch --version` |
| **Cài đặt trọn gói thiết bị** | `./tinytouch setup` |
| **Cập nhật lên bản mới nhất** | `tinytouch update` |
| **Kiểm tra trạng thái thiết bị** | `./tinytouch status` |
| **Thử nghiệm kết nối thiết bị** | `./tinytouch test` |
| **Chuyển sang chế độ tự gõ pass (Khuyên dùng)** | `./tinytouch mode hid` |
| **Chuyển sang chế độ SmartCard** | `./tinytouch mode piv` |
| **Xem 5 khe vân tay & Mật khẩu** | `./tinytouch slots` |
| **Đăng ký thêm ngón tay** | `./tinytouch enroll <1-5>` *(Ví dụ: `./tinytouch enroll 2`)* |
| **Gán mật khẩu riêng cho ngón** | `./tinytouch set-password <1-5>` |
| **Xóa mật khẩu riêng của ngón** | `./tinytouch clear-password <1-5>` |
| **Cấu hình phím bấm kết thúc** | `./tinytouch post-key <enter / tab / enter,space>` |
| **Đổi thời gian trễ giữa các phím** | `./tinytouch post-key --delay <số mili-giây (0-5000)>` |
| **Thêm máy Mac mới (Chế độ PIV)** | `./tinytouch add-computer` *(hoặc `./tinytouch pair`)* |
| **Quản lý máy tính đã kết nối** | `./tinytouch computers` |
| **Làm mới khóa mã hóa PIV** | `./tinytouch keys` |
| **Xem nhật ký hoạt động (Logs)** | `./tinytouch logs` |
| **Xóa 1 ngón tay cụ thể** | `./tinytouch delete <1-5>` |
| **Xóa toàn bộ vân tay** | `./tinytouch delete --all` |
| **Khôi phục cài đặt gốc** | `./tinytouch factory-reset` |

---

## ❓ CÂU HỎI THƯỜNG GẶP & XỬ LÝ SỰ CỐ

#### 1. Lỗi `zsh: permission denied: ./tinytouch`?
> 👉 **Cách sửa:** Gõ lệnh cấp quyền thực thi:
> ```bash
> chmod +x ./tinytouch
> ```

#### 2. Lỗi macOS báo "tinytouch cannot be opened because Apple cannot check it..."?
> 👉 **Cách sửa:** Chạy lệnh bỏ cờ kiểm dịch của macOS:
> ```bash
> xattr -d com.apple.quarantine ./tinytouch
> ```
> *(Hoặc vào **Cài đặt hệ thống** $\rightarrow$ **Quyền riêng tư & Bảo mật** $\rightarrow$ bấm **Open Anyway**)*.

#### 3. Tôi đổi mật khẩu máy Mac thì cần làm gì?
> 👉 Chỉ cần cắm tinyTouch vào máy Mac và chạy lại lệnh:
> ```bash
> ./tinytouch set-password 1
> ```
> Nhập mật khẩu mới là thiết bị sẽ tự động cập nhật ngay trên chip.

#### 4. Thiết bị có lưu mật khẩu của tôi an toàn không?
> 🛡️ **Tuyệt đối an toàn!** Mật khẩu được mã hóa phần cứng chuẩn **XTS-AES 256-bit** trực tiếp trong bộ nhớ Flash của chip. Kể cả khi có người tháo rời cảm biến hoặc can thiệp vật lý cũng không thể đọc trộm được mật khẩu.


