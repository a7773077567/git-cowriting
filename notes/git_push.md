## Synopsis

根據本地端參照(ref)更新遠端資料庫參照(ref)

Common Use：

```
git push [-f | --force] [<repository> [<refspec>…​]]
```

`[<repository> [<refspec>…​]]` 指定推送的地點，包含 repository（遠端 repo 名字） 和 refspec（參照的分支）

## Options

- `--set-upstream` （可簡化為 `-u`）

  - 設定 upstream (有人會翻成上游)
  - 在 Git 裡，每個分支最多可以設定一個 upstream，它會指向並追蹤（track）某個分支
  - 通常 upstream 會是遠端 Server 上的某個分支，但其實要設定在本地端的其它分支也可以
  - 主要是第一次 push 時，需要設定 upstream ，之後再執行 `git push` 時，就不用加其他參數，會直接幫你推到綁定的 upstream

    ```
    範例： `git push -u origin develop`
    1. 把本地的 develop 分支推到 origin (遠端節點) 上，遠端會出現 develop 分支
    2. 將遠端的 develop 分支視為本地 develop 的 upstream
    ```

- `--force` （可簡化為 `-f`）

  無視先來後到的規則，會覆蓋遠端的內容(upstream)，一切以本地端內容為主

  **使用時機**

  1. 用在個人的私人分支上

     只有自己使用這個分支，並且非常確定要以本地端紀錄為主

  2. 整理歷史紀錄

     在使用 rebase 整理 commit 歷史紀錄後，正常來說是推不上去，只能用 force push 解決

     尤其在協作狀況下

     - 一定要知會其他協作者，說好以此版本為主
     - 遠端沒有其他協作者的新 commit

> How to proper force push（ref: [Will Anderson - The Dark Side of the Force Push](https://willi.am/blog/2014/08/12/the-dark-side-of-the-force-push/)）

1. 確定所有使用到這個分支的開發成員，都已經把自己本地的 commit 推到遠端上了
2. 建議整個開發團隊先暫停此分支上的開發，等到整理後的分支推上遠端
3. 確認自己的本地分支有最新的變動(commit)
4. 使用 rebase 整理歷史紀錄，之後應該用 force push 才能推到遠端

最後，團隊其他人要怎麼在本地拿到最新的 git 紀錄？

- force pull: `git pull --force origin <rbranch>:<lbranch>`
- 組合技
  1.  `git checkout <yourbranch>`
  2.  `git fetch`
  3.  `git reset --hard origin/<yourbranch>` 也就是放棄目前所有檔案與 commit，還原成遠端版本

![](https://miro.medium.com/max/800/0*XaLzNzYkA6PZjbl9.jpg)

**狀況**

- 本地分支跟遠端分支想取不同的名字

  相關指令：

  `git push [<repository> [<refspec>…​]]`

  `git push [<repository> [object<src>:destination ref <dst>​]]`

  範例：

  - `git push -u origin develop`
  - `git push origin develop:develop`

  - 上面兩個指令的意思是一樣的：「把本地的 master 分支推上去後，在 Server 上更新 master 分支的進度，或是如果不存在該分支的話，就建立一個 master 分支」
  - 如果推上去後想改叫另一個名字，只要改掉`:<dst>`的參照名稱，如：`git push origin develop:mybranch`

- **想刪除遠端分支**

  相關指令：

  `git push [<repository> [<refspec>…​]]`

  `git push [<repository> [object<src>:destination ref <dst>​]]`

  範例：`git push origin :test`

  範例說明：會刪除遠端的 test 分支，可以想成是推空的內容上去，覆蓋掉原本遠端的 test 分支

## 參考資料

- [git book](https://git-scm.com/docs/git-push)
- 為你自己學 git
- [Will Anderson - The Dark Side of the Force Push](https://willi.am/blog/2014/08/12/the-dark-side-of-the-force-push/)
- [辛西亞的技能樹](https://cynthiachuang.github.io/Git-Force-to-Push-Commit-to-a-Remote-Repository-and-Overwrite-Local-Repository/)
