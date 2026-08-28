- Khái niệm đa hình: Đa hình là một phương thức/hành vi có cùng tên nhưng khi được thực hiện trên các đối tượng thuộc các lớp khác nhau thì có thể cho cách thực hiện hoặc kết quả khác nhau.
- Ý nghĩa của đa hình trong OOP:
  + Giúp chương trình linh hoạt và dễ mở rộng
  + Cho phép sử dụng một giao diện/phuong thức chung cho nhiều đối tượng khác nhau
  + Khi gọi cung một phương thức, chương trình sẽ tự xác định cách thực hiện phù hợp với đối tượng
  + Giảm việc phải viết nhiều đoạn code xư lý riêng biệt
- Một hành vi có thể được thực hiện khác nhau như thế nào?
   Ví dụ có lớp cha Ấn phẩm có phương thức:
  Lấy ra ()
  Các lớp con như Sách và Tạp chí đều có phương thức Lấy ra () nhưng cách thực hiện khác nhau:
  + Sách -> Lấy ra (): tìm sách theo ISBN hoặc tên tác giả.
  + Tạp chí -> Lấy ra (): tìm tạp chí theo tên hoặc só phát hành
  Khi chương trình gọi lấy ra (), nếu đối tượng là Sách thì thực hiện cách của Sách; nếu là Tạp chí thì thực hiện cách của Tạp chí.
Đây là đa hình: cùng một lời gọi Lấy ra () nhưng cho ra cách xử lý khác nhau tùy đối tượng.
