## Linux系统SSH客户端断开后保持进程继续运行配置方法

1. 在命令头尾分别加上 `nohup` 和 `&`，`nohup` 会输出程序的 PID，PID 可用于需要中断进程时结束进程，再按一下回车键就跳回 `shell` 命令行

   ```
   nohup python test.py &
   ```

2. 通过如下命令，可以持续的查看 `nohup.out` 的输出，达到监视程序的效果

   ```
   tail -f nohup.out
   ```

3. 通过重定向将程序的输出改为自己想要的文件名 `test.out`

   ```
   nohup python test.py >test.out &
   ```

4. 可以使用 `kill` 命令结束进程

   ```
   kill [PID]			// PID 程序号
   -9					// 强制杀
   ```



## ps 命令 显示进程状态

```
ps [options] [--help]
```

##### 参数

- `-A` 列出所有的进程
- `-w` 显示加宽可以显示较多的资讯
- `-au` 显示较详细的资讯

##### 通过端口号查看进程

```
lsof -i:端口号
```

##### 查找指定进程格式

```
ps -ef | grep 进程关键字			//可以是 python php 
```

##### 显示指定用户信息

```
ps -u y
```





## ubuntu 防火墙

1.  查看防火墙状态

   ```
   sudo ufw status
   ```

2. 开启防火墙

   ```
   sudo ufw enable
   ```

3. 关闭防火墙

   ```
   sudo ufw disable
   ```

4. 查看防火墙版本

   ```
   sudo ufw version
   ```

5. 默认允许外部访问本机

   ```
   sudo ufw default allow
   ```

6. 默认拒绝外部访问主机

   ```
   sudo ufw default deny
   ```

7. 允许外部访问 53 端口

   ```
   sudo ufw allow 53
   ```

8. 拒绝外部访问53端口

   ```
   sudo ufw deny 53
   ```

9. 允许某个IP地址访问本机所有端口

   ```javascript
   sudo ufw allow from 192.168.0.1
   ```



























