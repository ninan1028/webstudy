### git使用的一些记录

#### 初始化
>进入相应的目录 在 git bash命令行工具中 使用
  '$ git init'
#### 将本地文件加入版本库 
* '$ git add filename' 
* '$ git commit -m 'remark''
***

git add 后面可以输入多个文件的名字 用空格分隔

> git log  查看版本日志 
> 还可以使用 git log --pretty=online 来查看排版后的日志
#### 回退到以前的版本
首先，Git必须知道当前版本是哪个版本，在Git中，用HEAD表示当前版本，也就是最新的提交3628164...882e1e0（注意我的提交ID和你的肯定不一样），上一个版本就是HEAD^，上上一个版本就是HEAD^^，当然往上100个版本写100个^比较容易数不过来，所以写成HEAD~100。
'$ git git reset -- hard HEAD^'

