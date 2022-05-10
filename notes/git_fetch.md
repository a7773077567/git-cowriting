> ## Synopsis
當只想確認遠端資料庫的內容，還沒確定要合併時，使用`fetch`產生HEAD_FETCH分支，供你檢視最新`commit`紀錄、以及修訂內容。

```git
git fetch [<options>] [<repository> [<refspec>...]]
   
git fetch [<options>] <group>
   
git fetch --multiple [<options>] [(<repository> | <group>)...]
   
git fetch --all [<options>]
```

> ## Options

- `all`:
  - `fetch`所有遠端.
- `append(-a)`:
  - 在已經`fetch`的情景下,使用`-a`來達到添加新的`fetch`,不會覆蓋現在的`fetch`內容.


>**參考**: [Git Fetch: Definition & Examples](https://phoenixnap.com/kb/git-fetch)