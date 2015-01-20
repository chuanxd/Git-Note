#Ignoring Files


使用.gitignore 清單可以忽略特定檔案、目錄路徑，像是一些不需要版本控制的檔案或是一些環境設定。

.gitignore 裡#為註解符號

如果想要忽略的檔案已經加入Git版本控制了，可以使用git rm 指令。

```

git rm --cached <File Name>

```

Reference (https://help.github.com/articles/ignoring-files/)
