## Synopsis
當不想`add`、但想保留變更內容(`modified`)的情境

```git
git stash [push [-p|--patch] [-k|--[no-]keep-index] [-q|--quiet] [-u|--include-untracked] [-a|--all] [-m|--message <message>] [--pathspec-from-file=<file> [--pathspec-file-nul]][--] [<pathspec>...]]
```
## Options

- `list`
    - 檢視`stash`內暫存的內容，會依照commit順序有對應的`{index}` 值，
- `pop stash@{編號}`
    - 取出`stash`暫存內容
- `drop stash@{編號}`
    - 捨棄單筆`stash`暫存內容
- `-m "message"`
    - 修改`stash`儲存內容的描述:`git stash -m "message"`
- `apply `
    -  可以取出暫存內容,但不會清除`stash`
- `clear`
    - 清除全部的`stash`暫存內容
- `-u`
    -  暫存包含`untracked`的修訂
- `-m`



**狀況**
當前位置分支的`commit`還沒處理好，但被迫切換分支，處理別的任務，要如何保留下已處理的部分？
使用指令：`git stash` 
使用說明：只會保留`tracked`狀態的修訂內容

**尚未整理**
1. index值不能更改
2. stash一次取一筆
3. 利用stash訊息取出對應的stash內容
4. stash 預設是 stash push