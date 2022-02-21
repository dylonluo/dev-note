# development-note

## 目录
* 开发流程
* CI/CD开发

### CI/CD流程 -- github + jenkins + docker解决方案

#### Github

* 本地配置Github账号与token
* 从Git远程仓库复制项目到本地
* 打开本地项目，开发前update一下master
* New select 一个本地分支并进行开发
* 开发完成后标记好tag，commit到远程仓库

#### Jenkins部署
* 加上[ci build]的tag，本地开发分支会在jenkins打包后搜索"dev_"获取镜像码
* 通过jenkins部署到dev环境可以自测
* 自测测试后，在github上创建一个pull request合到master分支。
* 打包部署到test环境后，进行回归测试
*

#### 日志查看
1. 在lens查看日志，打开对应的集群，查看对应的pod

想要让Git回退历史，有以下步骤：

#### github 回退
使用git log命令，查看分支提交历史，确认需要回退的版本
使用git
```shell
reset --hard commit_id
```
命令，进行版本回退
使用
```shell
git push origin
```
命令，推送至远程分支
快捷命令：

回退上个版本：
```shell
git reset --hard HEAD^
```

#### 辅助工具
* Mac命令行工具oh-my-zsh
* 安装oh-my-zsh通过brew
```shell
brew install oh-my-zsh
```
