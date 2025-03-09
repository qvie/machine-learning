# machine-learning

Mã nguồn này triển khai thuật toán **Logistic Regression (Hồi quy Logistic)** để dự đoán khả năng một khách hàng đăng ký sản phẩm ngân hàng dựa trên tập dữ liệu *bank-additional-full.csv*. Quá trình xử lý bao gồm các bước chính như làm sạch, chuẩn hóa dữ liệu và đánh giá mô hình.  

Bắt đầu bằng việc kiểm tra thông tin tổng quan của dữ liệu, phát hiện và loại bỏ các giá trị trùng lặp để đảm bảo tính chính xác. Các biến phân loại được mã hóa bằng **LabelEncoder** nhằm chuyển đổi dữ liệu dạng văn bản thành số, giúp mô hình xử lý hiệu quả. Những đặc trưng chính được lựa chọn cho quá trình huấn luyện bao gồm:  

- **Tuổi tác (age):** Độ tuổi của khách hàng – một yếu tố quan trọng phản ánh khả năng tham gia các sản phẩm tài chính.  
- **Thời lượng cuộc gọi (duration):** Thời gian cuộc gọi, cho biết mức độ quan tâm của khách hàng đối với sản phẩm.  
- **Số lượng chiến dịch (campaign):** Số lần liên hệ trong chiến dịch hiện tại – đánh giá mức độ tiếp cận.  
- **Số ngày từ chiến dịch trước (pdays):** Khoảng thời gian kể từ lần liên hệ trước – phản ánh mức độ cập nhật thông tin.  
- **Số lần liên hệ trước (previous):** Số lần liên hệ thành công trước đó – thể hiện lịch sử tương tác.  
- **Lãi suất (euribor3m):** Yếu tố tài chính quan trọng, ảnh hưởng trực tiếp đến quyết định của khách hàng.  
- **Số lượng nhân viên ngân hàng (nr.employed):** Đại diện cho tình hình kinh tế và khả năng cung cấp dịch vụ.  

Dữ liệu đầu vào được chuẩn hóa bằng **StandardScaler** để đưa các đặc trưng về cùng một thang đo, giúp cải thiện hiệu suất và độ hội tụ của mô hình.  

Mô hình **Logistic Regression** được huấn luyện với tham số **max_iter=2000** nhằm đảm bảo khả năng hội tụ trên tập dữ liệu lớn. Hiệu suất của mô hình được đánh giá qua:  

- **Độ chính xác (Accuracy):** Mô hình đạt **90.32%**, cho thấy khả năng phân loại chính xác phần lớn khách hàng.  
- **Báo cáo phân loại (Classification Report):** Cung cấp các chỉ số như **Precision**, **Recall** và **F1-score**, giúp đánh giá chi tiết hiệu suất của mô hình trên từng lớp.  
- **Ma trận nhầm lẫn (Confusion Matrix):** Minh họa số lượng dự đoán đúng và sai, giúp xác định các lỗi mà mô hình mắc phải.  
- **Hệ số mô hình:** Cho biết mức độ ảnh hưởng của từng đặc trưng đến kết quả dự đoán.  

Mô hình này có ứng dụng thực tiễn trong lĩnh vực **ngân hàng**, giúp xác định các khách hàng tiềm năng có khả năng đăng ký sản phẩm. Dựa vào kết quả dự đoán, ngân hàng có thể tối ưu hóa chiến lược tiếp thị, tập trung vào những khách hàng có tiềm năng cao, từ đó nâng cao hiệu quả chiến dịch, giảm thiểu chi phí và cải thiện tỷ lệ chuyển đổi.  

Với độ chính xác **90.32%**, mô hình không chỉ mang lại khả năng dự đoán đáng tin cậy mà còn giúp các tổ chức tài chính ra quyết định thông minh hơn, cải thiện hiệu quả kinh doanh và tối ưu hóa quy trình hoạt động.
