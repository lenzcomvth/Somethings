# EoDServerTool - Hướng Dẫn Sử Dụng

## 📋 Tổng Quan

**EoDServerTool** là một ứng dụng desktop được phát triển bằng C# WinForms, được thiết kế để quản lý và chỉnh sửa dữ liệu item table cho game server. Ứng dụng cung cấp giao diện trực quan và các công cụ mạnh mẽ để thao tác với dữ liệu game một cách hiệu quả.

## 🚀 Tính Năng Chính

### 1. **Quản Lý Item Table**
- Mở và chỉnh sửa file item table
- Hỗ trợ nhiều loại item (Weapon, Armor, Consuming, v.v.)
- Hiển thị dữ liệu dạng bảng với khả năng sắp xếp và lọc

### 2. **Hệ Thống Copy/Paste/Undo/Redo**
- **Copy**: Sao chép một hoặc nhiều rows
- **Paste**: Dán dữ liệu với tự động gán ObjID mới
- **Undo/Redo**: Hoàn tác và khôi phục các thao tác (Ctrl+Z/Ctrl+Y)

### 3. **Quản Lý Rank và Set**
- Quản lý rank của items
- Quản lý set items và bonus
- Tìm kiếm và lọc theo rank

### 4. **Công Cụ Tùy Chỉnh**
- Multi Option: Xử lý nhiều options cùng lúc
- Custom All: Tùy chỉnh hàng loạt
- Merger Files: Gộp nhiều file
- Column Settings: Tùy chỉnh hiển thị cột

## 🎯 Hướng Dẫn Sử Dụng

### **Khởi Động Ứng Dụng**

1. **Mở File Item Table**
   - Menu `File` → `Open Item Table...`
   - Chọn file item table (.bit, .rar)
   - Ứng dụng sẽ tự động load và hiển thị dữ liệu

2. **Chọn Item Type**
   - Sử dụng ComboBox ở đầu bảng để chọn loại item
   - Các loại item: Weapon, Armor, Consuming, Accessory, v.v.

### **Thao Tác Cơ Bản với Dữ Liệu**

#### **1. Copy/Paste Rows**

**Copy:**
- Chọn một hoặc nhiều rows bằng cách click vào row header
- Sử dụng `Ctrl+C` hoặc Menu `Edit` → `📋 Copy`
- Dữ liệu được lưu vào clipboard và bộ nhớ nội bộ

**Paste:**
- Chọn Item Type đích
- Sử dụng `Ctrl+V` hoặc Menu `Edit` → `📄 Paste`
- Hệ thống tự động gán ObjID mới theo thứ tự tăng dần
- Ví dụ: Max ObjID hiện tại = 10, paste 3 rows → ObjID mới: 11, 12, 13

#### **2. Undo/Redo (Hoàn Tác/Khôi Phục)**

**Hoàn Tác (Undo):**
- `Ctrl+Z` hoặc Menu `Edit` → `↩️ Undo`
- Hoàn tác hành động gần nhất (Edit, Delete, Paste)

**Khôi Phục (Redo):**
- `Ctrl+Y` hoặc Menu `Edit` → `↪️ Redo`
- Khôi phục hành động đã hoàn tác

**Lưu ý:** Undo/Redo chỉ hoạt động cho các thao tác thay đổi dữ liệu, không áp dụng cho việc mở file.

#### **3. Chỉnh Sửa Ô Dữ Liệu**

**Sửa Ô:**
- Double-click vào ô cần sửa
- Nhập giá trị mới
- Nhấn Enter hoặc click ra ngoài để lưu
- Hệ thống tự động ghi nhận thay đổi để Undo/Redo

**Xóa Rows:**
- Chọn rows cần xóa
- Nhấn `Delete` key hoặc sử dụng context menu
- Xác nhận xóa (không cần xác nhận - xóa trực tiếp)

### **Công Cụ Nâng Cao**

#### **1. Multi Option**
- Menu `Custom` → `⚙️ Multi Option`
- Xử lý nhiều options cùng lúc
- Hữu ích cho việc cập nhật hàng loạt

#### **2. Custom All**
- Menu `Custom` → `🔧 Custom All`
- Tùy chỉnh toàn bộ dữ liệu theo quy tắc
- Áp dụng thay đổi cho nhiều items

#### **3. Merger Files**
- Menu `Custom` → `🔄 Merger File`
- Gộp nhiều file item table
- Tự động xử lý xung đột ObjID

#### **4. Column Settings**
- Menu `Custom` → `⚙️ Column Settings...`
- Tùy chỉnh hiển thị cột
- Ẩn/hiện cột theo nhu cầu
- Lưu cài đặt cho lần sử dụng sau

### **Quản Lý Rank và Set**

#### **1. Rank Management Tab**
- Chuyển sang tab "Rank Management"
- Quản lý rank của items
- Tìm kiếm và lọc theo rank

#### **2. Set Management**
- Quản lý set items và bonus
- Tạo và chỉnh sửa set
- Gán items vào set

## ⌨️ Phím Tắt

| Phím Tắt | Chức Năng | Mô Tả |
|-----------|-----------|-------|
| `Ctrl+C` | Copy | Sao chép rows đã chọn |
| `Ctrl+V` | Paste | Dán dữ liệu đã copy |
| `Ctrl+Z` | Undo | Hoàn tác hành động gần nhất |
| `Ctrl+Y` | Redo | Khôi phục hành động đã undo |
| `Delete` | Delete | Xóa rows đã chọn |
| `F5` | Refresh | Làm mới dữ liệu |

## 🎨 Giao Diện

### **Menu Bar**
```
File          Edit                    Custom                    Help
├── Open Item ├── 📋 Copy (Ctrl+C)   ├── ⚙️ Multi Option      └── About
├── Open XSD  ├── 📄 Paste (Ctrl+V)  ├── 🔧 Custom All
├── ───────── ├── 🆔 Copy Single ID  ├── 🔄 Merger File
└── Exit      ├── ───────────────    ├── ⚙️ Column Settings
              ├── ↩️ Undo (Ctrl+Z)    └── ─────────────
              ├── ↪️ Redo (Ctrl+Y)
              ├── ─────────────
              ├── 🔄 Refresh (F5)
              └── ─────────────
```

### **Main Interface**
- **Tab Control**: Chuyển đổi giữa các chức năng
- **DataGridView**: Hiển thị dữ liệu dạng bảng
- **Status Bar**: Hiển thị thông tin trạng thái và hướng dẫn
- **Info Label**: Hiển thị ObjID của row được chọn

## ⚠️ Lưu Ý Quan Trọng

### **1. Backup Dữ Liệu**
- Luôn backup file gốc trước khi chỉnh sửa
- Sử dụng chức năng Save thường xuyên
- Kiểm tra dữ liệu sau khi paste hoặc merge

### **2. ObjID Management**
- ObjID phải là duy nhất trong mỗi Item Type
- Hệ thống tự động gán ObjID mới khi paste
- Không được thay đổi ObjID thủ công trừ khi cần thiết

### **3. Undo/Redo**
- Undo/Redo chỉ hoạt động trong phiên làm việc hiện tại
- Khi mở file mới, lịch sử undo/redo sẽ bị xóa
- Mỗi thao tác edit, delete, paste đều được ghi nhận

### **4. Performance**
- Với file lớn, nên sử dụng filter để giảm tải
- Refresh dữ liệu khi cần thiết
- Đóng các form không sử dụng để tiết kiệm bộ nhớ

## 🔧 Xử Lý Sự Cố

### **1. Lỗi Load File**
- Kiểm tra định dạng file (.bit, .rar)
- Đảm bảo file không bị hỏng
- Kiểm tra quyền truy cập file

### **2. Lỗi Paste**
- Kiểm tra Item Type đích có phù hợp không
- Đảm bảo có đủ quyền ghi file
- Kiểm tra dung lượng ổ đĩa

### **3. Lỗi Undo/Redo**
- Kiểm tra xem có thao tác nào để undo/redo không
- Refresh dữ liệu nếu cần
- Kiểm tra log để tìm nguyên nhân

## 📝 Log và Debug

### **Log Files**
- Ứng dụng tự động log các thao tác quan trọng
- Log được lưu trong thư mục Log/
- Kiểm tra log khi gặp lỗi

### **Status Bar**
- Luôn hiển thị thông tin trạng thái
- Hướng dẫn sử dụng phím tắt
- Thông báo lỗi và thành công

## 🚀 Tính Năng Nâng Cao

### **1. Drag & Drop**
- Kéo thả file để mở
- Kéo thả rows để sắp xếp lại

### **2. Auto-Save**
- Tự động lưu thay đổi
- Backup tự động
- Recovery khi gặp sự cố

### **3. Batch Processing**
- Xử lý hàng loạt items
- Import/Export dữ liệu
- Validation dữ liệu

## 📞 Hỗ Trợ

### **Tài Liệu**
- Xem thêm các file markdown trong thư mục docs/
- Hướng dẫn chi tiết cho từng tính năng

### **Troubleshooting**
- Kiểm tra log files
- Xem status bar để biết thông tin lỗi
- Sử dụng Undo/Redo để khôi phục

---

**Phiên bản:** 1.0  
**Cập nhật lần cuối:** 2025  
**Tác giả:** EoDServerTool Development Team 