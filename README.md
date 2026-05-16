# Ruffle Launcher

一个基于 [Ruffle](https://ruffle.rs/) 构建的自包含、一体化 Flash 游戏启动器。  
专为轻松部署和 iframe 嵌入设计，非常适合在如 [Nextcloud](https://nextcloud.com/) 之类的应用中创建 Flash 游戏小组件。

---

## ⚠️ **重要声明** ⚠️

**本项目不包含任何受版权保护的 SWF 文件或 Flash 内容。**

此仓库仅包含 HTML、CSS 和 JavaScript 代码，用于提供加载远程 SWF 文件的界面。  
启动器本身不托管、分发或包含任何 Flash 游戏或受版权保护的内容。所有游戏文件均引用自外部来源（主要为 [Archive.org](https://archive.org/)），并在运行时动态加载。

**用户需自行确保其有权访问通过本启动器加载的任何远程 SWF 文件。**

---

## 功能特性

- **单文件集成**：所有内容都包含在一个 HTML 文件中，便于携带与部署
- **远程游戏支持**：可从任意支持 CORS 的 URL 加载 Flash 游戏
- **现代化界面**：Material Design 3 风格深色主题 UI
- **游戏库**：预置热门 Flash 游戏（Club Penguin、Papa 系列等）
- **自定义游戏**：添加并管理自己的游戏收藏
- **最近游玩**：快速访问最近玩的 3 个游戏
- **搜索功能**：跨全部分类进行全局搜索
- **分辨率控制**：支持预设与自定义分辨率
- **视图模式**：支持窗口填充与全屏模式
- **隐私控制**：一键清除全部启动器数据
- **URL 参数**：支持丰富的嵌入与自定义参数

## 在线演示

在线体验：

**[https://ruffle-launcher-5a5a1e.gitlab.io/](https://ruffle-launcher-5a5a1e.gitlab.io/)**

**iframe 嵌入注意事项：**  
由于跨域限制，GitLab Pages 演示版在不同域名 iframe 中可能无法正常运行（例如从自托管服务器嵌入）。  
如果需要 iframe 嵌入（例如 Nextcloud 小组件），请根据下面的 [快速安装](#quick-installation) 将启动器部署到自己的域名。

## 截图

截图来自 Nextcloud 仪表盘中的 [iFrame Widget](https://apps.nextcloud.com/apps/iframewidget)

<img src="./.screenshots/pizzatron_3000_example.png" width="800">

<img src="./.screenshots/cart_surfer_example.png" width="800">

<img src="./.screenshots/papas_freezeria_example.png" width="800">

## 快速安装

使用一条命令即可部署启动器：

```bash
# 创建目录
sudo mkdir -p /var/www/html/ruffle

# 下载启动器
sudo curl -Lo /var/www/html/ruffle/ruffle_launcher.html https://gitlab.com/nickgirga/ruffle-launcher/-/raw/master/public/index.html
