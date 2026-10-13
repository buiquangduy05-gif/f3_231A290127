Lab F3 - Nhập liệu & Form trong Flutter

Thông tin sinh viên:

Họ và tên: Bùi Quang Duy

MSSV: 231A290127


Tổng quan dự án

Đây là bài thực hành Lab F3 về việc sử dụng các control nhập liệu, quản lý trạng thái form và kiểm tra tính hợp lệ (validation) trong Flutter. Ứng dụng mô phỏng một biểu mẫu đăng ký học phần, bao gồm các thành phần:

TextFormField (Họ tên, MSSV, Email) kết hợp với các validator và inputFormatters chặn dữ liệu sai từ bàn phím.

Các control lựa chọn: DropdownButtonFormField, RadioGroup, CheckboxListTile, Slider, và SwitchListTile.

Quản lý trạng thái form bằng GlobalKey<FormState>.

Các tính năng Nâng cao (Đã hoàn thành)

Trong dự án này, em đã tích hợp thêm 2 tính năng nâng cao theo yêu cầu của đề bài:

1. Bài Nâng cao 2 (NC2): Ràng buộc logic hệ đào tạo và buổi học

Mô tả: Hệ thống kiểm tra tính hợp lệ chéo giữa các control nằm ngoài cơ chế của Form.

Chi tiết xử lý: Nếu người dùng tick chọn hệ "Vừa làm vừa học", hệ thống sẽ bắt buộc người dùng phải chọn buổi "Tối" trong danh sách Checkbox. Nếu người dùng cố tình bỏ trống hoặc chỉ chọn buổi Sáng/Chiều, hàm _dangKy() sẽ chặn lại, không cho phép hiển thị hộp thoại xác nhận và bắn ra một SnackBar cảnh báo dưới đáy màn hình.

2. Bài Nâng cao 3 (NC3): Bộ đếm ký tự cho ô nhập Họ Tên

Mô tả: Giới hạn số lượng ký tự nhập vào và hiển thị trực quan cho người dùng.

Chi tiết xử lý: Sử dụng thuộc tính maxLength: 50 tích hợp sẵn trong widget TextFormField của biến _hoTenCtrl. Việc này giúp Flutter tự động render một bộ đếm ký tự (ví dụ: 15/50) ở góc dưới bên phải của ô nhập, đồng thời tự động chặn người dùng gõ quá 50 ký tự mà không cần phải viết thêm hàm lắng nghe sự kiện (TextWatcher như trong Android).
