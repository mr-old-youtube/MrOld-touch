# Hướng dẫn ghép đôi tinyTouch với máy tính Windows

Áp dụng cho ứng dụng **tinyTouch Security cho Windows phiên bản 1.1.9** trở lên.

Tài liệu gồm hai trường hợp:

- **Trường hợp A:** Máy đăng nhập bằng **tài khoản cục bộ** (local account), tức tên đăng nhập kiểu `Admin`, `Viet` và không gắn email.
- **Trường hợp B:** Máy đăng nhập bằng **tài khoản Microsoft**, tức tài khoản gắn email như `ten@outlook.com`, `ten@gmail.com`.

Hai trường hợp chỉ khác nhau ở **ô Tài khoản** và **loại mật khẩu** cần nhập. Mọi bước còn lại giống nhau.

---

## 1. Chuẩn bị (chung cho cả hai trường hợp)

### 1.1. Yêu cầu

| Hạng mục | Yêu cầu |
|---|---|
| Hệ điều hành | Windows 11, hoặc Windows 10 bản 1809 trở lên (nên dùng 22H2). Chỉ hỗ trợ bản **64-bit** |
| Không hỗ trợ | Windows 32-bit, Windows 10 trên chip ARM, Windows ở chế độ S mode |
| Thiết bị | tinyTouch đã có **ít nhất 1 vân tay** đăng ký trên chip |
| Quyền | Tài khoản Windows có quyền Administrator để cài đặt |
| Mật khẩu | Bạn phải **nhớ mật khẩu đăng nhập Windows**. Mã PIN, khuôn mặt hay vân tay Windows Hello đều không dùng thay được. **Nếu quên mật khẩu, xem mục 5.2** |

> **Vì sao cần mật khẩu thật?** Khi bạn chạm vân tay, tinyTouch không thay thế cơ chế đăng nhập của Windows. Ứng dụng gửi **mật khẩu Windows** (lưu mã hóa trên máy) vào màn hình đăng nhập, giống như bạn tự gõ. Vì vậy mật khẩu phải đúng.

### 1.2. Xác định máy đang dùng loại tài khoản nào

1. Mở **Settings** (Win + I) rồi vào **Accounts** > **Your info**.
2. Đọc phần dưới tên của bạn:
   - Nếu thấy **"Local account"** thì làm theo **Trường hợp A**.
   - Nếu thấy **một địa chỉ email** cùng dòng "Manage my accounts" thì làm theo **Trường hợp B**.

Cách khác: tại màn hình đăng nhập Windows, nếu dưới tên người dùng có hiện email thì đó là tài khoản Microsoft.

> **Lưu ý:** Từ phiên bản 1.1.9, ứng dụng **tự nhận ra tài khoản Microsoft** và điền sẵn email vào ô Tài khoản. Bạn vẫn nên kiểm tra lại theo cách trên.

### 1.3. Cài đặt ứng dụng

1. Chạy file **`tinyTouch-Setup-x64.exe`**.
2. Nếu Windows hiện cảnh báo SmartScreen ("Windows protected your PC"), bấm **More info** rồi **Run anyway**. Cảnh báo xuất hiện vì bộ cài chưa được ký số.
3. Bấm **Yes** khi Windows hỏi quyền Administrator.
4. Bấm **Next** > **Install**, đợi cài xong.
5. Nếu bộ cài hỏi về tùy chọn *"Chỉ cho phép đăng nhập bằng Windows Hello cho tài khoản Microsoft"*, chọn **Yes** để tắt tùy chọn đó. Nếu không tắt, ô vân tay tinyTouch sẽ bị ẩn ở màn hình khóa. Xem thêm mục 4.2.
6. Ở trang cuối, giữ dấu tích **"Mở cài đặt tinyTouch Security & Ghép nối 1-Chạm"** rồi bấm **Finish**.
7. **Khởi động lại máy** để màn hình đăng nhập nạp ô (tile) tinyTouch. Cần làm bước này ở lần cài đầu tiên.

### 1.4. Kiểm tra kết nối thiết bị

1. Cắm tinyTouch vào cổng USB.
2. Mở ứng dụng **tinyTouch Security**, từ biểu tượng trên Desktop hoặc biểu tượng ở khay hệ thống góc phải dưới.
3. Ở góc trên bên phải, ô trạng thái phải hiện **"Đã kết nối (COMx)"**, ví dụ "Đã kết nối (COM5)".
   - Nếu hiện **"Chưa cắm USB"**: thử cắm lại, đổi cổng USB hoặc đổi cáp. Cáp phải truyền được dữ liệu, không chỉ sạc.
   - Nếu hiện **"Mất kết nối Service"**: đợi vài giây. Nếu vẫn vậy, khởi động lại máy.
4. Dòng **"Số Serial: … | Máy tính đã lưu trên chip: x/8"** cho biết chip đã ghép với bao nhiêu máy. Mỗi chip lưu tối đa **8 máy tính**.
5. Kéo xuống mục **4. Quản lý Vân tay trên Chip** và kiểm tra có ít nhất một slot **"✅ Đã đăng ký"**. Nếu chưa có, bấm **Đăng ký** ở một slot và làm theo hướng dẫn trên màn hình trước khi ghép đôi.

---

## 2. Trường hợp A: Tài khoản cục bộ (Local account)

### 2.1. Tìm đúng tên tài khoản

Tên tài khoản cục bộ là **tên đăng nhập**, không phải tên hiển thị. Cách xem chính xác nhất:

1. Mở **Command Prompt** (gõ `cmd` vào ô tìm kiếm).
2. Gõ lệnh sau rồi nhấn Enter:

   ```
   whoami
   ```

3. Kết quả có dạng `TEN-MAY\tenDangNhap`, ví dụ `DESKTOP-AB12CD\Viet`. Phần **sau dấu `\`** là tên cần nhập, ở ví dụ này là `Viet`.

Ứng dụng thường đã điền sẵn đúng tên này.

### 2.2. Ghép đôi

1. Trong ứng dụng, đến mục **1. Tài khoản Windows & Ghép nối Bảo mật 1-Chạm**.
2. **Tài khoản Windows:** kiểm tra tên đăng nhập, ví dụ `Viet`.
   - Không nhập tên máy phía trước (`DESKTOP-AB12CD\`).
   - Không nhập email.
3. **Mật khẩu Windows:** nhập mật khẩu bạn dùng để đăng nhập Windows. Phân biệt chữ hoa và chữ thường.
4. Bấm **Ghép nối 1-Chạm (Auto-Pair)**.
5. Khi dòng trạng thái báo *"Hãy chạm ngón tay đã đăng ký lên cảm biến tinyTouch để xác nhận..."*, **chạm một ngón tay đã đăng ký** lên cảm biến trong vòng **20 giây**.
6. Đợi dòng trạng thái báo **"Ghép nối thành công thiết bị … với tài khoản …!"**.
7. Kéo xuống mục **3. Danh sách Thiết bị đã Ghép nối** và kiểm tra có dòng dạng:

   ```
   <Serial> [Đang cắm]  —  Tài khoản: Viet  (Key ID: xxxxxxxxxxxxxxxx)
   ```

### 2.3. Trường hợp đặc biệt: tài khoản không có mật khẩu

Nếu tài khoản cục bộ **không đặt mật khẩu** (để trống), Windows không cho đăng nhập theo cách này. Bạn cần đặt mật khẩu trước: vào **Settings > Accounts > Sign-in options > Password > Add**, sau đó ghép đôi lại.

---

## 3. Trường hợp B: Tài khoản Microsoft

### 3.1. Những điểm khác biệt quan trọng

| | Cần nhập | KHÔNG được nhập |
|---|---|---|
| **Tài khoản** | **Địa chỉ email** của tài khoản Microsoft, ví dụ `ten@outlook.com` | Tên thư mục ngắn như `tenvi` hay `tenvi_000` (tên trong `C:\Users\…`) |
| **Mật khẩu** | **Mật khẩu tài khoản Microsoft**, tức mật khẩu đăng nhập outlook.com hoặc account.microsoft.com | **Mã PIN** Windows Hello |

> **Vì sao không dùng được PIN?** PIN chỉ dùng được trên máy đó và gắn với chip bảo mật TPM. Windows chỉ cho bên thứ ba như tinyTouch đăng nhập bằng mật khẩu tài khoản. Nếu nhập PIN, ghép đôi vẫn báo thành công, nhưng khi mở khóa Windows sẽ từ chối.

### 3.2. Kiểm tra trước khi ghép đôi

1. **Kiểm tra email tài khoản:** vào **Settings > Accounts > Your info**, ghi lại email hiển thị.
2. **Kiểm tra bạn còn nhớ mật khẩu:** đăng nhập thử tại trang `account.microsoft.com` bằng email và mật khẩu đó.
   - Nếu không nhớ, làm theo **mục 5.2** để đặt mật khẩu mới, sau đó quay lại đây.
3. **Tài khoản không mật khẩu (passwordless):** nếu bạn đã bật tính năng *"Passwordless account"* trên trang tài khoản Microsoft, tài khoản không còn mật khẩu nên tinyTouch **không thể dùng được**. Hãy tắt tính năng này tại `account.microsoft.com` > **Security** > **Advanced security options** > **Passwordless account**, rồi đặt lại mật khẩu.
4. **Tùy chọn chỉ dùng Windows Hello:** vào **Settings > Accounts > Sign-in options**, tìm mục *"For improved security, only allow Windows Hello sign-in for Microsoft accounts on this device"* và chuyển sang **Off**. Nếu để **On**, ô tinyTouch sẽ bị ẩn ở màn hình khóa.

### 3.3. Ghép đôi

1. Mở ứng dụng. Dòng trạng thái sẽ báo:

   > *Đã nhận diện tài khoản Microsoft: ten@outlook.com. Hãy nhập mật khẩu tài khoản Microsoft (không phải mã PIN).*

2. **Tài khoản Windows:** kiểm tra ô này đang là **email** của bạn. Nếu ô đang là tên ngắn, hãy xóa đi và gõ email đầy đủ.
3. **Mật khẩu Windows:** nhập **mật khẩu tài khoản Microsoft**.
4. Bấm **Ghép nối 1-Chạm (Auto-Pair)**.
5. **Chạm một ngón tay đã đăng ký** lên cảm biến trong vòng **20 giây**.
6. Đợi dòng trạng thái báo **"Ghép nối thành công…"**.
7. Kiểm tra mục **3. Danh sách Thiết bị đã Ghép nối**, dòng thiết bị phải hiện **Tài khoản là email**:

   ```
   <Serial> [Đang cắm]  —  Tài khoản: ten@outlook.com  (Key ID: xxxxxxxxxxxxxxxx)
   ```

### 3.4. Máy công ty dùng tài khoản cơ quan (Microsoft Entra ID / Azure AD)

Nếu máy do công ty cấp và đăng nhập bằng email công ty, ví dụ `ten@congty.com`, làm giống Trường hợp B: nhập **email công ty** và **mật khẩu công ty**. Ứng dụng tự nhận ra máy đã gia nhập Entra ID. Một số công ty chặn Credential Provider bên thứ ba bằng chính sách quản trị; khi đó cần hỏi bộ phận IT.

### 3.5. Đã lỡ ghép đôi bằng tên ngắn hoặc mã PIN

Không cần ghép lại từ đầu:

1. Mở ứng dụng. Nếu đã lưu tên ngắn, ứng dụng tự đổi ô Tài khoản sang email và hiện cảnh báo.
2. Nhập **mật khẩu tài khoản Microsoft** vào ô Mật khẩu.
3. Bấm **Cập nhật Mật khẩu**.

---

## 4. Kiểm tra sau khi ghép đôi (chung cho cả hai trường hợp)

### 4.1. Thử mở khóa

1. Trong mục **2. Chế độ Bảo vệ & Mở khóa Màn hình**, kiểm tra ô **"Mở khóa màn hình Windows (Win + L / Khởi động máy) bằng vân tay"** đã được tích.
2. Nhấn **Win + L** để khóa máy.
3. Ở màn hình khóa, ô tinyTouch hiện dòng **"Chạm ngón tay lên tinyTouch để mở khóa."**.
   - Nếu chỉ thấy ô PIN hoặc mật khẩu, bấm **Sign-in options** rồi chọn biểu tượng tinyTouch.
4. Chạm ngón tay đã đăng ký. Màn hình hiện **"Đã nhận vân tay, đang đăng nhập..."** rồi vào Windows.
5. Thử thêm: **khởi động lại máy** và chạm vân tay ở màn hình đăng nhập đầu tiên.

> Ở màn hình có ảnh nền và đồng hồ, bạn có thể chạm vân tay ngay mà không cần bấm phím. Nếu màn hình không đổi, nhấn một phím bất kỳ rồi chạm lại.

### 4.2. Ý nghĩa các dòng trạng thái trên ô tinyTouch ở màn hình khóa

| Dòng trạng thái | Nguyên nhân | Cách xử lý |
|---|---|---|
| Chạm ngón tay lên tinyTouch để mở khóa. | Sẵn sàng | Chạm vân tay |
| Chưa cắm tinyTouch… | Không thấy thiết bị qua USB | Cắm lại thiết bị, hoặc đăng nhập bằng PIN/mật khẩu |
| Máy này chưa ghép nối với tinyTouch… | Chưa ghép đôi, hoặc khóa của máy này đã bị xóa khỏi chip | Đăng nhập bằng PIN/mật khẩu rồi ghép đôi lại (mục 2 hoặc 3) |
| Vân tay không được chấp nhận… | Chạm sai ngón hoặc tín hiệu không hợp lệ | Chạm lại bằng ngón đã đăng ký |
| Mật khẩu Windows đã đổi… | Windows từ chối mật khẩu đang lưu | Xem mục 5.1 |
| Mở khóa bằng vân tay đang tắt… | Ô mở khóa trong app đang tắt | Bật lại trong mục 2 của app |
| Windows đang tạm khóa tài khoản… | Sai mật khẩu quá nhiều lần | Đợi hết thời gian khóa rồi đăng nhập bằng mật khẩu đúng |

> **Cơ chế bảo vệ:** Nếu Windows từ chối mật khẩu đã lưu **một lần**, tinyTouch **tự tạm dừng** mở khóa bằng vân tay để tránh khóa tài khoản do sai mật khẩu nhiều lần. Danh sách thiết bị trong app sẽ hiện **"⚠ Mật khẩu cần cập nhật"** cho tới khi bạn cập nhật mật khẩu đúng.

---

## 5. Các tình huống thường gặp

### 5.1. Đổi mật khẩu Windows hoặc mật khẩu tài khoản Microsoft

1. Ở màn hình khóa, đăng nhập bằng **mật khẩu mới** hoặc PIN.
2. Mở ứng dụng tinyTouch, nhập **mật khẩu mới** vào ô Mật khẩu Windows.
3. Bấm **Cập nhật Mật khẩu**. Không cần chạm vân tay hay ghép lại.

Với tài khoản Microsoft, nếu bạn đổi mật khẩu trên web, hãy đăng nhập Windows bằng mật khẩu mới ít nhất một lần trước khi cập nhật trong app.

### 5.2. Quên mật khẩu Windows nhưng vẫn vào được Windows bằng PIN hoặc khuôn mặt

Đây là trường hợp rất hay gặp: lâu ngày chỉ dùng PIN hoặc khuôn mặt nên quên mật khẩu thật. **tinyTouch không thể khôi phục hay hiển thị lại mật khẩu**, và mã PIN không dùng thay được. Bạn cần **đặt mật khẩu mới**, sau đó lưu mật khẩu mới vào tinyTouch. Cách làm tùy loại tài khoản.

#### Tài khoản Microsoft

1. Trên trình duyệt, mở `account.live.com/password/reset`. Cũng có thể vào `account.microsoft.com` > **Security** > **Change password**.
2. Nhập email tài khoản, nhận mã xác minh qua email phụ hoặc số điện thoại, rồi đặt **mật khẩu mới**.
3. Máy cần **có Internet**. Nhấn **Win + L**, chọn **Sign-in options** > biểu tượng **chìa khóa**, rồi đăng nhập bằng **mật khẩu mới** một lần để Windows nhận mật khẩu mới.
4. Mở ứng dụng tinyTouch, nhập mật khẩu mới vào ô **Mật khẩu Windows** rồi bấm **Cập nhật Mật khẩu**. Nếu chưa ghép đôi thì bấm **Ghép nối 1-Chạm** như mục 3.3.
5. Nhấn **Win + L** và chạm vân tay để thử lại.

> Nếu Windows vẫn nhận mật khẩu cũ ở bước 3, đợi vài phút cho mật khẩu mới đồng bộ rồi thử lại. Máy phải có mạng.

#### Tài khoản cục bộ (Local account)

Khi đang ở trong Windows với quyền Administrator, bạn có thể đặt mật khẩu mới **mà không cần biết mật khẩu cũ**:

1. Bấm **Start**, gõ `cmd`, chuột phải vào **Command Prompt** rồi chọn **Run as administrator**.
2. Gõ lệnh sau, thay `TenDangNhap` bằng tên đăng nhập của bạn (xem bằng lệnh `whoami` như mục 2.1):

   ```
   net user TenDangNhap *
   ```

3. Gõ **mật khẩu mới** hai lần rồi nhấn Enter. Khi gõ, màn hình không hiện ký tự nào; đó là bình thường. Thông báo *"The command completed successfully"* là đã xong.
4. Nhấn **Win + L**, chọn **Sign-in options** > biểu tượng **chìa khóa**, rồi đăng nhập bằng **mật khẩu mới** để chắc chắn mật khẩu đúng.
5. Mở ứng dụng tinyTouch, nhập mật khẩu mới rồi bấm **Cập nhật Mật khẩu**, hoặc **Ghép nối 1-Chạm** nếu chưa ghép.
6. Nhấn **Win + L** và chạm vân tay để thử lại.

> **Cảnh báo khi đặt lại mật khẩu bằng cách này:** Windows coi đây là "đặt lại" chứ không phải "đổi" mật khẩu, nên có thể **mất quyền truy cập**:
>
> - các file mã hóa bằng EFS (thuộc tính *Encrypt contents*),
> - mật khẩu đã lưu trong **Credential Manager** (ổ mạng, Remote Desktop…),
> - một số chứng chỉ cá nhân.
>
> Windows cũng có thể yêu cầu **thiết lập lại mã PIN** ở lần đăng nhập sau. Máy cá nhân thông thường ít bị ảnh hưởng. Nếu dùng EFS, hãy chép các file đó ra nơi khác trước khi đặt lại.

**Nếu tài khoản của bạn không có quyền Administrator**, lệnh trên sẽ báo *"Access is denied"*. Khi đó cần nhờ người có tài khoản Administrator trên máy chạy lệnh, hoặc vào **Settings > Accounts > Other users** để đặt lại mật khẩu cho bạn.

> **Cách khác cho bản Windows Pro:** chạy `lusrmgr.msc`, chọn **Users**, chuột phải vào tài khoản > **Set Password…**. Bản Windows Home không có công cụ này, hãy dùng lệnh `net user`.

#### Quên mật khẩu và không còn cách nào vào được Windows

- **Tài khoản Microsoft:** ở màn hình đăng nhập, bấm **I forgot my password** rồi làm theo hướng dẫn (cần Internet).
- **Tài khoản cục bộ:** ở màn hình đăng nhập, nhập sai một lần rồi bấm **Reset password** để trả lời **câu hỏi bảo mật** (Windows 10 bản 1803 trở lên), hoặc dùng **đĩa đặt lại mật khẩu** (password reset disk) nếu đã tạo trước. Nếu không có cả hai, cần một tài khoản Administrator khác trên máy, hoặc phải cài lại Windows.

> **Phòng ngừa:** sau khi ghép đôi xong, hãy ghi mật khẩu Windows vào nơi an toàn (ví dụ trình quản lý mật khẩu). Bạn vẫn cần nó khi đổi máy, khi tinyTouch không cắm, hoặc khi Windows yêu cầu mật khẩu sau khi cập nhật.

### 5.3. Dùng một tinyTouch cho nhiều máy tính

Lặp lại các bước ghép đôi trên từng máy. Mỗi máy có khóa bảo mật riêng. Một chip lưu tối đa **8 máy**. Xem số máy đã lưu ở dòng *"Máy tính đã lưu trên chip: x/8"*.

### 5.4. Nhiều tài khoản Windows trên cùng một máy

Mỗi thiết bị tinyTouch chỉ gắn với **một tài khoản Windows** trên một máy. Lần ghép đôi sau sẽ thay tài khoản đã lưu trước đó.

### 5.5. Gỡ ghép đôi

- **Xóa Thiết bị đã chọn khỏi máy tính này:** chỉ xóa thông tin lưu trên máy, chip vẫn giữ khóa.
- **Gỡ Máy Tính Này Khỏi Chip tinyTouch:** xóa khóa của máy này khỏi chip, cần chạm vân tay để xác nhận. Dùng khi bán hoặc trả máy.

### 5.6. Ghép đôi báo lỗi

| Thông báo | Cách xử lý |
|---|---|
| Hết thời gian chờ chạm vân tay xác nhận trên tinyTouch. | Bấm Ghép nối lại và chạm trong vòng 20 giây |
| Thiết bị từ chối thao tác: … | Chạm đúng ngón đã đăng ký; kiểm tra chip đã có vân tay |
| Chưa kết nối thiết bị tinyTouch qua cổng USB. | Cắm lại thiết bị và đợi trạng thái "Đã kết nối" |
| Vui lòng nhập đầy đủ Tài khoản Windows và Mật khẩu… | Điền đủ cả hai ô |

> **Lưu ý:** Khi ghép đôi, ứng dụng **không kiểm tra** mật khẩu bạn nhập có đúng hay không. Mật khẩu sai chỉ bị phát hiện ở lần mở khóa đầu tiên. Vì vậy hãy luôn **thử Win + L ngay sau khi ghép đôi** như mục 4.1.

### 5.7. Không đăng nhập được hoặc màn hình đăng nhập bị lỗi

- Luôn có thể bấm **Sign-in options** để đăng nhập bằng **PIN hoặc mật khẩu** như bình thường.
- **Chẩn đoán:** mở PowerShell bằng quyền Administrator, chạy lệnh sau rồi gửi file kết quả cho bộ phận hỗ trợ:

  ```
  powershell -ExecutionPolicy Bypass -File "C:\Program Files\tinyTouch\diagnose-logon.ps1"
  ```

- **Gỡ khẩn cấp:** nếu màn hình đăng nhập không hoạt động, vào Safe Mode rồi chạy `C:\Program Files\tinyTouch\emergency-disable-credential-provider.cmd` bằng quyền Administrator để tắt ô tinyTouch.

---

## 6. Bảo mật

- Mật khẩu Windows được **mã hóa bằng DPAPI** của Windows và lưu tại `C:\ProgramData\tinyTouch`. Chỉ hệ thống (SYSTEM) và Administrator đọc được thư mục này.
- Mật khẩu **không được lưu trên chip tinyTouch**. Chip chỉ lưu khóa xác thực AES-256 dùng để ký tín hiệu "đã chạm vân tay".
- Mỗi tín hiệu chạm chỉ dùng được một lần, có chống phát lại (replay).
- tinyTouch là **ô đăng nhập riêng của bên thứ ba**, không phải Windows Hello. PIN và khuôn mặt Windows Hello vẫn dùng song song bình thường.
