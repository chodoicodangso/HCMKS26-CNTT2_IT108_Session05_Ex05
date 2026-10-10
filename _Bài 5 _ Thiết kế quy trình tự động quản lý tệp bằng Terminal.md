## 1\. Sơ đồ luồng IPO

**Input**: Dữ liệu file thô trong thư mục Downloads.  
**Process**:  
Phân loại file dựa theo đuôi (.png, .jpg, .py, .tmp)  
Kiểm tra xem tên file có bị trùng với một thư mục con sẵn có ở nơi đích hay không.  
**Output**: Di chuyển ảnh vào media/, di chuyển code vào scripts/, xóa file .tmp.

## 2\. Xử lý trường hợp kiểm thử 

**Nguyên nhân lỗi:** Lệnh mv báo lỗi "Is a directory" vì không thể đè một file lên một thư mục trùng tên  
**Cách Robot xử lý:** Robot đọc thấy dòng lỗi này sẽ **bỏ qua (skip)** file đó để không bị crash, rồi chạy tiếp file khác  
3\. Danh sách câu lệnh kịch bản cho Robot  
mv Downloads/\*.png media/  
mv Downloads/\*.jpg media/  
mv Downloads/\*.py scripts/  
rm Downloads/\*.tmp