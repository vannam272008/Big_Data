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
 
 
 
 <div class="postcell post-layout--right">

                        <div class="s-prose js-post-body content-article" itemprop="text">
                            
                    <p pid="2">DataFrames là một từ thông dụng trong ngành công nghiệp ngày nay. Mọi người có xu hướng sử dụng nó với các ngôn ngữ phổ biến được sử dụng cho Phân tích dữ liệu như Python, Scala và R. Vậy, tại sao mọi người lại sử dụng nó nhiều như vậy? Chúng ta hãy xem điều này với hướng dẫn PySpark Dataframe của chúng tôi. Trong bài đăng này, tôi sẽ đề cập đến các chủ đề sau:</p> 
<ul> 
 <li><a href="https://www.edureka.co/blog/pyspark-dataframe-tutorial/#what" target="_blank" rel="nofollow">DataFrames là gì?</a></li> 
 <li><a href="https://www.edureka.co/blog/pyspark-dataframe-tutorial/#why" target="_blank" rel="nofollow">Tại sao chúng ta cần DataFrames?</a></li> 
 <li><a href="https://www.edureka.co/blog/pyspark-dataframe-tutorial/#features" target="_blank" rel="nofollow">Các tính năng của DataFrames</a></li> 
 <li><a href="https://www.edureka.co/blog/pyspark-dataframe-tutorial/#sources" target="_blank" rel="nofollow">Nguồn dữ liệu của PySpark</a></li> 
 <li><a href="https://www.edureka.co/blog/pyspark-dataframe-tutorial/#creation" target="_blank" rel="nofollow">Tạo khung dữ liệu</a></li> 
 <li><a href="https://www.edureka.co/blog/pyspark-dataframe-tutorial/#fifa" target="_blank" rel="nofollow">Pyspark DataFrames với FIFA World Cup và Superheroes Dataset</a></li> 
</ul> 
<h2><strong>Hướng dẫn về khung dữ liệu của PySpark: DataFrames là gì? </strong></h2> 
<p pid="3">DataFrames thường đề cập đến một cấu trúc dữ liệu, về bản chất là dạng bảng. Nó đại diện cho các hàng, mỗi hàng bao gồm một số quan sát. Các hàng có thể có nhiều định dạng dữ liệu (không đồng nhất), trong khi một cột có thể có dữ liệu cùng loại (đồng nhất). DataFrames thường chứa một số siêu dữ liệu ngoài dữ liệu; ví dụ, tên cột và hàng.</p> 
<p pid="33"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-36-545-52ab82fe-9dc6-43bb-8eca-58874c82c0d1.jpg"></p> 
<p pid="4">Chúng ta có thể nói rằng DataFrames không là gì, ngoài các cấu trúc dữ liệu 2 chiều, tương tự như bảng SQL hoặc bảng tính. Bây giờ, hãy tiếp tục với Hướng dẫn về khung dữ liệu PySpark này và hiểu lý do tại sao chính xác chúng ta cần Pyspark Dataframe.</p> 
<h2><strong>Tại sao chúng ta cần DataFrames?</strong></h2> 
<h3 pid="5"><strong>1. Xử lý dữ liệu có cấu trúc và bán cấu trúc</strong></h3> 
<p pid="34"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-36-619-eca1fcd0-7ac4-486f-8b24-4a7bbbc49ed5.jpg"></p> 
<p pid="6">DataFrames được thiết kế để xử lý một <strong>tập hợp lớn dữ liệu có cấu trúc cũng như bán cấu trúc</strong> . Các quan sát trong Spark DataFrame được tổ chức dưới các cột được đặt tên, giúp Apache Spark hiểu sơ đồ của Dataframe. Điều này giúp Spark tối ưu hóa kế hoạch thực hiện trên các truy vấn này. Nó cũng có thể xử lý petabyte dữ liệu.</p> 
<h3 pid="57">2. Cắt lát và thái hạt lựu</h3> 
<p pid="35"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-36-694-5c0633d6-bb5d-4ce7-8fe5-11f469851349.jpg"></p> 
<p pid="7">API DataFrames thường hỗ trợ các phương thức phức tạp để cắt và xử lý dữ liệu. Nó bao gồm các hoạt động như "chọn" các hàng, cột và ô theo tên hoặc theo số, lọc ra các hàng, v.v. Dữ liệu thống kê thường rất lộn xộn và chứa nhiều giá trị thiếu và không chính xác và vi phạm phạm vi. Vì vậy, một tính năng cực kỳ quan trọng của DataFrames là quản lý rõ ràng dữ liệu bị thiếu.</p> 
<h3 pid="59">3. Nguồn dữ liệu</h3> 
<p pid="36"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-36-790-41d88011-c136-4dd5-8ae6-7cb347b2c8c1.jpg"></p> 
<p pid="8">DataFrames đã hỗ trợ cho một loạt các định dạng và nguồn dữ liệu, chúng ta sẽ xem xét vấn đề này sau trong hướng dẫn Pyspark DataFrames này. Họ có thể lấy dữ liệu từ nhiều nguồn khác nhau.</p> 
<h3 pid="9"><strong>4. Hỗ trợ nhiều ngôn ngữ</strong></h3> 
<p pid="37"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-36-849-8cb82bb0-403c-4b76-8441-79e54d5776d7.jpg"></p> 
<p pid="10">Nó có hỗ trợ API cho các ngôn ngữ khác nhau như Python, R, Scala, Java, giúp mọi người có nền tảng lập trình khác nhau dễ sử dụng hơn.</p> 
<h2><strong>Các tính năng của DataFrames</strong></h2> 
<p pid="38"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-36-927-3156016a-bdfd-49ab-b9b1-a6878a618ac1.jpg"></p> 
<ul> 
 <li>DataFrames được <strong>phân phối</strong> trong tự nhiên, làm cho nó có cấu trúc dữ liệu có khả năng chịu lỗi và có tính sẵn sàng cao.</li> 
 <li><strong>Đánh giá lười biếng</strong> là một chiến lược đánh giá giữ đánh giá biểu thức cho đến khi cần giá trị của nó. Nó tránh đánh giá lặp đi lặp lại. Đánh giá lười biếng trong Spark có nghĩa là việc thực thi sẽ không bắt đầu cho đến khi một hành động được kích hoạt. Trong Spark, hình ảnh đánh giá lười biếng xuất hiện khi biến đổi Spark xảy ra.</li> 
 <li>DataFrames là <strong>bất biến</strong> trong tự nhiên. Bằng cách bất biến, ý tôi là nó là một đối tượng có trạng thái <strong>không thể sửa đổi</strong> sau khi nó được tạo. Nhưng chúng ta có thể biến đổi các giá trị của nó bằng cách áp dụng một phép biến đổi nhất định, như trong RDD.</li> 
</ul> 
<h2><strong>Nguồn dữ liệu của PySpark </strong></h2> 
<p pid="11">DataFrames trong Pyspark có thể được tạo theo nhiều cách:</p> 
<p pid="39"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-41-044-02184c6b-1c87-469b-a3aa-e3c0161381ca.jpg"></p> 
<p pid="12">Dữ liệu có thể được tải thông qua <strong>tệp CSV, JSON, XML</strong> &nbsp;hoặc tệp Parquet. Nó cũng có thể được tạo bằng <strong>RDD</strong> hiện có và thông qua bất kỳ cơ sở dữ liệu nào khác, như <strong>Hive</strong> hoặc <strong>Cassandra</strong> . Nó cũng có thể lấy dữ liệu từ HDFS hoặc hệ thống tệp cục bộ.</p> 
<p pid="13">Hãy tiếp tục với hướng dẫn PySpark DataFrame này và hiểu cách tạo DataFrames.</p> 
<p pid="14">Chúng tôi sẽ tạo&nbsp; <code>Employee</code><span id="_tmp_pre_2">&nbsp;</span>và các&nbsp; <code>Department</code>&nbsp;trường hợp.</p> 
<pre class="ql-syntax s-code-block"><code lang="text/x-scala" class="hljs python"><table class="hljs-ln"><tbody><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="1"><div class="hljs-ln-n" data-line-number="1"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="1"><span class="hljs-keyword">from</span> pyspark.sql <span class="hljs-keyword">import</span> *</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="2"><div class="hljs-ln-n" data-line-number="2"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="2"> </td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="3"><div class="hljs-ln-n" data-line-number="3"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="3">Employee = Row(<span class="hljs-string">"firstName"</span>, <span class="hljs-string">"lastName"</span>, <span class="hljs-string">"email"</span>, <span class="hljs-string">"salary"</span>)</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="4"><div class="hljs-ln-n" data-line-number="4"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="4"> </td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="5"><div class="hljs-ln-n" data-line-number="5"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="5">employee1 = Employee(<span class="hljs-string">'Basher'</span>, <span class="hljs-string">'armbrust'</span>, <span class="hljs-string">'bash@edureka.co'</span>, <span class="hljs-number">100000</span>)</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="6"><div class="hljs-ln-n" data-line-number="6"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="6">employee2 = Employee(<span class="hljs-string">'Daniel'</span>, <span class="hljs-string">'meng'</span>, <span class="hljs-string">'daniel@stanford.edu'</span>, <span class="hljs-number">120000</span> )</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="7"><div class="hljs-ln-n" data-line-number="7"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="7">employee3 = Employee(<span class="hljs-string">'Muriel'</span>, <span class="hljs-literal">None</span>, <span class="hljs-string">'muriel@waterloo.edu'</span>, <span class="hljs-number">140000</span> )</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="8"><div class="hljs-ln-n" data-line-number="8"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="8">employee4 = Employee(<span class="hljs-string">'Rachel'</span>, <span class="hljs-string">'wendell'</span>, <span class="hljs-string">'rach_3@edureka.co'</span>, <span class="hljs-number">160000</span> )</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="9"><div class="hljs-ln-n" data-line-number="9"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="9">employee5 = Employee(<span class="hljs-string">'Zach'</span>, <span class="hljs-string">'galifianakis'</span>, <span class="hljs-string">'zach_g@edureka.co'</span>, <span class="hljs-number">160000</span> )</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="10"><div class="hljs-ln-n" data-line-number="10"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="10"> </td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="11"><div class="hljs-ln-n" data-line-number="11"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="11">print(Employee[<span class="hljs-number">0</span>])</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="12"><div class="hljs-ln-n" data-line-number="12"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="12"> </td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="13"><div class="hljs-ln-n" data-line-number="13"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="13">print(employee3)</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="14"><div class="hljs-ln-n" data-line-number="14"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="14"> </td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="15"><div class="hljs-ln-n" data-line-number="15"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="15">department1 = Row(id=<span class="hljs-string">'123456'</span>, name=<span class="hljs-string">'HR'</span>)</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="16"><div class="hljs-ln-n" data-line-number="16"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="16">department2 = Row(id=<span class="hljs-string">'789012'</span>, name=<span class="hljs-string">'OPS'</span>)</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="17"><div class="hljs-ln-n" data-line-number="17"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="17">department3 = Row(id=<span class="hljs-string">'345678'</span>, name=<span class="hljs-string">'FN'</span>)</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="18"><div class="hljs-ln-n" data-line-number="18"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="18">department4 = Row(id=<span class="hljs-string">'901234'</span>, name=<span class="hljs-string">'DEV'</span>)</td></tr></tbody></table></code></pre> 
<p pid="15">Tiếp theo, chúng tôi sẽ tạo một&nbsp; <code>DepartmentWithEmployees</code><span id="_tmp_pre_1">&nbsp;</span>ví dụ từ&nbsp; <code>Employee</code><span id="_tmp_pre_4">&nbsp;một</span> nd&nbsp; <code>Departments</code><span id="_tmp_pre_5">.</span></p> 
<pre class="ql-syntax s-code-block"><code lang="text/x-scala" class="hljs ini"><table class="hljs-ln"><tbody><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="1"><div class="hljs-ln-n" data-line-number="1"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="1"><span class="hljs-attr">departmentWithEmployees1</span> = Row(department=department1, employees=[employee1, employee2, employee5])</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="2"><div class="hljs-ln-n" data-line-number="2"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="2"><span class="hljs-attr">departmentWithEmployees2</span> = Row(department=department2, employees=[employee3, employee4])</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="3"><div class="hljs-ln-n" data-line-number="3"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="3"><span class="hljs-attr">departmentWithEmployees3</span> = Row(department=department3, employees=[employee1, employee4, employee3])</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="4"><div class="hljs-ln-n" data-line-number="4"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="4"><span class="hljs-attr">departmentWithEmployees4</span> = Row(department=department4, employees=[employee2, employee3])</td></tr></tbody></table></code></pre> 
<p pid="16">Hãy tạo DataFrame của chúng tôi từ danh sách các hàng:</p> 
<pre class="ql-syntax s-code-block"><code lang="text/x-sql" class="hljs makefile"><table class="hljs-ln"><tbody><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="1"><div class="hljs-ln-n" data-line-number="1"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="1">departmentsWithEmployees_Seq = [departmentWithEmployees1, departmentWithEmployees2]</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="2"><div class="hljs-ln-n" data-line-number="2"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="2">dframe = spark.createDataFrame(departmentsWithEmployees_Seq)</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="3"><div class="hljs-ln-n" data-line-number="3"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="3">display(dframe)</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="4"><div class="hljs-ln-n" data-line-number="4"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="4">dframe.show()</td></tr></tbody></table></code></pre> 
<h2><strong>Pyspark DataFrames Ví dụ 1: Bộ dữ liệu FIFA World Cup </strong></h2> 
<p pid="17">Ở đây chúng tôi đã lấy Bộ dữ liệu cầu thủ FIFA World Cup. Chúng tôi sẽ tải dữ liệu này ở định dạng CSV vào DataFrame và sau đó chúng tôi sẽ tìm hiểu về các biến đổi và hành động khác nhau có thể được thực hiện trên DataFrame này.</p> 
<p pid="40"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-41-106-b90f6959-8cd2-400e-ae74-c3c2fee1be3a.jpg"></p> 
<h3><strong>Đọc dữ liệu từ tệp CSV </strong></h3> 
<p pid="18">Hãy tải dữ liệu từ tệp CSV. Ở đây chúng ta sẽ sử dụng phương thức <strong>spark.read.csv</strong> để tải dữ liệu vào DataFrame , <code>fifa_df</code>. Phương thức thực tế là <strong>spark.read.format [csv / json]</strong> .</p> 
<pre class="ql-syntax s-code-block"><code lang="text/x-sql" class="hljs python"><table class="hljs-ln"><tbody><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="1"><div class="hljs-ln-n" data-line-number="1"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="1">fifa_df = spark.read.csv(<span class="hljs-string">"path-of-file/fifa_players.csv"</span>, inferSchema = <span class="hljs-literal">True</span>, header = <span class="hljs-literal">True</span>)</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="2"><div class="hljs-ln-n" data-line-number="2"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="2"> </td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="3"><div class="hljs-ln-n" data-line-number="3"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="3">fifa_df.show()</td></tr></tbody></table></code></pre> 
<p pid="41"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-41-186-7fdaae63-f328-4549-b737-e237c330f4f1.jpg"></p> 
<h3><strong>Lược đồ của DataFrame </strong></h3> 
<p pid="19">Để xem sơ đồ, tức là cấu trúc của DataFrame, chúng ta sẽ sử dụng phương thức <strong>printSchema</strong> . Điều này sẽ cung cấp cho chúng tôi các cột khác nhau trong DataFrame của chúng tôi, cùng với loại dữ liệu và các điều kiện không thể thực hiện được cho cột cụ thể đó.</p> 
<pre class="ql-syntax s-code-block"><code lang="text/x-sql" class="hljs css"><span class="hljs-selector-tag">fifa_df</span><span class="hljs-selector-class">.printSchema</span>()</code></pre> 
<p pid="42"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-41-251-58e4b9b9-1703-4733-b776-f5f795754f49.jpg"></p> 
<h3><strong>Tên cột và Đếm (Hàng và Cột) </strong></h3> 
<p pid="20">Khi chúng tôi muốn xem tên và số lượng hàng và cột của một DataFrame cụ thể, chúng tôi sử dụng các phương pháp sau.</p> 
<pre class="ql-syntax s-code-block"><code lang="text/x-scala" class="hljs swift"><table class="hljs-ln"><tbody><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="1"><div class="hljs-ln-n" data-line-number="1"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="1">fifa_df.columns <span class="hljs-comment">//Column Names</span></td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="2"><div class="hljs-ln-n" data-line-number="2"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="2"> </td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="3"><div class="hljs-ln-n" data-line-number="3"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="3">fifa_df.<span class="hljs-built_in">count</span>() <span class="hljs-comment">// Row Count</span></td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="4"><div class="hljs-ln-n" data-line-number="4"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="4"> </td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="5"><div class="hljs-ln-n" data-line-number="5"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="5">len(fifa_df.columns) <span class="hljs-comment">//Column Count</span></td></tr></tbody></table></code></pre> 
<p pid="43"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-41-305-b00a1d2e-5fe2-4108-8431-f198a6b483a1.jpg"></p> 
<pre class="ql-syntax s-code-block"><code lang="text/plain" class="hljs"><table class="hljs-ln"><tbody><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="1"><div class="hljs-ln-n" data-line-number="1"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="1">37784</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="2"><div class="hljs-ln-n" data-line-number="2"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="2"> </td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="3"><div class="hljs-ln-n" data-line-number="3"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="3">8</td></tr></tbody></table></code></pre> 
<h3><strong>Mô tả một cột đặc biệt </strong></h3> 
<p pid="21">Nếu chúng ta muốn xem tóm tắt về bất kỳ cột cụ thể nào của DataFrame, chúng tôi sử dụng <code>describe</code><span id="_tmp_pre_8">&nbsp;</span>phương thức này. Phương pháp này cung cấp cho chúng tôi bản tóm tắt thống kê của cột đã cho, nếu không được chỉ định, nó cung cấp tóm tắt thống kê của DataFrame.</p> 
<pre class="ql-syntax s-code-block"><code lang="text/x-sql" class="hljs python"><table class="hljs-ln"><tbody><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="1"><div class="hljs-ln-n" data-line-number="1"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="1">fifa_df.describe(<span class="hljs-string">'Coach Name'</span>).show()</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="2"><div class="hljs-ln-n" data-line-number="2"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="2">fifa_df.describe(<span class="hljs-string">'Position'</span>).show()</td></tr></tbody></table></code></pre> 
<p pid="44"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-41-376-b748b594-8275-43a9-9e57-64fff20f7195.jpg"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-41-435-7ff7e10c-047b-44f7-ba8c-2c3d1a004665.jpg"></p> 
<h3><strong>Chọn nhiều cột </strong></h3> 
<p pid="22">Nếu chúng tôi muốn chọn các cột cụ thể từ DataFrame, chúng tôi sử dụng&nbsp; <code>select</code>&nbsp;phương thức.</p> 
<pre class="ql-syntax s-code-block"><code lang="text/x-sql" class="hljs csharp">fifa_df.<span class="hljs-keyword">select</span>(<span class="hljs-string">'Player Name'</span>,<span class="hljs-string">'Coach Name'</span>).show()</code></pre> 
<p pid="45"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-41-490-d3482a54-2354-42f5-b18a-714e08373ccd.jpg"></p> 
<h3><strong>Chọn nhiều cột khác biệt </strong></h3> 
<pre class="ql-syntax s-code-block"><code lang="text/x-sql" class="hljs csharp">fifa_df.<span class="hljs-keyword">select</span>(<span class="hljs-string">'Player Name'</span>,<span class="hljs-string">'Coach Name'</span>).distinct().show()</code></pre> 
<p pid="46"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-41-545-54693a7e-a952-40d8-95c1-84d00155708d.jpg"></p> 
<h3><strong>Lọc dữ liệu </strong></h3> 
<p pid="23">Để lọc dữ liệu, theo điều kiện được chỉ định, chúng tôi sử dụng&nbsp; <code>filter</code>&nbsp;lệnh. Ở đây, chúng tôi đang lọc DataFrame của chúng tôi dựa trên điều kiện ID đối sánh phải bằng 1096 và sau đó chúng tôi đang tính toán có bao nhiêu bản ghi / hàng trong đầu ra được lọc.</p> 
<pre class="ql-syntax s-code-block"><code lang="text/x-scala" class="hljs swift"><table class="hljs-ln"><tbody><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="1"><div class="hljs-ln-n" data-line-number="1"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="1">fifa_df.<span class="hljs-built_in">filter</span>(fifa_df.<span class="hljs-type">MatchID</span>=='<span class="hljs-number">1096</span>').show()</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="2"><div class="hljs-ln-n" data-line-number="2"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="2"> </td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="3"><div class="hljs-ln-n" data-line-number="3"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="3">fifa_df.<span class="hljs-built_in">filter</span>(fifa_df.<span class="hljs-type">MatchID</span>=='<span class="hljs-number">1096</span>').<span class="hljs-built_in">count</span>()  <span class="hljs-comment">//to get the count</span></td></tr></tbody></table></code></pre> 
<p pid="47"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-41-610-af8193a8-06e4-44f9-96f6-b6dc06cec30b.jpg"></p> 
<h3><strong>Lọc dữ liệu (Nhiều tham số) </strong></h3> 
<p pid="24">Chúng tôi có thể lọc dữ liệu của mình dựa trên nhiều điều kiện (AND hoặc OR)</p> 
<pre class="ql-syntax s-code-block"><code lang="text/x-sql" class="hljs python">fifa_df.filter((fifa_df.Position==<span class="hljs-string">'C'</span>) &amp;&amp; (fifa_df.Event==<span class="hljs-string">"G40'"</span>)).show()</code></pre> 
<p pid="48"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-41-669-08d42bac-5f0d-4fdc-989a-39da623ada8b.jpg"></p> 
<h3><strong>Sắp xếp dữ liệu (OrderBy) </strong></h3> 
<p pid="25">Để sắp xếp dữ liệu chúng tôi sử dụng&nbsp; <code>OrderBy</code>&nbsp;phương pháp. Theo mặc định, nó sắp xếp theo thứ tự tăng dần, nhưng chúng ta cũng có thể thay đổi nó theo thứ tự giảm dần.</p> 
<pre class="ql-syntax s-code-block"><code lang="text/x-sql" class="hljs css"><span class="hljs-selector-tag">fifa_df</span><span class="hljs-selector-class">.orderBy</span>(<span class="hljs-selector-tag">fifa_df</span><span class="hljs-selector-class">.MatchID</span>)<span class="hljs-selector-class">.show</span>()</code></pre> 
<p pid="49"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-41-726-e39c731f-c7b8-40b8-b9bd-a471bd08d65e.jpg"></p> 
<h2><strong>PySpark Dataframes Ví dụ 2: Bộ dữ liệu Superheros </strong></h2> 
<p pid="50"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-41-782-438a0ef7-ae67-47da-a6d0-b47989ca26cc.jpg"></p> 
<h3><strong>Đang tải dữ liệu </strong></h3> 
<p pid="26">Ở đây chúng tôi sẽ tải dữ liệu theo cách tương tự như chúng tôi đã làm trước đó.</p> 
<pre class="ql-syntax s-code-block"><code lang="text/x-sql" class="hljs python"><table class="hljs-ln"><tbody><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="1"><div class="hljs-ln-n" data-line-number="1"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="1">Superhero_df = spark.read.csv(<span class="hljs-string">"path-of file/superheros.csv"</span>, inferSchema = <span class="hljs-literal">True</span>, header = <span class="hljs-literal">True</span>)</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="2"><div class="hljs-ln-n" data-line-number="2"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="2"> </td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="3"><div class="hljs-ln-n" data-line-number="3"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="3">Superhero_df.show(<span class="hljs-number">10</span>)</td></tr></tbody></table></code></pre> 
<p pid="51"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-41-895-38b26a01-345e-49c0-af23-d2466853208a.jpg"></p> 
<h3><strong>Lọc dữ liệu </strong></h3> 
<pre class="ql-syntax s-code-block"><code lang="text/x-scala" class="hljs swift"><table class="hljs-ln"><tbody><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="1"><div class="hljs-ln-n" data-line-number="1"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="1"><span class="hljs-type">Superhero_df</span>.<span class="hljs-built_in">filter</span>(<span class="hljs-type">Superhero_df</span>.<span class="hljs-type">Gender</span> == '<span class="hljs-type">Male'</span>).<span class="hljs-built_in">count</span>() <span class="hljs-comment">//Male Heros Count</span></td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="2"><div class="hljs-ln-n" data-line-number="2"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="2"> </td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="3"><div class="hljs-ln-n" data-line-number="3"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="3"><span class="hljs-type">Superhero_df</span>.<span class="hljs-built_in">filter</span>(<span class="hljs-type">Superhero_df</span>.<span class="hljs-type">Gender</span> == '<span class="hljs-type">Female'</span>).<span class="hljs-built_in">count</span>() <span class="hljs-comment">//Female Heros Count</span></td></tr></tbody></table></code></pre> 
<h3><strong>Phân nhóm dữ liệu </strong></h3> 
<p pid="27"><code>GroupBy</code><span id="_tmp_pre_12">&nbsp;</span>được sử dụng để nhóm DataFrame dựa trên cột được chỉ định. Ở đây, chúng tôi đang nhóm DataFrame dựa trên cột&nbsp; <code>Race</code><span id="_tmp_pre_13">&nbsp;</span>và sau đó với&nbsp; <code>count</code>&nbsp;chức năng, chúng tôi có thể tìm thấy số lượng của chủng tộc cụ thể.</p> 
<pre class="ql-syntax s-code-block"><code lang="text/x-sql" class="hljs swift"><table class="hljs-ln"><tbody><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="1"><div class="hljs-ln-n" data-line-number="1"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="1"><span class="hljs-type">Race_df</span> = <span class="hljs-type">Superhero_df</span>.groupby(<span class="hljs-string">"Race"</span>)\</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="2"><div class="hljs-ln-n" data-line-number="2"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="2">.<span class="hljs-built_in">count</span>()\</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="3"><div class="hljs-ln-n" data-line-number="3"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="3">.show()</td></tr></tbody></table></code></pre> 
<p pid="52"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-41-959-38bd672c-067e-457d-ae84-f831fe7535fe.jpg"></p> 
<h3><strong>Thực hiện các truy vấn SQL </strong></h3> 
<p pid="28">Chúng ta cũng có thể chuyển các truy vấn SQL trực tiếp đến bất kỳ DataFrame nào, vì chúng ta cần tạo một bảng từ DataFrame bằng&nbsp; <code>registerTempTable</code><span id="_tmp_pre_15">&nbsp;</span>phương thức và sau đó sử dụng&nbsp;&nbsp; <code>sqlContext.sql()</code><span id="_tmp_pre_16">&nbsp;</span>để truyền các truy vấn SQL.</p> 
<pre class="ql-syntax s-code-block"><code lang="text/x-sql" class="hljs python"><table class="hljs-ln"><tbody><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="1"><div class="hljs-ln-n" data-line-number="1"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="1">Superhero_df.registerTempTable(<span class="hljs-string">'superhero_table'</span>)</td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="2"><div class="hljs-ln-n" data-line-number="2"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="2"> </td></tr><tr><td class="hljs-ln-line hljs-ln-numbers" data-line-number="3"><div class="hljs-ln-n" data-line-number="3"></div></td><td class="hljs-ln-line hljs-ln-code" data-line-number="3">sqlContext.sql(<span class="hljs-string">'select * from superhero_table'</span>).show()</td></tr></tbody></table></code></pre> 
<p pid="53"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-41-895-38b26a01-345e-49c0-af23-d2466853208a.jpg"></p> 
<pre class="ql-syntax s-code-block"><code lang="text/x-sql" class="hljs sql">sqlContext.sql('<span class="hljs-keyword">select</span> <span class="hljs-keyword">distinct</span>(Eye_color) <span class="hljs-keyword">from</span> superhero_table<span class="hljs-string">').show()</span></code></pre> 
<p pid="54"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-42-080-f86dadd7-497c-42f2-b23d-ef3203b64811.jpg"></p> 
<pre class="ql-syntax s-code-block"><code lang="text/x-sql" class="hljs sql">sqlContext.sql('<span class="hljs-keyword">select</span> <span class="hljs-keyword">distinct</span>(Eye_color) <span class="hljs-keyword">from</span> superhero_table<span class="hljs-string">').count()</span></code></pre> 
<pre class="ql-syntax s-code-block"><code lang="text/x-sql" class="hljs sql">sqlContext.sql('<span class="hljs-keyword">select</span> <span class="hljs-keyword">max</span>(Weight) <span class="hljs-keyword">from</span> superhero_table<span class="hljs-string">').show()</span></code></pre> 
<p pid="55"><img src="https://cdn.helpex.vn/upload/2019/2/19/ar/04-21-42-194-f35f7770-4b48-4776-bf95-9cc36d1fbeb4.jpg"></p> 
<p pid="29">Và với điều này, chúng ta đã kết thúc Hướng dẫn về Khung dữ liệu PySpark này.</p> 
<p pid="31">Tôi hy vọng các bạn có ý tưởng về PySpark DataFrame là gì, tại sao nó được sử dụng trong ngành và các tính năng của nó trong hướng dẫn PySpark DataFrame này. Xin chúc mừng, bạn không còn là người mới sử dụng DataFrames.</p>
                
            

            


            
                        </div>

                        <div class="mt24 mb12">
                            <div class="post-taglist grid gs4 gsy fd-column">
                                <div class="ps-relative">
                                        <a href="/articles/it-code/tagged/big-data" class="post-tag js-gps-track" title="" rel="tag">big data</a>
                                        <a href="/articles/it-code/tagged/du-lieu-lon" class="post-tag js-gps-track" title="" rel="tag">dữ liệu lớn</a>
                                        <a href="/articles/it-code/tagged/pyspark" class="post-tag js-gps-track" title="" rel="tag">pyspark</a>
                                        <a href="/articles/it-code/tagged/dataframes" class="post-tag js-gps-track" title="" rel="tag">dataframes</a>
                                        <a href="/articles/it-code/tagged/huong-dan" class="post-tag js-gps-track" title="" rel="tag">hướng dẫn</a>
                                </div>
                            </div>
                        </div>

                        <div class="mb0 ">
                            <div class="mt16 grid gs8 gsy fw-wrap jc-end ai-start pt4">
                                <div class="grid--cell mr16" style="flex: 1 1 100px;">
                                    <div class="post-menu">
                                        <a href="javascript:" rel="nofollow" itemprop="url" class="js-share-link js-gps-track tpd-hideOnClickOutside" title="">chia sẻ</a>
                                        <span class="lsep">|</span>
                                        <button id="btnFollowPostAr-5c6b21e6ae03f628d053c29e" class="s-btn s-btn__link fc-black-400 h:fc-black-700 pb2 js-follow-post js-follow-question js-gps-track pr6" role="button">
                                            theo dõi
                                        </button>

                                    </div>
                                </div>

                                <div class="post-signature owner grid--cell">
                                    <div class="user-info user-hover">
                                        <div class="user-action-time">
                                            đã viết <span title="7/14/2018 2:00:00 AM" class="relativetime">02:00:00 14/07/2018</span>
                                        </div>
                                        <div class="user-gravatar32">
                                            <a href="/user/55ee42e98b75f32e3414f11f" class="tip_user float-left">
                                                <div class="gravatar-wrapper-32">
                                                    <img src="https://cdn.helpex.vn/upload/2020/06/23/55ee42e98b75f32e3414f11f-073457723_50x50.jpg" alt="" width="32" height="32" class="bar-sm">
                                                </div>
                                            </a>
                                        </div>
                                        <div class="user-details" itemprop="author" itemscope="" itemtype="http://schema.org/Person">
                                            <a href="/user/55ee42e98b75f32e3414f11f" class="tip_user">Lê Diệu Linh</a><span class="d-none" itemprop="name">Lê Diệu Linh</span>
                                            <div class="-flair">
                                                <span class="reputation-score" title="điểm uy tín " dir="ltr"><i class="fas fa-screwdriver pr2"></i> 5 5 385</span>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>

                    </div>
