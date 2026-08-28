# LỚP ĐỐI TƯỢNG
## 1. Khái niệm
Lớp đối tượng là tập hợp các đối tượng có những **thuộc tính và hành vi chung**.
Lớp đối tượng được sử dụng để mô tả một nhóm đối tượng cùng loại trong chương trình hướng đối tượng.

## 2. Thành phần của lớp đối tượng
Một lớp đối tượng thường xác định:
- Thuộc tính (Attribute): mô tả dữ liệu, đặc điểm hoặc trạng thái của đối tượng.
- Phương thức (Method): mô tả các hành vi hoặc chức năng mà đối tượng có thể thực hiện.
Mỗi đối tượng cụ thể được tạo ra từ một lớp được gọi là một thể hiện (Instance) của lớp.
Các đối tượng thuộc cùng một lớp có cấu trúc giống nhau nhưng giá trị thuộc tính có thể khác nhau.

## 3. Ví dụ
Xét lớp đối tượng `SinhVien`:

```cpp
class SinhVien {
private:
    string hoTen;
    int tuoi;
    float diemTB;

public:
    void hocBai();
    void hienThiThongTin();
};
