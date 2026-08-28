  1. Khái niệm trừu tượng hóa (Abstraction)
Trừu tượng hóa là quá trình mô hình hóa các đặc điểm quan trọng của đối tượng thành các lớp (Class), chỉ giữ lại những thuộc tính và hành vi cần thiết, bỏ qua các chi tiết không quan trọng.
Trong lập trình hướng đối tượng, trừu tượng hóa gồm:
Trừu tượng hóa theo chức năng.
Trừu tượng hóa theo dữ liệu.
  2. Trừu tượng hóa đối tượng theo chức năng
Khái niệm: Là quá trình mô hình hóa các phương thức (method) của lớp dựa trên các hành động của đối tượng.
Các bước
B1:Xác định các hành động của đối tượng.
B2:Nhóm các đối tượng có hành động giống nhau.
B3:Xây dựng lớp tương ứng.
B4:Biến các hành động chung thành phương thức của lớp.
Ví dụ
Đối tượng Sinh viên có các hành động:
Đăng ký môn học
Học bài
Làm bài tập
Thi
class SinhVien {
    void dangKyMonHoc() {}
    void hocBai() {}
    void lamBaiTap() {}
    void thi() {}
}
Các hành động trên chính là các phương thức của lớp.
3. Trừu tượng hóa đối tượng theo dữ liệu
Khái niệm
Là quá trình mô hình hóa các thuộc tính của lớp dựa trên các thuộc tính của đối tượng.
Ví dụ
Một Ô tô có các thuộc tính:
Nhãn hiệu
Màu sắc
Giá bán
Công suất động cơ
class OTo {
    String nhanHieu;
    String mauSac;
    double giaBan;
    int congSuatDongCo;
}
Các biến trên chính là thuộc tính (attributes) của lớp.
  4. Ví dụ tổng hợp
class Xe {
    // Thuộc tính
    String hangXe;
    String mauSac;
    int tocDo;
    // Phương thức
    void khoiDong() {}
    void tangToc() {}
    void phanh() {}
    void tatMay() {}
}
Sử dụng:
Xe xe1 = new Xe();
xe1.hangXe = "Toyota";
xe1.mauSac = "Đen";
xe1.khoiDong();
xe1.tangToc();
  5. Ý nghĩa của trừu tượng hóa
Trừu tượng hóa giúp chỉ tập trung vào những thuộc tính và hành vi cần thiết, đồng thời ẩn đi các chi tiết cài đặt. Nhờ đó, chương trình đơn giản hơn, dễ sử dụng, dễ bảo trì, dễ mở rộng và tăng khả năng tái sử dụng mã nguồn.
