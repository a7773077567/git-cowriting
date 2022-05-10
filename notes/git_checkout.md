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




**參考**
[How to Check Out a Remote Git Branch?](https://www.studytonight.com/git-guide/how-to-check-out-a-remote-git-branch)