* Kế thừa
- Khái niệm: là cơ chế cho phép một lớp mới kế thừa các thuộc tính và phương thức của một lớp đã có.
- Lớp cha: là lớp được kế thừa.
  ví dụ:
  class Animal {
    String name;
    void eat() {
        System.out.println("Đang ăn");
    }
}
=> Animal là lớp cha
- Lớp con: là lớp kế thừa từ lớp cha.
  ví dụ:
  class Dog extends Animal {
    void bark() {
        System.out.println("Gâu gâu");
    }
}
=> Dog là lớp con của Animal
- Ý nghĩa:Kế thừa có những ý nghĩa chính:
  + Tái sử dụng code: lớp con sử dụng lại code của lớp cha.
  + Giảm code trùng lặp: những đặc điểm chung chỉ cần viết một lần ở lớp cha.
  + Dễ mở rộng chương trình: có thể tạo thêm các lớp con với đặc điểm riêng.
  + Tạo mối quan hệ giữa các lớp: thể hiện quan hệ "là một" (is-a)
  + Hỗ trợ tính đa hình: lớp cha có thể tham chiếu đến đối tượng của lớp con.
* Đóng gói
- - Khái niệm: là cơ chế gộp dữ liệu và các phương thức xử lý dữ liệu vào trong một lớp, đồng thời hạn chế quyền truy cập trực tiếp vào dữ liệu bên trong đối tượng.
 ví dụ:
  class Student {
    private String name;
    private double score;
    public String getName() {
        return name;
    }
    public void setName(String name) {
        this.name = name;
    }
    public double getScore() {
        return score;
    }
    public void setScore(double score) {
        if (score >= 0 && score <= 10) {
            this.score = score;
        }
    }
}
- Che giấu dữ liệu: là việc ngăn không cho bên ngoài truy cập trực tiếp vào những dữ liệu không nên được phép truy cập.
- Bảo vệ dữ liệu: Kiểm soát việc thay đổi dữ liệu để đảm bảo dữ liệu hợp lệ.
* Ví dụ: 
  class Person {
    private String name;
    public void setName(String name) {
        this.name = name;
    }
    public String getName() {
        return name;
    }
}
class Student extends Person {
    private double score;
    public void setScore(double score) {
        if (score >= 0 && score <= 10) {
            this.score = score;
        }
    }
    public double getScore() {
        return score;
    }
}
