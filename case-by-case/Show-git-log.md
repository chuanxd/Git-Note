#Show git log

使用git log 來查詢commit logs 記錄，git log可以顯示目前所在branch 的commit logs 記錄，預設會顯示commit sha-1 、commit author、 commit date以及 commit message。

```

//預設顯示現在所在branch commit logs
git log

//顯示特定branch commit logs
git log <branch name>

//顯示特定commit log

git log -p <commit sha-1>

//顯示commit sha-1 與 commit messag

git log --oneline

//git log --oneline 如下顯示結果：
7c41b52 branch-2-3
adb2e95 branch-2-2
54ef718 branch-2-1
f2c0739 commit-2
1e1c3b2 2 commit
63a1849 first commit

``` 
