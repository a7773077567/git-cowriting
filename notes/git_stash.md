## Synopsis
當不想`add`、但想保留變更內容(`modified`)的情境

```git
git stash [push [-p|--patch] [-k|--[no-]keep-index] [-q|--quiet] [-u|--include-untracked] [-a|--all] [-m|--message <message>] [--pathspec-from-file=<file> [--pathspec-file-nul]][--] [<pathspec>...]]
```
## Options

- `list`
    - 檢視使用`stash`保存的內容，會依照使用順序有對應的`index`值，
- `pop stash@{編號}`
    - 要從`stash`內取出的內容
- `drop stash@{編號}`
    - 要從`stash`內捨棄的內容


**狀況**
當前位置分支的`commit`還沒處理好，但被迫切換分支，處理別的任務，要如何保留下已處理的部分？
使用指令：`git stash` 
使用說明：只會保留`tracked`狀態的修訂內容