## 基本用法

设置用户基本信息

```shell
git config --global user.email 'xxx@qq.com'
git config --global user.name 'your_name'
```

熟悉常用命令，理解工作区、暂存区、代码库

```shell
git clone <remote_repo_url>
git status # 查看当前工作区、暂存区状态
git add filename #
git add . #
git commit -m "简单描述"
git push # 同步到远程仓库
git pull
```

## 上传已有项目

第一次上传已有项目

1. 通过 git init 初始化当前项目
2. 通过 git add . 将所有文件添加到暂存区
3. 通过 git commit -m "init project"
4. 设置远程仓库地址 git remote add origin https://github.com/hereisxinyu/first.git
5. git branch -M 'main' 将默认的 master 分支重命名为 main 分支
6. git push -u origin 'main'。备注：-u => --up-stream 缩写

## 踩的坑

git push 使用用户名密码提交代码失败

原因：Support for password authentication was removed on August 13, 2021. Please use a personal access token instead.

解决办法

1. user -> settings -> developer settings -> personal access token -> generate new token
2. 设仓库远程路径设置成使用 token

```shell
git remote set-url origin https://<token>@github.com/<repo_name>/
```

## 更进一步

后续需要深入的学习方向 - 分支 branch

- 分支的目的
- 新建分支语法
  - git branch -b <branch_name>
- 分支合并策略
