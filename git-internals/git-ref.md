#Git ref

參照名稱(ref) ，ref 是 Git 的指標，在相對的時間、位址對應相對的Git 物件。

大部份的ref 參照名稱會指向git commit 物件。

##Git 有四種不同的指標：

###HEAD

HEAD 指向目前所在的branch 的commit 物件位置，如果你的branch 被更新，HEAD 隨即會指向最新的commit 物件。

HEAD 永遠會指向目前的工作目錄。

###ORIG_HEAD

你可以在ORGIN_HEAD 指標中找到合併(merge、rebase)、重設(reset)前的HEAD commit 物件。

找到這些物件可以幹嘛呢？  你可以進一步的執行回覆或是執行比較。

###FETCH_HEAD

當使用git fetch 指令時，fetch 遠端的資料會被 FETCH_HEAD 指向，也就是說git fetch 所下載的資料並不會影嚮你所在的branch HEAD 資料。

###MERGE_HEAD

在執行合併時另一個branch 的HEAD 會被暫時的被記錄在MERGE_HEAD 中。


##Git ref 所在的位置

```

.git/ref
.git/refs/ref
.git/refs/tags/ref
.git/refs/heads/ref
.git/refs/remotes/ref
.git/refs/remotes/ref/HEAD

```

Git 的工作目錄.git 是可以被變更的，Git 內部文件使用$GIT_DIR 變數儲存.git 目前的工作目錄。

##顯示所有的參照(ref)

使用git show-ref 顯示所有的ref

```

git show-ref

```
