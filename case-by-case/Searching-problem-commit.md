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

##範例 Sample

假設有個檔案有時個版本，在其中一個版本之後出了問題，要找到其中一行code 在何時加入的 commit。

檔案最新的內容為：

```

1
2
3
4
5
6
7
8
9
10

```

第一次的版本為1 ，第二次的版本添加了2，以此類退每個版本添加一項數字到十個版本。

假設在5這個數字是添加錯誤的，也許正確應該是其他的內容，以下使用git bisect 指令來查詢出被加入的commit。

```

//執行git bisect

git bisect start

//告訴git bisect 目前所在的HEAD 是錯誤的commit

git bisect bad

//告訴git bisect 哪個commit 是還沒有錯誤的資料內容

git bisect good <SHA-1>

//接著git bisect 會切換到剛剛執行good 與 bad commit 中間的commit SHA-1
//如果資料內容是錯誤的，那麼請執行

git bisect bad

//git bisect 會切換HEAD往另一邊的中間 commit
//直到找到問題的資料內容被添加時候的第一個commit 

//git bisect 會顯示問題所在地commit SHA-1

<SHA-1> is the first bad commit
//下面會接著顯示這個commit 作者是誰以、commit 的時間點、commit message、commit files

```
