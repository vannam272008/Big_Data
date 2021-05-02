# Machine Learning

## Spark MLlib
  - Apache Spark cung cấp một API Học máy được gọi là MLlib . PySpark cũng có API học máy này bằng Python. Nó hỗ trợ các loại thuật toán khác nhau, được đề cập bên dưới:

  <img src="https://github.com/vannam272008/Big_Data/blob/main/Machine%20Learning/1.PNG">
  
  => Có hai cách phổ biến để phân nhóm các thuật toán Machine learning. Một là dựa trên phương thức học (learning style), hai là dựa trên chức năng (function) (của mỗi thuật toán).
  
### *Phân nhóm dựa trên phương thức học

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
  - Dimension Reduction là sự biến đổi dữ liệu từ không gian chiều-cao thành không gian chiều-thấp để biểu diễn ở dạng chiều-thấp đồng thời giữ lại một số thuộc tính có ý nghĩa của dữ liệu gốc, có ý tưởng là gần với chiều nội tại (intrinsic dimension).

**Semi-Supervised Learning (Học bán giám sát)**
  - kết hợp các ví dụ có gắn nhãn và không gắn nhãn để sinh một hàm hoặc một bộ phân loại thích hợp. Cụ thể là: Các bài toán khi chúng ta có một lượng lớn dữ liệu X nhưng chỉ một phần trong chúng được gán nhãn.
  - Ví dụ: chỉ có một phần ảnh hoặc văn bản được gán nhãn (ví dụ bức ảnh về người, động vật hoặc các văn bản khoa học, chính trị) và phần lớn các bức ảnh/văn bản khác chưa được gán nhãn được thu thập từ internet.

**Reinforcement Learning (Học củng cố hoặc Học tăng cường)**
  - Thuật toán học một chính sách hành động tùy theo các quan sát về thế giới. Mỗi hành động đều có tác động tới môi trường, và môi trường cung cấp thông tin phản hồi để hướng dẫn cho thuật toán của quá trình học.
  - Các bài toán giúp cho một hệ thống tự động xác định hành vi dựa trên hoàn cảnh để đạt được lợi ích cao nhất (maximizing the performance).
  - Chủ yếu được áp dụng vào Lý Thuyết Trò Chơi (Game Theory), các thuật toán cần xác định nước đi tiếp theo để đạt được điểm số cao nhất.
 
### *Phân nhóm dựa trên chức năng

**Một số thuật toán phổ biến:**

**Regression Algorithms (Thuật toán hồi quy):**
  + Linear Regression: Là một phương pháp phân tích quan hệ giữa biến phụ thuộc Y với một hay nhiều biến độc lập X.
  + Logistic Regression: Trong thống kê, mô hình logistic được sử dụng để mô hình xác suất của một lớp hoặc sự kiện nào đó tồn tại như: vượt qua/thất bại, thắng/thua, sống/chết, có bệnh/không có bệnh,...
  + Stepwise Regression: Hồi quy từng bước là một phương pháp phù hợp với các mô hình hồi quy trong đó việc lựa chọn các biến dự báo được thực hiện bằng một thủ tục tự động.
 
 **Classification Algorithms (Thuật toán phân loại):**
  + Linear Classifier: Sử dụng các đặc điểm của một đối tượng để xác định nó thuộc về lớp nào.
  + Support Vector Machine (SVM): Để phân loại và phân tích hồi quy. SVM dạng chuẩn nhận dữ liệu vào và phân loại chúng vào hai lớp khác nhau. Do đó SVM là một thuật toán phân loại nhị phân.
  + Kernel SVM: Các thuật toán SVM sử dụng một tập hợp các hàm toán học được định nghĩa là hạt nhân. Chức năng của kernel là lấy dữ liệu đầu vào và biến đổi nó thành dạng yêu cầu. Các thuật toán SVM khác nhau sử dụng các loại hàm nhân (kernel function) khác nhau.
  + Sparse Representation-based classification (SRC): Là một phương pháp nhận dạng khuôn mặt mạnh mẽ.

**Instance-based Algorithms:**
  + k-Nearest Neighbor (kNN): Là một phương pháp thống kê phi tham số. Sử dụng cho phân loại bằng thống kê và phân tích hồi quy.
  + Learning Vector Quantization (LVQ):  Là một thuật toán phân loại được giám sát dựa trên nguyên mẫu. LVQ là đối tác được giám sát của các hệ thống lượng tử hóa vector.
 
**Bayesian Algorithms (Thuật toán Bayes):**
  + Naive Bayes: Áp dụng định lý Bayes với các giả định về tính độc lập mạnh mẽ (naive) giữa các đối tượng.
  + Gaussian Naive Bayes: Sử dụng chủ yếu trong loại dữ liệu mà các thành phần là các biến liên tục.
 
**Clustering Algorithms (Thuật toán phân cụm):**
  + k-Means clustering: Là 1 phương pháp lượng tử hóa vector dùng để phân các điểm dữ liệu cho trước vào các cụm khác nhau.
  + k-Medians clustering: Là một biến thể của phân cụm k-Means, tính giá trị trung bình cho mỗi cụm để xác định trọng tâm của nó, thay vì tính toán trung vị.

**Ensemble Algorithms:**
  + Boosting: Là một thuật toán meta tổng hợp để chủ yếu làm giảm sự thiên vị, và cũng là phương sai trong học tập có giám sát, và một nhóm các thuật toán học máy chuyển đổi những người học yếu thành những người mạnh.
  + AdaBoost: Adaptive Bo boost, là một thuật toán tổng hợp phân loại thống kê. Nó có thể được sử dụng kết hợp với nhiều loại thuật toán học tập khác để cải thiện hiệu suất.
  + Random Forest: Là một phương pháp học tập tổng hợp để phân loại, hồi quy và các nhiệm vụ khác hoạt động bằng cách xây dựng vô số cây quyết định tại thời điểm training và xuất ra lớp là chế độ (mode) của các lớp (phân loại) hoặc dự đoán mean/average prediction (hồi quy) của các cây riêng lẻ. Phù hợp với thói quen thích nghi quá mức  của cây quyết định (overfitting) đối với tập huấn luyện của chúng (training set).

## Ví dụ về Machine Learning (Áp dụng thuật toán Logistic Regression cho Bank Marketing dataset để giải quyết bài toán khách hàng đã đăng ký gửi tiền có kỳ hạn hay chưa) thực hiện trên Google Colab

  **Config Spark context và đọc data từ Drive**
  
  <img src="https://github.com/vannam272008/Big_Data/blob/main/Machine%20Learning/Config%20Spark%20context%20v%C3%A0%20%C4%91%E1%BB%8Dc%20data%20t%E1%BB%AB%20Drive.PNG">
  
  **Chuyển đổi dạng dữ liệu chuỗi sang số để dễ tính toán và xử lý**
  
  <img src="https://github.com/vannam272008/Big_Data/blob/main/Machine%20Learning/Convert%20String%20col%20to%20Numeric.PNG">
  
  **Xóa đi những cột mà không chuyển được sang dạng số**
  
  <img src="https://github.com/vannam272008/Big_Data/blob/main/Machine%20Learning/Drop%20String%20col.PNG">
  
  **Lấy feature_names và dùng VectorAssembler để transform data thành một vector duy nhất rồi gán vào cột features**
  
  <img src="https://github.com/vannam272008/Big_Data/blob/main/Machine%20Learning/Use%20VectorAssembler%20to%20transform%20data%20into%20single%20vector.PNG">
  
  **Tách train test sau đó sử dụng thư viện LogisticRegression để mô hình hóa xác suất của cột features vừa tạo ở trên**
  
  <img src="https://github.com/vannam272008/Big_Data/blob/main/Machine%20Learning/Split%20the%20training%20test%20and%20use%20library%20LogisticRegression.PNG">
  
  **Sau đó dùng fit và transform để fit và dự đoán data**
  
  <img src="https://github.com/vannam272008/Big_Data/blob/main/Machine%20Learning/Fit%20model%20and%20Transform%20data.PNG">
  
  **Tính Aaccuracy (độ chính xác) bằng thư viện MulticlassClassificationEvaluator**
  
  <img src="https://github.com/vannam272008/Big_Data/blob/main/Machine%20Learning/Calculate%20Accuracy.PNG">
  
  **Link Google Colab**
  
  https://colab.research.google.com/drive/1YmEBiUx73VI93FU3QzfxALLdANGaCEhd?usp=sharing
   
## Tài liệu tham khảo
  1. https://ichi.pro/vi/spark-for-machine-learning-su-dung-python-va-mllib-74075263465224
  2. https://vi.wikipedia.org/wiki/H%E1%BB%8Dc_m%C3%A1y
  3. https://machinelearningcoban.com/2016/12/27/categories/
