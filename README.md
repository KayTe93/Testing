Phát hiện tính sống động (Face Liveness Detection) của khuôn mặt bằng các kỹ thuật trí tuệ nhân tao

Tính Năng Nổi Bật

Hệ thống sử dụng cơ chế bảo mật **"Hybrid 2 Lớp"** (Kép):

1. Phân tích Bề mặt (Passive Liveness)
    + Sử dụng mạng nơ-ron tích chập (TextureCNN) để soi chi tiết lỗ chân lông và độ phản xạ ánh sáng của da.
    + Phát hiện ngay lập tức nếu đưa màn hình điện thoại hoặc ảnh in vào camera.

2. Thử thách Hành vi (Active Liveness)
    + Sử dụng **MediaPipe Face Mesh** (Google) để theo dõi cử động khuôn mặt.
    + Yêu cầu người dùng thực hiện chuỗi hành động: Chớp mắt, Cười, Mở miệng.
    + Bộ đếm thời gian thực: Hiển thị số lần chớp mắt, số lần cười ngay trên màn hình.


Cài Đặt Môi Trường
yêu cầu Python 3.7 trở lên và các thư viện sau:
cài đặt thư viện :
    pip install torch torchvision opencv-python mediapipe numpy pillow


Hướng Dẫn Sử Dụng
Bước 1: Chuẩn bị dữ liệu
- Thu thập ảnh khuôn mặt thật và ảnh
- Chuẩn bị video hoặc ảnh giả (ảnh in)
Bước 2: Huấn luyện mô hình TextureCNN
- Chạy script huấn luyện mô hình với dữ liệu đã chuẩn bị (train_texture_cnn.py)
- Lưu mô hình đã huấn luyện để sử dụng sau này
Bước 3: Chạy hệ thống phát hiện tính sống động
- Chạy script chính (face_liveness_detection.py)
- chạy realtime_app_v2.py
- Hướng camera vào khuôn mặt và làm theo
- Quan sát kết quả phát hiện tính sống
- Điều chỉnh ngưỡng phát hiện nếu cần thiết


---