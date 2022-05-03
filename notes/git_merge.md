## Synopsis

可以用來合併分支，把多個歷史紀錄整合起來。

- 合併分支的語法

```
git merge <分支名稱>
```

- 使用引數

```
git merge [-n] [--stat] [--no-commit] [--squash] [--[no-]edit] [-s <strategy>] [-X <strategy-option>] [-S[<keyid>]] [--[no-]rerere-autoupdate] [-m <msg>]
[<commit>...]

git merge <msg> HEAD <commit>...

git merge --abort
```

## 一場成功的合併，需要注意以下幾點

1. 合併之前，清楚的知道自己在哪個分支，同時確認工作目錄是乾淨的
2. 合併之後，可以使用 git log 來查看剛剛合併的版本紀錄，有成功正常來說就會多一個新版本
3. 不要發生 “衝突” ，有發生請盡快先解決再進行合併

## 狀況

合併後的分支要刪除嗎？  
答：可留可不留，可以參考這篇：https://gitbook.tw/chapters/branch/about-merged-branch
