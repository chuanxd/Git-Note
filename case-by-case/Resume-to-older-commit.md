#Resume to older commit

當工作到一半想取消所做的更動，或是玩壞了、後悔修改可以使用git reset 指令來回復檔案變動。

git reset 可以回復到特定的commit 節點，預設為HEAD，可以在git reset 後加上特定commit。

```

//完全清除變動，回復到目前的HEAD 未修改狀態
git reset --hard

//回復到目前的HEAD，保留變動檔案在 staging area
git reset --soft

//保留變動在 working tree
git reset 

```

