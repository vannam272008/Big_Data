# Machine Learning
## Spark MLlib
  - Apache Spark cung cấp một API Học máy được gọi là MLlib . PySpark cũng có API học máy này bằng Python. Nó hỗ trợ các loại thuật toán khác nhau, được đề cập bên dưới:

  <img src="https://github.com/vannam272008/Big_Data/blob/main/Machine%20Learning/1.PNG">
  
  => Có hai cách phổ biến để phân nhóm các thuật toán Machine learning. Một là dựa trên phương thức học (learning style), hai là dựa trên chức năng (function) (của mỗi thuật toán).
### Phân nhóm dựa trên phương thức học
**Supervised Learning (Học có giám sát)**
  - Thuật toán tạo ra một hàm ánh xạ dữ liệu vào tới kết quả mong muốn. Một phát biểu chuẩn về một việc học có giám sát là bài toán phân loại: chương trình cần học (cách xấp xỉ biểu hiện của) một hàm ánh xạ một vector tới một vài lớp bằng cách xem xét một số mẫu dữ liệu - kết quả của hàm đó.
  - Hiểu đơn giản sẽ là thuật toán dự đoán đầu ra của một dữ liệu dựa trên các cặp (input, output) đã biết từ trước. Cặp dữ liệu này còn được gọi là (data, label). Supervised learning là nhóm phổ biến nhất trong các thuật toán Machine Learning.
  - Trong đó được chia thành 2 loại nhỏ:

**Classification (Phân loại)**
  - Các label của input data được chia thành một số hữu hạn nhóm.
  - Spark.mllib hỗ trợ nhiều phương pháp khác nhau để phân loại nhị phân, phân loại đa lớp và phân tích hồi quy.
  - Một số thuật toán phổ biến : Decision Tree, Naive Bayes,...
  - Ví dụ: phân loại tin nhắn có phải là spam hay không?

**Regression (Hồi quy tuyến tính)**
  - Các label không được chia thành các nhóm mà là một giá trị thực cụ thể.
  - Mục tiêu của hồi quy là tìm mối quan hệ và sự phụ thuộc giữa các biến. Giao diện làm việc với mô hình hồi quy tuyến tính và tóm tắt mô hình tương tự như trường hợp hồi quy logistic.
  - Ví dụ : + phân loại Email, gồm có email công việc, email gia đình, email spam, ...

**Unsupervised Learning (Học không giám sát)**
  - Mô hình hóa một tập dữ liệu, không có sẵn các ví dụ đã được gắn nhãn. Có thể hiểu đơn giản là chúng ta không biết được outcome hay label (nhãn) mà chỉ có dữ liệu đầu vào.
  - Dựa vào cấu trúc của dữ liệu để thực hiện một công việc nào đó
  - Ví dụ: phân nhóm (clustering) hoặc giảm số chiều của dữ liệu (dimension reduction) để thuận tiện trong việc lưu trữ và tính toán.
  - Clustering nhằm mục đích nhóm các tập con của các thực thể với nhau dựa trên một số khái niệm về sự giống nhau.
