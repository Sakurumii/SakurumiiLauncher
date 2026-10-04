# SKRML · SakurumiLauncher

SKRML 是 Sakurumii 自制的樱花粉主题 Minecraft 启动器（Windows）。
从下载游戏、管理版本，到装入模组与光影，所有琐碎步骤都被收进一个温柔的窗口里——你只管玩。

## ✨ 特性一览

| 功能 | 说明 |
| --- | --- |
|  **一键下载** | 原版、Fabric、Forge 全支持，选好版本点一下，依赖文件自动补齐 |
|  **LittleSkin 登录** | Yggdrasil 外置登录，皮肤与头像自动同步，进服务器就是你的模样 |
|  **模组管理** | Modrinth 资源免 Key 浏览，自动分页翻阅，找到即装，装完即玩 |
|  **光影管理** | 光影包一目了然，浏览、下载、启用一步到位 |
|  **Java 自动配置** | 自动检测本机 Java，缺什么就装什么，官方运行时一键到位 |
|  **日志实时查看** | 游戏日志实时滚动，崩溃原因一眼看清，排查不再抓瞎 |

##🎨 界面设计

- 樱花粉主题（`#f472b6` 系），支持浅色 / 深色切换
- 左侧边栏：主页 · 版本管理 · 模组管理 · 光影管理 · 设置 · 关于
- 主页集成档案卡（皮肤头像）、版本选择卡与「启动游戏」大按钮
- 版本标签颜色区分：原版（灰）、Fabric（绿）、Forge（粉）

## 🛠 技术栈

- **GUI**：CustomTkinter（樱花粉主题定制）
- **游戏核心**：minecraft-launcher-lib（版本下载、依赖解析、游戏启动）
- **打包**：PyInstaller 单文件 exe（嵌入项目根目录 `icon.png`）
- **网络**：requests（`verify=False` 绕过代理 SSL 拦截 + 自动重试）
- **官网**：Cloudflare Workers 静态站（teal 青色主题）

## 📥 下载

访问官网获取最新版本：**[skrml.sakurumii.top](https://skrml.sakurumii.top)**

> 首次进入启动器会显示制作者信息弹窗，并自动加载默认皮肤头像（苦力怕娘）。

##  运行与打包

### 环境要求

- Windows 10/11
- Python 3.10+（开发用；打包后为单文件 exe，无需 Python）

### 本地运行

```bash
