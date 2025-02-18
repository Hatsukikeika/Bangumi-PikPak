# 项目说明

<p align="center">
    <img title="mikan project" src="https://mikanani.me/images/mikan-pic.png" alt="" width="10%">
    <img title="pikpak" src="https://raw.githubusercontent.com/YinBuLiao/Bangumi-PikPak/main/img/pikpak.png">
</p>

***

本项目是基于 [Mikan Project](https://mikanani.me)、[PikPak](https://mypikpak.com/) 的全自动追番整理下载工具。只需要在 [Mikan Project](https://mikanani.me) 上订阅番剧，就可以全自动追番。

## Bangumi-PikPak 功能说明

- 简易单次配置就能持续使用
- 无需介入的 `RSS` 解析器，解析番组信息并且自动生成下载规则。
- 根据番剧更新时间进行整理
- 无需维护完全无感使用
- 对于 Mikan RSS 的反代支持。

## 使用Alist将PikPak中的番剧列出

- 列出方法:https://alist.nn.ci/zh/guide/drivers/pikpak.html

## 开发中的功能

- 全自动重命名
- 根据番剧名称进行分类
- 指定番剧补番

## 配置教程
- 使用的Python版本需为3.10或更高
- 编辑`main.py`**同目录**下的`config.json`
  ```
  "username": "用户名",
  "password": "密码",
  "path": "文件夹ID",
  "rss": "RSS链接"
  ```
  注意转义，若密码为`1\2"\"`，需写成`1\\2\"\\\"`

- 开机自动启动:
  
  完成编辑之后，可以通过安装Pyinstaller来生成可执行文件
  ```
  pip install pyinstaller
  ```
  然后运行
  ```
  pyinstaller --onefile --noconsole main.py
  ```
  **如果想要界面，删去`--noconsole`参数**

  生成的可执行程序保存在dist目录下，将其加入启动项（创建任务计划程序/写入注册表/放入启动文件夹）



## 常见问题

### 文件夹ID:

可以通过 https://mypikpak.com/ 获取。

![截图](https://raw.githubusercontent.com/YinBuLiao/Bangumi-PikPak/main/img/b5900bc5d4695980707fda98f5c3e84a.png)

### RSS链接:

订阅番剧后，在「首页」分类的右下角，复制「RSS 订阅 」旁的图标内的链接。

蜜柑计划的 RSS 只记录了开始订阅番剧后更新的内容，并且 RSS 更新有些许延迟，请耐心等待。

![截图](https://raw.githubusercontent.com/YinBuLiao/Bangumi-PikPak/main/img/781e0a53fdf5aa6a1ea44c291e98c012.png)

请注意，RSS 订阅的链接格式应为：https://mikanani.me/RSS/MyBangumi?token=xxx%3d%3d 。
