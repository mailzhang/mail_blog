

# git 常见问题
## fatal: unable to access 'https://github.com/nefulan/MyVuepress.git/': Failed to connect to github.com port 443: Timed out
```shell
git config --global --unset http.proxy
git config --global --unset https.proxy
```

OpenSSL SSL_read: Connection was reset, errno 10054
```shell
git config --global http.sslVerify "false"
```

# mac安装brew包错
## curl: (7) Failed to connect to raw.githubusercontent.com port 443: Connection refused
https://zhuanlan.zhihu.com/p/115450863
```shell
# 7890 和 789 需要换成你自己本地监听的端口
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:789
```


# 为终端配置代理

背景：使用 ssr 时，网页软件可以正常使用；但命令窗口无法通过代理，例如拉取 github 时网络超时

启动命令
```shell
1087 为 ssr 本地代理端口
HTTP 使用此命令：

export http_proxy=http://127.0.0.1:1087
HTTPS 使用此命令：

export https_proxy=http://127.0.0.1:1087
```
查看代理
```shell
echo $http_proxy
echo $https_proxy
```

取消命令
```shell
unset http_proxy
unset https_proxy
```

macos文件改动

```shell
.zprofile 
.zshrc  

```