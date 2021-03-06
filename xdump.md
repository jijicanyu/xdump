# xdump.py

### Usage

```
python3 xdump.py
```

### About

```
xdump.py是一个python3下的脱库脚本,只要提供一句话webshell和相关密码就可脱库,与一般大马脱库的区别在于这里的脱库可
订制,可灵活变换代码以绕过waf,相当于用chopper的思路来脱库,不过脱库方法可订制,且比一般大马的脱库更好用,理论上
xdump.py可脱任意大小的数据库,不用担心会超时,因为xdump采用的是每次只脱部分少量数据[eg.每次脱200条数据],也可在代
码中设置每次延时一定时间再继续脱少量数据.

```

### Detail

```
支持两种脱库用法

1.不抓包模式
不抓包模式目前仅测试过mysql+php的脱库,其他类型应该暂不支持,因为不抓包模式用的是固定的php连接数据库的代码

2.抓包模式
抓包模式支持菜刀支持的所有数据库和脚本组合类型的脱库,需要抓包才能用.抓包方法如下:

a.chopper连上webshell
b.charles设置好本地sock5代理.[eg.127.0.0.1:8889]
c.proxfier设置chopper的代理为charles提供的127.0.0.1:8889
d.在chopper中配置好数据库连接参数并连接数据库
e.在chopper连上数据库后随便双击某个数据库的某个表
f.将e步骤在charles中抓取的包整理下存放在本地,整理的格式在代码中有示例,需要提供header和post两份数据,示例文件如下
link:https://github.com/3xp10it/xdump
g.运行python3 xdump.py

```
