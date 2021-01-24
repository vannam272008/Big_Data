# Tổng quan về Spark
## Khái niệm Spark
 - Apache Spark là một open source cluster computing framework được phát triển sơ khởi vào năm 2009 bởi AMPLab tại đại học California. Spark được ứng dụng công nghệ vào phân tích và xử lý dữ liệu nhanh chóng.
 - Spark cho phép xây dựng và phân tích nhanh các mô hình dự đoán, ngoài ra còn cung cấp khả năng truy xuất toàn bộ dữ liệu cùng một lúc, do đó ta không cần phải lấy mẫu dữ liệu giống như ngôn ngữ lập trình R. Spark còn cung cấp tính năng streaming, được dùng để xây dựng các mô hình real-time bằng cách nạp toàn bộ dữ liệu vào bộ nhớ.
 - Tốc độ xử lý của Spark có được do việc tính toán được thực hiện cùng lúc trên nhiều máy khác nhau. Đồng thời việc tính toán được thực hiện ở bộ nhớ trong (in-memories) hay thực hiện hoàn toàn trên RAM.
## Thành phần của Apache Spark
 - Matei Zaharia, cha đẻ của Spark, sử dụng Hadoop từ những ngày đầu. Đến năm 2009 ông viết Apache Spark để giải quyết những bài toán học máy ở đại học UC Berkely vì Hadoop MapReduce hoạt động không hiệu quả cho những bài toán này. Rất sớm sau đó ông nhận ra rằng Spark không chỉ hữu ích cho học máy mà còn cho cả việc xử lý luồng dữ liệu hoàn chỉnh.
 - Apache Spark gồm có 5 thành phần chính : Spark Core, Spark Streaming, Spark SQL, MLlib và GraphX, trong đó:
  + **Spark Core:** là nền tảng cho các thành phần còn lại và các thành phần này muốn khởi chạy được thì đều phải thông qua Spark Core do Spark Core đảm nhận vai trò thực hiện công việc tính toán và xử lý trong bộ nhớ (In-memory computing) đồng thời nó cũng tham chiếu các dữ liệu được lưu trữ tại các hệ thống lưu trữ bên ngoài.
  + **Spark SQL:** cho phép truy vấn dữ liệu cấu trúc qua các câu lệnh SQL. Spark SQL có thể thao tác với nhiều nguồn dữ liệu như Hive tables, Parquet, và JSON.
  + **Spark Streaming:** được sử dụng để thực hiện việc phân tích stream bằng việc coi stream là các mini-batches và thực hiệc kỹ thuật RDD transformation đối với các dữ liệu mini-batches này, ngoài ra còn cung cấp API để dễ dàng xử lý dữ liệu stream.
  + **MLlib (Machine Learning Library):** là một nền tảng học máy phân tán bên trên Spark do kiến trúc phân tán dựa trên bộ nhớ. Cung cấp rất nhiều thuật toán của học máy như: classification, regression, clustering, collaborative filtering…
  + **Graphx:** là nền tảng, thư viện để xử lý đồ thị dựa trên Spark. Nó cung cấp các Api để diễn tảcác tính toán trong đồ thị bằng cách sử dụng Pregel Api.
 ## Ưu điểm & Nhược điểm của Spark
 ### Ưu điểm:
 - Xử lý dữ liệu: Spark xử lý dữ liệu theo lô và thời gian thực.
 - Spark giúp mọi người tiếp cận với công nghệ tính toán song song dễ dàng hơn rất nhiều. Người dùng chỉ cần một vài kiến thức cơ bản về database cộng với lập trình Python hay Scala là có thể sử dụng được.
 - Độc lập với các nhà cung cấp dịch vụ Hadoop: Hầu hết các nhà cung cấp dịch vụ Hadoop đều hỗ trợ Spark.
 - Tính tương thích: Dễ dàng tích hợp với các công cụ báo cáo như: Business Intelligence, Analytics, Data Integration Tools và định dạng tệp được hỗ trợ bởi cụm Hadoop.
 - Hỗ trợ ngôn ngữ: hỗ trợ Java, Scala, Python và R. Hỗ trợ viết spark job bằng cú pháp SQL.
 - Phân tích thời gian thực: 
  + Apache Spark xử lý dữ liệu đến từ các luồng sự kiện thời gian thực với tốc độ hàng triệu sự kiện mỗi giây.
  + Apache Spark còn được sử dụng để xử lý phát hiện gian lận trong khi thực hiện các giao dịch ngân hàng.
### Nhược điểm:
 - Spark không có hệ thống file của riêng mình, nó sử dụng hệ thống file khác như: HDFS, Cassandra, S3,….
 - Spark Streaming tạo ra độ trễ trong xử lý dữ liệu (độ trễ chính bằng mini-batch duration) và do đó nhiều chuyên gia cho rằng Spark Streaming không thực sự là công cụ xử lý streaming giống như Storm hoặc Flink. Spark Streaming không thực sự real-time.
 - Apache Spark đòi hỏi rất nhiều RAM để chạy trong bộ nhớ, do đó chi phí của Spark khá cao.
## Mục tiêu sử dụng Spark
 - Xử lý dữ liệu nhanh và tương tác
 - Xử lý đồ thị
 - Công việc lặp đi lặp lại
 - Xử lý thời gian thực
 - joining Dataset
 - Machine Learning
 - Apache Spark là Framework thực thi dữ liệu dựa trên Hadoop HDFS. Apache Spark không thay thế cho Hadoop nhưng nó là một framework ứng dụng. Apache Spark tuy ra đời sau nhưng được nhiều người biết đến hơn Apache Hadoop vì khả năng xử lý hàng loạt và thời gian thực.
## Những công ty đang sử dụng Apache Spark hiện nay
<img src="https://viblo.asia/uploads/fdac5aee-56e7-4a29-83f8-edc8dff6b9c8.jpg">
- Netflix
- Ebay
- Yahoo
- Twitter
- Ooyala


## Tổng kết
- Đối với các nhà cung cấp giải pháp CNTT, Apache Spark là một lá bài quan trọng trong việc sử dụng các công nghệ cốt lõi để xây dựng những data warehouses hiện đại. Đây là một phân khúc lớn trong ngành IT có khả năng thu về hàng tỉ đô doanh thu hằng năm. Spark đưa ra một khái niệm mới mang nhiều hứa hẹn trong tương lai đó là data lakes. Đây là một nơi lưu trữ một lượng dữ liệu khổng lồ với nhiều định dạng khác nhau và được truy vấn để xử lý khi cần thiết. Data lakes đưa ra một framework thương mại có thể tạo ra một môi trường lưu trữ vô hạn bất kỳ loại dữ liệu nào.
- Với sự phát triển mạnh mẽ trong vài năm trở lại đây của Apache Spark thì lập trình viên, các nhà khoa học máy tính có thêm công cụ hữu hiệu để phục vụ công việc của mình và người ta sẽ dần quên “Hadoop Stack” mà thay thế vào đó sẽ là “Big data Stack”, với nhiều sự lựa chọn hơn không chỉ là Hadoop.
# Tổng quan về Mapreduce
## Khái niệm và thành phần của Mapreduce
 - MapReduce là mô hình được thiết kế độc quyền bởi Google, nó có khả năng lập trình xử lý các tập dữ liệu lớn song song và phân tán thuật toán trên 1 cụm máy tính.
 - MapReduce trở thành một trong những thành ngữ tổng quát hóa trong thời gian gần đây.
 - Mapreduce gồm 2 pha : map và reduce.
  + Hàm Map() : Các xử lý một cặp (key, value) để sinh ra một cặp (keyI, valueI) - key và value trung gian. Dữ liệu này input vào hàm Reduce.
  + Ở giữa Map() và Reduce() thì còn 1 bước trung gian đó chính là Shuffle. Sau khi Map hoàn thành  xong công việc của mình thì Shuffle sẽ làm nhiệm vụ chính là thu thập cũng như tổng hợp từ khóa/giá trị trung gian đã được map sinh ra trước đó rồi chuyển qua cho Reduce tiếp tục xử lý.
  + Hàm Reduce() : tiếp nhận từ khóa trung gian và những giá trị tương ứng với lượng từ khóa đó. Sau đó, tiến hành ghép chúng lại để có thể tạo thành một tập khóa khác nhau. Các cặp khóa/giá trị này thường sẽ thông qua một con trỏ vị trí để đưa vào các hàm reduce. Quá trình này sẽ giúp cho lập trình viên quản lý dễ dàng hơn một lượng danh sách cũng như  phân bổ giá trị sao cho  phù hợp nhất với bộ nhớ hệ thống.
 - Đây là mô hình dựa vào các khái niệm biển đối của bản đồ và reduce những chức năng lập trình theo hướng chức năng. Thư viện của thủ tục Map() và Reduce() sẽ được viết bằng nhiều loại ngôn ngữ khác nhau. Thủ tục được cài đặt miễn phí và được sử dụng phổ biến nhất là là Apache Hadoop.
## Hoạt động
 B1: Đọc dữ liệu đầu vào
 B2: Xử lý dữ liệu đầu vào (thực hiện hàm map)
 B3: Sắp xếp và trộn các kết quả thu được từ các máy tính phân tán thích hợp nhất.
 B4: Tổng hợp các kết quả trung gian thu được ( thực hiện hàm reduce)
 B5: Đưa ra kết quả cuối cùng.
<img src="https://s3-ap-southeast-1.amazonaws.com/kipalog.com/m%C3%B4%20h%C3%ACnh%20ho%E1%BA%A1t%20%C4%91%E1%BB%99ng.png_5a3zte8t56">
## Luồng dữ liệu nền tảng của Mapreduce
 - Input Reader
 - Map Function
 - Partition Function
 - Compare Function
 - Reduce Function
 - Output Writer
## Ưu điểm của Mapreduce
- MapReduce có khả năng xử lý dễ dàng mọi bài toán có lượng dữ liệu lớn nhờ khả năng tác vụ phân tích và tính toán phức tạp. Xuất kết quả trong khoảng thời gian ngắn.
- Mapreduce có khả năng chạy song song trên các máy có sự phân tán  khác nhau giúp mang lại nhiều hiệu quả cho toàn hệ thống.
- MapRedue có khả năng thực hiện trên nhiều nguồn ngôn ngữ lập trình khác nhau như: Java, C/ C++, Python, Perl, Ruby,… tương ứng với nó là những thư viện hỗ trợ. 
- các ứng dụng MapReduce dần hướng đến quan tâm nhiều hơn cho việc phát hiện các mã độc để có thể xử lý chúng. Nhờ vậy, hệ thống mới có thể vận hành trơn tru và được bảo mật nhất.
# Tài liệu tham khảo
1. https://viblo.asia/p/tim-hieu-ve-apache-spark-ByEZkQQW5Q0
2. https://www.mastercode.vn/blog/web-development/apache-spark-la-gi.85
3. https://viblo.asia/p/tong-quan-ve-apache-spark-cho-he-thong-big-data-RQqKLxR6K7z
4. https://kipalog.com/posts/Tong-quan-mo-hinh-lap-trinh-MapReduce
5. https://topdev.vn/blog/hadoop-la-gi/
