<!--
 * @Author: shouxie
 * @Date: 2020-04-27 15:29:26
 * @Description: 
 -->
# redis_note
up!up!up!

#### redis-菜鸟教程

> REmote DIctionary Server(Redis) 是一个由Salvatore Sanfilippo写的key-value存储系统。
Redis是一个开源的使用ANSI C语言编写、遵守BSD协议、支持网络、可基于内存亦可持久化的日志型、Key-Value数据库，并提供多种语言的API。
它通常被称为数据结构服务器，因为值（value）可以是 字符串(String), 哈希(Hash), 列表(list), 集合(sets) 和 有序集合(sorted sets)等类型。

开源免费的
遵守BSD协议
高性能的key-value数据库。

**Redis 与其他 key - value 缓存产品有以下三个特点：**

- Redis支持数据的持久化，可以将内存中的数据保存在磁盘中，重启的时候可以再次加载进行使用。
- Redis不仅仅支持简单的key-value类型的数据，同时还提供list，set，zset，hash等数据结构的存储。
- Redis支持数据的备份，即master-slave模式的数据备份。

**Redis 优势**
- 性能极高 – Redis能读的速度是110000次/s,写的速度是81000次/s 。
- 丰富的数据类型 – Redis支持二进制案例的 Strings, Lists, Hashes, Sets 及 Ordered Sets 数据类型操作。
- 原子 – Redis的所有操作都是原子性的，意思就是要么成功执行要么失败完全不执行。单个操作是原子性的。多个操作也支持事务，即原子性，通过MULTI和EXEC指令包起来。
- 丰富的特性 – Redis还支持 publish/subscribe, 通知, key 过期等等特性。

**Redis与其他key-value存储有什么不同？**
1. Redis有着更为复杂的数据结构并且提供对他们的原子性操作，这是一个不同于其他数据库的进化路径。Redis的数据类型都是基于基本数据结构的同时对程序员透明，无需进行额外的抽象。

2. Redis运行在内存中但是可以持久化到磁盘，所以在对不同数据集进行高速读写时需要权衡内存，因为数据量不能大于硬件内存。在内存数据库方面的另一个优点是，相比在磁盘上相同的复杂的数据结构，在内存中操作起来非常简单，这样Redis可以做很多内部复杂性很强的事情。同时，在磁盘格式方面他们是紧凑的以追加的方式产生的，因为他们并不需要进行随机访问。


#### redis 安装
1. 官网下载压缩包（下载 stable 版本，稳定版本。）
2. 安装到/usr/local 进行解压
```shell
## 解压：
tar zxvf redis-5.0.3.tar.gz
# 移动到： 
mv redis-5.0.3 /usr/local/
# 切换到：
cd /usr/local/redis-5.0.3/
# 编译测试 
sudo make test
# 编译安装 
sudo make install
```

mac 配置redis环境变量
添加：export PATH=$PATH:/usr/local/redis-5.0.3/
```shell
open .bash_profile
source .bash_profile
```

启动：redis-server
测试redis
新建一个终端窗口，输入命令行redis-cli

安装redis客户端：
redis客户端在官网是要收费的，好在作者也是比较良心，开源了项目，可以去github上下载测试版。