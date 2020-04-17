## Array
### Concat
* **Concat** là phương pháp được sử dụng để nối hai hoặc nhiều mảng.
* Cú pháp: *array1.concat(array2, array3, ..., arrayX)*
* Ví dụ: var array1 = ["Cecilie", "Lone"];
var array2 = ["Emil", "Tobias", "Linus"];
var array3= array1.concat(array2);
### Filter
* **filter()** tạo ra một mảng chứa đầy tất cả các phần tử mảng vượt qua một bài kiểm tra (được cung cấp dưới dạng hàm).
* Lưu ý:
    * .filter () không thực thi hàm cho các phần tử mảng không có giá trị.
    * .filter () không thay đổi mảng ban đầu.
* Cú pháp:  *array.filter(function(currentValue, index, arr), thisValue)*
* Ví dụ: var ages = [32, 33, 16, 40];

    function checkAdult(age) {
    return age >= 18;
    }

    function myFunction() {
  document.getElementById("demo").innerHTML = ages.filter(checkAdult);
}
### Fill
* **fill()** phương pháp lấp đầy những yếu tố nhất định trong một mảng với một giá trị tĩnh.
Bạn có thể chỉ định vị trí bắt đầu và kết thúc điền. Nếu không được chỉ định, tất cả các yếu tố sẽ được điền.
* Lưu ý: phương pháp này ghi đè lên mảng ban đầu.
* Cú pháp:  *array.fill(value, start, end)*
* Ví dụ: var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.fill("Kiwi");
### Reduce
* **Reduce()** phương pháp làm giảm mảng đến một giá trị duy nhất.
	Các phương pháp thực hiện một chức năng được cung cấp cho mỗi giá trị của mảng (từ trái sang phải). reduce()
Giá trị trả về của hàm được lưu trữ trong bộ tích lũy (kết quả / tổng).
* Lưu ý: 
    * Không thực thi hàm cho các phần tử mảng không có giá trị.
    * Phương pháp này không thay đổi mảng ban đầu.
* Cú pháp: *array.reduce(function(total, currentValue, currentIndex, arr), initialValue)*
* Ví dụ: var numbers = [175, 50, 25];

    document.getElementById("demo").innerHTML = numbers.reduce(myFunc);

    function myFunc(total, num) {
  return total - num;
}
### forEach
* **forEach()** phương pháp gọi một chức năng một lần cho mỗi phần tử trong một mảng, theo thứ tự
* Lưu ý: hàm không được thực thi cho các phần tử mảng không có giá trị.
* Cú pháp: *array.forEach(function(currentValue, index, arr), thisValue) *
* Ví dụ: var fruits = ["apple", "orange", "cherry"];
fruits.forEach(myFunction);

    function myFunction(item, index) {
  document.getElementById("demo").innerHTML += index + ":" + item + "<br>";
}
### Find
* **find()** phương thức trả về giá trị của phần tử đầu tiên trong một mảng mà vượt qua một bài kiểm tra (được cung cấp như một chức năng).
Phương thức find () thực thi hàm một lần cho mỗi phần tử có trong mảng:
    * Nếu nó tìm thấy một phần tử mảng trong đó hàm trả về một giá trị đúng , find () trả về giá trị của phần tử mảng đó (và không kiểm tra các giá trị còn lại)
    * Nếu không, nó trả về không xác định
* Lưu ý: 
    *  find () không thực thi hàm cho mảng trống.
    *  find () không thay đổi mảng ban đầu.
* Cú pháp: *array.find(function(currentValue, index, arr),thisValue)*
* Ví dụ: var ages = [3, 10, 18, 20];

    function checkAdult(age) {
  return age >= 18;
}

    function myFunction() {
  document.getElementById("demo").innerHTML = ages.find(checkAdult);
}
### indexOf
* **indexOf()**  tìm kiếm mảng cho mục được chỉ định và trả về vị trí của nó.
    * Tìm kiếm sẽ bắt đầu tại vị trí đã chỉ định hoặc ở đầu nếu không có vị trí bắt đầu nào được chỉ định và kết thúc tìm kiếm ở cuối mảng.
    * Trả về -1 nếu không tìm thấy mục.
    * Nếu mục có mặt nhiều lần, phương thức indexOf trả về vị trí xuất hiện đầu tiên.
* Lưu ý: Mục đầu tiên có vị trí 0, mục thứ hai có vị trí 1.
* Cú pháp: *array.indexOf(item, start)*
* Ví dụ: var fruits = ["Banana", "Orange", "Apple", "Mango"];
    var a = fruits.indexOf("Apple");
### slice
* **slice()** trả về các phần tử đã chọn trong một mảng, dưới dạng một đối tượng mảng mới.
chọn các phần tử bắt đầu tại đối số bắt đầu đã cho và kết thúc tại, nhưng không bao gồm , đối số kết thúc đã cho .
* Lưu ý: Mảng ban đầu sẽ không bị thay đổi
* Cú pháp: *array.slice(start, end)*
* Ví dụ: var fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
var citrus = fruits.slice(1, 3)
### valueOf
* **valueOf()** trả về mảng.Phương thức này là phương thức mặc định của đối tượng mảng. Mảng .valueOf () sẽ trả về giống như Mảng.
* Cú pháp: *array.valueOf()*
* Ví dụ: var fruits = ["Banana", "Orange", "Apple", "Mango"];
var v = fruits.valueOf();
### pop
* **pop()** loại bỏ phần tử cuối cùng của một mảng và trả về phần tử đó.
* Cú pháp: *array.pop()*
* Ví dụ: var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.pop();
### push
* **push()** thêm các mục mới vào cuối một mảng và trả về độ dài mới.
* Cú pháp: *array.push(item1, item2, ..., itemX)*
* Ví dụ: var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.push("Kiwi");
---
## Map
* map.set(key, value) lưu trữ giá trị bằng khóa.
* map.get(key) trả về giá trị theo khóa, undefined nếu key không tồn tại trên bản đồ.
* map.has(key) trả về true nếu key tồn tại, false nếu không.
* map.delete(key)loại bỏ giá trị bằng khóa.
* map.clear()  loại bỏ mọi thứ khỏi bản đồ.
* map.size trả về số phần tử hiện tại.
* map.keys()trả về một lần lặp cho các khóa,
* map.values() trả về một lần lặp cho các giá trị
* map.entries()trả về một lần lặp cho các mục [key, value], nó được sử dụng theo mặc định for..of   
---
## Tree
* Đặc điểm chính của cấu trúc cây là đệ quy Nói cách khác, một cây bao gồm các cây con, trong đó lần lượt bao gồm các cây con, đến lượt nó.Cuối cùng, ở dưới cùng, có những chiếc lá - và bây giờ chúng không có con cháu và không dẫn đến đâu cả.
* Một cây bao gồm các nút và các cạnh giữa chúng. Các xương sườn trong thực tế không tồn tại, chúng chỉ cần để hình dung kết nối và, nếu cần, để mô tả nó. Các nút được chia thành hai loại: nội bộ (những người có con cháu) và các nút lá (những người không có con cháu). Trong trường hợp của một hệ thống tệp, các nút lá được thể hiện bằng các tệp và các nút bên trong là các thư mục
* Trong cây, mỗi đỉnh có một cha mẹ. Ngoại lệ duy nhất là nút gốc - nó không có cha mẹ và cây bắt đầu với nó. Số lượng con cháu ở bất kỳ đỉnh nội bộ, nói chung, có thể là bất kỳ. Ngoài ra, cây làm nổi bật khái niệm độ sâu (độ sâu), xác định số lượng bước bạn cần đi dọc theo các đỉnh từ gốc để đạt được hiện tại (bước bạn đang nhìn). Các đỉnh ở cùng độ sâu với cha mẹ chung được gọi là anh em hoặc chị em. 











