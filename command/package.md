> `.deb`是Debian软件包格式的文件扩展名

## dpkg包管理命令

__常用__

```
dpkg -i xxx 安装 DEB 包命令
dpkg -i xxx 升级 DEB 包命令（和安装命令相同）
dpkg -r xxx # 卸载 DEB 包命令（不卸载配置文件）
dpkg -P xxx # 卸载 DEB 包命令（卸载配置文件）
dpkg -l | grep xxx 检查是否安装了某个包
```

__其他__

```
dpkg-deb -c xxx 查询 DEB 包中包含的文件列表命令
dpkg –info xxx 查询 DEB 包中包含的内容信息命令
dpkg -l xxx 查询系统中所有已安装 DEB 包
```

## apt-get包管理命令

__常用__

```
apt-get install xxx 安装
apt-get remove xxx 卸载(不删除配置文件)
apt-get remove -purge xxx 卸载(删除配置文件)
apt-cache search xxx 搜索
apt-get upgrade 更新已安装的包
apt-get update 更新源索引
```

__其他__

```
apt-cache show xxx 获取包的相关信息，如说明、大小、版本等
apt-get install xxx – – reinstall 重新安装包
apt-get -f install 修复安装"-f = ——fix-missing"
apt-get dist-upgrade 升级系统
apt-get dselect-upgrade 使用 dselect 升级
apt-cache depends xxx 了解使用依赖
apt-cache rdepends xxx 是查看该包被哪些包依赖
apt-get build-dep xxx 安装相关的编译环境
apt-get source xxx 下载该包的源代码
apt-get clean && sudo apt-get autoclean 清理无用的包
apt-get check 检查是否有损坏的依赖
```

## Linux包转换工具Alien

在Debian系列中使用alien将rpm转换为deb并安装

```
alien -d package.rpm
dpkg -i package.deb
```
