#Creat a branch

一般新開一個branch 會從原本branch 的HEAD建立新的branch 分支出來，例如你要從master 建立一個新的branch 出來開發，會在master 最新的commit 節點建立新的branch。

```

//建立一個名為"_myBranch" 的branch
git branch _myBranch

//切換到"_myBranch" branch 上
git checkout _myBranch

```

##建立branch並且切換到新建立的btanch上

```

git branch -b _myBranch

```
