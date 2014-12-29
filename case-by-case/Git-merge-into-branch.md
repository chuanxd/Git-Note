#Git merge into branch

Merge 合併。

當branch 完成後想合併回Master 或 其他branch 時，可以使用git merge 指令來完成branch 之間的檔案合併。

git merge 是一個神聖的行為。

git merge 影響是兩個合併branch 之間的關係，如果Master 主線與多人共同合作，那麼錯誤的結果會影響所有合作夥伴，當然是在你錯誤的合併後執行git push 之後才會影響別人。

在開始合併之前建議讓工作目錄保持乾淨，確保branch commit 記錄正確性、一致性。

以下範例已branch 合併回master 為示範：

```

//在開始合併前建議先讓master 更新至與遠端master 一致，確保master 為最新。

git checkout master

//git fetch and git rebase，抓取遠端資料並且更新基礎參考位置

git pull --rebase

//更新master 之後，緊接著更新branch 與遠端branch 一致，也許你會有合作夥伴也在相同branch 工作。

git checkout <branch name>

git pull --rebase

//master 與 branch 都與遠端一致後，為了降低合併後的衝突，建議先從master 抓取在master 上有的commit 但branch 並沒有的commit 記錄。

git merge origin/master

//也可以使用fetch and rebase

git fetch origin master

git rebase origin <branch name>

//到目前為止也許會產生衝突，如果產生衝突，請解決衝突。
//如果一切順利，那麼緊接著執行git merge master合併 branch

git checkout master

//建議使用no fast forword 方式進行合併

git merge --no-ff <branch name>

//如果產生了衝突，請面對它、接受它、處理它。

//合併完之後先不要急著與工作夥伴分享合併結果，先看看git brancn line 是否與合併前設想的結果相同
//你可以使用git GUI工具來檢視branch line ，可以執行gitk 指令開啓Git 內建GUI。 
//如果嫌gitk 太醜，可以安裝其他git GUI， 像是： [Source Tree](http://www.sourcetreeapp.com/)

gitk

//確認合併後結果正確，可以與大家分享你的程式，使用git push 散播希望種子。

git push origin master


```

##Fast Forward

git merge 指令預設使用Fast forward 來進行合併。

Fast forward 是指合併過程中，將當前barcnch HEAD 參考點指向合併進來的點，達到快速指向。

以下解釋已master 與branch 進行Fast forward 合併：

```

Master A---
        \ 
Branch   B

```

執行git merge --ff 之後

```

Master A---B

```

線路上看不到branch 因為透過Fast forward 進行合併，branch 已經和併入到master 線路裡。

Fast forward 認為master 合併前與branch 之間的差異就是B commit 節點，所以master HEAD 直接指向B。

使用Fast forward 可以減少一個merge commit 記錄，因此無法輕易追蹤merge 進入master 節點，也不好進行某些在branch 上面開發的commit 記錄。

建議使用git merge --no-ff 指令進行合併動作。

```

Master A------C
        \    /
Branch   B---

```



