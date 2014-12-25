#Create a commit

當工作到一個段落或是修改完成之後，可以建立一個commit 紀錄



```
//在commit 之前將修改變動的檔案加入 staging area
git add <file paht>
//良好的commit 紀錄，在參數 -m 之後加上commit 訊息
git commit -m 'Commit message'

```

##將所有修改變動檔案加入staging area

```

//將所有變動檔案加入 staging area
git add --all

//或是
git add -A

//將現在目錄底下變動的檔案加入staging area
git add .

```

##將變動檔案加入staging area 並且提交Commit 訊息

```

//commit -a 參數無法將新增檔案加入staging area，新增檔案需要使用git add 指令加入staging area。

git commit -a -m 'Commit message'

```
