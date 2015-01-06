#Branch naming conventions

當開發一段時間後，Repository 會擁有許多Branch 分支，多人開發共同專案也會有許多Branch ，這時就該有個Branch 分支的命名規則，讓Branch 好管理、好識別。

###Git 有branch 命名規則

1. 不能包含任何空白字元
2. 不能使用特殊字元包含否定號、脫字符號、冒號、問號、星號、左中括號(~, ^, :, ?, *, [)
3. 不能包含ASCII 字元小於 \040 (8進位 octal) 及 DEL字元 \177 (8進位 octal)
4. 不能包含連續 兩個點 (..)
5. 不能以減號為字首 -
6. 可以使用斜線 / 來建立階層名稱，不能以斜線 / 結尾
7. 斜線之後不可使用 .  ，如 Huei/.mybranch ，這是犯規的

###善用斜線來建立階層式管理Branch

如果有五個分支：

*timmy/branch1
*timmy/branch2
*huei/branch1
*liz/branch1
*nicole/branch1

在某些Git GUI 工具(如source tree)自動利用斜線歸納整理branch 分組，自動分成四組timmy, huei, liz, nicole，可以輕鬆管理自己創立的分支及方便快速識別他人分。

```

//在Terminal 底下你可以利用git show-branch 與斜線命名方式快速搜尋分支

git show-branch 'timmy/*'

//將會顯示所有timmy/ 開頭的branch 

```
