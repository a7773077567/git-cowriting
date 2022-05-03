## Synopsis

移動或重新命名檔案、資料夾、分支等等

```git
 git fetch [<options>] [<repository> [<refspec>...]]
   or: git fetch [<options>] <group>
   or: git fetch --multiple [<options>] [(<repository> | <group>)...]
   or: git fetch --all [<options>]
```

## Options

- `r`


**狀況**
當只想確認遠端資料庫的內容，還沒確定要合併時，使用`fetch`產生HEAD_FETCH分支，供你檢視最新`commit`紀錄、以及修訂內容。