> ## **_Synopsis_**

- 將當前的 HEAD 重置(reset)到指定狀態

```
git reset [-q] [<tree-ish>] [--] <pathspec>…​
git reset [-q] [--pathspec-from-file=<file> [--pathspec-file-nul]] [<tree-ish>]
git reset (--patch | -p) [<tree-ish>] [--] [<pathspec>…​]
git reset [--soft | --mixed [-N] | --hard | --merge | --keep] [-q] [<commit>]
```

> ## **_Common Command_**

### `git reset [<mode>] [<commit>]`

選用不同的 mode 參數，會決定如何處理：

1. 當前工作目錄及暫存區的檔案
2. commit 拆出來的檔案會丟回工作目錄

- `--mixed`

  - 預設的模式。沒有特別加參數的情況下，會使用 --mixed 模式。
  - 會把 index file 丟掉
  - 會保留 working tree 的檔案
  - commit 拆出來的檔案會留在 working tree

- `--soft`

  - 在不改變 index file 和 working tree 的狀況下，將 HEAD reset 到某 commit 點。
  - commit 拆出來的檔案會被丟回 index。

- `--hard`

  - index file 或 working tree 的檔案都會被刪除。
  - commit 拆出來得檔案會直接被丟掉。

> ## **_備註_**
>
> 參考資料: [為你自己學 git - 剛剛的 commit 後悔了，想要拆掉重做... ](https://gitbook.tw/chapters/using-git/reset-commit)

- \*註: **commit 「拆」出來的檔案**
  只是一種形容，並不會完全把 commit 紀錄刪掉，而是指當前 commit 點跟 reset commit 點的內容差異，還是可以由其他方法找到 commit。

- \*註: 名詞說明
  - Working Tree > Working Directory
  - index file > Staging Directory
