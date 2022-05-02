## Synopsis

遠端數據庫修改的內容合併到本地端數據庫的分支上，是git fetch +  git merge FETCH_HEAD 的縮寫

```
  git pull [<options>] [<repository> [<refspec>...]]
```

## Options
- `rebase`
  - rebase 主要都是被用在尚未提交至遠端的 commit，達到重整的作用，以及多人協作時在同一條分支上的開發，避免產生多餘的 commit 紀錄，git pull+git rebase

**狀況**
andy 和 rex在同一個branch上開發，各自commit若有一方push上另一個人無法推上去，必須先git pull，此時會造成額外commit因為git pull＝git fetch+git merge，所以使用git pull --rebase