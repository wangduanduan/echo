# 安装依赖包

```
go get -u github.com/labstack/echo/...
go get github.com/codegangsta/gin
```

中间可能遇到的问题，这些问题都可以通过搜索解决

1. 安装某些包超时
2. GOPTAH没有设置对之类的

安装包说明
- echo是一个web框架
- gin可以用来在代码改变时，重新运行服务

# 运行服务

```
./dev.sh
```

在浏览器中打开localhost:3000，可以看到hello, world!。

修改serve.go的代码，然后刷新页面，可以有新的输出。

# gin的说明

当用gin去启动serve.go时，就不能直接通过serve监听的端口去访问服务，而需要通过gin的端口访问服务。

其中gin的默认端口是3000， gin代理的serve端口是3001。所以如果你的服务运行的端口如果不是3001，你就需要用--appPort去指定端口值。

--port value, -p value        port for the proxy server (default: 3000)
--appPort value, -a value     port for the Go web server (default: 3001)

