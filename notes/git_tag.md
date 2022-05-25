## intro

### 什麼是**標籤**？

標籤會指向某一個 commit，標籤的名字不可以重複，可以說是 git 版控這本書的索引便利貼，能幫助你快速找到對應的 commit 點。

通常會拿來標示軟體開發的特定的里程碑，例如軟體版號(1.0.0)或是 beta-release。

## Synopsis

- 列出 git 中所有的標籤

  ```git
  git tag
  ```

- 建立標籤

  1. 建立輕量標籤(lightweight tag)

  ```git
  git tag  <tagname> <commit>
  ```

  2. 建立附註標籤(annotated tag)

  ```git
  git tag -a -m <msg> <tagname> <commit>
  ```

- 刪除標籤

  ```git
  git tag -d <tagname>
  ```

- 顯示標籤含該 commit 資訊
  ```git
  git show <tagname>
  ```

## Options

- `-f`

  - 一般建立新標籤時，不可以有相同名稱的標籤存在，除非使用 --force option

- `-a`, `--annotate`

  - Make an unsigned, annotated tag object
  - 建立有附註的標籤
  - 要搭配 `-m <msg>` 一起使用

- `-l`, `--list`
  - 可以搭配 `<pattern>`，搜尋指定內容標籤
  - 範例：
    ```
    $ git tag -l "v1.8.5*"
      v1.8.5
      v1.8.5-rc0
      v1.8.5-rc1
      v1.8.5-rc2
      v1.8.5-rc3
      v1.8.5.1
      v1.8.5.2
      v1.8.5.3
      v1.8.5.4
      v1.8.5.5
    ```

## 標量標籤 v.s 附註標籤

在叫出 tag 時(`git show <tagname>`)，顯示的資訊量不同，兩者都會有該 commit 點的資訊，附註標籤會多包含 tag 的資訊，包括：tagger 和 date。

## 其他

`git push` 指令預設不會傳送標籤到遠端 repo，如果要把標籤推上遠端需要加上其他參數，請參考[git book](https://git-scm.com/book/zh-tw/v2/Git-%E5%9F%BA%E7%A4%8E-%E6%A8%99%E7%B1%A4)
