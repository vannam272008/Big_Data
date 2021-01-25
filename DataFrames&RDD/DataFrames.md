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
 
 
 
 <div id="content" class="snippet-hidden">
            <script type="text/javascript">
    articleId = "5c6b21e6ae03f628d053c29e";
    seoUrlTopic = 'it-code';
</script>
<div itemprop="mainEntity" itemscope="" itemtype="http://schema.org/Article">
    <link itemprop="image" href="https://helpex.vn/images/300x300.png">
    <div class="inner-content clearfix">
        <div id="question-header" class="grid sm:fd-column">
            <h1 itemprop="name" class="grid--cell fs-headline1 fl1 ow-break-word mb16">
                <a href="/article/huong-dan-pyspark-dataframe-gioi-thieu-ve-dataframes-5c6b21e6ae03f628d053c29e" class="question-hyperlink"><b>Hướng dẫn PySpark DataFrame: Giới thiệu về DataFrames</b></a>
            </h1>
            <div class="ml12 aside-cta grid--cell print:d-none sm:ml0 sm:mb12 sm:order-first sm:as-end">
                <a href="/articles/it-code/write" class="ws-nowrap s-btn s-btn__primary">
                    Tạo bài viết [IT &lt;code&gt;]
                </a>
            </div>
        </div>
        <div class="grid fw-wrap pb8 mb16 bb bc-black-2">
            <div class="grid--cell ws-nowrap mr16 mb8" title="7/14/2018 2:00:00 AM">
                <span class="fc-light mr2">Đã viết</span>
                <time itemprop="dateCreated" datetime="7/14/2018 2:00:00 AM">2 năm trước</time>
            </div>
            <div class="grid--cell ws-nowrap mr16 mb8">
                <span class="fc-light mr2">Hoạt động</span>
                <a href="javascript:" class="s-link s-link__inherit" title="1/24/2021 11:12:31 PM">8 giờ trước</a>
            </div>
            <div class="grid--cell ws-nowrap mb8" title="Đã xem 5,208 lần">
                <span class="fc-light mr2">Đã xem</span>
                5.2k
            </div>
        </div>
        <div id="mainbar" class="article-detail" role="main" aria-label="article" data-topic-id="5bee3d942722a8b5b5d84a1b">
            <div class="question" id="article">
                <div class="post-layout">
                    <div class="votecell post-layout--left mt4 pr24">
                        <div class="js-voting-container grid fd-column ai-stretch gs4 fc-black-200 p-sticky">
                            <div class="js-vote-up-btn grid--cell s-btn s-btn__unset c-pointer">
                                <a href="/user/55ee42e98b75f32e3414f11f" class="tip_user">
                                    <img src="https://cdn.helpex.vn/upload/2020/06/23/55ee42e98b75f32e3414f11f-073457723_50x50.jpg" width="32" class="border-radius3">
                                </a>
                            </div>
                            <button class="js-vote-up-btn grid--cell s-btn s-btn__unset c-pointer" title="">
                                <svg aria-hidden="true" class="m0 svg-icon iconArrowUpLg" width="36" height="36" viewBox="0 0 36 36">
                                    <path d="M2 26h32L18 10 2 26z"></path>
                                </svg>
                            </button>
                            <div class="js-vote-count grid--cell fc-black-500 fs-title grid fd-column ai-center" itemprop="upvoteCount">6</div>
                            <button class="js-vote-down-btn grid--cell s-btn s-btn__unset c-pointer" title="">
                                <svg aria-hidden="true" class="m0 svg-icon iconArrowDownLg" width="36" height="36" viewBox="0 0 36 36">
                                    <path d="M2 10h32L18 26 2 10z"></path>
                                </svg>
                            </button>

                            <button class="js-bookmark-btn s-btn s-btn__unset c-pointer py4 js-gps-track mb12" title="">
                                <svg aria-hidden="true" class="svg-icon iconBookmark" width="18" height="18" viewBox="0 0 18 18">
                                    <path d="M6 1a2 2 0 00-2 2v14l5-4 5 4V3a2 2 0 00-2-2H6zm3.9 3.83h2.9l-2.35 1.7.9 2.77L9 7.59l-2.35 1.7.9-2.76-2.35-1.7h2.9L9 2.06l.9 2.77z"></path>
                                </svg>
                                <div class="js-bookmark-count mt4">0</div>
                            </button>

                            <div class="js-vote-up-btn grid--cell s-btn s-btn__unset c-pointer mb8 border_bbc0c4 border-radius3">
                                <a class="ficon-social" id="share-fb" href="javascript:void(0)" onclick="javascript:genericSocialShare('https://facebook.com/sharer.php?u=' + window.location.href)" title="Facebook Share"><i class="fab fa-facebook-f"></i></a>
                            </div>
                            <div class="js-vote-up-btn grid--cell s-btn s-btn__unset c-pointer mb8 border_bbc0c4 border-radius3">
                                <a class="ficon-social" id="share-gp" href="javascript:void(0)" onclick="javascript:genericSocialShare('https://plus.google.com/share?url=' + window.location.href)" title="Google Plus Share"><i class="fab fa-google"></i></a>
                            </div>
                            <div class="js-vote-up-btn grid--cell s-btn s-btn__unset c-pointer mb8 border_bbc0c4 border-radius3">
                                <a class="ficon-social" id="share-tw" href="javascript:void(0)" onclick="javascript:genericSocialShare('http://twitter.com/share?text=Chia sẻ bài viết từ Helpex.vn&amp;url=' + window.location.href)" title="Twitter Share"><i class="fab fa-twitter"></i></a>
                            </div>
                            <div class="js-vote-up-btn grid--cell s-btn s-btn__unset c-pointer mb8 border_bbc0c4 border-radius3">
                                <a class="ficon-social" id="share-email" href="javascript:void(0)" onclick="javascript:genericSocialShare('mailto:?subject=Chia sẻ bài viết từ Helpex.vn&amp;body=' + window.location.href)" title="E-Mail Share"><i class="far fa-envelope"></i></a>
                            </div>
                        </div>
                    </div>
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

                    <div class="post-layout--right">

                        <div id="comments-link-5c6b21e6ae03f628d053c29e">
                                <a class="js-add-link comments-link disabled-link" title="" href="#" role="button">thêm 1 bình luận</a>
                                <span class="js-link-separator dno">&nbsp;|&nbsp;</span>
                                <a class="js-show-link comments-link " title="mở rộng để hiển thị tất cả các bình luận về bài đăng này" href="#" onclick="" role="button"></a>
                        </div>
                    </div>
                </div>
            </div>

        </div>
        <div id="sidebar" class="show-votes">
        <div class="module sidebar-related">
            <h4 id="h-related">Bài viết liên quan</h4>
            <div class="related js-gps-related-questions">
                        <div class="spacer js-gps-track article-summary">
                            <a href="/article/6-cach-theo-doi-nguoi-dung-thuc-su-khac-voi-google-analytics-5c6b1374ae03f628d053b7c1" alt="">
                                <img src="https://cdn.helpex.vn/upload/ar/2017/10/03/6-cach-theo-doi-nguoi-dung-thuc-su-khac-voi-google-analytics-073726103.jpg" alt="6 cách theo dõi người dùng thực sự khác với Google Analytics" title="" width="115">
                            </a>
                            <a href="/article/6-cach-theo-doi-nguoi-dung-thuc-su-khac-voi-google-analytics-5c6b1374ae03f628d053b7c1" class="question-hyperlink fw-normal">6 cách theo dõi người dùng thực sự khác với Google Analytics [2]</a>
                        </div>
                        <div class="spacer js-gps-track article-summary">
                            <a href="/article/cach-toi-thieu-hoa-du-lieu-sap-xep-va-toi-da-hoa-du-lieu-thong-minh-help-1-5c6b1377ae03f628d053b7c5" alt="">
                                <img src="https://cdn.helpex.vn/upload/ar/2016/05/19/cach-toi-thieu-hoa-du-lieu-sap-xep-va-toi-da-hoa-du-lieu-thong-minh-help-1-095935528.jpg" alt="Cách tối thiểu hóa dữ liệu sắp xếp và tối đa hóa dữ liệu thông minh [Help 1]?" title="" width="115">
                            </a>
                            <a href="/article/cach-toi-thieu-hoa-du-lieu-sap-xep-va-toi-da-hoa-du-lieu-thong-minh-help-1-5c6b1377ae03f628d053b7c5" class="question-hyperlink fw-normal">Cách tối thiểu hóa dữ liệu sắp xếp và tối đa hóa dữ liệu thông minh [Help 1]? [0]</a>
                        </div>
                        <div class="spacer js-gps-track article-summary">
                            <a href="/article/giai-phap-phan-tich-du-lieu-lon-giup-ngan-chan-nan-buon-nguoi-5c6b1378ae03f628d053b7c8" alt="">
                                <img src="https://cdn.helpex.vn/upload/ar/2015/04/03/giai-phap-phan-tich-du-lieu-lon-giup-ngan-chan-nan-buon-nguoi-080930711.jpg" alt="Giải pháp phân tích dữ liệu lớn giúp ngăn chặn nạn buôn người" title="" width="115">
                            </a>
                            <a href="/article/giai-phap-phan-tich-du-lieu-lon-giup-ngan-chan-nan-buon-nguoi-5c6b1378ae03f628d053b7c8" class="question-hyperlink fw-normal">Giải pháp phân tích dữ liệu lớn giúp ngăn chặn nạn buôn người [4]</a>
                        </div>
                        <div class="spacer js-gps-track article-summary">
                            <a href="/article/hadoop-va-kho-du-lieu-doi-thu-doi-hinh-trong-mo-hoac-danh-sach-b-moi-5c6b1378ae03f628d053b7ca" alt="">
                                <img src="https://cdn.helpex.vn/upload/ar/2017/09/23/hadoop-va-kho-du-lieu-doi-thu-doi-hinh-trong-mo-hoac-danh-sach-b-moi-070054771.jpg" alt="Hadoop và kho dữ liệu: Đối thủ, Đội hình trong mơ hoặc Danh sách B mới?" title="" width="115">
                            </a>
                            <a href="/article/hadoop-va-kho-du-lieu-doi-thu-doi-hinh-trong-mo-hoac-danh-sach-b-moi-5c6b1378ae03f628d053b7ca" class="question-hyperlink fw-normal">Hadoop và kho dữ liệu: Đối thủ, Đội hình trong mơ hoặc Danh sách B mới? [5]</a>
                        </div>
                        <div class="spacer js-gps-track article-summary">
                            <a href="/article/su-dung-python-cho-khoi-luong-cong-viec-du-lieu-lon-phan-2-5c6b1379ae03f628d053b7cc" alt="">
                                <img src="https://cdn.helpex.vn/upload/ar/2019/09/07/su-dung-python-cho-khoi-luong-cong-viec-du-lieu-lon-phan-2-125918470.jpg" alt="Sử dụng Python cho khối lượng công việc dữ liệu lớn (Phần 2)" title="" width="115">
                            </a>
                            <a href="/article/su-dung-python-cho-khoi-luong-cong-viec-du-lieu-lon-phan-2-5c6b1379ae03f628d053b7cc" class="question-hyperlink fw-normal">Sử dụng Python cho khối lượng công việc dữ liệu lớn (Phần 2) [4]</a>
                        </div>
                        <div class="spacer js-gps-track article-summary">
                            <a href="/article/thong-so-dieu-chinh-trong-gbm-de-tao-mo-hinh-tot-nhat-5c6b1379ae03f628d053b7cf" alt="">
                                <img src="https://cdn.helpex.vn/upload/ar/2016/08/13/thong-so-dieu-chinh-trong-gbm-de-tao-mo-hinh-tot-nhat-064802256.jpg" alt="Thông số điều chỉnh trong GBM để tạo mô hình tốt nhất" title="" width="115">
                            </a>
                            <a href="/article/thong-so-dieu-chinh-trong-gbm-de-tao-mo-hinh-tot-nhat-5c6b1379ae03f628d053b7cf" class="question-hyperlink fw-normal">Thông số điều chỉnh trong GBM để tạo mô hình tốt nhất [2]</a>
                        </div>
                        <div class="spacer js-gps-track article-summary">
                            <a href="/article/tuan-nay-tai-hadoop-va-hon-the-nua-hoc-sau-va-truyen-truc-tiep-5c6b137aae03f628d053b7d1" alt="">
                                <img src="https://cdn.helpex.vn/upload/ar/2019/09/18/tuan-nay-tai-hadoop-va-hon-the-nua-hoc-sau-va-truyen-truc-tiep-113256525.jpg" alt="Tuần này tại Hadoop và hơn thế nữa: Học sâu và truyền trực tiếp" title="" width="115">
                            </a>
                            <a href="/article/tuan-nay-tai-hadoop-va-hon-the-nua-hoc-sau-va-truyen-truc-tiep-5c6b137aae03f628d053b7d1" class="question-hyperlink fw-normal">Tuần này tại Hadoop và hơn thế nữa: Học sâu và truyền trực tiếp [5]</a>
                        </div>
                        <div class="spacer js-gps-track article-summary">
                            <a href="/article/tim-phan-mem-phan-tich-du-lieu-phu-hop-cho-nhu-cau-cua-ban-5c6b137bae03f628d053b7d4" alt="">
                                <img src="https://cdn.helpex.vn/upload/ar/2019/05/08/tim-phan-mem-phan-tich-du-lieu-phu-hop-cho-nhu-cau-cua-ban-042947681.jpg" alt="Tìm phần mềm phân tích dữ liệu phù hợp cho nhu cầu của bạn" title="" width="115">
                            </a>
                            <a href="/article/tim-phan-mem-phan-tich-du-lieu-phu-hop-cho-nhu-cau-cua-ban-5c6b137bae03f628d053b7d4" class="question-hyperlink fw-normal">Tìm phần mềm phân tích dữ liệu phù hợp cho nhu cầu của bạn [4]</a>
                        </div>
                        <div class="spacer js-gps-track article-summary">
                            <a href="/article/phan-tich-nang-cao-de-xu-ly-tien-mat-5c6b137cae03f628d053b7d8" alt="">
                                <img src="https://cdn.helpex.vn/upload/ar/2017/02/19/phan-tich-nang-cao-de-xu-ly-tien-mat-091808353.jpg" alt="Phân tích nâng cao để xử lý tiền mặt" title="" width="115">
                            </a>
                            <a href="/article/phan-tich-nang-cao-de-xu-ly-tien-mat-5c6b137cae03f628d053b7d8" class="question-hyperlink fw-normal">Phân tích nâng cao để xử lý tiền mặt [6]</a>
                        </div>
                        <div class="spacer js-gps-track article-summary">
                            <a href="/article/apache-flume-loc-regex-5c6b137cae03f628d053b7db" alt="">
                                <img src="https://cdn.helpex.vn/upload/ar/2019/02/18/apache-flume-loc-regex-092643238.jpg" alt="Apache Flume: Lọc Regex" title="" width="115">
                            </a>
                            <a href="/article/apache-flume-loc-regex-5c6b137cae03f628d053b7db" class="question-hyperlink fw-normal">Apache Flume: Lọc Regex [6]</a>
                        </div>
                        <div class="spacer js-gps-track article-summary">
                            <a href="/article/5-trinh-dieu-khien-quan-trong-de-kich-hoat-phan-tich-tu-phuc-vu-thanh-cong-5c6b137dae03f628d053b7de" alt="">
                                <img src="https://cdn.helpex.vn/upload/ar/2020/05/24/5-trinh-dieu-khien-quan-trong-de-kich-hoat-phan-tich-tu-phuc-vu-thanh-cong-042325072.jpg" alt="5 trình điều khiển quan trọng để kích hoạt phân tích tự phục vụ thành công" title="" width="115">
                            </a>
                            <a href="/article/5-trinh-dieu-khien-quan-trong-de-kich-hoat-phan-tich-tu-phuc-vu-thanh-cong-5c6b137dae03f628d053b7de" class="question-hyperlink fw-normal">5 trình điều khiển quan trọng để kích hoạt phân tích tự phục vụ thành công [3]</a>
                        </div>
                        <div class="spacer js-gps-track article-summary">
                            <a href="/article/5-dau-hieu-doanh-nghiep-cua-ban-can-kinh-doanh-thong-minh-5c6b137dae03f628d053b7e0" alt="">
                                <img src="https://cdn.helpex.vn/upload/ar/2019/10/07/5-dau-hieu-doanh-nghiep-cua-ban-can-kinh-doanh-thong-minh-081036699.jpg" alt="5 dấu hiệu doanh nghiệp của bạn cần kinh doanh thông minh" title="" width="115">
                            </a>
                            <a href="/article/5-dau-hieu-doanh-nghiep-cua-ban-can-kinh-doanh-thong-minh-5c6b137dae03f628d053b7e0" class="question-hyperlink fw-normal">5 dấu hiệu doanh nghiệp của bạn cần kinh doanh thông minh [8]</a>
                        </div>
                        <div class="spacer js-gps-track article-summary">
                            <a href="/article/wxpython-tim-hieu-ve-treectrls-5c6b1380ae03f628d053b7e3" alt="">
                                <img src="https://cdn.helpex.vn/upload/ar/2017/04/07/wxpython-tim-hieu-ve-treectrls-061527962.jpg" alt="WxPython: Tìm hiểu về TreeCtrls" title="" width="115">
                            </a>
                            <a href="/article/wxpython-tim-hieu-ve-treectrls-5c6b1380ae03f628d053b7e3" class="question-hyperlink fw-normal">WxPython: Tìm hiểu về TreeCtrls [2]</a>
                        </div>
                        <div class="spacer js-gps-track article-summary">
                            <a href="/article/trong-tuong-lai-quan-diem-hien-tai-cua-chung-toi-ve-du-lieu-ca-nhan-se-gay-soc-5c6b1380ae03f628d053b7e5" alt="">
                                <img src="https://cdn.helpex.vn/upload/ar/2016/11/14/trong-tuong-lai-quan-diem-hien-tai-cua-chung-toi-ve-du-lieu-ca-nhan-se-gay-soc-103537748.jpg" alt="Trong tương lai, quan điểm hiện tại của chúng tôi về dữ liệu cá nhân sẽ gây sốc" title="" width="115">
                            </a>
                            <a href="/article/trong-tuong-lai-quan-diem-hien-tai-cua-chung-toi-ve-du-lieu-ca-nhan-se-gay-soc-5c6b1380ae03f628d053b7e5" class="question-hyperlink fw-normal">Trong tương lai, quan điểm hiện tại của chúng tôi về dữ liệu cá nhân sẽ gây sốc [6]</a>
                        </div>
                        <div class="spacer js-gps-track article-summary">
                            <a href="/article/dung-tu-nhan-chim-minh-voi-du-lieu-lon-hadoop-co-the-la-huyet-mach-cua-ban-5c6b1384ae03f628d053b7e8" alt="">
                                <img src="https://cdn.helpex.vn/upload/ar/2018/06/23/dung-tu-nhan-chim-minh-voi-du-lieu-lon-hadoop-co-the-la-huyet-mach-cua-ban-032618847.jpg" alt="Đừng tự nhấn chìm mình với dữ liệu lớn: Hadoop có thể là huyết mạch của bạn" title="" width="115">
                            </a>
                            <a href="/article/dung-tu-nhan-chim-minh-voi-du-lieu-lon-hadoop-co-the-la-huyet-mach-cua-ban-5c6b1384ae03f628d053b7e8" class="question-hyperlink fw-normal">Đừng tự nhấn chìm mình với dữ liệu lớn: Hadoop có thể là huyết mạch của bạn [7]</a>
                        </div>
                        <div class="spacer js-gps-track article-summary">
                            <a href="/article/bigquery-va-nguoi-dung-moi-top-3-wtf-khoanh-khac-5c6b1387ae03f628d053b7e9" alt="">
                                <img src="https://cdn.helpex.vn/upload/ar/2019/12/08/bigquery-va-nguoi-dung-moi-top-3-wtf-khoanh-khac-034603457.jpg" alt="BigQuery và người dùng mới: Top 3 &quot;WTF!?&quot; Khoảnh khắc" title="" width="115">
                            </a>
                            <a href="/article/bigquery-va-nguoi-dung-moi-top-3-wtf-khoanh-khac-5c6b1387ae03f628d053b7e9" class="question-hyperlink fw-normal">BigQuery và người dùng mới: Top 3 "WTF!?" Khoảnh khắc [5]</a>
                        </div>
                        <div class="spacer js-gps-track article-summary">
                            <a href="/article/bat-dau-voi-apache-ignite-phan-2-5c6b1389ae03f628d053b7eb" title="Điểm hữu ích">
                                <div class="answer-votes answered-accepted default">6</div>
                            </a>
                            <a href="/article/bat-dau-voi-apache-ignite-phan-2-5c6b1389ae03f628d053b7eb" class="question-hyperlink fw-normal">Bắt đầu với Apache Ignite (Phần 2)</a>
                        </div>
                        <div class="spacer js-gps-track article-summary">
                            <a href="/article/apache-spark-xu-ly-dau-thoi-gian-null-khi-doc-csv-trong-spark-2.0.0-5c6b138aae03f628d053b7ed" alt="">
                                <img src="https://cdn.helpex.vn/upload/ar/2018/04/13/apache-spark-xu-ly-dau-thoi-gian-null-khi-doc-csv-trong-spark-2.0.0-094933407.jpg" alt="Apache Spark: Xử lý dấu thời gian Null khi đọc CSV trong Spark 2.0.0" title="" width="115">
                            </a>
                            <a href="/article/apache-spark-xu-ly-dau-thoi-gian-null-khi-doc-csv-trong-spark-2.0.0-5c6b138aae03f628d053b7ed" class="question-hyperlink fw-normal">Apache Spark: Xử lý dấu thời gian Null khi đọc CSV trong Spark 2.0.0 [6]</a>
                        </div>
                        <div class="spacer js-gps-track article-summary">
                            <a href="/article/du-lieu-lon-cho-bi-thay-doi-tro-choi-hoac-ten-moi-cho-cung-mot-ky-thuat-cu-5c6b138dae03f628d053b7ef" alt="">
                                <img src="https://cdn.helpex.vn/upload/ar/2017/08/14/du-lieu-lon-cho-bi-thay-doi-tro-choi-hoac-ten-moi-cho-cung-mot-ky-thuat-cu-125613481.jpg" alt="Dữ liệu lớn cho BI: Thay đổi trò chơi hoặc Tên mới cho cùng một kỹ thuật cũ?" title="" width="115">
                            </a>
                            <a href="/article/du-lieu-lon-cho-bi-thay-doi-tro-choi-hoac-ten-moi-cho-cung-mot-ky-thuat-cu-5c6b138dae03f628d053b7ef" class="question-hyperlink fw-normal">Dữ liệu lớn cho BI: Thay đổi trò chơi hoặc Tên mới cho cùng một kỹ thuật cũ? [5]</a>
                        </div>
                        <div class="spacer js-gps-track article-summary">
                            <a href="/article/truc-quan-hoa-du-lieu-va-ke-chuyen-xung-quanh-bo-suu-tap-bao-tang-bang-api-5c6b1391ae03f628d053b7f1" alt="">
                                <img src="https://cdn.helpex.vn/upload/ar/2015/06/27/truc-quan-hoa-du-lieu-va-ke-chuyen-xung-quanh-bo-suu-tap-bao-tang-bang-api-020514557.jpg" alt="Trực quan hóa dữ liệu và kể chuyện xung quanh bộ sưu tập bảo tàng bằng API" title="" width="115">
                            </a>
                            <a href="/article/truc-quan-hoa-du-lieu-va-ke-chuyen-xung-quanh-bo-suu-tap-bao-tang-bang-api-5c6b1391ae03f628d053b7f1" class="question-hyperlink fw-normal">Trực quan hóa dữ liệu và kể chuyện xung quanh bộ sưu tập bảo tàng bằng API [4]</a>
                        </div>
            </div>
        </div>
        <div class="module sidebar-related">
            <h4 id="h-related">Câu hỏi liên quan</h4>
            <div class="related js-gps-related-questions">
                    <div class="spacer js-gps-track">
                        <a href="/question/cau-hinh-xml-so-voi-cau-hinh-dua-tren-chu-thich-da-dong-5cbd97ccae03f64844b64e47" title="Điểm hữu ích">
                            <div class="answer-votes  default">129</div>
                        </a>
                        <a href="/question/cau-hinh-xml-so-voi-cau-hinh-dua-tren-chu-thich-da-dong-5cbd97ccae03f64844b64e47" class="question-hyperlink">Cấu hình Xml so với cấu hình dựa trên chú thích [đã đóng]?</a>
                    </div>
                    <div class="spacer js-gps-track">
                        <a href="/question/lam-cach-nao-de-tao-kieu-dau-vao-nut-hoat-dong-nhu-mot-sieu-lien-ket-va-chuyen-huong-bang-cach-su-dung-yeu-cau-get-ban-sao-5cbd97cdae03f64844b64e60" title="Điểm hữu ích">
                            <div class="answer-votes  default">129</div>
                        </a>
                        <a href="/question/lam-cach-nao-de-tao-kieu-dau-vao-nut-hoat-dong-nhu-mot-sieu-lien-ket-va-chuyen-huong-bang-cach-su-dung-yeu-cau-get-ban-sao-5cbd97cdae03f64844b64e60" class="question-hyperlink">Làm cách nào để tạo kiểu đầu vào = nút hoạt động như một siêu liên kết và chuyển hướng bằng cách sử dụng yêu cầu get? [bản sao]?</a>
                    </div>
                    <div class="spacer js-gps-track">
                        <a href="/question/tuan-tu-hoa-ca-the-lop-thanh-json-5cbd97cdae03f64844b64e72" title="Điểm hữu ích">
                            <div class="answer-votes  default">129</div>
                        </a>
                        <a href="/question/tuan-tu-hoa-ca-the-lop-thanh-json-5cbd97cdae03f64844b64e72" class="question-hyperlink">Tuần tự hóa cá thể lớp thành JSON?</a>
                    </div>
                    <div class="spacer js-gps-track">
                        <a href="/question/tai-sao-mot-lop-java-nen-thuc-hien-so-sanh-5cbd97ceae03f64844b64e8c" title="Điểm hữu ích">
                            <div class="answer-votes  default">129</div>
                        </a>
                        <a href="/question/tai-sao-mot-lop-java-nen-thuc-hien-so-sanh-5cbd97ceae03f64844b64e8c" class="question-hyperlink">Tại sao một lớp Java nên thực hiện so sánh?</a>
                    </div>
                    <div class="spacer js-gps-track">
                        <a href="/question/bien-dich-chuoi-html-dong-tu-co-so-du-lieu-5cbd97cfae03f64844b64ea1" title="Điểm hữu ích">
                            <div class="answer-votes  default">129</div>
                        </a>
                        <a href="/question/bien-dich-chuoi-html-dong-tu-co-so-du-lieu-5cbd97cfae03f64844b64ea1" class="question-hyperlink">Biên dịch chuỗi HTML động từ cơ sở dữ liệu?</a>
                    </div>
                    <div class="spacer js-gps-track">
                        <a href="/question/cac-truong-mau-bi-vo-hieu-hoa-khong-gui-du-lieu-5cbd97cfae03f64844b64eb4" title="Điểm hữu ích">
                            <div class="answer-votes  default">129</div>
                        </a>
                        <a href="/question/cac-truong-mau-bi-vo-hieu-hoa-khong-gui-du-lieu-5cbd97cfae03f64844b64eb4" class="question-hyperlink">Các trường mẫu bị vô hiệu hóa không gửi dữ liệu?</a>
                    </div>
                    <div class="spacer js-gps-track">
                        <a href="/question/lam-the-nao-de-hinh-anh-dan-tu-chuc-nang-clipboard-hoat-dong-trong-gmail-va-google-chrome-12-5cbd97cfae03f64844b64ec2" title="Điểm hữu ích">
                            <div class="answer-votes  default">129</div>
                        </a>
                        <a href="/question/lam-the-nao-de-hinh-anh-dan-tu-chuc-nang-clipboard-hoat-dong-trong-gmail-va-google-chrome-12-5cbd97cfae03f64844b64ec2" class="question-hyperlink">Làm thế nào để hình ảnh dán từ chức năng clipboard hoạt động trong Gmail và Google Chrome 12+?</a>
                    </div>
                    <div class="spacer js-gps-track">
                        <a href="/question/lam-cach-nao-de-tuy-chinh-ltkieu-nhap-tap-tin-tren-mang-gtgt-5cbd97cfae03f64844b64eda" title="Điểm hữu ích">
                            <div class="answer-votes  default">129</div>
                        </a>
                        <a href="/question/lam-cach-nao-de-tuy-chinh-ltkieu-nhap-tap-tin-tren-mang-gtgt-5cbd97cfae03f64844b64eda" class="question-hyperlink">Làm cách nào để tùy chỉnh &lt;kiểu nhập = tập tin trên mạng &gt;&gt;?</a>
                    </div>
                    <div class="spacer js-gps-track">
                        <a href="/question/bat-ctrl-c-trong-c-5cbd97d0ae03f64844b64f05" title="Điểm hữu ích">
                            <div class="answer-votes  default">129</div>
                        </a>
                        <a href="/question/bat-ctrl-c-trong-c-5cbd97d0ae03f64844b64f05" class="question-hyperlink">Bắt Ctrl-C trong C?</a>
                    </div>
                    <div class="spacer js-gps-track">
                        <a href="/question/lam-cach-nao-de-lay-noi-dung-cua-iframe-trong-javascript-5cbd97d0ae03f64844b64f1e" title="Điểm hữu ích">
                            <div class="answer-votes  default">129</div>
                        </a>
                        <a href="/question/lam-cach-nao-de-lay-noi-dung-cua-iframe-trong-javascript-5cbd97d0ae03f64844b64f1e" class="question-hyperlink">Làm cách nào để lấy nội dung của iframe trong Javascript?</a>
                    </div>
                    <div class="spacer js-gps-track">
                        <a href="/question/html-hien-thi-hinh-anh-sau-khi-chon-ten-tep-trung-lap-5cbd97d1ae03f64844b64f3c" title="Điểm hữu ích">
                            <div class="answer-votes  default">129</div>
                        </a>
                        <a href="/question/html-hien-thi-hinh-anh-sau-khi-chon-ten-tep-trung-lap-5cbd97d1ae03f64844b64f3c" class="question-hyperlink">HTML - Hiển thị hình ảnh sau khi chọn tên tệp [trùng lặp]?</a>
                    </div>
                    <div class="spacer js-gps-track">
                        <a href="/question/intellij-idea-nhay-tu-giao-dien-sang-lop-trien-khai-trong-java-5cbd97d1ae03f64844b64f49" title="Điểm hữu ích">
                            <div class="answer-votes  default">129</div>
                        </a>
                        <a href="/question/intellij-idea-nhay-tu-giao-dien-sang-lop-trien-khai-trong-java-5cbd97d1ae03f64844b64f49" class="question-hyperlink">IntelliJ IDEA nhảy từ giao diện sang lớp triển khai trong Java?</a>
                    </div>
                    <div class="spacer js-gps-track">
                        <a href="/question/cau-hoi-phong-van-lap-trinh-vien-javascript-chuyen-nghiep-co-cau-tra-loi-da-dong-5cbd97d1ae03f64844b64f5c" title="Điểm hữu ích">
                            <div class="answer-votes  default">129</div>
                        </a>
                        <a href="/question/cau-hoi-phong-van-lap-trinh-vien-javascript-chuyen-nghiep-co-cau-tra-loi-da-dong-5cbd97d1ae03f64844b64f5c" class="question-hyperlink">Câu hỏi phỏng vấn lập trình viên JavaScript chuyên nghiệp (có câu trả lời) [đã đóng]?</a>
                    </div>
                    <div class="spacer js-gps-track">
                        <a href="/question/lam-cach-nao-de-lam-tron-trung-binh-den-2-chu-so-thap-phan-trong-postgresql-5cbd97d2ae03f64844b64f7b" title="Điểm hữu ích">
                            <div class="answer-votes  default">129</div>
                        </a>
                        <a href="/question/lam-cach-nao-de-lam-tron-trung-binh-den-2-chu-so-thap-phan-trong-postgresql-5cbd97d2ae03f64844b64f7b" class="question-hyperlink">Làm cách nào để làm tròn trung bình đến 2 chữ số thập phân trong PostgreSQL?</a>
                    </div>
                    <div class="spacer js-gps-track">
                        <a href="/question/trong-xcode-lam-the-nao-de-chan-tat-ca-cac-canh-bao-trong-cac-tep-nguon-cu-the-5cbd97d2ae03f64844b64f88" title="Điểm hữu ích">
                            <div class="answer-votes  default">129</div>
                        </a>
                        <a href="/question/trong-xcode-lam-the-nao-de-chan-tat-ca-cac-canh-bao-trong-cac-tep-nguon-cu-the-5cbd97d2ae03f64844b64f88" class="question-hyperlink">Trong Xcode, làm thế nào để chặn tất cả các cảnh báo trong các tệp nguồn cụ thể?</a>
                    </div>
                    <div class="spacer js-gps-track">
                        <a href="/question/lam-cach-nao-de-phat-hien-khi-ket-noi-wifi-duoc-thiet-lap-trong-android-5cbd97d5ae03f64844b64f98" title="Điểm hữu ích">
                            <div class="answer-votes  default">129</div>
                        </a>
                        <a href="/question/lam-cach-nao-de-phat-hien-khi-ket-noi-wifi-duoc-thiet-lap-trong-android-5cbd97d5ae03f64844b64f98" class="question-hyperlink">Làm cách nào để phát hiện khi kết nối WIFI được thiết lập trong Android?</a>
                    </div>
                    <div class="spacer js-gps-track">
                        <a href="/question/co-cach-nao-de-day-lui-cu-hich-cuoi-cung-cua-toi-den-git-khong-ban-sao-5cbd97d6ae03f64844b64fb9" title="Điểm hữu ích">
                            <div class="answer-votes  default">129</div>
                        </a>
                        <a href="/question/co-cach-nao-de-day-lui-cu-hich-cuoi-cung-cua-toi-den-git-khong-ban-sao-5cbd97d6ae03f64844b64fb9" class="question-hyperlink">Có cách nào để đẩy lùi cú hích cuối cùng của tôi đến Git không? [bản sao]?</a>
                    </div>
                    <div class="spacer js-gps-track">
                        <a href="/question/chay-exe-tu-ma-c-%23-5cbd97d6ae03f64844b64fc0" title="Điểm hữu ích">
                            <div class="answer-votes  default">129</div>
                        </a>
                        <a href="/question/chay-exe-tu-ma-c-%23-5cbd97d6ae03f64844b64fc0" class="question-hyperlink">Chạy exe từ mã C #?</a>
                    </div>
                    <div class="spacer js-gps-track">
                        <a href="/question/tao-tap-lenh-sql-day-du-tu-cac-lan-di-chuyen-dau-tien-cua-ma-5-cua-ma-5-5cbd97d6ae03f64844b64fc9" title="Điểm hữu ích">
                            <div class="answer-votes  default">129</div>
                        </a>
                        <a href="/question/tao-tap-lenh-sql-day-du-tu-cac-lan-di-chuyen-dau-tien-cua-ma-5-cua-ma-5-5cbd97d6ae03f64844b64fc9" class="question-hyperlink">Tạo tập lệnh SQL đầy đủ từ các lần di chuyển đầu tiên của mã 5 của mã 5?</a>
                    </div>
                    <div class="spacer js-gps-track">
                        <a href="/question/canvas-bi-nhiem-doc-co-the-khong-duoc-xuat-khau-5cbd97d6ae03f64844b64fd4" title="Điểm hữu ích">
                            <div class="answer-votes  default">129</div>
                        </a>
                        <a href="/question/canvas-bi-nhiem-doc-co-the-khong-duoc-xuat-khau-5cbd97d6ae03f64844b64fd4" class="question-hyperlink">Canvas bị nhiễm độc có thể không được xuất khẩu?</a>
                    </div>
            </div>
        </div>


</div>

    </div>
</div>
        </div>
