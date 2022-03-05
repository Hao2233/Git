# 第二章 Git常用命令

## 2.1  设置用户签名

1. 基本语法

```
// 设置用户名
git config --global user.name 用户名
// 设置用户邮箱
git config --global user.email 邮箱
```

2. 如何验证设置用户成功
```
// mac 
vim ~/.gitconfig
// windows 
open .gitconfig
```

__注意__
这里设置的用户名和邮箱是必须的，但与设置GitHub是没有关系的

## 2.2 初始化本地库

1. 基本语法

```
git init
```

2. 为什么要初始化

增加git管理目录权限
使得git可以追踪目录历史版本

## 2.2 查看本地库状态

1. 基本语法

```
git status
```

第一行输出当前文件位于Git哪个分支
第二行输出尚未暂存的变更 git add
第三行输出未跟踪的文件   git commint

## 2.3 添加到暂存区

1. 基本语法

```
git add 需要提交到文件
```

2. 全部提交

将本地修改的文件全部提交到暂存区
```
git add --all 
```

3. 删除提交到暂存区的文件

注意这里只是删除了提交记录，而不是删除本地文件
```
git rm --cached 文件名称
```

## 2.4 提交本地库

提交到本地库的作用是形成历史记录

1. 基本命令

```
git commit -m "提交日志" 文件名称
```

必须输入日志记录

2. 查看Git版本信息的命令

```
// 查看 commit 版本 记录
git reflog

// 查看git详细记录
git log
```

## 2.5 版本穿梭

1. 基本语法

```
// 1. 首先获取版本号
git reflog

// 2. 输入需要穿梭回去的版本
git reset --hard 版本号
```

## 2.6 查看git修改信息
```
git diff
```

## 2.7 git 乱码

```
// git status 乱码
git config --global core.quotepath false

// git commit 乱码
git config --global i18n.commitencoding utf-8
```

## 2.8 git 中英文切换

1. macos下
修改~/.zshrc 文件

切换为英文
alias git='LANG=en_US git'

切换为中文
alias git='LANG=zh_CN git'

