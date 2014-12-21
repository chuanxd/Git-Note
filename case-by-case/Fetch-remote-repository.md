#Fetch remote repository

下載遠端repository 資料可以使用git pull 和 git fetch 指令，定期同步資料可以避免不必要的資料衝突。

git pull 指令會先執行git fetch 下載遠端資料，接著執行git merge 合併資料，git merge 會產生一個commit。

git fetch 指令僅下載資料下來，並沒有合併資料，可以與git rebase 指令搭配使用。


```

//使用git pull 更新資料

git pull

//使用 --rebase 參數，指令會先執行git fetch 接著執行git rebase 合併

git pull --rebse

//下載遠端資料

git fetch origin

//合併資料

git rebase origin <branch name>

```
