> ## **_Synopsis_**

- 顯示 commit 記錄, 可以看到各種資訊, 包括 commit, HEAD 位置, 作者, 時間等

> ## **_options_**

- `--oneline`
  - 只顯示 SHA-1 跟 message
- `--graph`
  - 顯示文字線圖
- `--all`
  - 假裝所有 refs 都在 refs/heads 裡, 所以也會顯示其他分支的記錄
- `--author=<pattern>`
  - 顯示符合此格式之作者的 commit 記錄
- `--grep=<pattern>`
  - 顯示符合此格式之 commit 訊息的 commit 記錄
- `-S<string>`
  - 顯示檔案含有這個文字的 commit 記錄
- `--since=<date> | --after=<date>`
  - 顯示在此時間之後的 commit 記錄
- `--until=<date> | --before=<date>`
  - 顯示在此時間之後的 commit 記錄
- `-p <path>`
  - 顯示此檔案在每次 commit 記錄的更動
