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

## RDD

- Resilient Distributed Datasets (RDD) là một cấu trúc dữ liệu cơ bản của Spark. Nó là một tập hợp bất biến phân tán của một đối tượng. Mỗi dataset trong RDD được chia ra thành nhiều phần vùng logical. Có thể được tính toán trên các node khác nhau của một cụm máy chủ (cluster).

- RDDs có thể chứa bất kỳ kiểu dữ liệu nào của Python, Java, hoặc đối tượng Scala, bao gồm các kiểu dữ liệu do người dùng định nghĩa. Thông thường, RDD chỉ cho phép đọc, phân mục tập hợp của các bản ghi. RDDs có thể được tạo ra qua điều khiển xác định trên dữ liệu trong bộ nhớ hoặc RDDs, RDD là một tập hợp có khả năng chịu lỗi mỗi thành phần có thể được tính toán song song.

<b>- Có hai cách để tạo RDDs:</b>
- Tạo từ một tập hợp dữ liệu có sẵn trong ngôn ngữ sử dụng như Java, Python, Scala.
- Lấy từ dataset hệ thống lưu trữ bên ngoài như HDFS, Hbase hoặc các cơ sở dữ liệu quan hệ.

## Tại sao chúng ta cần RDD?

- Chia sẻ dữ liệu chậm trong MapReduce do sao chép, tuần tự hóa và IO đĩa . Hầu hết các ứng dụng Hadoop, chúng dành hơn 90% thời gian để thực hiện các thao tác đọc-ghi HDFS.
- Hỗ trợ tính toán xử lý trong bộ nhớ. Điều này có nghĩa là, nó lưu trữ trạng thái bộ nhớ như một đối tượng trên các công việc và đối tượng có thể chia sẻ giữa các công việc đó. Chia sẻ dữ liệu trong bộ nhớ nhanh hơn mạng và Đĩa từ 10 đến 100 lần.
- Tất cả công việc trong Spark được thể hiện dưới dạng tạo RDD mới, chuyển đổi RDD hiện có hoặc gọi các hành động trên RDD để tính toán kết quả. Spark tự động phân phối dữ liệu có trong RDD trên toàn bộ cụm của bạn và song song hóa các thao tác bạn thực hiện trên chúng.

<b>- Iterative Operation trên Spark RDD:</b>

<img src="https://github.com/vannam272008/Big_Data/blob/main/DataFrames%26RDD/5.PNG">

<b>- Interactive Operations trên Spark RDD:</b>

<img src="https://github.com/vannam272008/Big_Data/blob/main/DataFrames%26RDD/6.PNG">

<b>- Các loại RDD</b>

<img src="https://github.com/vannam272008/Big_Data/blob/main/DataFrames%26RDD/7.PNG">

- Các RDD biểu diễn một tập hợp cố định, đã được phân vùng các record để có thể xử lý song song.
- Các record trong RDD có thể là đối tượng Java, Scale hay Python tùy lập trình viên chọn. Không giống như DataFrame, mỗi record của DataFrame phải là một dòng có cấu trúc chứa các field đã được định nghĩa sẵn.
- RDD đã từng là API chính được sử dụng trong series Spark 1.x và vẫn có thể sử dụng trong version 2.X nhưng không còn được dùng thường xuyên nữa.
- RDD API có thể được sử dụng trong Python, Scala hay Java:
  + Scala và Java: Perfomance tương đương trên hầu hết mọi phần. (Chi phí lớn nhất là khi xử lý các raw object)
  + Python: Mất một lượng performance, chủ yếu là cho việc serialization giữa tiến trình Python và JVM
  
## Các transformation và action với RDD
- RDD cung cấp các transformation và action hoạt động giống như DataFrame lẫn DataSets. Transformation xử lý các thao tác lazily và Action xử lý thao tác cần xử lý tức thời.

<img src="https://github.com/vannam272008/Big_Data/blob/main/DataFrames%26RDD/8.PNG">

<b>- Một số transformation:</b>

=> Nhiều phiên bản transformation của RDD có thể hoạt động trên các Structured API, transformation xử lý lazily, tức là chỉ giúp dựng execution plans, dữ liệu chỉ được truy xuất thực sự khi thực hiện action.

 - <b>distinct:</b> loại bỏ trùng lắp trong RDD
 - <b>filter:</b> tương đương với việc sử dụng where trong SQL – tìm các record trong RDD xem những phần tử nào thỏa điều kiện. Có thể cung cấp một hàm phức tạp sử dụng để filter các record cần thiết – Như trong Python, ta có thể sử dụng hàm lambda để truyền vào filter
 - <b>map:</b> thực hiện một công việc nào đó trên toàn bộ RDD. Trong Python sử dụng lambda với từng phần tử để truyền vào map
 - <b>flatMap:</b> cung cấp một hàm đơn giản hơn hàm map. Yêu cầu output của map phải là một structure có thể lặp và mở rộng được.
 - <b>sortBy:</b> mô tả một hàm để trích xuất dữ liệu từ các object của RDD và thực hiện sort được từ đó.
 - <b>randomSplit:</b> nhận một mảng trọng số và tạo một random seed, tách các RDD thành một mảng các RDD có số lượng chia theo trọng số.

<b>- Một số action:</b>

=> Action thực thi ngay các transformation đã được thiết lập để thu thập dữ liệu về driver để xử lý hoặc ghi dữ liệu xuống các công cụ lưu trữ.

 - <b>reduce:</b> thực hiện hàm reduce trên RDD để thu về 1 giá trị duy nhất.
 - <b>count:</b> đếm số dòng trong RDD.
 - <b>countApprox:</b> phiên bản đếm xấp xỉ của count, nhưng phải cung cấp timeout vì có thể không nhận được kết quả.
 - <b>countByValue:</b> đếm số giá trị của RDD chỉ sử dụng nếu map kết quả nhỏ vì tất cả dữ liệu sẽ được load lên memory của driver để tính toán chỉ nên sử dụng trong tình huống số dòng nhỏ và số lượng item khác nhau cũng nhỏ.
 - <b>countApproxDistinct:</b> đếm xấp xỉ các giá trị khác nhau.
 - <b>countByValueApprox:</b> đếm xấp xỉ các giá trị.
 - <b>first:</b> lấy giá trị đầu tiên của dataset.
 - <b>max và min:</b> lần lượt lấy giá trị lớn nhất và nhỏ nhất của dataset take và các method tương tự: lấy một lượng giá trị từ trong RDD. take sẽ trước hết scan qua một partition và sử dụng kết quả để dự đoán số lượng partition cần phải lấy thêm để thỏa mãn số lượng lấy. top và takeOrdered: top sẽ hiệu quả hơn takeOrdered vì top lấy các giá trị đầu tiên được sắp xếp ngầm trong RDD.
 - <b>takeSamples:</b> lấy một lượng giá trị ngẫu nhiên trong RDD.

<b>Một số kỹ thuật đối với RDD</b>
 - <b>Lưu trữ file.</b>
 - <b>Caching:</b> Tăng tốc xử lý bằng cache.
 - <b>Checkpointing:</b> Lưu trữ lại các bước xử lý để phục hồi.
 
## Dưới đây là demo có sử dụng RDD (Bài toán tìm từ xuất hiện nhiều nhất)
- <b> Đầu tiên tạo SparkConf sau đó tạo SparkContext từ SparkConf.</b>

<img src="https://github.com/vannam272008/Big_Data/blob/main/DataFrames%26RDD/9.PNG">

- <b>Đọc file.</b>

<img src="https://github.com/vannam272008/Big_Data/blob/main/DataFrames%26RDD/10.PNG">

- <b>Sử dụng hàm map() để trả về một tập dữ liệu phân tán mới. </b>

<img src="https://github.com/vannam272008/Big_Data/blob/main/DataFrames%26RDD/11.PNG">

- <b>Sử dụng hàm reduceByKey().

<img src="https://github.com/vannam272008/Big_Data/blob/main/DataFrames%26RDD/12.PNG">

- <b>Cuối cùng, xuất ra từ xuất hiện nhiều lần nhất và số lần xuất hiện.</b>

<img src="https://github.com/vannam272008/Big_Data/blob/main/DataFrames%26RDD/13.PNG">

# Link Colab: https://colab.research.google.com/drive/1iz4iukvfX5IJtfvzfNS-ME__-TVfsXB8?usp=sharing

# Tài liệu tham khảo
1. https://www.edureka.co/blog/pyspark-dataframe-tutorial/#what
2. https://blog.vietnamlab.vn/xu-ly-du-lieu-voi-spark-dataframe/
3. https://spark.apache.org/docs/latest/rdd-programming-guide.html
4. https://www.tutorialspoint.com/apache_spark/apache_spark_rdd.htm
5. https://helpex.vn/article/rdd-trong-spark-la-gi-va-tai-sao-chung-ta-can-no-5c6afe5bae03f628d053a84c
6. https://laptrinh.vn/books/apache-spark/page/apache-spark-rdd


