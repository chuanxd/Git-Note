#Stash working directory

在變動修改後要進行branch 切換，但還未進行commit 動作，可以先將變更修改的檔案存放到stash 堆疊存放。

使用git stash 指令來存放，git stash 是一個stack 堆疊暫存結構，Fast-in Last-out 先進後出，每個存入stash 堆疊裡面的資料都有編號，stash@{0} 是最新的資料，讓存入下一筆暫存資料後，原本stash@{0}的資料會變成 stash@{1}，stash@{0} 將優先能夠取出堆疊中。

```

//將資料存入stash 中

git stash save

//git stash 預設為save，所以可以使用:

git stash

//加入暫存訊息

git stash save '<Stash Message>'

//取出stash 堆疊資料

git stash pop

//列出stash 堆疊中的資料

git stash list

//列出stash 堆疊中最新一筆暫存的資料

git stash show

//指定列出stash 堆疊中暫存的資料
//以下為指定第二筆暫存資料

git stash show stash@{1}

//列出stash 堆疊中最新一筆修改資料對比

git stash show -p

//指令列出stash 堆疊暫存資料對比
//以下指定stash 堆疊第二筆資料對比

git stah show -p stash@{1}

//取出特定stash 堆疊中的資料

git stash apply stash@{id}

//git stash apply 取出資料還會存在於stash 堆疊中，需要手動清除，請參考下面的指令清除。

```

關於刪除stash 堆疊資料

```

//刪除stash 最上層資料

git stash drop

//刪除stash 堆疊特定資料

git stash drop stash@{<id>}

//如果是刪除stash 堆疊第二個資料

git stash drop stash@{1}

//清空stash 堆疊

git stash clear

```
