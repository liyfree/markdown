

### 1.Linux安装Git

1. 进入Linux服务器，使用wget下载Git安装包

   `wget https://github.com/git/git/archive/v2.27.0.tar.gz`

2. 使用tar命令解压压缩文件

   `tar -zxvf v2.27.0.tar.gz`

3. 安装编译源码所需依赖，命令为

   `yum install curl-devel expat-devel gettext-devel openssl-devel zlib-devel gcc perl-ExtUtils-MakeMaker`

   出现提示，输入y

4. 安装依赖时，yum自动安装了Git，需要卸载旧版本Git，命令为： 

   `yum remove git` 出现提示输入y即可

5. 进入解压后的文件夹，命令 `cd git-2.27.0` ，然后执行编译，命令为 `make prefix=/usr/local/git all` 耐心等待编译即可

6. 安装Git至/usr/local/git路径，命令为 `make prefix=/usr/local/git install`

7. 打开环境变量配置文件，命令 `vim /etc/profile` ，在底部加上Git相关配置信息

   export PATH=$PATH:/usr/local/git/bin

8. `执行 source /etc/profile`命令，使配置文件生效

### 2.Git学习

1. 初始化仓库，使用`git init`命令
2. 添加要提交的文件 `git add a.txt`,将文件加入本次提交
3. 添加本次提交的说明、注释，将本改变提交到本地仓库  `git commit -m '本次提交说明'`
4. 比较文件不同 `git diff a.txt`
5. 使用git push 推送到远程仓库
6. 使用git pull 从仓库拉取最新代码
7. 使用git clone ‘项目地址’ 从远程仓库克隆一个项目
