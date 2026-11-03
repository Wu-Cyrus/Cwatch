# Cwatch

Cwatch 是 Ubuntu 上的实时调参工具，可以实现变量的观察与修改，相当于单片机keil中的watch功能，配合plotjugger使用最佳。

## 下载与安装

[Cwatch 0.1.0 安装包](https://github.com/Wu-Cyrus/Cwatch/releases/download/v0.1.0/cwatch_0.1.0-1_amd64.deb) · [SHA-256 校验文件](https://github.com/Wu-Cyrus/Cwatch/releases/download/v0.1.0/SHA256SUMS)

适用 Ubuntu 22.04 amd64。在下载目录执行：

```sh
sha256sum -c SHA256SUMS
sudo apt install ./cwatch_0.1.0-1_amd64.deb
```

从应用菜单打开 **Cwatch**。在“文件”中选择工程或打开已保存的 `.cwatch` 文件，用终端或 VS Code 启动目标。双击当前值可输入数值或算式，按 Enter 写入并回读。

- **C/C++**：首次验证建议使用 `-g -O0` 构建。支持有固定对象入口的全局变量、静态变量、普通成员和定长数组。多个实例时可手动选择。
- **Python**：本包提供 CPython 3.10、3.11 的观察桥。要在自己的可写虚拟环境中启用，请替换以下两个绝对路径，然后重新启动目标程序。

```sh
cd /usr/lib/cwatch
/usr/bin/python3 -c 'from pathlib import Path; import sys; from robotwatch.python_backend import enable; enable(Path(sys.argv[1]),Path(sys.argv[2]))' /path/to/project /path/to/venv/bin/python
```

本仓库提供闭源应用的发行文件和使用说明，第三方组件的许可证随包安装在 `/usr/share/doc/cwatch/licenses/`。
