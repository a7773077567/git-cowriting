> ## **_Synopsis_**

- 當分支的 tip 變動時, 也可以理解成 HEAD 移動時, 就會產生一筆記錄, 是完整的版本記錄, 不是單純的 `git log` 顯示的版本記錄, 所以當使用以下指令皆會產生記錄
  - `commit`
  - `checkout`
  - `pull`
  - `push`
  - `merge`
  - `reset`
  - `clone`
  - `branch`
  - `rebase`
  - `stash`
- 記錄版本變更有個基本原則
  - 透過指令修改了任何參照(ref)的內容, 或則變更任何分支的**HEAD**參照內容
- 這些記錄不會被同步到遠端

> ## **_subcommands_**

- `show`
  - default, 顯示 ref 變動的記錄
  - `git reflog show` 是 `git log -g --abbrev-commit --pretty=oneline` 的 alias

> ## **_options_**

- `--all`
  - 顯示所有 refs 的 reflogs
