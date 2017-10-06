# Git 使用总结

## 基本概念

- 工作区
  + 就是平常编写代码的目录文件区域
- 暂存区
  + 临时备份
  + 分批次提交
- 版本库（每一次的 commit 都提交到了版本库）

## 基本操作

- git init [repo-name]
  + 在本地初始化 Git 仓库
- git add
  + 把工作区文件的改动提交到暂存区
  + git add 文件名 文件名 目录名...
  + git add --all
  + git add .
  + git add *
- git rm --cached 文件名
  + 凡是被 git add 过的文件都会被 Git 跟踪管理起来
  + 移除被 Git 跟踪管理的文件
- git commit -m '提交日志'
  + 将暂存区的状态提交到版本库形成一个历史记录
  + git commit -a -m '提交日志' 提交工作区自上次commit之后的变化，直接到仓库区
  + git commit --amend -m [message]
    * 使用一次新的commit，替代上一次提交，如果代码没有任何新变化，则用来改写上一次commit的提交信息
- git status
- git log
- gitk

## 撤销操作

## 远程操作

### 已有远程仓库

- git clone 远程仓库地址
  + git clone 下来的仓库自动在 remote 中添加了一个名字为 origin 的仓库地址信息
- git push
  + 推送
- git pull
  + 拉取

这种方式拿到的仓库，自动记录了远程仓库的地址，所以你每次 push 和 pull 的时候它都知道往哪儿 push 和 pull。

### 已有本地仓库，需要推送到远程仓库

- 现在远端创建一个远程仓库
- git push 远程仓库地址

如果每一次 push 的时候都手动的拼写远程仓库地址很麻烦，所以这里使用 `remote` 命令把远程仓库记录起来。

```bash
# git remote 就是用来管理远程仓库地址的
# 一个项目可以存储在任何地方，既可以放到 GitHub 也可以同时放到码云
$ git remote add 别名（推荐使用origin） 远程仓库地址
```

- git push 仓库地址别名 本地分支:远程分支
- git push 仓库地址 分支名称
- git push --set-upstream 远程仓库 分支

## 分支操作

项目已上线，还在继续开发或者说增加新的功能。

- 第三方登陆
  + 工作区、暂存区已经很乱了，这个功能也还没有完成
- 紧急任务：目前线上的版本出现了一个 bug

## 使用 Git 的分支策略（工作流）

- Git Flow
- GitHub Flow

## GitHub 多人协同

- Pull Request
- Collaborators

var a = 123

- 代码格式
- 方法
  + 是否多余
  + 方法体太大了
- 变量命名是否规范

## 总结

- 分支使用管理策略，工作流
  + 更加的规范、合理的协同开发
- GitHub 协同的方式
  + Pull Request
  + Collaborators
- GitHub
  + config 配置
  + gist
  + explore
  + follow
  + watch
  + star
- 从开源项目中去学习
  + node.js 阶段
