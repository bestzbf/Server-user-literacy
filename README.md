# Server-user-literacy
服务器用户指南


# 服务器用户扫盲

用户数据在/home/你的名字缩写 （如/home/zbf）

数据集数据放在/mnt/d/data/

## conda环境

可以看到已有的conda环境

```
conda env list
```

可以看到我的模板环境pt_cuda118（torch版本2.1.2   ）

克隆一个自己的环境

```
conda create --name 你的环境名 --clone pt_cuda118
```

示例

```
conda create --name zbfhj --clone pt_cuda118
```

模板环境torch版本2.1.2   如不兼容自己创对应版本torch的conda环境，注意cuda版本为11.8



## 上传下载文件到本地

#### 登入自己百度云

首次运行时，需进行百度云的 OAuth2 授权：

```
bypy info
```

运行后，命令行会输出一个 URL。

打开 URL，在浏览器中登录百度账号，授予权限后，将生成的授权码复制到命令行中。


#### 下载文件到本地

##### 下载单个文件：

```
bypy download <远程文件路径> [本地保存路径]
```


示例：

```
bypy download /apps/bypy-folder/example.txt ./downloads/
```

bypy download /apps/bypy-folder/example.txt ./downloads/

##### 下载整个文件夹：

```
bypy download <远程文件夹路径> [本地保存路径]
```

示例：

示例：

```
bypy download /apps/bypy-folder ./downloads/
```

#### 上传文件到百度云

##### 上传单个文件：

```
bypy upload <本地文件路径> [远程目标路径]

```

示例：

```
bypy upload example.txt /apps/bypy-folder/
```

##### 上传整个文件夹：

```
bypy upload <本地文件夹> [远程目标路径]
```


示例：

```
bypy upload ./local-folder /apps/bypy-folder/
```

##### 其他操作参考[csdn](https://blog.csdn.net/m0_61565919/article/details/144958325)

