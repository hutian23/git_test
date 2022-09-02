# 查看配置信息

### --local：仓库级，--global：全局级，--system：系统级

```git config <--local | --global | --system> -l```

# 查看当前生效的配置信息

```git config -l```


# 配置提交记录中的用户信息

`git config --global user.name <用户名>`

`git config --global user.email <邮箱地址>`


# 更改Git缓存区的大小

如果提交的内容较大，默认缓存较小，提交会失败

缓存大小单位：B，例如：524288000（500MB）

`git config --global http.postBuffer <缓存大小>`


# 克隆

默认在当前目录下创建和版本库名相同的文件夹并下载版本到该文件夹下

`git clone <远程仓库的网址>`

-b 指定要克隆的分支，默认是master分支

`git clone <远程仓库的网址> -b <分支名称> <本地目录>`

## 初始化项目所在目录,用于在目录中创建新的git仓库

```git init```

所有有关此项目的快照数据都存放在这里.(.git 默认隐藏)

`git status` 查看本地仓库的状态
<br>
<br>
<br>

# 操作远程仓库

`git remote`列出存在的远程仓库

`git remote -v` 仓库详细信息

`git remote add <远程仓库的别名> <远程仓库的URL地址>`    ***添加远程仓库***

`git remote rename <现名> <新名>` 修改名称

`git remote remove <远程仓库的别名>` 删除远程仓库


# 分支命令

`git branch -v` 列出本地所有分支并显示最后一次提交

`git branch <分支名>` 创建新分支，基于上一次提交建立

# git add

```
# 把指定的文件添加到暂存区中
$ git add <文件路径>

# 添加所有修改、已删除的文件到暂存区中
$ git add -u [<文件路径>]
$ git add --update [<文件路径>]

# 添加所有修改、已删除、新增的文件到暂存区中，省略 <文件路径> 即为当前目录
$ git add -A [<文件路径>]
$ git add --all [<文件路径>]

# 查看所有修改、已删除但没有提交的文件，进入一个子命令系统
$ git add -i [<文件路径>]
$ git add --interactive [<文件路径>]

```