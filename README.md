 Đồ án tương tác trực quan hóa dữ liệu và áp dụng Machine Learning
---------------------------------------
# 1. Giới thiệu đề tài
- Nhận thấy Marketing là một lĩnh vực quan trọng trong kinh doanh và được áp dụng rộng rãi trong nhiều ngành công nghiệp. Dữ liệu về marketing cung cấp thông tin về xu hướng tiêu dùng, phản hồi khách hàng, chiến lược tiếp thị và quảng cáo, hiệu quả các chiến dịch tiếp thị, và nhiều yếu tố khác liên quan đến việc xây dựng và quản lý thương hiệu.
Sử dụng trực quan hóa dữ liệu trong marketing có nhiều lợi ích, bao gồm:
-	Hiểu rõ hơn về khách hàng: Khai phá dữ liệu giúp phân tích và hiểu rõ hơn về thông tin khách hàng, từ đó có thể tạo ra chiến lược marketing phù hợp và tăng cường sự tương tác với khách hàng.
- Tối ưu hóa chiến dịch quảng cáo: Bằng cách sử dụng khai phá dữ liệu, các nhà quảng cáo có thể tối ưu hóa chiến dịch quảng cáo của mình, từ việc chọn đối tượng khách hàng phù hợp cho đến tối ưu hóa chiến lược quảng cáo.
- Phân cụm khách hàng,từ đó hiểu rõ từng nhóm khách hàng và có chiến lược tối ưu cho từng nhóm khách hàng.
# 2.Thông tin về dataset
- Tập dữ liệu mà nhóm chúng em chọn có tên là "Marketing Data" và được lưu trữ trên trang Kaggle. Nguồn dữ liệu thu thập: https://www.kaggle.com/datasets/jackdaoud/marketing-data 
- Tập dữ liệu này bao gồm thông tin về các chiến dịch tiếp thị của một công ty trong vòng 3 năm (2012-2014). 
- Tập dữ liệu này bao gồm các biến : Đã có chi tiết trong file readme.txt
# 3. Nội dung chính dự án
## 3.1 Làm sạch dữ liệu:
- Trực quan tập dữ liệu và loại bỏ Outlier
![image](https://github.com/nguyenthanhhungDE/Data-Visualization/assets/134383281/d5cab3f7-612f-4440-8c8c-b433d3c8e6c0)

- Kiểm tra tìm Missing data và fill bằng phương pháp mean
![image](https://github.com/nguyenthanhhungDE/Data-Visualization/assets/134383281/26558368-9b85-41d3-8616-197e1d1725b3)

- Tạo các cột cần thiết và chuyển đôi kiểu dữ liệu
![image](https://github.com/nguyenthanhhungDE/Data-Visualization/assets/134383281/89678a70-4f02-4cb6-b939-749519b9e47c)

- Vẽ biểu đồ tương quan
![image](https://github.com/nguyenthanhhungDE/Data-Visualization/assets/134383281/006fdf43-c960-4080-b6d9-3afda0b24c14)

## 3.2 Tiền xử lí dữ liệu:
- Mã hóa các cột biến phân loại
- Chuẩn hóa dữ liệu bằng phương pháp Scale data using Standard Scaler
![image](https://github.com/nguyenthanhhungDE/Data-Visualization/assets/134383281/91d0b4ac-f9d8-4f98-9106-96d66e5071c0)

- Giảm chiều dữ liệu xuống còn 3 thuộc tính và trực quan các quan sát
![image](https://github.com/nguyenthanhhungDE/Data-Visualization/assets/134383281/7848b236-ad6f-4b2e-8979-f8f0ab17c057)

3.2 Xây dựng thuật toán K-means phân cụm khách hàng:
- Tìm số cụm K phù hợp bằng Elbow
![image](https://github.com/nguyenthanhhungDE/Data-Visualization/assets/134383281/7079541a-69a7-4b47-8773-e8f361a3b54e)
- Tìm thuật toán phân cụm phù hợp
![image](https://github.com/nguyenthanhhungDE/Data-Visualization/assets/134383281/1770d568-f25c-4a9f-a73f-85de08791ff0)

- Trực quan hóa kết quả phân cụm
![image](https://github.com/nguyenthanhhungDE/Data-Visualization/assets/134383281/258460fd-168e-4fe6-af9a-41e969bad26e)
## 3.4 Đánh giá kết quả
- Sự phân bố các cụm
![image](https://github.com/nguyenthanhhungDE/Data-Visualization/assets/134383281/3d9293a2-f34a-44ff-b76f-8020a3c8ae6b)
- Phân cụm dựa trên tổng chi tiêu và thu nhập
![image](https://github.com/nguyenthanhhungDE/Data-Visualization/assets/134383281/4237ef6b-04ee-465e-83d0-064ce0d20ac8)
##### Nhóm 0: chi tiêu thấp và thu nhập thấp
##### Nhóm 3: chi tiêu thấp và thu nhập trung bình
##### Nhóm 2: chi tiêu cao và thu nhập trung bình
##### Nhóm 1: chi tiêu cao và thu nhập cao
- Gán nhãn cụm dữ liệu
![image](https://github.com/nguyenthanhhungDE/Data-Visualization/assets/134383281/6c29ecf7-5040-4fee-89ed-4b0131b1c8f4)
##### chúng ta sẽ phân loại Nhóm 0 là Khách hàng Bình thường, Nhóm 1 là Khách hàng Đặc biệt, Nhóm 2 là Khách hàng Tốt, và Nhóm 3 là Khách hàng có tiềm năng.
- Chi tiêu của từng cụm khách hàng
![image](https://github.com/nguyenthanhhungDE/Data-Visualization/assets/134383281/af4c79f8-3d04-4a72-9910-aa1cc7f0de70)
- Mức chi tiêu cho từng mặt hàng của từng cụm khách hàng
![image](https://github.com/nguyenthanhhungDE/Data-Visualization/assets/134383281/6ceda3b9-deac-4ca2-9d19-0d95b61ec374)
- Tỷ lệ chấp nhận chiến dịch quảng cáo của từng nhóm khác hàng
![image](https://github.com/nguyenthanhhungDE/Data-Visualization/assets/134383281/31bc4d00-1d64-440e-9d58-cabf86c1c00f)
- Kết quả mua hàng qua ưu đãi
![image](https://github.com/nguyenthanhhungDE/Data-Visualization/assets/134383281/501ed6c6-b1b8-4ac9-9919-cb8fb8b12917)
