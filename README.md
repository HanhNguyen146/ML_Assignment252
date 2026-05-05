# Dự đoán Bệnh lý Tim mạch (Heart Disease Prediction)

Dự án áp dụng các thuật toán Machine Learning (Decision Tree, Logistic Regression, Random Forest) để dự đoán khả năng mắc bệnh tim mạch. Mã nguồn được viết và thực thi trên môi trường Google Colab.

## 1. Cấu trúc file Notebook
File `heart_desease_L03.ipynb` được chia làm 4 phần chính, yêu cầu thực thi tuần tự:
* **Phần 1 - Tiền xử lý & EDA:** Tải dữ liệu tự động từ Google Drive, làm sạch, cân bằng dữ liệu bằng SMOTE, chọn lọc đặc trưng (Feature Selection) và lưu tập dữ liệu đã xử lý.
* **Phần 2 - Decision Tree:** Huấn luyện, dò tìm siêu tham số (Coarse/Fine Tuning), tối ưu ngưỡng (Threshold Tuning) và trực quan hóa cây.
* **Phần 3 - Logistic Regression:** Huấn luyện baseline và đánh giá.
* **Phần 4 - Random Forest:** Huấn luyện bằng GridSearchCV, đánh giá và trực quan hóa Feature Importance.

## 2. Hướng dẫn sử dụng trên Google Colab
1. Tải file `.ipynb` lên Google Colab.
2. Trên thanh menu, chọn **Runtime** -> **Run all** (hoặc nhấn `Ctrl + F9`) để chạy toàn bộ file từ trên xuống dưới.
3. **Không cần tải dữ liệu thủ công:** Khối mã đầu tiên đã tích hợp sẵn đoạn code tự động tải dataset gốc từ Google Drive thông qua `file_id`.

## 3. Quản lý Output 
Toàn bộ các file sinh ra trong quá trình chạy sẽ được lưu trữ tạm thời trong thư mục ảo (session storage) của Colab. Nếu session bị đóng, các file này sẽ mất:
* **Thư mục `eda_plots/`:** Chứa các biểu đồ phân tích EDA, phân phối Target và PCA.
* **File dữ liệu:** `heart_train_cleaned.csv` và `heart_test_cleaned.csv` (dùng cho các mô hình ở phần sau).
* **File model:** `preprocessor.pkl`, `selector.pkl`, `decision_tree_model.pkl`, `logistic_regression_model.pkl`, `random_forest_model.pkl`
Vui lòng nhấp vào biểu tượng thư mục ở thanh bên trái của Colab để xem và tải xuống các file này nếu cần.
`link data để train và test`: https://drive.google.com/drive/folders/1a1qutKATEA0QA9JL4nl3I6FKT2c6rCHu?usp=sharing
`link model`: https://drive.google.com/drive/folders/13vTMzHz9GiWDrPrGTrKQ6IcqnPf65KYy?usp=sharing

## 4. Phân công công việc

| Họ và Tên | MSSV | Nhiệm vụ |
|-----------|------|---------|
| Nguyễn Minh Hạnh | 2310895 | Decision Tree |
| Trần Minh Trí | 2313627 | Tiền xử lý & EDA |
| Huyền Câm Ly | 2312008 | Random Forest |
| Phạm Thanh Tín | 2313459 | Logistic Regression |