# 「linux」家中常备 linux CL

> CL (Command Line)

最近对 Linux 有了需要

以前不擅长记录，现在为此补充一下

## scp

scp <from\> <to\>  
scp -i <pem\> <from\> <to\>

### directory

scp -r <from\> <to\>
scp -r a_dir root@server:/keep_in_this_dir

## cp

cp <from\> <to\>

## ssh

```sh
ssh -i <pem\> user@server <<eeooff
#############
# some code #
#############
exit
eeooff
```

关于<< eeooff的含义

```sh
cmd << text
 ...
 ...
 ...
 text
```

> 从命令行读取输入，直到遇到与text相同的行结束。

```sh
#带参数本地脚本
ssh root@xxx.xxx.xxx.xxx 'bash -s' < test.sh helloworld

#执行远程服务器上的脚本
ssh root@xxx.xxx.xxx.xxx "/home/nick/test.sh"

#执行远程服务器上带参数的脚本
ssh root@xxx.xxx.xxx.xxx /home/nick/test.sh helloworld
```

或许日后结合nodejs整理一个库，叫space-terminal.
