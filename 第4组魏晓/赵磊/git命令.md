## git
####告诉git你是谁
```
git config --global user.name xxxx
git config --global user.email xxxx@qq.com
git config --list
```

####初始化git
```
git init
```

####创建并且进入目录
```
mkdir gitTest && cd gitTest
```

####显示所有的文件
```
ls -al 显示隐藏的
```

####创建文件
```
touch xxx.txt
cat xxx.txt 查看内容
```

####查看git状态
```
git status
```

####添加到缓存区
```
git add .
```

####提交到历史库
```
git commit -m '描述信息'
```

####对比代码
```
git diff  工作区和暂存区
git diff --cached  暂存区和历史区
git diff master(分支名称)  工作区和历史区
```

####查看日志
```
git log  过多时可以使用上下键查看，不想看的时候，按q退出
```

####查看所有的日志
```
git reflog
```

####回滚，回到某个版本
```
git reset --hard xxxxxx(版本号)
```

####vi编辑
```
vi xxx.txt
i 编辑模式
esc + ：wq 保存并退出， 强制退出 q！
```

####分支管理
```
git branch  查看分支
git branch xxx  创建分支
git checkout xxx  切换分支
git branch -D xxx  删除分支（不能在当前分支删除自己）
git checkout -b xxx  创建并且切换（相当于将当前的内容克隆一份）
git merge xxx  在当前的分支上，去合并另外一个分支xxx

产生冲突的时候，要去手动解决提交新的代码
```

####在github上创建新的仓库
- 创建新的空仓库
```
new repository
```
- 本地要创建一个README.md 和 .gitignore
```
echo '.idea' >> .gitignore
echo 'welcome' >> README.md
echo 'hellow' > README.md 
一个>和两个>的区别是，一个>是新写的内容把旧的内容覆盖了，两个>>是在那个文件里继续追加内容
```
- 提交并关联仓库
```
git add .
git commit -m 'xxx'
git remote add origin xxxxxxxx（地址）
git remote -v  查看所有的关联
```