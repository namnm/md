# Tìm hiểu về cấu trúc dữ liệu cây

## Cấu trúc dữ liệu cây là gì

  * Trong khoa học máy tính, cây là một cấu trúc dữ liệu được sử dụng rộng rãi gồm một tập hợp các nút (tiếng Anh: node) được liên kết với nhau theo quan hệ cha-con. Cây trong cấu trúc dữ liệu đầu tiên là mô phỏng (hay nói cách khác là sự sao chép) của cây (có gốc) trong lý thuyết đồ thị. Hầu như mọi khái niệm trong cây của lý thuyết đồ thị đều được thể hiện trong cấu trúc dữ liệu. Tuy nhiên cây trong cấu trúc dữ liệu đã tìm được ứng dụng phong phú và hiệu quả trong nhiều giải thuật. Khi phân tích các giải thuật trên cấu trúc dữ liệu cây, người ta vẫn thường vẽ ra các cây tương ứng trong lý thuyết đồ thị.

  * Các nút trong cây: Một nút có thể chứa một giá trị, một điều kiện, một cấu trúc dữ liệu riêng biệt hoặc chính một cây. Mỗi nút trong một cây có thể không có hoặc có một số nút con, các nút con có mức cao hơn nó (theo quy ước khác với cây tự nhiên, cây trong cấu trúc dữ liệu phát triển từ trên xuống). Một nút có con được gọi là nút cha của các nút con. Một nút có nhiều nhất một nút cha.
    1. Nút gốc: Trong mỗi cây có một nút đặc biệt được gọi là nút gốc (hay nói đơn giản là gốc). Nút gốc là nút duy nhất không có nút cha. Nút gốc là nơi khởi đầu của nhiều giải thuật trên cây. Tất cả các nút khác được nối về nút gốc bằng một đường đi qua các cạnh hay các liên kết

    2. Các nút lá: Các nút không có nút con được gọi là nút lá hay gọi đơn giản là lá.

    3. Các nút trong (nút nhánh): Nút trong của một cây là nút trên cây có ít nhất một con, nghĩa là các nút không phải là lá. Các khái niệm về mức của mỗi nút, chiều cao của cây được định nghĩa giống như cây trong lý thuyết đồ thị.

  * Cây con: Một cây con là một bộ phận của cấu trúc dữ liệu cây mà tự nó cũng là một cây. Một nút bất kỳ trong cây T, cùng với các nút dưới nó tạo thành một cây con của T.

  * Cây trong lý thuyết đồ thị: Trong lý thuyết đồ thị, một cây là một đồ thị liên thông và không có chu trình. Cây như vậy còn được gọi là cây tự do. Một cây có gốc là một cây tư do, trong đó có một đỉnh được chọn làm gốc và các cạnh được định hướng là hướng của các đường đi đơn ra khỏi gốc tới các đỉnh khác. Trong trường hợp này, hai đỉnh bất kỳ được nối với nhau bao hàm ‎ chúng có qua hệ cha-con. Một đồ thị không chu trình với nhiều thành phần liên thông được gọi là một rừng.

  * Cây sắp thứ tự: Có hai dạng cấu trúc cơ sở của cây là cây không thứ tự và cây có thứ tự. Một cây không thứ tự là cây có cấu trúc cây, trong đó giữa các con của một nút, không có thứ tự nào. Một cây, trong đó các con của một nút tuân theo một thứ tự xác định được gọi là cây có thứ tự. Các cây có thứ tự có nhiều ứng dụng sâu sắc trong cấu trúc của cây. Cây tìm kiếm nhị phân là một cây sắp thứ tự điển hình.

## Cây nhị phân (Binary tree)

  * Cây tìm kiếm ứng với n khóa k1, k2, ... kN là cây nhị phân mà mỗi nút đều được gán một khóa sao cho với mỗi mỗi nút k:

    Mọi khóa trên cây con trái đều nhỏ hơn khóa trên nút k
    Mọi khóa trên cây con phải đều lớn hơn khóa trên nút k

    Cây tìm kiếm nhị phân là một cấu trúc dữ liệu cơ bản được sử dụng để xây dựng các cấu trúc dữ liệu trừu tượng hơn như các tập hợp, đa tập hợp, các dãy kết hợp.

    Nếu một BST có chứa các giá trị giống nhau thì nó biểu diễn một đa tập hợp. Cây loại này sử dụng các bất đẳng thức không nghiêm ngặt. Mọi nút trong cây con trái có khóa nhỏ hơn khóa của nút cha, mọi nút trên cây con phải có nút lớn hơn hoặc bằng khóa của nút cha.

    Nếu một BST không chứa các giá trị giống nhau thì nó biểu diễn một tập hợp đơn trị như trong lý thuyết tập hợp. Cây loại này sử dụng các bất đẳng thức nghiêm ngặt. Mọi nút trong cây con trái có khóa nhỏ hơn khóa của nút cha, mọi nút trên cây con phải có khóa lớn hơn khóa của nút cha.

    Việc chọn đưa các giá trị bằng nhau vào cây con phải (hay trái) là tùy theo mỗi người. Một số người cũng đưa các giá trị bằng nhau vào cả hai phía, nhưng khi đó việc tìm kiếm trở nên phức tạp hơn.

  * Các khái niệm cơ bản về cây nhị phân:

    1. Đường: là một dãy các nút cùng với các cạnh của một cây.

    2. Nút gốc (Root): nút trên cùng của cây được gọi là nút gốc. Một cây sẽ chỉ có một nút gốc và một đường xuất phát từ nút gốc tới bất kỳ nút nào khác. Nút gốc là nút duy nhất không có bất kỳ nút cha nào.

    3. Nút cha: bất kỳ nút nào ngoại trừ nút gốc mà có một cạnh hướng lên một nút khác thì được gọi là nút cha.

    4. Nút con: nút ở dưới một nút đã cho được kết nối bởi cạnh dưới của nó được gọi là nút con của nút đó.

    5. Nút lá: nút mà không có bất kỳ nút con nào thì được gọi là nút lá.

    6. Cây con: cây con biểu diễn các con của một nút.

    7. Truy cập: kiểm tra giá trị của một nút khi điều khiển là đang trên một nút đó.

    8. Duyệt: duyệt qua các nút theo một thứ tự nào đó.

    9. Bậc: bậc của một nút biểu diễn số con của một nút. Nếu nút gốc có bậc là 0, thì nút con tiếp theo sẽ có bậc là 1, và nút cháu của nó sẽ có bậc là 2, …

    10. Khóa (Key): biểu diễn một giá trị của một nút dựa trên những gì mà một thao tác tìm kiếm thực hiện trên nút.

  * Các phép toán trên BST
    1. Tìm kiếm (Searching): Việc tìm một khóa trên BST có thể thực hiện nhờ đệ quy. Chúng ta bắt đầu từ gốc. Nếu khóa cần tìm bằng khóa của gốc thì khóa đó trên cây, nếu khóa cần tìm nhỏ hơn khoa ở gốc, ta phải tìm nó trên cây con trái, nếu khóa cần tìm lớn hơn khóa ở gốc, ta phải tìm nó trên cây con phải. Nếu cây con (trái hoặc phải) là rỗng thì khóa cần tìm không có trên cây.

    2. Chèn (Insertion): Phép chèn bắt đầu giống như phép tìm kiếm; Nếu khóa của gốc khác khóa cần chèn ta tìm nó trong cây con trái hoặc phải. Nếu cây con trái hoặc phải tương ứng là rỗng (không tìm thấy) thì thêm một nút và gán cho nút ấy khóa cần chèn.

    3. Xóa (Deletion):
    Xóa một lá: Vì lá không có con nên chỉ cần giải phóng nó khỏi cây
    Xóa nút có một con: Xóa và thay thế nó bằng con duy nhất của nó.
    Xóa một nút có hai con: Xóa nút đó và thay thế nó bằng nút có khóa lớn nhất trong các khóa nhỏ hơn khóa của nó (được gọi là "nút tiền nhiệm" -nút cực phải của cây con trái) hoặc nút có khóa nhỏ nhất trong các khóa lớn hơn nó (được gọi là "nút kế vị" - nút cực trái của cây con phải)

    4. Phép duyệt: Khi một cây tìm kiếm nhị phân được tạo ra, tất cả các nút có thể được duyệt theo thứ tự giữa nhờ duyệt đệ quy cây con bên trái, in nút đang duyệt, rồi duyệt đệ quy cây con bên phải, tiếp tục làm như vây với mỗi nút của cây trong quá trình đệ quy. Với mọi cây nhị phân, cây có thể được duyệt theo thứ tự trước() hoặc theo thứ tự sau(), cả hai cách đều hữu dụng với cây tìm kiếm nhị phân.

    5. Sắp xếp: Một cây tìm kiếm nhị phân có thể được sử dụng như một giải thuật sắp xếp đơn giản nhưng hiểu quả. Giống như heapsort, chúng ta chèn tất cả các giá trị chúng ta muốn sắp xếp vào một cây tìm kiếm nhị phân và in ra kết quả theo thứ tự.

## Cây đỏ đen (Red-black tree)

  * Là một dạng cây tìm kiếm nhị phân tự cân bằng, một cấu trúc dữ liệu được sử dụng trong khoa học máy tính. Cấu trúc ban đầu của nó được đưa ra vào năm 1972 bởi Rudolf Bayer. Ông gọi chúng là các "B-cây cân bằng" còn tên hiện nay được đưa ra từ 1978 bởi Leo J. Guibas và Robert Sedgewick. Nó là cấu trúc phức tạp nhưng cho kết quả tốt về thời gian trong trường hợp xấu nhất. Các phép toán trên chúng như tìm kiếm (search), chèn (insert), và xóa (delete) trong thời gian O (log n), trong đó n là số các phần tử của cây.

  Một cây đỏ-đen là một cây nhị phân, là một cấu trúc dữ liệu trong khoa học máy tính để tổ chức các thành phần dữ liệu có thể so sánh, chẳng hạn các số. Trong cây nhị phân các thành phần dữ liệu được đưa vào các nút (node). Trong các nút có một nút nằm ở vị trí khởi đầu không là con của nút nào được gọi là gốc. Các nút khác đều là con của một nút nào đó và có không quá hai con. Từ nút gốc có một đường đi duy nhất đến mỗi nút khác trên cây.

  Các nút không có con được gọi là lá (leaf node). Trong cây đỏ đen, các lá được gán giả là null; nghĩa là chúng không chứa bất kỳ dữ liệu nào.

  Các cây tìm kiếm nhị phân, bao gồm cả cây đỏ-đen, thỏa mãn tính chất: mỗi nút được gán một giá trị sao cho giá trị trên mỗi nút nhỏ hơn hoặc bằng tất cả các giá trị trên các nút thuộc cây con phải và lớn hơn các giá trị nằm trên cây con trái. Điều đó làm cho quá trình tìm kiếm nhanh hơn.

  * Các tính chất của cây đỏ đen:
    * Mỗi nút của cây đỏ-đen có thuộc tinh "màu" nhận một trong hai giá trị "đỏ" hoặc "đen". Ngoài ra:
      1. Một nút hoặc là đỏ hoặc đen.
      2. Gốc là đen.
      3. Cả hai con của mọi nút đỏ là đen. (và suy ra mọi nút đỏ có nút cha là đen.).
      4. Tất cả các đường đi từ một nút đã cho tới các lá chứa một số như nhau các nút đen.

  * Tính chất 4 còn được gọi là tính chất "cân bằng đen". Số các nút đen trên một đường đi từ gôc tới mỗi lá được gọi là độ dài đen của đường đi đó. Trong bài này chỉ xét các đường đi từ gốc tới các lá nên ta sẽ gọi tắt các đường đi như vậy là đường đi. Sức mạnh của cây đỏ đen nằm trong các tính chất trên. Từ các tính chất này suy ra trong các đường đi từ gốc tới các lá đường đi dài nhất không vượt quá hai lần đường đi ngắn nhất. Do đó cây đỏ đen là gần cân bằng. Vì các thuật toán chèn, xóa, tìm kiếm trong trường hợp xấu nhất đều tỷ lệ với chiều cao của cây nên cây đỏ đen rất hiệu quả trong các trường hợp xấu nhất,không giống như cây tìm kiếm nhị phân thông thường.

  * Để thấy rõ sức mạnh này, ta chú ý rằng không có đường đi nào từ gôc tới một lá chứa hai nút đỏ liền nhau (theo tính chất 4). Do đó trên mỗi đường số nút đỏ không nhiều hơn số nút đen. Đường đi ngắn nhất là đường đi chỉ có nút đen, đường đi dài nhất có thể là đường đi xen kẽ giữa các nút đỏ và đen. Theo tính chất 5, số các nút đen trên hai đường đi đó bằng nhau, và do đó đường đi dài nhất không vượt quá hai lần đường đi ngắn nhất.

  * Trong nhiều biểu diễn của dữ liệu cây, có thể có các nút chỉ có một con và có các lá có chứa dữ liệu. Tuy nhiên có thể biểu diễn cây đỏ đen ta có một chút thay đổi mà không làm thay đổi tính chất cơ bản của cây và độ phức tạp của các thuật toán. Với mục đích này, ta đưa thêm các lá null vào làm con phải hoặc con trái hoặc cả hai của những nút không có chúng, các lá này không chứa dữ liệu mà chỉ làm nhiệm vụ thông báo rằng tại đây cây đã kết thúc, như hình vẽ ở trên. Việc thêm các nút này làm cho tất cả các nút trong của cây đều chứa dữ liệu và có hai con, hay khác đi cây đỏ đen cùng với các lá null là cây nhị phân đầy dủ. Khi đó số các "lá null" nhiều hơn số các nút chứa dữ liệu của cây một lá.

  * Một số người định nghĩa cây đỏ đen bằng cách gán màu đỏ đen cho các cạnh chứ không phải các nút. Tuy nhiên điều đó không tạo nên sự khác biệt. Khi ấy màu của mỗi nút tương ứng với màu của cạnh nối nó với nút cha.

  * Các phép toán trên cây đỏ đen
    * Có thể áp dụng ngay các phép chèn, xóa trong cây tìm kiếm nhị phân vào cây đỏ đen mà không cần sửa chữa gì vì cây đỏ đen là trường hợp riêng của cây tìm kiếm nhị phân. Tuy nhiên, khi đó có thể có một số tính chất trong định nghĩa của cây đỏ đen sẽ bị vi phạm. Việc khôi phục các tính chất đỏ đen sẽ cần một số nhỏ cỡ O(log n) hoặc trung bình chỉ O(1) các phép đổi màu (tốn rất ít thời gian) và không quá ba phép quay cho phép xóa, hai cho phép chèn. Toàn bộ các giải thuật chèn và xóa có độ phức tạp thời gian cỡ O(log n).

    1. Phép chèn
      - Phép chèn bắt đầu bằng việc bổ sung một nút như trong cây tìm kiếm nhị phân bình thường và gán cho nó màu đỏ. Ta xem xét để bảo toàn tính chất đỏ đen từ các nút lân cận với nút mới bổ sung. Thuật ngữ nút chú bác sẽ dùng để chỉ nút anh (hoặc em) với nút cha của nút đó như trong cây phả hệ. Chú ý rằng:

      - Tính chất 3 (Tất cả các lá -là các nút null là đen) giữ nguyên.

      - Tính chất 4 (Cả hai con của nút đỏ là đen) nếu bị thay đổi chỉ bởi việc thêm một nút đỏ có thể sửa bằng cách gán màu đen cho một nút đỏ hoặc một phép quay.

      - Tính chất 5 (Tất cả các đường đi từ gôc tới các lá có cùng một số nút đen) nếu bị thay đổi chỉ bởi việc thêm một nút đỏ có thể sửa bằng cách gán màu đen cho một nút đỏ hoặc một phép quay.

    2. Phép xoá
      - Trong cây tìm kiếm nhị phân bình thường khi xóa một nút có cả hai con (không là lá null), ta tìm phần tử lớn nhất trong cây con trái hoặc phần tử nhỏ nhất trong cây con phải, chuyển giá trị của nó vào nút đang muốn xóa (xem Cây tìm kiếm nhị phân). Khi đó chúng ta xóa đi nút đã được copy giá trị, nút này có ít hơn hai con (không là lá null). Vì việc copy giá trị không làm mất tính chất đỏ đen nên không cần phải sửa chữa gì cho thao tác này. Việc này chỉ đặt ra khi xóa các nút có nhiều nhất một con (không là lá null)

      - Nếu ta xóa một nút đỏ, ta có thể chắc chắn rằng con của nó là nút đen. Tất cả các đường đi đi qua nút bị xóa chỉ đơn giản bớt đi một nút đỏ do đó tính chất 5 không thay đổi. Ngoài ra, cả nút cha và nút con của nút bị xóa đều là nút đen, do đó tính chất 3 và 4 vẫn giữa nguyên.. Một trường hợp đơn giản khác là khi xóa một nút đen chỉ có một con là nút đỏ. Khi xóa nút đó các tính chất 4 và 5 bị phá vỡ, nhưng nếu gán lại màu cho nút con là đen thì chúng lại được khôi phục.

## Cây AVL

  * Một cây AVL là một cây tìm kiếm nhị phân tự cân bằng, và là cấu trúc dữ liệu đầu tiên có khả năng này. Trong một cây AVL, tại mỗi nút chiều cao của hai cây con sai khác nhau không quá một. Hiệu quả là các phép chèn (insertion), và xóa (deletion) luôn chỉ tốn thời gian O(log n) trong cả trường hợp trung bình và trường hợp xấu nhất. Phép bổ sung và loại bỏ có thể cần đến việc tái cân bằng bằng một hoặc nhiều phép quay.

  * Cây AVL là cây nhị phân tìm kiếm mà sự khác biệt về chiều cao giữa cây con trái và cây con bên phải không vượt quá 1. Các thao tác cơ bản với cây AVL là thêm node hoặc xóa node khỏi cây cũng giống với cây nhị phân tìm kiếm, chỉ có sự khác biệt là ta cần duy trì sự cân bằng của cây (sự khác biệt về chiều cao giữa cây con bên trái và cây con bên phải của các node không được vượt quá 1).

  * Ưu điểm của cây AVL: Hiệu năng tìm kiếm luôn được đảm bảo kể cả trong trường hợp xấu nhất (bằng O(logN)).

  * Nhược điểm: Khi chèn phần tử hoặc xóa phần tử khỏi cây thì cần thêm một thao tác đó là giữ cho cây cân bằng.

  * Hệ số cân bằng (Balance Factor)

    * Gọi B là giá trị của ( chiều cao của cây con bên trái - chiều cao của cây con bên phải)

    * Để duy trì sự khác biệt về chiều cao giữa cây con trài và cây con phải ở mỗi node nhỏ hơn hoặc bằng 1, mỗi node sẽ được lưu một giá trị B. Giá trị này được gọi là hệ số cân bằng, những node có trị tuyệt đối của hệ số cân bằng vượt quá 1 thì cần được điều chỉnh lại.

    * Hệ số cân bằng của các node ở mức cuối cùng (node lá) luôn luôn bằng không.

  * Các phép quay AVL

  * Khi có một yếu tố gây ra sự mất cân bằng của cây, AVL sẽ thực hiện quá trình tự điều chỉnh để lấy lại sự cân bằng bởi các phép quay, bao gồm:

    * Quay trái

    * Quay phải

    * Quay trái - phải

    * Quay phải - trái

  * Phép quay trái

    * Trong trường hợp cây ở trạng thái không cân bằng khi một node được chèn vào làm con phải của một cây có một node gốc và một node con phải. Lúc này ta phải thực hiện phép quay trái để đưa cây trở lại trạng thái cân bằng.

  * Phép quay phải

    * Trong trường hợp cây ở trạng thái không cân bằng khi một node được chèn vào làm con trái của một cây có một node gốc và một node con trái. Lúc này ta phải thực hiện phép quay phải để đưa cây trở lại trạng thái cân bằng

  * Phép quay trái - phải

    * Phép quay kết hợp có đôi chút phức tạp hơn so với các phép quay trái và quay phải ở trên. Với phép quay trái-phải, ta sẽ thực hiện việc quay trái trước và quay phải sau đó.

  * Phép quay phải-trái

    * Phép quay này là kết hợp của phép quay phải và theo sau bởi một phép quay trái.

  * Chèn phần tử vào cây AVL

##  Cây splay

  * Cây splay là một cây tìm kiếm nhị phân tự cân bằng. Nó có thực hiện các thao tác cơ bản như chèn, tìm, và xóa trong thời gian trừ dần O(log n). Với nhiều dãy thao tác không ngẫu nhiên, cây splay chạy nhanh hơn các loại cây tìm kiếm nhị phân khác ngay cả khi dãy thao tác không được biết trước. Cây splay được Daniel Dominic Sleator và Robert Endre Tarjan phát minh năm 1985.

  * Mọi thao tác trên cây đều dựa trên một thao tác cơ bản gọi là splay (mở rộng). Khi thực hiện thao tác splay trên một nút của cây, cây được sắp xếp lại sao cho nút đó nằm ở gốc của cây. Một cách để thực hiện thao tác đó là trước hết tìm kiếm nút trên cây như cây nhị phân thông thường rồi thực hiện một chuỗi các phép quay cây theo một cách nhất định để đưa nút đó lên gốc. Thay vào đó, cũng có thể dùng một thuật toán từ trên xuống dưới kết hợp tìm kiếm và quay ngay trong quá trình tìm.

  * Ưu điểm

    * Việc cây splay thực hiện nhanh chóng các thao tác là dựa trên tính tự tối ưu hóa của cây theo đó các nút hay được truy cập được di chuyển lại gần với gốc. Chiều cao xấu nhất là O(n) nhưng điều này rất hiếm khi xảy ra, và chiều cao trung bình là O(log n). Việc các nút hay sử dụng nằm ở gần gốc của cây là một ưu điểm lớn cho nhiều ứng dụng thực tế như các thuật toán cho bộ nhớ đệm và dọn rác.

    * Các ưu điểm bao gồm:

      1. Lập trình đơn giản hơn nhiều loại cây nhị phân cân bằng khác như cây đỏ đen và cây AVL.
      2. Tốc độ trung bình ngang với các cây khác.[cần dẫn nguồn]
      3. Tốn ít bộ nhớ do không phải lưu trữ thêm thông tin để cân bằng cây.

  * Nhược điểm

    * Một nhược điểm của cây splay là chiều cao của cây có thể là tuyến tính. Chẳng hạn, trường hợp này xảy ra khi truy cập lần lượt n phần tử của cây theo thứ tự tăng dần. Do chiều cao tương ứng với thời gian tìm kiếm, thời gian tìm kiếm trong trường hợp xấu nhất cũng là tuyến tính. Tuy nhiên cũng cần ghi chú là chi phí trừ dần trong trường hợp xấu nhất là O(log n).

    * Cây splay thay đổi cấu trúc rất nhiều ngay cả khi thực hiện thao tác tìm kiếm (trong khi chẳng hạn, cây đỏ đen không thực hiện thay đổi nào khi tìm kiếm). Điều này khiến việc sử dụng cây splay trong môi trường đa luồng rất phức tạp và kém hiệu quả hơn các cây khác.

  * Các thao tác

    * Khi truy cập một nút x, ta thực hiện thao tác splay trên nút x để chuyển nó về vị trí gốc. Thao tác splay bao gồm nhiều bước splay, mỗi bước di chuyển x về gần gốc hơn. Việc luôn luôn thực hiện splay trên nút vừa được truy cập khiến các nút mới truy cập nằm gần gốc và cây luôn giữ hình dạng gần cân bằng.

    * Mỗi bước splay phụ thuộc vào ba yếu tố:
      1. x là nút con trái hay phải của cha nó là p,
      2. p có là nút gốc hay không
      3. p là nút con trái hay phải của cha nó là g.

    * Sau mỗi bước splay nút cha của g là gg phải cập nhật để trỏ tới x. Nếu gg không tồn tại thì x là nút gốc mới.

    * Mỗi bước splay thuộc một trong ba kiểu sau:

    * Bước zig: Thực hiện bước này nếu p là gốc. Cây được quay trên cạnh nối x và p. Chỉ cần thực hiện phép zig khi x ở độ sâu lẻ khi thao tác splay bắt đầu.

    * Bước zig-zig: Thực hiện bước này khi p không là gốc và x và p đều là nút con trái hoặc đều là nút con phải. Ảnh dưới là cho trường hợp x và p đều là nút con trái (trường hợp kia hoàn toàn đối xứng). Cây quay trên cạnh nối p và cha nó là g, sau đó quay trên cạnh nối x và p. Ghi chú đây là bước duy nhất khác với phương pháp quay về gốc của Allen và Munro[2] đã được tìm ra trước cây splay.

    * Bước zig-zag: Thực hiện bước này khi p không là gốc và x là nút con phải và p là nút con trái hoặc ngược lại. Cây quay trên cạnh nối x và p, rồi quay trên cạnh nối x và nút cha mới là g.

    * Chèn
      * Để chèn x vào cây:
        1. Đầu tiên chèn như cây tìm kiếm nhị phân thông thường.
        2. Thực hiện thao tác splay trên x để đưa nó về gốc.

    * Xóa
      * Để xóa x, ta dùng phương pháp như cho cây nhị phân thông thường: nếu x có hai con, đổi chỗ x và nút phải nhất của cây con trái của x hoặc nút trái nhất của cây con phải của x. Sau đó xóa nút x ở vị trí mới. Bằng phương pháp này, ta luôn đưa về trường hợp xóa nút với 0 hoặc 1 nút con.

      * Không như cây nhị phân thông thường, sau khi xóa xong, ta thực hiện thao tác splay trên nút cha của nút mới được xóa.










