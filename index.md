# Mac 安装MongoDB 

## 1、[下载压缩包](https://fastdl.mongodb.org/osx/mongodb-osx-ssl-x86_64-4.0.0.tgz)
   下载地址：https://fastdl.mongodb.org/osx/mongodb-osx-ssl-x86_64-4.0.0.tgz

## 2、解压

## 3、修改文件名称 mongodb

## 4、把重命名之后的mongodb文件夹复制到/usr/local目录下
   快捷键：**`shift + command +G`**

## 5、修改环境变量 

**打开配置文件**

```sh
$ open -e .bash_profile
```

 **添加内容**

```
export PATH=${PATH}:/zhangjinxiu/Documents/my/mongodb/bin
```

## 6、添加文件夹
  ```sh
$ sudo mkdir -p data/db
  ```

## 7、启动服务
切换到`mongodb/bin`目录下 
 打一个`terminal`命令行工具  执行命令 

```sh
$ sudo ./mongod
```

## 8、进入mogodb环境
打一个`terminal`命令行工具 
打一个`terminal`命令行工具 执行命令 

```sh
$ sudo ./mongo
```

## 9、关闭mongodb服务
使用命令 `use admin` 切换到`admin`

使用命令 `db.shutdownServer();` 关闭`mogodb`服务  

 

# MongoDB 可视化管理工具使用
**1、下载工具 直接使用** 
https://studio3t.com/download/?utm_source=knowledge-base&utm_medium=button

**2、克隆 https://github.com/mrvautin/adminMongo** 
安装 

```sh
$ npm i
```


启动

```sh
$ npm start 
```

浏览器输入网址http://127.0.0.1:1234查看

*查看[MongoDB 用户名密码登录](https://www.jianshu.com/p/79caa1cc49a5)介绍*

# 备注
`MongoDB`官网： https://docs.mongodb.com/manual/installation/
`mongodb`进程号的查找方式：

```sh
$ ln -s /data/db/mongod.lock ./mongodb.pid
$ cat ./mongodb.pid
```
> mongodb的data目录下mongod.lock中记录了pid
