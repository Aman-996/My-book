# Git远程仓库

👧远程仓库：将本地仓库文件上传至github等诸如此类的网站中进行保存，类似于“云端保存”。

👧rm-rf/：运行此命令会导致磁盘内容全被删除。

👧Repo：远程仓库简称

👧GitHub：用来备份.git/文件而已

## 一、github

### 1、我的github网址

https://github.com/Aman-996

### 2、上传文件

①建立远程仓库文件夹，如图：

<img src="/Users/wuyuman/Library/Application Support/typora-user-images/image-20200822133455239.png" alt="image-20200822133455239" style="zoom:50%;" />

**注：创建过程中不要修改其余选项，除属实需要以外。**

②复制github远程仓库地址至命令行（**在https和ssh地址中选择<u>ssh</u>地址**，使用https会重复输入密码），如图：

![image-20200822133839581](/Users/wuyuman/Library/Application Support/typora-user-images/image-20200822133839581.png)

②返回远程仓库文件夹，本地仓库中的文件就已经出现在此了，如图：

<img src="/Users/wuyuman/Library/Application Support/typora-user-images/image-20200822134208690.png" alt="image-20200822134208690" style="zoom:50%;" />

③上传其他分支的方式：

方法一：git push origin X:X（左边X代表源头，右边X代表目标）

方法二：git checkout X

​               git push -u origin X



### 3、git remote

1、git remote add 仓库名（默认为origin，注：上传新的文件，需重新命名一个新的仓库名）可创建一个新的远程仓库；

2、git remote 可用于查看当前远程库；

3、git remote -v / --verbose 可查看详细信息;

4、git remote remove 仓库名：可删除对应的远程仓库文件夹。



### 4、git pull

1、在进行上传时，如果提示需要用到git pull，就运行；

2、它的作用是：取回远程主机某个分支的更新，再与本地的指定分支合并；

3、如远程仓库中代码有所变动，就需要先git pull。



### 5、git push

1、命令用于将本地分支的更新；

2、上传文件至远程仓库。



### 6、git clone

1、自己的代码最好用SSH地址，别人的代码只能用HTTPS进行下载；

2、git clone 地址，进行克隆（下载）远程仓库中的文件；

3、如需下载其他分支文件，应先cd进入对应目录；

4、没有办法下载某个分支，只能下载整个仓库，然后git checkout分支名或者通过一些复杂的命令；

5、git clone <u>git@?/xxx.git</u>：会在当前目录下创建一个xxx目录；

6、git clone <u>git@?/xxx.git</u>  <u>yyy</u>：会在本地新建yyy目录；

7、git clone <u>git@?/xxx.git</u> .：不会新建目录，使用当前目录容纳代码和.git（末尾是一个“.”符号，注意空格，最好是放入一个空目录中，不建议采用）。



