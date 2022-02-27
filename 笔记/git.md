### 1. 初始化git仓库
```
git init
```
### 2. git提交到缓存区

```
git add README.md
git add --all
```
### 3. git提交到工作区
```
git commit -m "first commit"
git commit -m -a
```
### 4. git提交到远程仓库GitHub
```
git push
```
### 5. 查看git提交历史
```
git log
```
### 6. 查看git状态
```
git status
```
### 7. 查看git修改信息
```
git diff
```

### 8. 修改当前项目分支为main
git branch -M main

### 8.1 修改默认分支为main
git config --global init.defaultBranch main

## git 乱码
git status 乱码

解决方法：
git config --global core.quotepath false

git commit 乱码

解决方法：
git config --global i18n.commitencoding utf-8

git status 乱码

解决方法：
git config --global i18n.logoutputencoding utf-8

## git 中英文切换

修改~/.zshrc 文件

切换为英文
alias git='LANG=en_US git'

切换为中文
alias git='LANG=zh_CN git'

