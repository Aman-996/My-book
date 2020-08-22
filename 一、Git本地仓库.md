# Git的本地仓库：

## 一、配置git：

### 1、git六行配置：

```
git config --global user.name 你的英文名
git config --global user.email 你的邮箱
git config --global push.default simple
git config --global push.default simple
git config --global core.editor "code --wait"
git config --global core.autocrlf input
```

### 2、配置后对应指令:

<img src="/Users/wuyuman/Library/Application Support/typora-user-images/image-20200803210956541.png" alt="image-20200803210956541" style="zoom:50%;" />



## 二、配置环境变量：

### 1、vs code配置：

1.找到程序安装路径

2.终端中运行 vim.bashrc并进入

3.进入界面如下：

<img src="/Users/wuyuman/Library/Application Support/typora-user-images/image-20200803222330031.png" alt="image-20200803222330031" style="zoom: 50%;" />

（1）进入编辑模式（i键）；

（2）将"/Applications/Visual Studio Code.app/Contents/Resources/app/bin“路径写入终端中；

（3）或者在wuyuman文件夹中打开隐藏文件【快捷键：⌘⇧.(Command + Shift + .)】，找到.bashrc并进入复制该路径；

（4）进入执行模式（esc键），输入冒号（英文格式:），输入wq进行保存；

（5）进入终端后，写入source ~/.bashrc（进行路径保存）；

（6）写入echo $PATH（可查看写入路径）；

（7）写入code，如能启动vs code，即配置成功；

（8）code . ：打开当前目录。

or:

（1）打开wuyuman 路径下隐藏文件.bashrc；

（2）输入code执行文件路径，按command s 进行保存；

（3）进入终端，写入**source ~/.bashrc**进行路径保存。





## 三、Git 只是一个命令

### 1、git解决的问题——版本控制

（1）👧阿蔓词典：<u>**版本控制**</u>：在提交一个文件前进行复制存档，以便随时能够调用之前修改过的版本。

​          如图：

<img src="/Users/wuyuman/Library/Application Support/typora-user-images/image-20200804001036015.png" alt="image-20200804001036015" style="zoom:50%;" />

（2）git可以让代码有版本（随时可以退回到某个版本）。

### 2、git的功能

（1）git init：初始化（创建目录）

​                                       A.git init会创建.git目录

​                                       B..git作用是容纳代码”快照“

如图：

![image-20200804200751334](/Users/wuyuman/Library/Application Support/typora-user-images/image-20200804200751334.png)

（2）**git add 路径**：需要提交的变动

​                                                  A.选择哪些变动是需要提交的

​                                                  B.路径可以是绝对路径、相对路径、"."和"*"

（3）.gitignore：描述哪些变动是不需要提交的

​                                                  A.Mac中常见的有：.DS_Store

​                                                 B.其他：①node_modules；(文件太大)

​                                                                ②.idea；

​                                                                ③.vscode

（4）**git commit**  -m 字符串：提交，并说明提交理由

​                                                                                 A.如果字符串里有空格，就要用引号包起来

​                                                                                 B.字符串是中文，也要用英文格式的引号包起来

（5）git status：用于查看提交和未提交的文件

（6）git commit -v：同（4），这个命令可以帮助我们回顾改了些什么（推荐）

​                                            A：v全称为：verbose：啰嗦的

​                                            B：git commit -v --amend：查询修改历史

（7）git log:查看各个版本更改的详细信息

（8）git reset --hard xxxxxx:

​                                           A：回到某个版本

​                                           B：xxxxxx代表版本号前六位

​                                           C：必须先进行commit提交，否则将直接删除文件

（9）git reflog：

​                                           A：可查看所有提交过后的文件

​                                           B：复制文件对应的版本号进行git reset可直接回到对应版本

（10）总结：如图：

![image-20200811225326630](/Users/wuyuman/Library/Application Support/typora-user-images/image-20200811225326630.png)

（11）git branch x（分支）：

​                               A：可以创造平行时间线（分支）

​                               B：可查看当前在哪条线上

（12）git checkout x（分支）/master(主线)：

​                               A：用于切换分支

（13）总结：如图

![image-20200811232738648](/Users/wuyuman/Library/Application Support/typora-user-images/image-20200811232738648.png)

（14）git merge:合并文件