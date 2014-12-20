#Push to remote refs

當commit 結束後你可以將你的commit push 更新到遠端 repository。

```

//當你commit 後，使用git status 會顯示類似以下訊息
//(以下訊息在branch master)
//git status 顯示你目前所在的branch，以及你有一個commit 還沒更新到遠端repository
//並且提示你可以使用git push 來發佈你的commit 到遠端 repository。

On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working directory clean


//如果依照上面git status 所顯示的訊息，來更新遠端 repository，指令如下：

git push origin master

//使用git push 更新遠端repository

git push origin <branch name>


```
