#Remove untracked files from the working tree

可以使用git clean 來清理在工作目錄上沒有受版本控制的檔案，有些檔案是因為被忽略追蹤而存在的。

```

//列出沒有被追蹤的檔案

git clean -nd

//刪除沒有被追蹤的檔案

git clean -fd

```
