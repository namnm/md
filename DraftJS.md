## Tìm hiểu về DraftJS
---
## DraftJS là gì

* DraftJS là một framework để xây dựng các trình soạn thảo văn bản phong phú trong React, được cung cấp bởi một mô hình bất biến và trừu tượng hóa về sự khác biệt giữa các trình duyệt.

* DraftJS cho phép bạn xây dựng bất kỳ loại nhập văn bản phong phú nào, cho dù bạn chỉ muốn hỗ trợ một vài kiểu văn bản nội tuyến hoặc xây dựng trình soạn thảo văn bản phức tạp để soạn các bài viết dạng dài.

* Draft.js đã được giới thiệu tại React.js Conf vào tháng 2 năm 2016

## Cài đặt DraftJS

`npm install draft-js react react-dom
# or alternately
yarn add draft-js react react-dom`

* Draft.js sử dụng một số tính năng ECMAScript hiện đại không có sẵn cho IE11. Nếu bạn gặp sự cố ngoài luồng, hãy thử cài đặt shim hoặc polyfill cùng với Draft.

`npm install draft-js react react-dom babel-polyfill
# or
yarn add draft-js react react-dom es6-shim`

## Các API hiện có

* Editor Component
* EditorChangeType
* EditorState
* ContentState
* ContentBlock
* CharacterMetadata
* Entity
* SelectionState
* CompositeDecorator
* Data Conversion
* RichUtils
* AtomicBlockUtils
* KeyBindingUtil
* Modifier
