# Spark Properties 

- Thuộc tính Spark kiểm soát hầu hết các cài đặt ứng dụng và được cấu hình riêng cho từng ứng dụng. Các thuộc tính này có thể được đặt trực tiếp trên SparkConf được chuyển đến SparkContext. SparkConf cho phép định cấu hình một số thuộc tính chung (ví dụ: URL chính và tên ứng dụng), cũng như các cặp key-value tùy ý thông qua phương thức set(). Ví dụ: chúng ta có thể khởi tạo một ứng dụng với hai luồng như sau:

  + Lưu ý chạy với local [2] , nghĩa là hai luồng - thể hiện sự song song “tối thiểu”, có thể giúp phát hiện lỗi chỉ tồn tại khi chúng tôi chạy trong bối cảnh phân tán.
  
    <img src="https://github.com/vannam272008/Big_Data/blob/main/Spark_Properties/1.PNG">
  
  + Lưu ý rằng có thể có nhiều hơn 1 luồng ở chế độ cục bộ và trong những trường hợp như Spark Streaming và có thể yêu cầu nhiều hơn 1 luồng để ngăn chặn bất kỳ loại starvation issues (vấn đề chết đói) nào.

  + Các thuộc tính chỉ định một số khoảng thời gian nên được cấu hình với một đơn vị thời gian. Định dạng sau được chấp nhận:
    + 25ms (milliseconds)
    + 5s (seconds)
    + 10m or 10min (minutes)
    + 3h (hours)
    + 5d (days)
    + 1y (years)
  + Thuộc tính chỉ định kích thước byte phải được cấu hình với đơn vị kích thước. Định dạng sau được chấp nhận:
    + 1b (bytes)
    + 1k or 1kb (kibibytes = 1024 bytes)
    + 1m or 1mb (mebibytes = 1024 kibibytes)
    + 1g or 1gb (gibibytes = 1024 mebibytes)
    + 1t or 1tb (tebibytes = 1024 gibibytes)
    + 1p or 1pb (pebibytes = 1024 tebibytes)
  + Trong khi các số không có đơn vị thường được hiểu là byte, một số ít được hiểu là KiB hoặc MiB. Xem tài liệu về các thuộc tính cấu hình riêng lẻ. Việc chỉ định đơn vị là mong muốn nếu có thể.
  
## Dynamically Loading Spark Properties (Tải động các thuộc tính Spark)

- Trong một số trường hợp, có thể muốn tránh mã hóa cứng các cấu hình nhất định trong SparkConf.
- Spark shell và công cụ spark-submit hỗ trợ hai cách để tải cấu hình động. Đầu tiên là các tùy chọn dòng lệnh, chẳng hạn như --master, như được hiển thị ở trên. spark-submitcó thể chấp nhận bất kỳ thuộc tính Spark nào bằng cách sử dụng --conf flag, nhưng sử dụng cờ đặc biệt cho các thuộc tính đóng một phần trong việc khởi chạy ứng dụng Spark. Chạy dòng lệnh: ./bin/spark-submit --helpsẽ hiển thị toàn bộ danh sách các tùy chọn này.
- bin/spark-submitcũng sẽ đọc các tùy chọn cấu hình conf/spark-defaults.conf, trong đó mỗi dòng bao gồm một khóa và một giá trị được phân tách bằng khoảng trắng.

## Xem thuộc tính Spark

- Giao diện người dùng web ứng dụng tại http://<driver>:4040 liệt kê các thuộc tính Spark trong tab "Environment". Đây là một nơi hữu ích để kiểm tra để đảm bảo rằng các thuộc tính của bạn đã được đặt chính xác. Lưu ý rằng chỉ có giá trị xác định một cách rõ ràng thông qua spark-defaults.conf, SparkConf hoặc command line sẽ xuất hiện. Đối với tất cả các thuộc tính cấu hình khác, bạn có thể giả sử giá trị mặc định được sử dụng.

## Thuộc tính có sẵn

- Hầu hết các thuộc tính kiểm soát cài đặt nội bộ đều có giá trị mặc định hợp lý. Một số tùy chọn phổ biến nhất để đặt là:

  + Application Properties (Thuộc tính ứng dụng)
  + Runtime Environment (Môi trường thực thi)
  + Shuffle Behavior 
  + Spark UI (Giao diện người dùng Spark)
  + Compression and Serialization (Nén và tuần tự hóa)
  + Memory Management (Quản lý bộ nhớ)
  + Execution Behavior (Hành vi Thực thi)
  
  
  
  

  
  
