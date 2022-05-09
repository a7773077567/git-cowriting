> ## **_Synopsis_**

- 將檔案內容加至暫存區(index)
- 會將目前在 working tree 的檔案新增至 index, 然後等待至下一次的 commit
- 當 `add` 時, index 會對目前 working tree 的內容做 snapshot, 成為下一次 commit 的內容
- 如果 working tree 有再更新的話, 就必須再 `add` 一次
  > ## **_Options_**
- `-p`
  - `add -p <file>`
  - 進入互動模式, 選擇要 `add` 的區塊, git 會問你要使用那種 patch
    - `y` 選擇全部
    - `e` 手動選擇區塊
    - `q` 離開
