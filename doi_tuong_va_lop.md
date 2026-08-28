
1. Khái niệm Đối tượng (Object)
- Lập trình hướng đối tượng (OOP) là một mô hình lập trình dựa trên khái niệm "đối tượng".
Các đối tượng này có thể là bất kỳ thực thể nào trong thế giới thực, từ con người, đồ vật cho đến các khái niệm trừu tượng.
- Một đối tượng bao gồm 2 thông tin: thuộc tính và phương thức.
Thuộc tính (Attribute): Là những thông tin, đặc điểm miêu tả trạng thái của đối tượng. Ví dụ, đối với đối tượng "xe máy", thuộc tính có thể là màu sắc, dung tích xi lanh, biển số xe.
Phương thức (Method): Là những hành động mà đối tượng có thể thực hiện hoặc tác động lên đối tượng khác. Với "xe máy", phương thức có thể là "khởi động", "tăng tốc", "phanh".
 
2. Khái niệm Lớp (Class)

- Một lớp là một kiểu dữ liệu bao gồm các thuộc tính và các phương thức được định nghĩa từ trước. Đây là sự trừu tượng hóa của đối tượng. 
  Khác với kiểu dữ liệu thông thường, một lớp là một đơn vị (trừu tượng) bao gồm sự kết hợp giữa các phương thức và các thuộc tính. 
  Hiểu nôm na hơn là các đối tượng có các đặc tính tương tự nhau được gom lại thành một lớp đối tượng.

3. Mối quan hệ giữa Lớp và Object

•	Lớp (Class) là bản vẽ thiết kế trên giấy (chưa sử dụng bộ nhớ khi chưa thể tạo).

•	Object (Object) là nhà thực tế được xây dựng dựa trên bản thiết kế đó (tìm kiếm dung lượng bộ nhớ thực tế khi chạy chương trình).

•	Từ một lớp , ta có thể khởi tạo nhiều đối tượng khác nhau với các thuộc tính giá trị riêng biệt.

Ví dụ minh họa chi tiết 

#include <iostream>
#include <string>
using namespace std;

// 1. Định nghĩa LỚP (Class)
class SinhVien {
private:
    // Thuộc tính (Attributes) - Đặc trưng của sinh viên
    string ten;
    string maSV;
    float diemTB;

public:
    // Constructor (Hàm khởi tạo)
    SinhVien(string name, string id, float score) {
        ten = name;
        maSV = id;
        diemTB = score;
    }

    // Hành vi (Behaviors) - Phương thức thể hiện hành động của sinh viên
    void hienThiThongTin() {
        cout << "Ma SV: " << maSV << " | Ten: " << ten << " | Diem TB: " << diemTB << endl;
    }

    void xepLoai() {
        if (diemTB >= 8.0) {
            cout << ten << " dat loai: Gioi" << endl;
        } else if (diemTB >= 6.5) {
            cout << ten << " dat loai: Kha" << endl;
        } else {
            cout << ten << " dat loai: Trung Binh/Yeu" << endl;
        }
    }
};

int main() {
    // 2. Khởi tạo các ĐỐI TƯỢNG (Objects) từ Lớp SinhVien
    SinhVien sv1("Nguyen Van A", "SV001", 8.5); // Đối tượng 1
    SinhVien sv2("Tran Thi B", "SV002", 6.0);  // Đối tượng 2

    // 3. Gọi các HÀNH VI của từng đối tượng
    cout << "--- Thong tin Sinh Vien 1 ---" << endl;
    sv1.hienThiThongTin();
    sv1.xepLoai();

    cout << "\n--- Thong tin Sinh Vien 2 ---" << endl;
    sv2.hienThiThongTin();
    sv2.xepLoai();

    return 0;
}
C++
    sv2.hienThiThongTin();
    sv2.xepLoai()}
    
Giải thích ví dụ:
•	class SinhVien: Khai báo Lớp SinhVien.

•	ten, maSV, diemTB: Thuộc tính của sinh viên.

•	hienThiThongTin(), xepLoai(): Các hành vi của sinh viên.

•	sv1, sv2: Là hai đối tượng có thể được tạo ra từ lớp SinhVien, lưu giữ các thông tin khác nhau trong bộ nhớ.

