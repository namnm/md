# Chủ đề 1: Cách sử dụng git

### Ý nghĩa, cách dùng các câu lệnh / tính năng:
  * init: tạo một kho lưu trữ Git trống hoặc khởi tạo lại kho lữu trữ hiện có.
    → Cách dùng: git init.
  * remote add: thêm remote repo.
    → Cách dùng: git remote add <remote-name> https://github.com/repo.git
  * remote set-url: thay đổi url.
    → Cách dùng: git set-url origin <new_url>
  * pull: lấy tất cả sự thay đổi trên 1 branch hiện tại về hợp nhất  nó với sự thay đổi hiện tại trên local.
    → Cách dùng: git pull
  * push: đẩy tất cả những thay đổi từ local lên trên server.
    → Cách dùng: git push origin <branch_name>
  * push -f (push --force): nó sẽ ghi đè lên remote repo bằng code ở local của mình, mà không cần quan tâm đến việc bên phía remote đang chứa thứ gì. Vì vậy rất dễ làm mất code mà các thành viên trước đó đã push.
    → Cách dùng: git push -f <branch_name>(không nên dùng). Thay vì dùng git push -f, chúng ta nên dùng git push --force-with-lease. Nó sẽ giúp ta đảm bảo không làm mất code trước đó.
  * push -u: hay push --set-upstream là lệnh để ta đẩy branch hiện tại ở local lên remote.
    → Cách dùng: git push --set-upstream <remote> <branch_name>.
  * fetch: cập nhật thông tin mới nhất từ git remote repo. Những thông tin mà nó cập nhật như: branch hoặc những thay đổi từ git remote repo mà ta chưa cập nhật về local repo.
    → Cách dùng: git fetch.
  * fetch --prune: dùng để xoá các branch không còn được sử dụng nữa.
    → Cách dùng: git fetch --prune <name>
  * branch: tạo thêm một branch mới.
    → Cách dùng: git branch <name>
  * branch -D: xóa một branch.
    → Cách dùng: git branch -D <branch_name>.
  * checkout: thoát khỏi branch hiện tại và di chuyển qua branch khác.
    → Cách dùng: git checkout <branch_name>
  * checkout -b: tạo một branch mới và chuyển sang branch này.
    → Cách dùng: git branch -b <branch_name>.
  * stash: Lưu lại tất cả thay đổi mà bạn chưa commit, thường được dùng khi muốn đổi sang một branch khác mà đang làm dở branch hiện tại.
    → Cách dùng: git stash.
  * stash pop: Xóa các thay đổi không cần thiết.
    → Cách dùng: git stash pop stash@{1}.
  * add: thêm những file mà bạn đã thay đổi từ local lên trên server.
    → Cách dùng: git add <name_file>
  * add . :  đẩy tất cả những thay đổi từ local lên trên server.
    → Cách dùng: git add.
  * add -A: cập nhật ở tất cả các index khác.
    → Cách dùng: git add -A
  - commit: Ghi lại các thay đổi vào kho lưu trữ.
    → Cách dùng: git commit
  * commit -m: Chú thích những gì bạn vừa mới add lên trên server.
 	→ Cách dùng: git commit -m “comment”.
  * commit -am: thay đổi nội dung lần commit gần nhất.
    → Cách dùng: git commit --amend.
  * reset: hoàn tác lại commit chưa push.
    → Cách dùng: git reset ...
  * reset HEAD~: hoàn tác lại commit gần nhất, vẫn giữ thay đổi ở index.
    → Cách dùng: git reset HEAD~.
  * merge: hợp nhất branch hiện tại vào một branch nào đó mà bạn muốn.
    → Cách dùng: git merge <branch_merge>.
  * rebase: giống với merge. Ví dụ: muốn merge branch A vào branch B. Khi dùng rebase thì nó sẽ đưa toàn bộ branch A lên trên branch B làm thay đổi lịch sử commit.
  * How to resolve conflict correctly?
    * Có 2 cách để resolve conflict:
        1. Cách thứ nhất là dùng git rebase:
            - Trường hợp sử dụng git rebase: Khi chúng ta có branch và thay đổi trên cả 2 branch đều trên cùng 1 file và cùng 1 dòng.
            - Thứ tự thực hiện:
                + git rebase
                + resolve conflict
                + Sau khi git rebase sẽ xảy ra một số conflict, việc của chúng ta là mở những file đó và kiểm tra xem những xung đột đó là gì và chỉnh sửa.
                + Sau khi chỉnh sửa các và giải quyết thì sử dụng git add <Tên file> để add file conflict đã giải quyết. Hoặc git add . để add tất cả.
                + Sau đó sử dụng git rebase --continue để tiếp tục rebase
                + Chúng ta có thể sử dụng git rebase --abort để ngừng việc rebase.
                + git push with -f. [Hạn chế sử dụng -f vì việc này sẽ gây ảnh hưởng tới lịch sử commit, nếu trong trường hợp branch chỉ có một mình sử dụng thì không sao, nhưng trong trường hợp như branch master hoặc branch mà nhiều người xài chung thì nên hạn chế, hoặc không nên xài]. -f tương ứng --force
        2. Cách thứ hai là dùng git merge:
            - Trường hợp sử dụng git merge:
            - Khi chúng ta có 2 branch A và B. Branch A delete một file X và branch B không xoá file X mà modified trên file X.
            - Thứ tự thực hiện:
                + git merge
                + resolve conflict
                + commit and push
*****
### Lỗi trong quá trình thực hiện:
    + Lỗi 1: Resolve conflict sai
        + Chưa biết cách sử dụng sourcetree.
        + Khi kiểm tra commit trên sourcetree chưa được cẩn thận. Nên khi resolve conflict bị thiếu code và không đúng với commit trước khi rebase. → Cần cẩn thận hơn để tránh sau khi conflict thì code không chạy, làm tốn thời gian conflict lại.
        + Sau khi resolve conflict xong thì chưa chỉnh sửa code ngăn nắp, các dấu ngoặc và thứ tự tab căn lề vẫn chưa đúng. → Cần code ngăn nắp hơn, tạo cảm giác dễ chịu cho mọi người khi làm việc với code của mình.
    + Lỗi 2: Chưa làm đúng trình tự hướng dẫn
        + Khi tạo new repo thì có dư thêm nhiều commit không liên quan.[Do tạo không đúng cách yêu cầu]
    + Lỗi 3: Khi research thì tìm hiểu rất nhiều, lý thuyết tốt, nhưng chưa biết cách áp dụng → cần áp dụng những gì đã tìm được khi research vào bài tập, thực hành nhiều với những kiến thức đó
        Ví dụ: lệnh fork push được viết tắt là git push -f
