# DataFrames
 ## Khái niệm
 - DataFrames là một từ thông dụng trong ngành công nghiệp ngày nay. Mọi người có xu hướng sử dụng nó với các ngôn ngữ phổ biến được sử dụng cho Phân tích dữ liệu như Python, Scala và R.
 - DataFrames thường đề cập đến một cấu trúc dữ liệu, về bản chất là dạng bảng. Nó đại diện cho các hàng, mỗi hàng bao gồm một số quan sát. Các hàng có thể có nhiều định dạng dữ liệu (không đồng nhất), trong khi một cột có thể có dữ liệu cùng loại (đồng nhất). DataFrames thường chứa một số siêu dữ liệu ngoài dữ liệu; ví dụ, tên cột và hàng.
 <img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-36-545-52ab82fe-9dc6-43bb-8eca-58874c82c0d1.jpg">

## Lý do cần DataFrames
  <b>1. Xử lý dữ liệu có cấu trúc và bán cấu trúc (Processing Structured and Semi-Structured Data)</b>
  
  DataFrames được thiết kế để xử lý một tập hợp lớn dữ liệu có cấu trúc cũng như bán cấu trúc . Các quan sát trong Spark DataFrame được tổ chức dưới các cột được đặt tên, giúp Apache Spark hiểu sơ đồ của Dataframe. Điều này giúp Spark tối ưu hóa kế hoạch thực hiện trên các truy vấn này. Nó cũng có thể xử lý petabyte dữ liệu.
  
  <b>2. Cắt lát và thái hạt lựu (Slicing and Dicing)</b>
  
  API DataFrames thường hỗ trợ các phương thức phức tạp để cắt và xử lý dữ liệu. Nó bao gồm các hoạt động như "chọn" các hàng, cột và ô theo tên hoặc theo số, lọc ra các hàng, v.v. Dữ liệu thống kê thường rất lộn xộn và chứa nhiều giá trị thiếu và không chính xác và vi phạm phạm vi. Vì vậy, một tính năng cực kỳ quan trọng của DataFrames là quản lý rõ ràng dữ liệu bị thiếu.
 
 <b>3. Nguồn dữ liệu (Data Sources)</b>
 
 DataFrames đã hỗ trợ cho một loạt các định dạng và nguồn dữ liệu, chúng ta sẽ xem xét vấn đề này sau trong hướng dẫn Pyspark DataFrames này. Họ có thể lấy dữ liệu từ nhiều nguồn khác nhau.
 
 <b>4. Hỗ trợ nhiều ngôn ngữ (Support for Multiple Languages) </b>
 
 Nó có hỗ trợ API cho các ngôn ngữ khác nhau như Python, R, Scala, Java, giúp mọi người có nền tảng lập trình khác nhau dễ sử dụng hơn.
 
 ## Các tính năng của DataFrames
 - DataFrames được phân phối trong tự nhiên, làm cho nó có cấu trúc dữ liệu có khả năng chịu lỗi và có tính sẵn sàng cao
 - Đánh giá lười biếng là một chiến lược đánh giá giữ đánh giá biểu thức cho đến khi cần giá trị của nó. Nó tránh đánh giá lặp đi lặp lại. Đánh giá lười biếng trong Spark có nghĩa là việc thực thi sẽ không bắt đầu cho đến khi một hành động được kích hoạt. Trong Spark, hình ảnh đánh giá lười biếng xuất hiện khi biến đổi Spark xảy ra.
 - DataFrames là bất biến trong tự nhiên. Bằng cách bất biến, ý tôi là nó là một đối tượng có trạng thái không thể sửa đổi sau khi nó được tạo. Nhưng chúng ta có thể biến đổi các giá trị của nó bằng cách áp dụng một phép biến đổi nhất định, như trong RDD.
 
 ## Nguồn dữ liệu của PySpark
 <b> DataFrames trong Pyspark có thể được tạo theo nhiều cách: </b>
 - Dữ liệu có thể được tải thông qua tệp CSV, JSON, XML  hoặc tệp Parquet. Nó cũng có thể được tạo bằng RDD hiện có và thông qua bất kỳ cơ sở dữ liệu nào khác, như Hive hoặc Cassandra . Nó cũng có thể lấy dữ liệu từ HDFS hoặc hệ thống tệp cục bộ.
 - Hãy tiếp tục với hướng dẫn PySpark DataFrame này và hiểu cách tạo DataFrames.
 
 ## Đọc dữ liệu từ tệp CSV
 
<img src="https://github.com/vannam272008/Big_Data/blob/main/DataFrames%26RDD/1.PNG">
 
 ## Lược đồ của DataFrame
 
 Để xem sơ đồ, tức là cấu trúc của DataFrame, chúng ta sẽ sử dụng phương thức printSchema . Điều này sẽ cung cấp cho chúng tôi các cột khác nhau trong DataFrame của chúng tôi, cùng với loại dữ liệu và các điều kiện không thể thực hiện được cho cột cụ thể đó.
 
<img src="https://github.com/vannam272008/Big_Data/blob/main/DataFrames%26RDD/2.PNG">

## Tên cột và Count (Hàng và Cột)
Khi muốn xem tên và số lượng hàng và cột của một DataFrame cụ thể, ta sử dụng phương pháp sau:

<img src="https://github.com/vannam272008/Big_Data/blob/main/DataFrames%26RDD/3.PNG">

## Select nhiều cột

<img src="https://github.com/vannam272008/Big_Data/blob/main/DataFrames%26RDD/4.PNG">

Còn có một số khác như: Lọc dữ liệu (filter), Sắp xếp dữ liệu (OrderBy),...

# Apache Spark RDD

Resilient Distributed Datasets (RDD) là một cấu trúc dữ liệu cơ bản của Spark. Nó là một tập hợp bất biến phân tán của một đối tượng. Mỗi dataset trong RDD được chia ra thành nhiều phần vùng logical. Có thể được tính toán trên các node khác nhau của một cụm máy chủ (cluster).

RDDs có thể chứa bất kỳ kiểu dữ liệu nào của Python, Java, hoặc đối tượng Scala, bao gồm các kiểu dữ liệu do người dùng định nghĩa. Thông thường, RDD chỉ cho phép đọc, phân mục tập hợp của các bản ghi. RDDs có thể được tạo ra qua điều khiển xác định trên dữ liệu trong bộ nhớ hoặc RDDs, RDD là một tập hợp có khả năng chịu lỗi mỗi thành phần có thể được tính toán song song.

<b>Có hai cách để tạo RDDs:</b>
- Tạo từ một tập hợp dữ liệu có sẵn trong ngôn ngữ sử dụng như Java, Python, Scala.
- Lấy từ dataset hệ thống lưu trữ bên ngoài như HDFS, Hbase hoặc các cơ sở dữ liệu quan hệ.


# Tài liệu tham khảo
1. https://www.edureka.co/blog/pyspark-dataframe-tutorial/#what
2. https://blog.vietnamlab.vn/xu-ly-du-lieu-voi-spark-dataframe/


