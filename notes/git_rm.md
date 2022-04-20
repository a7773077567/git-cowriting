## Synopsis

將檔案從暫存區(index)或工作目錄(working tree)移除

```git
git rm [-f | --force] [-n] [-r] [--cached] [--ignore-unmatch] [--quiet] [--pathspec-from-file=<file> [--pathspec-file-nul]] [--] [<pathspec>…​]
```

## Options

- `r`
  - 指定資料夾名稱(leading directory name)，可以遞迴刪除其中所有檔案
- `--cached`
  - 可將檔案從暫存區(index)退回到 untracked 狀態; 不會對工作目錄(working tree) 的檔案造成變動。
    （Use this option to unstage and remove paths only from the index. Working tree files, whether modified or not, will be left alone.）

**狀況**

- 不小心把 `node_modules/` 加到暫存區(index)中，要如何移除整個資料夾內的檔案？
  使用指令: `git rm -r --cached folderName/`
  指令說明: 可將檔案從暫存區(index)退回 untracked 狀態
