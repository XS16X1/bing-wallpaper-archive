# 📸 bing-wallpaper-archive

本项目旨在归档2016-03-05至今的必应每日壁纸json数据，同时提供批处理下载器以便进行下载。

总图片数：**3682**

最新数据日期：**20260402**

## 🚀 功能特色

### 必应json数据

- ✅ 配套 JSON 数据使用 GitHub Actions 每日北京时间 00:00 自动更新

### 批处理下载器

- ✅ 支持分辨率选择：原图、4K、2K、1080P 或自定义尺寸
- ✅ 支持按时间范围批量下载
- ✅ 按照年份存放下载的图片
- ✅ 自动跳过已下载文件，避免重复下载
- ✅ 所有图片均通过官方进行下载

注：

- 20190510之前的壁纸只提供下载1080P分辨率
- https://cdn.bimg.cc 域名官方不支持下载，这是欠费了？
---

## 📦 项目结构

```text
📁 项目根目录
├── 20**/                           # 每天划分的 JSON 数据
├── Bing_zh-CN_all.json             # 所有已归档的必应壁纸 JSON 数据
├── update_bing.sh                  # Bash 脚本：自动下载并合并 JSON 数据
├── bing-wallpaper-downloader.bat   # Windows 批处理脚本，支持交互下载壁纸
└── .github/workflows
    └── update-bing.yml             # GitHub Actions 自动每日更新任务
```

## ⚙️ 使用方式

- 方式一：下载[release](https://github.com/Zhu-junwei/bing-wallpaper-archive/releases/)中的[bing-wallpaper-downloader.bat](https://github.com/Zhu-junwei/bing-wallpaper-archive/releases/download/v1.3/bing-wallpaper-downloader.bat)脚本运行后按照提示下载图片。
- 方式二：下载[release](https://github.com/Zhu-junwei/bing-wallpaper-archive/releases)中的`bing-wallpaper-archive-20xx.zip`图片压缩包。
- 方式三：根据项目的json数据构建自己的下载程序

## 📥 数据获取

GitHub：

```
# 全量数据
https://raw.githubusercontent.com/Zhu-junwei/bing-wallpaper-archive/master/Bing_zh-CN_all.json
# 指定日期数据
https://raw.githubusercontent.com/Zhu-junwei/bing-wallpaper-archive/master/2025/07/20.json
```

jsdelivr：

```
# 全量数据 cdn加速
https://cdn.jsdelivr.net/gh/Zhu-junwei/bing-wallpaper-archive/Bing_zh-CN_all.json
# 如果cdn不是最新数据，建议使用下面链接重置
https://purge.jsdelivr.net/gh/Zhu-junwei/bing-wallpaper-archive/Bing_zh-CN_all.json

# 指定日期数据 cdn加速
https://cdn.jsdelivr.net/gh/Zhu-junwei/bing-wallpaper-archive/2025/07/20.json
```

## ⚠️ 注意事项

- 可能存在有些图片无法下载的现象，请自行测试。
- 通过git下载的bat文件可能存在换行符是`LF`的情况，需要手动调整，或通过本项目的release进行下载。

## 💖 鸣谢

项目前期初始数据来自[flow2000/bing-wallpaper-api](https://github.com/flow2000/bing-wallpaper-api)
