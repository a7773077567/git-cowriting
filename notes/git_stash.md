## Synopsis

- 當不想`add`、但想保留變更內容(`modified`)的情境
- `stash` 的每筆記錄會有一個對應的 `stash@{n}` index
- `stash` 的 index 無法更改名稱, 但可以修改 `stash` 的 message
- 可以使用 regexp 找出符合的 message, 及其對應的 `stash`
- 一次只能取一筆 `stash`

```git
git stash [push [-p|--patch] [-k|--[no-]keep-index] [-q|--quiet] [-u|--include-untracked] [-a|--all] [-m|--message <message>] [--pathspec-from-file=<file> [--pathspec-file-nul]][--] [<pathspec>...]]
```

## Subcommands

- `list`
  - 檢視 `stash` 內暫存的內容，會依照 commit 順序有對應的 `{index}` 值，
- `pop`
  - `$git stash pop stash@{n}`
  - 取出 `stash` 套用至目前的 branch, 同時刪除 list 記錄, 可以看成是 `apply + drop`
  - 如果沒有給 index, 則刪除編號最小的那筆 (最新)
- `drop`
  - `$git stash drop stash@{n}`
  - 捨棄單筆`stash`暫存內容
  - 如果沒有給 index, 則刪除編號最小的那筆 (最新)
- `apply `
  - 可以取出暫存內容,但不會清除`stash`
- `clear`
  - 清除全部的`stash`暫存內容

## Optionals

- `-u`
  - 暫存包含`untracked`的修訂
- `-m`
  - `$git stash -m <"message">`
  - `$git stash push -m "<"message">`
  - 儲存 `stash` 的同時給予自訂的 message

**狀況**
當前位置分支的`commit`還沒處理好，但被迫切換分支，處理別的任務，要如何保留下已處理的部分？
使用指令：`git stash`
使用說明：只會保留`tracked`狀態的修訂內容
