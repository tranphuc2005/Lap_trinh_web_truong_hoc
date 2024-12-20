# **Website Quản Lý Thông Tin Sinh Viên và Tài Liệu Lớp Học**

## **1. Giới Thiệu**
Website này được thiết kế để quản lý thông tin sinh viên, tài liệu của lớp học và các chức năng liên quan đến giáo viên và sinh viên. Các tính năng bao gồm quản lý thông tin người dùng, giao bài, trả bài, trò chơi giải đố, upload dữ liệu, backup và import người dùng. Hệ thống này sử dụng cơ sở dữ liệu MySQL để lưu trữ dữ liệu người dùng và tài liệu.

---

## **2. Tính Năng Chính**
### **2.1. Quản Lý Sinh Viên**
- **Giáo viên** có thể **thêm, sửa, xóa thông tin** của sinh viên, bao gồm các trường: tên đăng nhập, mật khẩu, họ tên, email, và số điện thoại.
- **Sinh viên** có thể **thay đổi các thông tin của mình**, trừ tên đăng nhập và họ tên.
- Tất cả người dùng có thể **xem danh sách người dùng** và **xem thông tin chi tiết** của người khác, bao gồm cả **để lại tin nhắn** cho người dùng đó. Người dùng có thể **sửa hoặc xóa tin nhắn đã gửi**.

### **2.2. Giao Bài và Trả Bài**
- **Giáo viên** có thể **upload bài tập** dưới dạng tệp tin, và **sinh viên** có thể **xem danh sách bài tập** và **tải về** bài tập.
- **Sinh viên** có thể **upload bài làm** của mình tương ứng với bài tập đã giao. **Chỉ giáo viên** mới có quyền **xem danh sách bài làm**.

### **2.3. Trò Chơi Giải Đố**
- **Giáo viên** có thể tạo **trò chơi giải đố** với các yêu cầu sau:
  - Tạo **challenge**: Giáo viên upload một tệp tin txt chứa bài thơ hoặc văn bản, tên tệp không có dấu và các từ cách nhau bằng khoảng trắng. Cung cấp gợi ý về quyển sách.
  - **Sinh viên** nhập **đáp án** dựa trên gợi ý và nếu đúng sẽ xem được nội dung bài thơ hoặc văn bản.
  
### **2.4. Upload Tệp XML để Thêm Nhiều User**
- **Giáo viên** có thể **upload tệp XML** để thêm nhiều người dùng vào hệ thống. Mẫu XML:
  ```xml
  <?xml version="1.0" encoding="UTF-8"?>
  <user>
    <username>johndoe</username>
    <email>johndoe@example.com</email>
    <phone>+1 (555) 1234567</phone>
    <fullname>John Doe</fullname>
    <role>admin</role>
  </user>
- Sau khi upload, hệ thống sẽ hiển thị danh sách các người dùng trong bảng với các thông tin: username, email, phone, fullname, role và password mặc định là 123qweaA@. Giáo viên có thể lưu và cập nhật các người dùng vào cơ sở dữ liệu.

### **2.5. Lấy Ảnh và Tài Liệu từ Link Ngoài**
Học sinh và giáo viên có thể nhập URL của ảnh hoặc tài liệu và hệ thống sẽ tự động hiển thị preview của tài liệu hoặc ảnh đó.

### **2.6. Backup và Import Người Dùng**
Giáo viên có thể backup thông tin người dùng trong cơ sở dữ liệu dưới dạng đối tượng và tải về file backup.
Sau đó, import file backup vào hệ thống để lưu lại các thông tin vào cơ sở dữ liệu.

## **3. Yêu Cầu Hệ Thống**
- **Hệ điều hành:** Linux, macOS, hoặc Windows.
- **Cơ sở dữ liệu:** MySQL.
- **Ngôn ngữ lập trình:** PHP (hoặc ngôn ngữ lập trình tùy chọn).
- **Web Server:** Apache hoặc Nginx.
- **Trình duyệt:** Chrome, Firefox hoặc các trình duyệt hiện đại khác.
