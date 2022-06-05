> ## Synopsis

```
       git checkout [-q] [-f] [-m] [<branch>]
       git checkout [-q] [-f] [-m] --detach [<branch>]
       git checkout [-q] [-f] [-m] [--detach] <commit>
       git checkout [-q] [-f] [-m] [[-b|-B|--orphan] <new_branch>] [<start_point>]
       git checkout [-f|--ours|--theirs|-m|--conflict=<style>] [<tree-ish>] [--] <pathspec>...
       git checkout [-f|--ours|--theirs|-m|--conflict=<style>] [<tree-ish>] --pathspec-from-file=<file> [--pathspec-file-nul]
       git checkout (-p|--patch) [<tree-ish>] [--] [<pathspec>...]
```

> ## Options

- `<branch>`:HEAD 會指向這個分支
- `--track <remote>/<remote-branch>`: 會根據指定遠端分支在本地建立本地分支

**狀況**

- 想複製其他分支的檔案到當前分支
  1. 確認當前分支（複製檔案移動的目的地），到根目錄
  2. 複製整個資料夾：`git checkout <分支名稱> -- <資料夾名稱>`
  3. 複製資料夾中的單個檔案：`git checkout <分支名稱> -- <資料夾名稱/檔案名稱>`
     p.s 如果在子目錄，檔案路徑須指明相對路徑

**參考**
[How to Check Out a Remote Git Branch?](https://www.studytonight.com/git-guide/how-to-check-out-a-remote-git-branch)
