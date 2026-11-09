# Cwatch

Cwatch 是 Ubuntu 上的实时调参工具，不依赖于ros实现，因而可以实现所有全局变量的观察与修改，相当于单片机keil中的watch功能，弥补了rqt等传统ros调试工具的缺陷，大大提升了机器人上位机调参的便捷性。

## 下载与安装

[Cwatch 0.2.0 安装包](https://github.com/Wu-Cyrus/Cwatch/releases/download/v0.2.0/cwatch_0.2.0-1_amd64.deb) 

适用 Ubuntu 22.04 amd64。在下载目录执行：

```
sudo apt install ./cwatch_0.1.0-1_amd64.deb
```


```sh
cd /usr/lib/cwatch
/usr/bin/python3 -c 'from pathlib import Path; import sys; from robotwatch.python_backend import enable; enable(Path(sys.argv[1]),Path(sys.argv[2]))' /path/to/project /path/to/venv/bin/python
```

本仓库提供闭源应用的发行文件和使用说明，第三方组件的许可证随包安装在 `/usr/share/doc/cwatch/licenses/`。
