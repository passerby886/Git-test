# Git-test

#用于git测试

# 创建git流程

* git init（git仓库初始化）
* git clone http......（从github中克隆代码到本地）
* git add <files>（将工作区的文件添加到暂存区）
* git commit -m "提交描述"（将暂存区的文件添加到本地仓库）



# 回退版本

* git reset的三种模式（回退到上一个版本）
* git reset --soft（保留工作区和暂存区的内容）
* git reset --hard（不保留工作区和暂存区的内容）
* git reset --mixed（保留工作区但不保留暂存区的内容）



# 比较内容

* git diff（比较工作区\&暂存区的版本内容是否一致）
* git diff HEAD（比较工作区\&本地仓库的版本内容是否一致）
* git diff --cached（比较暂存区\&本地仓库的版本内容是否一致）
* git diff <版本ID1> <版本ID2> （比较两个版本之间的内容是否一致）
* git diff HEAD~ HEAD（比较上一个版本和当前版本的内容是否一致， HEAD~和HEAD^都表示上一个版本， HEAD~2表示head之前两个版本）
* git diff HEAD~3 HEAD file3（比较head之前的第三个版本和当前版本的file3文件的差异）
* git diff <分支1> <分支2> （比较两个分支之间的差异）



# 删除文件

* rm file; git add file（linux中自带的删除文件的命令，将工作区的文件删除后，将消息告知暂存库，然后同步删除）
* git rm <file> （git提供的方便的方式，直接删除工作区和暂存库的文件文件）
* git rm --cached <file> （只从暂存区删除文件，保留工作区的文件）
* git rm -r\*（递归删除某个目录下所有子目录和文件，删除后需要提交git commit -m "删除目标目录及其内容"  # 备注信息写清楚删除的是什么）



# 查看文件

* git ls-tree -r HEAD --name-only（查看版本库中的文件）
* git ls-files（查看被跟踪的文件（暂存区），若提交过，则版本库中也有一部分）



# 忽略文件

* .gitignore中添加所有日志文件，临时文件，敏感文件等不需要添加到暂存区的文件，将需要忽略的文件名放到.gitignore中，提交的时候就只有.gitignore文件

# SSH key
- 生成ssh key命令：ssh-keygen -t rsa -b 4096，然后再根目录29594@dds MINGW64 ~/.ssh/：中生成drwxr-xr-x 1 29594 197609    0 Dec  4 16:07 ./
drwxr-xr-x 1 29594 197609    0 Dec  4 16:07 ../
-rw-r--r-- 1 29594 197609   55 Aug  1 12:36 config
-rw-r--r-- 1 29594 197609 3369 Dec  4 15:59 id_rsa
-rw-r--r-- 1 29594 197609  735 Dec  4 16:07 id_rsa.pub
-rw-r--r-- 1 29594 197609  840 Aug  1 12:43 known_hosts
-rw-r--r-- 1 29594 197609   96 Aug  1 12:43 known_hosts.old
其中config配置ssh登录github的域名端口，rsa私钥等，rsa.pub是ssh登录GitHub的公钥，在github设置中设置后，就可以通过命令行在本地ssh连接github

- 克隆仓库：git clone <repo-address的ssh连接>（或者直接使用https克隆也行）
- 推送更新内容：git push <remote> <branch>
- 拉取更新内容： git pull <remote>

# 拉取远程仓库
- 在本地 Git 仓库中，添加一个名为origin的远程仓库关联，核心是让本地仓库和远程 GitHub 仓库建立连接，后续能通过git push（推送代码）、git pull（拉取代码）等命令和远程仓库交互：git remote add origin git@github.com:passerby886/Git-test.git
- 


