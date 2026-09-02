# 🌟 HƯỚNG DẪN CÀI ĐẶT & SỬ DỤNG THIẾT BỊ TINYTOUCH

Chào mừng bạn đến với **tinyTouch** — Thiết bị xác thực cảm biến vân tay cao cấp mở khóa 1 chạm siêu tốc dành cho hệ điều hành **macOS** (MacBook, Mac mini, Mac Studio, iMac).
Link mua  https://s.shopee.vn/6Akenn3gQu
---

## 🎯 TÍNH NĂNG NỔI BẬT
* ⚡ **Mở khóa Mac 1 chạm:** Chạm nhẹ ngón tay để mở khóa màn hình ngay tức thì.
* 🔑 **Tự động điền mật khẩu:** Hỗ trợ đăng nhập Apple Passwords, Keychain, Safari, 1Password, Bitwarden, trình duyệt Web...
* 🖐️ **Đa tài khoản (5 Ngón tay - 5 Mật khẩu):** Mỗi ngón tay có thể mở một mật khẩu/tài khoản khác nhau.
* 🛡️ **Phê duyệt quyền Admin:** Xác thực nhanh khi cài ứng dụng, phân quyền hệ thống hoặc lệnh `sudo` trong Terminal.
* 🔒 **100% Phần cứng độc lập:** Không cần cài đặt Python, không chạy bất kỳ dịch vụ ngầm nào trên máy Mac, cắm là chạy (Plug & Play).
* 🛡️ **Bảo mật phần cứng cấp quân sự:** Mã hóa phần cứng XTS-AES 256-bit chống trích xuất dữ liệu và khóa 2 lớp chống tráo cảm biến.
* 🌙 **Thiết kế Stealth Mode:** Đèn LED thông minh tự động tắt hoàn toàn khi ở chế độ chờ.

---

## 📋 YÊU CẦU HỆ THỐNG
* Máy Mac chạy macOS (Intel hoặc Apple Silicon M1 / M2 / M3 / M4).
* **KHÔNG CẦN CÀI PYTHON:** Phần mềm đã được đóng gói độc lập, chạy trực tiếp 100%.
* Cáp kết nối USB-C hoặc USB-A cắm thiết bị tinyTouch vào máy Mac.

---

## 🌐 CÁCH 1: KHỞI TẠO QUA TRÌNH DUYỆT WEB (CHO WINDOWS, LINUX & CHẾ ĐỘ HID)
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

## 💻 CÁCH 2: CÀI ĐẶT TRỌN GÓI BẰNG ỨNG DỤNG CHO MACOS (CLI)
*(Dành cho người dùng Mac muốn tích hợp sâu SmartCard PIV hoặc cài đặt qua Terminal)*

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

### ⌨️ 2. Khi ở chế độ HID (Cắm là dùng trên Mac, Windows, Linux):
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
| **Cài đặt trọn gói thiết bị** | `./tinytouch setup` |
| **Cập nhật lên bản mới nhất** | `tinytouch update` |
| **Thêm máy Mac mới (Chế độ PIV)** | `./tinytouch add-computer` *(hoặc `./tinytouch pair`)* |
| **Chuyển sang chế độ tự gõ pass (Khuyên dùng)** | `./tinytouch mode hid` |
| **Chuyển sang chế độ SmartCard** | `./tinytouch mode piv` |
| **Xem 5 khe vân tay & Mật khẩu** | `./tinytouch slots` |
| **Đăng ký thêm ngón tay** | `./tinytouch enroll <1-5>` *(Ví dụ: `./tinytouch enroll 2`)* |
| **Gán mật khẩu riêng cho ngón** | `./tinytouch set-password <1-5>` |
| **Xóa mật khẩu riêng của ngón** | `./tinytouch clear-password <1-5>` |
| **Kiểm tra trạng thái thiết bị** | `./tinytouch status` |
| **Thử nghiệm kết nối thiết bị** | `./tinytouch test` |
| **Đổi mật khẩu máy Mac** | `./tinytouch set-password 1` |
| **Xóa 1 ngón tay** | `./tinytouch delete <1-5>` |
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


