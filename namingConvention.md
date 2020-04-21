# Chủ đề 2: Các quy ước đặt tên (naming convention)
    * Khái niệm naming convention (quy ước đặt tên): là một tập hợp các quy tắc để chọn chuỗi ký tự dùng cho các định danh biểu thị các biến, hàm, kiểu, và các thực thể khác trong mã nguồn và tài liệu.
    * Một số cách đặt tên thông dụng:
        + Cú pháp camelCase: ký tự đầu tiên của từ đầu tiên viết thường, ký tự đầu tiên của những chữ tiếp theo viết hoa. Vd: camelCase, getNumber,...
        + Cú pháp PascalCase: viết hoa chữ cái đầu của mỗi từ: PascalCase, ProductName,...
        + Cú pháp snake_case: tất cả các chữ cái đều viết thường, các chữ cách nhau bởi dấu gạch dưới. Vd: user_name, last_name,...
    * Một số nguyên tắc kèm theo:
        + Tên lớp thì đặt theo PascalCase
        + Tên biến, tên hàm đặt theo camelCase hoặc snake_case
        + Hằng số đặt theo UPPER_CASE, vd: CLICK_COUNTER
        + Tên biến, tên lớp thường là danh từ, cụm danh từ hoặc tính từ: UserModel, userName, downloadCounter, isDownloaded
        + Tên hàm thường bắt đầu bằng động từ: getUserName, setUserModel, increaseDownloadCounter
        + Tên thì phải có nghĩa, KHÔNG ĐƯỢC đặt tên kiểu viết tắt (dlCounter, uName, idl, a, a1, doFA)
        + Tránh đặt những tên quá chung chung, tối nghĩa: top, best, doIncrease, getAll
    * Bracket: có nhiều kiểu đặt bracket như K&R style, Allman style, GNU, Whitesmiths, Horstmann, Pico, Lisp,.... Nhưng K&R, Allman là 2 cách đặt thông dụng nhất.
    * Cách đặt bracket theo 2 kiểu:
        + K&R: mỗi hàm có dấu ngoặc mở ở dòng tiếp theo ở cùng mức thụt đầu dòng với tiêu đề của nó. Các câu lệnh trong dấu ngoặc nhọn được thụt vào và dấu ngoặc đóng nằm ở cùng mức thụt vào như tiêu đề của hàm tại một dòng riêng. Các khối bên trong một hàm, dấu ngoặc mở được đặt cùng dòng với câu lệnh điều khiển. Dấu ngoặc đóng vẫn nằm trong một dòng riêng, trừ khi được theo sau bởi 1 số từ khoá như else hoặc while.
        + Allman: mỗi hàm có dấu ngoặc mở ở dòng tiếp theo ở cùng mức thụt đầu dòng với tiêu đề của nó. Các câu lệnh trong dấu ngoặc nhọn được thụt vào và dấu ngoặc đóng nằm ở cùng mức thụt vào như tiêu đề của hàm tại một dòng riêng.
    * Lưu ý: Trong JavaScript nên để dấu mở ngoặc nhọn cùng dòng với câu lệnh điều khiển.
### Naming convention in JavaScript

    * Cách đặt tên trong javascript:
        + Biến và function thì nên đặt theo camelCase.
        + Class thì nên đặt theo kiểu Pascal.
        + Constant thì đặt theo kiểu UPPER_CASE.
    * Lưu ý khi đặt tên:
        + Tên phải thể hiện đầy đủ ý nghĩa và vai trò của nó:
        + Tránh dùng từ nhiều nghĩa, dùng những từ có ý nghĩa cụ thể.
        + Chỉ rõ hành vi thay vì ý định.
        + Chèn thêm những thông tin quan trọng vào tên.
        + Tên phải rõ ràng để tránh bị hiểu nhầm.
