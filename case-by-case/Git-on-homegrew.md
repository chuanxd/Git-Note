Git on homebrew

使用homebrew 來安裝更新管理Git 版本。

```

//安裝homebrew

ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

//更新homebrew 版本

brew update

//使用homebrew 安裝git

brew install git

//Restart Termintal 關閉並重開Termintal

//查看 git 版本

git version

//應該還是舊版的

//執行 which git 查看git 安裝目錄

which git

//修改路徑

.bash_profile

export PATH=/usr/local/git/bin:$PATH

//或是

echo 'export PATH="/usr/local/bin:/usr/local/sbin:~/bin:$PATH"' >> ~/.bash_profile

//查看git 版本

git version

//使用homebrew 更新git

brew upgrade git

//更換路徑就可以完成了

echo 'export PATH="/usr/local/bin:/usr/local/sbin:~/bin:$PATH"' >> ~/.bash_profile

```
