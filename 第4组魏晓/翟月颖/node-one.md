# 要点：
## 1、
- 在Node中每个文件执行前，会套用一个闭包函数，在这个函数中this指向发生了变化
```
 计算客户端访问服务器端所用的时间、代码所用的时间
 console.timeEnd()
```

- 挂载在global对象上的属性 可以在任何模块中使用

- node主线程是单线程的，进程中包含线程，node中一个进程只能包含一个线程,允许开子进程
## 2、js中模块
- (seajs cmd,requirejs amd,node commonjs)
- cmd 就近依赖，amd 依赖前置
## 3、commonjs优点：
- 提高了可维护性，有利于分工协作，高内聚低耦合
###### 如何定义模块:
- 创建一个js文件，每个文件就是一个模块，多个模块可以组成一个包
###### 如何导出一个模块
- exports/module.exports
###### 如何使用一个模块
- require
#### 3.发布自己的包
- package.json
    - name不能和已发布的包重名
    - main里对应的主文件件写一个
- 发布要切换到npm
- 添加用户 有的话可以登录
```
npm addUser
```
- 发布
```
npm publish
```
- 卸载包
```
npm unpublish  --force
```
## 4、模块的查找机制

> 为什么-g安装的可以在命令行下使用,npm可以在命令行下使用，所有的全局包 都安装在npm上，会在npm下创建一个脚本文件，可以映射到真实的文件上，所以通过全局安装的可以直接在命令行下使用

## bower(管理前端文件的)
npm(管理node模块的) ->安装的文件放到node_modules下 不能指定安装目录
bower(管理前端文件的) ->制定目录下载 只管理前端文件(在git中下载)
```
npm install bower -g
```
### 1.1初始化 bower.json记录依赖
```
bower init
```
### 1.2下载文件
```
bower install bootstrap --save
```
### 1.3 指定目录
```
.bowerrc
{"directory":"src/public/lic"}
```


> 默认安装到bower_component下

### 发布hexo
```
npm install hexo-cli -g
```

### 生成blog
```
hexo init
```

### 启动服务
```
hexo server
```

### 文章放在_posts下
md格式文件

### 仓库名
```
github名.github.io
```

### 发布到git上需要下载一个插件
```
npm install hexo-deployer-git --save
```

### 配置_config.yml
```
deploy:
  type: git
  repo: https://username:password@github.com/zuyuan/zuyuan.github.io.git
  branch: master
  message: push
```

## 如果重新提交
### 生成
```
hexo g
```

### 发布
```
hexo deploy
```

### 访问网址
```
zuyuan.github.io
```