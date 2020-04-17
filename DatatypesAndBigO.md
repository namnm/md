##Tìm hiểu về Big-O và các các kiểu dữ liệu trong lập trình nói chung

##Big-O (time-complexity and memory-complexity)

* Khái niệm Big O hoạc với tên gọi khác trong tiếng Việt là “độ phức tạp của thuật toán” là thuật ngữ thường dùng để chỉ khoảng thời gian tiêu hao để chạy một thuật toán. Các lập trình viên thường sử dụng Big O như một phương tiện để so sánh mức độ hiệu quả của nhiều cách xử lý khác nhau cho cùng một vấn đề.

##Mảng trong lập trình nói chung

* Mảng là một tập hợp các phần tử cố định có cùng một kiểu, được lưu trữ liên tiếp nhau trong các ô nhớ. Kiểu phần tử có thể là có các kiểu bất kỳ: ký tự, số, chuỗi ký tự…; cũng có khi ta sử dụng kiểu mảng để làm kiểu phần tử cho một mảng (trong trường hợp này ta gọi là mảng của mảng hay mảng nhiều chiều).

* Mảng là kiểu dữ liệu được sử dụng rất thường xuyên. Chẳng hạn người ta cần quản lý một danh sách họ và tên của khoảng 100 sinh viên trong một lớp. Nhận thấy rằng mỗi họ và tên để lưu trữ ta cần một biến kiểu chuỗi, như vậy 100 họ và tên thì cần khai báo 100 biến kiểu chuỗi. Nếu khai báo như thế này thì đoạn khai báo cũng như các thao tác trên các họ tên sẽ rất dài dòng và rắc rối. Vì thế, kiểu dữ liệu mảng giúp ích ta trong trường hợp này; chỉ cần khai báo một biến, biến này có thể coi như là tương đương với 100 biến chuỗi ký tự; đó là 1 mảng mà các phần tử của nó là chuỗi ký tự.

##Danh sách trong lập trình nói chung

* Là một trong những cấu trúc cơ bản nhất được cài đặt trong hầu hết các chương trình ứng dụng. Danh sách là một kiểu dữ liệu trừu tượng gồm nhiều nút cùng các kiểu dữ liệu, các nút trong danh sách có thứ tự.

* Có 2 cách cài đặt danh sách:
Cài đặt theo kiểu kế tiếp, ta có danh sách kề
Cài đặt theo kiểu liên kết, ta có danh sách liên kết.

* Danh sách là một tập hợp các nút cùng kiểu dữ liệu, các nút trong danh sách có thứ tự.

* Lợi ích chính của danh sách liên kết so với mảng thông thường là các phần tử danh sách có thể được chèn hay xóa một cách dễ dàng mà không cần phân bổ lại hoặc sắp xếp lại toàn bộ cấu trúc vì các mục dữ liệu không cần được lưu trữ liên tục trong bộ nhớ hay trên đĩa, trong khi tái cấu trúc một mảng tại thời gian chạy là một hoạt động tốn kém hơn nhiều. Danh sách liên kết cho phép chèn hay xóa nút tại bất kỳ điểm nào trong danh sách. Mặc khác, vì bản thân danh sách liên kết được liên kết đơn giản nên không cho phép truy cập ngẫu nhiên tới dữ liệu hoặc bất kỳ hình thức đánh chỉ mục hiệu quả nào, nhiều toán tử cơ bản như lấy nút cuối cùng của danh sách, tìm một nút có chứa dữ liệu đã cho, hay tìm vị trí của nút để chèn một nút mới sẽ yêu cầu lặp qua hầu hết hoặc tất cả các phần tử của danh sách. Những ưu điểm và nhược điểm của danh sách liên kết được đưa ra dưới đây. Danh sách liên kết là động, vì vậy độ dài của nó có thể tăng hay giảm khi cần thiết. Mỗi nút không cần phải theo nút trước đó trong bộ nhớ.

##Map trong lập trình nói chung

* Các cấu trúc dữ liệu như mảng hay xâu ký tự, khi truy xuất dữ liệu bạn sẽ sử dụng một tham số gọi là chỉ số, ví dụ như arr[1], str[2], … Đối với cấu trúc dữ liệu map, để truy xuất dữ liệu bạn sẽ sử dụng một tham số gọi là key Cấu trúc dữ liệu kiểu map là một cấu trúc dữ liệu ánh xạ giữa cái gọi là khoá (key) sang giá trị của khoá đó (gọi là value) Trong cấu trúc dữ liệu này, mỗi một key sẽ nhận một giá trị khác nhau.

##Set trong lập trình nói chung

* Set là tập hợp hữu hạn các phần tử (thành viên) và có 2 tính chất:
Các phần tử không được sắp xếp theo thứ tự
Mỗi phần tử không được xuất hiện nhiều hơn 1 lần

##Hash table trong lập trình nói chung

* Cấu trúc dữ liệu Hash Table là một cấu trúc dữ liệu lưu giữ dữ liệu theo cách thức liên hợp. Trong HashTable, dữ liệu được lưu giữ trong định dạng mảng, trong đó các giá trị dữ liệu có giá trị chỉ mục riêng. Việc truy cập dữ liệu trở nên nhanh hơn nếu chúng ta biết chỉ mục của dữ liệu cần tìm. Do đó, với loại cấu trúc dữ liệu Hash Table này thì các hoạt động chèn và hoạt động tìm kiếm sẽ diễn ra rất nhanh, bất chấp kích cỡ của dữ liệu là bao nhiêu. Hash Table sử dụng mảng như là một kho lưu giữ trung gian và sử dụng kỹ thuật Hash để tạo chỉ mục tại nơi phần tử được chèn vào

##Tree trong lập trình tình nói chung

* Trong khoa học máy tính, cây là một cấu trúc dữ liệu được sử dụng rộng rãi gồm một tập hợp các nút (tiếng Anh: node) được liên kết với nhau theo quan hệ cha-con. Cây trong cấu trúc dữ liệu đầu tiên là mô phỏng (hay nói cách khác là sự sao chép) của cây (có gốc) trong lý thuyết đồ thị. Hầu như mọi khái niệm trong cây của lý thuyết đồ thị đều được thể hiện trong cấu trúc dữ liệu. Tuy nhiên cây trong cấu trúc dữ liệu đã tìm được ứng dụng phong phú và hiệu quả trong nhiều giải thuật. Khi phân tích các giải thuật trên cấu trúc dữ liệu cây, người ta vẫn thường vẽ ra các cây tương ứng trong lý thuyết đồ thị.


##Cây nhị phân trong lập trình nói chung

* Cây nhị phân là một cấu trúc dữ liệu đặc biệt được sử dụng cho mục đích lưu trữ dữ liệu. Một cây nhị phân có một điều kiện đặc biệt là mỗi nút có thể có tối đa hai nút con. Một cây nhị phân tận dụng lợi thế của hai kiểu cấu trúc dữ liệu: một mảng đã sắp thứ tự và một danh sách liên kết (Linked List), do đó việc tìm kiếm sẽ nhanh như trong mảng đã sắp thứ tự và các thao tác chèn và xóa cũng sẽ nhanh bằng trong Linked List.




