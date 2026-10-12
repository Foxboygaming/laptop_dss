HƯỚNG DẪN CÀI ĐẶT VÀ CHẠY DỰ ÁN LAPTOP DSS (HỆ TRỢ GIÚP QUYẾT ĐỊNH)

========================================================================
PHẦN 1: CÀI ĐẶT MÔI TRƯỜNG NỀN TẢNG (PYTHON)
========================================================================
1. Tải Python: Truy cập https://www.python.org/downloads/ 
   - Khuyên dùng: Python 3.10, 3.11 hoặc 3.12 (Không dùng bản 3.15 để tránh lỗi thư viện).
2. Khi chạy file cài đặt Python, **BẮT BUỘC** phải tích chọn ô:
   [x] Add python.exe to PATH (nằm ở dưới cùng màn hình cài đặt đầu tiên).
   Sau đó mới bấm "Install Now".


========================================================================
PHẦN 2: LẤY MÃ NGUỒN VÀ MỞ COMMAND PROMPT (CMD)
========================================================================
1. Tải mã nguồn dự án (file ZIP) và giải nén vào máy tính.
2. Mở thư mục gốc của dự án (thư mục chứa file app.py, train_model.py...).
3. Click chuột vào thanh địa chỉ của thư mục, xóa toàn bộ đường dẫn hiện tại, gõ chữ 'cmd' rồi nhấn Enter. Cửa sổ lệnh màu đen sẽ hiện ra tại đúng thư mục này.


========================================================================
PHẦN 3: CÀI ĐẶT CÁC THƯ VIỆN LÕI BẮT BUỘC
========================================================================
Để hệ thống AI và giao diện Web chạy mượt mà, không bị xung đột phiên bản, bạn cần copy và dán CHÍNH XÁC dòng lệnh sau vào cửa sổ CMD vừa mở, rồi nhấn Enter:

py -m pip install pandas streamlit joblib "scikit-learn==1.3.2" "numpy<2"

* Đợi hệ thống tải và cài đặt xong (thông báo "Successfully installed...").


========================================================================
PHẦN 4: CÁCH CHẠY DỰ ÁN
========================================================================

> LỆNH 1: KHỞI CHẠY GIAO DIỆN WEB (CHÍNH)
Sau khi cài thư viện xong, gõ lệnh sau để mở phần mềm:

py -m streamlit run app.py

- Hệ thống sẽ cấp một đường link (Local URL: http://localhost:8501).
- Trình duyệt sẽ tự động mở trang web lên để bạn sử dụng.


> LỆNH 2: HUẤN LUYỆN LẠI MÔ HÌNH (TÙY CHỌN)
* Lưu ý: Bạn CHỈ CẦN chạy lệnh này nếu bạn vừa cập nhật/thêm mới dữ liệu vào file `training_dataset.csv` và muốn tạo ra file mô hình AI mới.
- Tại cửa sổ CMD, gõ lệnh:

py train_model.py

- Sau khi lệnh chạy xong (không báo lỗi), bạn mới chạy lại Lệnh 1 để mở Web.
