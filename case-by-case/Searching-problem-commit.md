#Searching Problem Commit

git bisect 指令可以搜尋出有問題的commit ，git bisect 使用二分法來搜尋問題點。

bisect 英文有對分的意思。

```

//當你執行git bisect start 的時候，HEAD 會切換到匿名的branch 上
git bisect start

//HEAD 基本上都是不正常commit 之後
git bisect bad

//有了不正常的端點，就要給正常的commit 端點
git bisect good <正常commit 的 SHA-1>

```

給了正常與不正常的端點之後，git bisect 會從這個範圍內執行二分法來詢問。

```

//檢查內容，如果是對的，執行

git bisect good

//錯的內容則執行

git bisect bad

```

最後找到問題的commit 時會顯示出 commit 的 SHA-1

```

//離開git bisect 模式
git bisect reset

//會跳到原本的branch HEAD

```
