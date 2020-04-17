## Tìm hiểu về SlateJS
---
## SlateJS là gì

* Slate là một framework hoàn toàn tùy biến để xây dựng các trình soạn thảo văn bản phong phú.
Slate cho phép bạn xây dựng các trình soạn thảo trực quan, phong phú như các trình soạn thảo trong Medium, Dropbox Paper hoặc Google Docs, đang trở thành cổ phần bảng cho các ứng dụng trên web mà không cần codebase của bạn bị phức tạp.
Nó có thể làm điều này bởi vì tất cả logic của nó được triển khai với một loạt các plugin, vì vậy bạn không bao giờ bị hạn chế bởi những gì là hoặc không có trong "core". Bạn có thể nghĩ về nó giống như một triển khai có thể cắm được của nội dung có thể được xây dựng dựa trên React. Nó được lấy cảm hứng từ các thư viện như Draft.js, Prosemirror và Quill.

## Tại sao phải tạo ra SlateJS

* Trước khi tạo Slate, tôi đã thử rất nhiều thư viện văn bản phong phú khác ngoài đó, Draft.js, Prosemirror, Quill, v.v. Điều tôi nhận thấy là trong khi việc lấy các ví dụ đơn giản để làm việc là đủ dễ dàng, khi bạn bắt đầu thử xây dựng một cái gì đó như Medium, Dropbox Paper hoặc Google Docs, bạn gặp vấn đề sâu hơn ...

+ "Schema" của trình soạn thảo đã được mã hóa cứng và khó tùy chỉnh. Những thứ như in đậm và in nghiêng được hỗ trợ, nhưng còn ý kiến, hoặc nhúng, hoặc thậm chí nhiều nhu cầu cụ thể hơn về tên miền thì sao?

+ Chuyển đổi các tài liệu theo chương trình là rất phức tạp. Viết như một người dùng có thể đã làm việc, nhưng thực hiện các thay đổi theo chương trình, điều rất quan trọng để xây dựng các hành vi nâng cao, là không phức tạp.

+ Việc chuyển đổi sang HTML, Markdown, v.v ... dường như là một điều phải suy nghĩ lại. Những điều đơn giản như chuyển đổi một tài liệu sang HTML hoặc Markdown liên quan đến việc viết rất nhiều code, cho những trường hợp có vẻ như rất phổ biến và dễ dàng.

+ Sáng tạo lại view xem có vẻ không hiệu quả và hạn chế. Hầu hết các editors đều đưa ra quan điểm của riêng họ, thay vì sử dụng các công nghệ hiện có như React, vì vậy bạn phải học một hệ thống hoàn toàn mới với "gotchas" mới.

+ Xây dựng các tài liệu phức tạp, lồng nhau là không thể. Nhiều editors được thiết kế xung quanh các tài liệu "phẳng" đơn giản, làm cho những thứ như bảng, nhúng và chú thích trở nên khó lý luận và đôi khi không thể.

## Nguyên tắc vận hành

+ First-class plugins. Phần quan trọng nhất của Slate là các plugin là các thực thể hạng nhất. Điều đó có nghĩa là bạn hoàn toàn có thể tùy chỉnh trải nghiệm chỉnh sửa, để xây dựng các trình soạn thảo phức tạp như Medium hay Dropbox, mà không phải chiến đấu chống lại các giả định của thư viện.

+ Schema-less core. Logic cốt lõi của Slate giả định rất ít về lược đồ dữ liệu bạn sẽ chỉnh sửa, điều đó có nghĩa là không có giả định nào được đưa vào thư viện sẽ khiến bạn gặp khó khăn khi bạn cần vượt qua các trường hợp sử dụng cơ bản nhất.

+ Nested document model. Mô hình tài liệu được sử dụng cho Slate là một cây đệ quy lồng nhau, giống như chính DOM. Điều này có nghĩa là việc tạo các thành phần phức tạp như bảng hoặc trích dẫn khối lồng nhau là có thể cho các trường hợp sử dụng nâng cao. Nhưng thật dễ dàng để giữ cho nó đơn giản bằng cách chỉ sử dụng một cấp bậc duy nhất.

+ Song song với DOM. Mô hình dữ liệu của Slate dựa trên DOM ĐỔI tài liệu là một cây lồng nhau, nó sử dụng các lựa chọn và phạm vi và nó hiển thị tất cả các trình xử lý sự kiện tiêu chuẩn. Điều này có nghĩa là các hành vi nâng cao như bảng hoặc trích dẫn khối lồng nhau là có thể. Khá nhiều thứ bạn có thể làm trong DOM, bạn có thể làm trong Slate.

+ Lệnh trực quan. Tài liệu Slate được chỉnh sửa bằng "lệnh", được thiết kế ở mức độ cao và cực kỳ trực quan để viết và đọc, do đó chức năng tùy chỉnh càng biểu cảm càng tốt. Điều này làm tăng đáng kể khả năng suy luận về code của bạn.

+ Mô hình dữ liệu sẵn sàng hợp tác. Mô hình dữ liệu Slate sử dụng đặc biệt là cách các hoạt động được áp dụng cho tài liệu, đã được thiết kế để cho phép chỉnh sửa cộng tác được xếp chồng lên nhau, vì vậy bạn sẽ không cần phải suy nghĩ lại mọi thứ nếu bạn quyết định làm cho trình soạn thảo của mình hợp tác.

+ Xóa ranh giới "core". Với kiến ​​trúc đầu tiên là plugin và lõi không có lược đồ, nó trở nên rõ ràng hơn rất nhiều khi ranh giới nằm giữa "core" và "tùy chỉnh", điều đó có nghĩa là trải nghiệm core không bị sa lầy trong các trường hợp khác.

## Ví dụ

* [Plain text](https://www.slatejs.org/examples/plaintext) -  hiển thị trường hợp cơ bản nhất: một <textarea> được tạo điểm nhấn.

* [Rich text](https://www.slatejs.org/examples/richtext) - hiển thị các tính năng bạn mong đợi từ một trình soạn thảo cơ bản.

* [Markdown preview](https://www.slatejs.org/examples/markdown-preview) - chỉ ra cách thêm các trình xử lý chính cho các phím tắt giống như Markdown.

* [Links](https://www.slatejs.org/examples/links) - hiển thị cách bọc văn bản trong các Link với dữ liệu liên quan.

* [Images](https://www.slatejs.org/examples/images) - chỉ ra cách sử dụng các nút để thêm hình ảnh.

* [Hovering toolbar](https://www.slatejs.org/examples/hovering-toolbar) - cho thấy một menu theo ngữ cảnh có thể được thực hiện như thế nào.

* [Tables](https://www.slatejs.org/examples/tables) - chỉ ra cách lồng các hình khối để kết xuất các thành phần nâng cao hơn.

* [Paste HTML](https://www.slatejs.org/examples/paste-html) - chỉ ra cách sử dụng trình tuần tự HTML để xử lý HTML đã dán.

* [Mentions ](https://www.slatejs.org/examples/mentions) - chỉ ra cách sử dụng các nút để làm @ -mentions đơn giản.
