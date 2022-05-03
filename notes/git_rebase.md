## Synopsis

舉例現在有兩個 branch, cat 跟 dog 各別從 master 長出來, 並且分別有兩個 commit 點, 然後要將 cat rebase 到 dog 上, 必須切換到 cat, 並輸入 `git rebase dog`, 此時背後的運作機制會將 cat 的第一個 commit 點跟 dog 最新的 commit 點做合併, 然後產生新的 commit 點, 接著 cat 的第二個 commit 點會跟這個新的 commit 點做合併, 並產生新的 commit 點後完成 rebase, 此時 head 在 cat 上.

## 注意

commit 點合併的時候如果有衝突要先解決衝突才會進入下一個 commit 合併的動作, 在解決完衝突之前都是正在 rebase 中的狀態.

## 如何取消 rebase

先用 reflog 找出 rebase 的點, 輸入 `git reset <sha-1 值> --hard`
這樣就會回到 rebase 前的狀態
