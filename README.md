# git-tutorial
# Git 快速上手


**第一次用 Git，把一个项目从 GitHub 拉到本地，改点东西，再和别人一起合并回去。**

下面是一个最常见的实际流程：
第一次使用时:
安装git
打开下载 https://git-scm.com/
重开终端
验证git --version

在自己电脑上配置一次身份信息
git config --global user.name "Your Name"
git config --global user.email "you@example.com"



把项目下载到本地
```bash
cd E:\github
git clone https://github.com/username/project.git
cd project
```bash

之后可以在E:\github\project 直接cmd打开

为改动创建一个分支（团队协作必做）
```bash
git switch -c yourbranch  #switch切换分支(branch) -c create创建

修改文件

保存修改
git add . #.全部
git commit -m "说明这次改了什么" #commit可回退

把本地分支推动到远程仓库
git push -u origin yourbranch # push上传代码 -u ? origin ?
或git push #区别是?

在 GitHub 上合并（merge）

更新本地主分支 #会直接覆盖E:\github\project 吗?
git switch main
git pull #pull下载代码

# git-tutorial
# Git 快速上手

第一次用 Git，把一个项目从 GitHub 拉到本地，改点东西，再和别人一起合并回去。

下面是一个最常见的实际流程。

--------------------------------
第一次使用时（只做一次）
--------------------------------

安装 git  
打开下载：https://git-scm.com/  
安装完成后，重开终端  

验证是否安装成功：
git --version

--------------------------------
配置本地身份信息（只做一次）
--------------------------------

在自己电脑上配置一次身份信息（用于记录 commit 作者）：

git config --global user.name "Your Name"
git config --global user.email "you@example.com"

说明：
- 这是本地 Git 的身份信息
- 不是 GitHub 网页登录
- 只需要配置一次

--------------------------------
把项目下载到本地
--------------------------------

cd E:\github
git clone https://github.com/username/project.git
cd project

说明：
- cd E:\github：选择一个本地目录作为存放位置
- git clone：从 GitHub 下载项目，并在当前目录下创建 project 文件夹
- cd project：进入真正的 Git 仓库目录（.git 在这里）

之后也可以直接在：
E:\github\project
目录下直接打开 CMD / 终端继续操作。

--------------------------------
为改动创建一个分支（团队协作必做）
--------------------------------

git switch -c yourbranch

注解：
- switch：切换分支（branch）
- -c：create，新建分支
- yourbranch：你自己的分支名

作用：
从当前分支复制一份，新建分支，并切换到该分支上工作。

--------------------------------
修改文件
--------------------------------

在当前分支下修改文件。  
这一步 Git 不会自动保存任何内容。

--------------------------------
保存修改（本地）
--------------------------------

git add .            # . 表示把所有修改加入暂存区
git commit -m "说明这次改了什么"   # commit 生成一个可回退的版本

说明：
- add 只是“选择要保存的内容”
- commit 才是真正保存
- commit 只发生在本地

--------------------------------
把本地分支推送到远程仓库
--------------------------------

git push -u origin yourbranch

注解：
- push：把本地提交上传到远程
- origin：远程仓库的默认名字（clone 时自动设置）
- yourbranch：当前分支名
- -u：建立本地分支和远程分支的关联

第一次推送分支必须写全：
git push -u origin yourbranch

之后可以简写为：
git push

区别说明：
- 第一次 push：需要告诉 Git 推到哪个远程、哪个分支
- 之后 push：Git 已经记住目标位置

--------------------------------
在 GitHub 上合并（merge）
--------------------------------

在 GitHub 网页上操作：

1. 打开仓库页面
2. 点击 Compare & pull request
3. 确认修改内容
4. 点击 Merge

此时远程主分支（main）已经包含你的修改。

--------------------------------
更新本地主分支
--------------------------------

git switch main
git pull

说明：
- switch main：切换回本地主分支
- pull：从远程下载并合并最新代码

会不会直接覆盖 E:\github\project ？

不会乱覆盖：
- 如果本地没有未提交修改，会直接更新文件
- 如果本地有未提交修改，Git 会提示或阻止操作

前提：本地修改已经 commit。

--------------------------------
常用检查命令
--------------------------------

git status

作用：
- 查看当前分支
- 查看哪些文件被修改
- 查看是否有未提交内容

--------------------------------
流程总结
--------------------------------

clone 项目  
→ 新建分支  
→ 修改文件  
→ add + commit  
→ push 分支  
→ GitHub merge  
→ pull 更新








