# Show Git status

顯示 Git 工作狀態
顯示目前所在 branch
顯示已修改檔案但未加入 staging area
顯示 staging area 清單

```sh
git status
```

顯示乾淨、且簡短的狀態資訊

```sh
git status -s
```

## 符號對照表

```
X          Y     Meaning
-------------------------------------------------
          [MD]   not updated
M        [ MD]   updated in index
A        [ MD]   added to index
D         [ M]   deleted from index
R        [ MD]   renamed in index
C        [ MD]   copied in index
[MARC]           index and work tree matches
[ MARC]     M    work tree changed since index
[ MARC]     D    deleted in work tree
-------------------------------------------------
D           D    unmerged, both deleted
A           U    unmerged, added by us
U           D    unmerged, deleted by them
U           A    unmerged, added by them
D           U    unmerged, deleted by us
A           A    unmerged, both added
U           U    unmerged, both modified
-------------------------------------------------
?           ?    untracked
!           !    ignored
-------------------------------------------------
```

refs: https://git-scm.com/docs/git-status
