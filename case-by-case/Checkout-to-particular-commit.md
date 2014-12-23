#Checkout to particular commit

可以使用git checkout 指令將HEAD 指向到特定commit 節點，不會影響到原本所在的branch。

HEAD 是指向目前所在branch 最尾端的節點，如果沒有特定只向別的節點，那麼HEAD 所指向的位置就是branch 最新的commit 節點。

```

git checkout <commit sha-1>

```
