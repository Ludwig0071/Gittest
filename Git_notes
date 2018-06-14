### 1. git add 命令添加所有改动内容
git add xx命令可以将xx文件添加到暂存区，如果有很多改动可以通过 git add -A .来一次添加所有改变的文件。

注意 -A 选项后面还有一个句点。 git add -A表示添加所有内容， git add . 表示添加新文件和编辑过的文件不包括删除的文件; git add -u 表示添加编辑或者删除的文件，不包括新添加的文件。

### 2. Git 提交时报错warning: LF will be replaced by CRLF in ××××.××
第一次提交时可能会出现
```bash
warning: LF will be replaced by CRLF
# 在xxx.xx文件中LF将被CRLF替换

# 注：
# LF：Line Feed 换行
# CRLF：Carriage Return Line Feed 回车换行键
```
虽然只是个warning 也还是可以提交

处理方法：配置选项修改 把core.autocrlf 设置成false
``` bash
git config –global core.autocrlf true #这个是转换，也是默认值
git config –global core.autocrlf input #貌似是上库转换，从库中迁出代码不转换
git config –global core.autocrlf false #这个一般是window上的，不转换
```

### 3.Git切换远程仓库地址
方法一：修改命令<br>
``` bash
git remote set-url origin url
```
方法二：先删后加
``` bash
git remote rm origin
git remote add origin git@github.com:sheng/demo.git
```
方法三：修改config文件<br>
.git文件夹 --> config文件 --> 修改git remote origin地址

方法四：通过第三方git客户端修改

### 4.删除git远程库中已存在的文件,并且在本地保留
1. 备份项目
2. git rm --cached xxxx //从版本库中删除xxxx文件，但在工作目录中仍然保留。可以使用
git rm -r --cached directory_name递归删除目录
3. 在.gitignore中添加要忽略的文件
4. 把修改的文件commit并且push到服务端
5. 从git上重新拉取这个项目。