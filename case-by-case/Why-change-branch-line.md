#Why change branch line ?

Git commit, pull, rebase, merge, push, reset, revert 都是相當重要的指令，在執行指令前應清楚了解執行指令的目的與指令背後的行為，最重要的是指令執行為之後的結果。

Git 是版本控制的工具，使用工具前必須預先設想使用工具後的結果。

造成branch line 換線原因為使用git merge --ff 快速指向合併。

以下範例為master 與branch 進行合併後造成換線：

```

Master A---C---
        \
Branch   B---D---

```

從Master A點創立了Branch 分隻出來開發，在開發期間開發了B點與D點，而在開發進行間，Master 增加了C點，Branch 開發完畢要合併回Master，使用了Fast forward 進行合併。

```

Master A---B---D---E
        \         /
Branch   ---C-----

```

產生了換線，因為Fast forward 進行快速指向合併，將Master HEAD 指向 Branch HEAD又Branch 沒有C 點導致Master 直接切換成Branch ，原本在Master 上的 C點將會被獨立出來在Master之外，雖說檔案並無損失，但是改變了git flow 原有結構，如果結構在每次合併都產生改變，對於專案後續維護將產生困難。
	
使用git merge --no-ff 進行合併可以避免不必要的btanch line 切換。

[請參考Git-merge-into-branch.md](https://github.com/chuanxd/Git-Note/blob/master/case-by-case/Git-merge-into-branch.md)


git merge 是神聖的行為。
