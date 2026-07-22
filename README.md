# 个人管理工作台

一个纯前端的个人管理工作台，包含锻炼打卡、减重打卡、编程学习、阅读打卡四大功能模块。支持手机桌面快捷方式，数据保存在本地浏览器。

## 功能

| 模块 | 功能 |
|------|------|
| 💪 锻炼打卡 | 每日运动打卡、运动类型/时长记录、连续天数统计、月度图表 |
| ⚖️ 减重打卡 | 每日体重记录、饮食控制打卡、体重趋势折线图 |
| 💻 编程学习 | 学习任务管理（待开始/进行中/已完成）、分类标签、每日学习时长统计 |
| 📚 阅读打卡 | 书籍管理、阅读进度条、每日阅读页数/时长记录 |
| 🏠 仪表盘 | 今日打卡概览、本周热力图、打卡趋势图、快捷打卡 |
| ⚙️ 设置 | 数据导出/导入备份、清空数据、添加到主屏幕说明 |

## 部署方法（任选一种）

### 方案一：腾讯云对象存储 COS（推荐）

1. 登录 [腾讯云控制台](https://console.cloud.tencent.com/cos)
2. 创建存储桶（选择离你近的地域，访问权限设为「公有读私有写」）
3. 上传 `index.html` 和 `manifest.json` 两个文件
4. 在存储桶 →「权限管理」→「静态网站」中开启静态网站托管
5. 访问分配的域名（类似 `https://<bucket>.cos-website.<region>.myqcloud.com`）
6. 在手机浏览器打开该域名，按下方「添加到主屏幕」操作

### 方案二：GitHub Pages（完全免费）

```bash
# 1. 创建 GitHub 仓库，如 workbench
# 2. 上传 index.html 和 manifest.json
# 3. 在仓库 Settings → Pages → Source 选择 main 分支
# 4. 等待几分钟后访问 https://<用户名>.github.io/workbench/
```

### 方案三：Cloudflare Pages（完全免费，速度快）

1. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com)
2. 进入 Pages → Create a project → Upload assets
3. 上传 `index.html` 和 `manifest.json`
4. 部署完成后获得 `https://<项目名>.pages.dev` 域名

### 方案四：Vercel（完全免费）

1. 注册 [Vercel](https://vercel.com)
2. New Project → 上传文件或关联 GitHub 仓库
3. 部署后获得 `https://<项目名>.vercel.app` 域名

## 添加到手机主屏幕

部署后用手机浏览器打开网站：

**iOS（iPhone/iPad）：**
1. 用 Safari 打开网站
2. 点击底部「分享」按钮
3. 选择「添加到主屏幕」
4. 确认后桌面会出现图标，点开即可全屏使用

**Android：**
1. 用 Chrome 打开网站
2. 点击右上角「⋮」菜单
3. 选择「添加到主屏幕」
4. 确认后桌面会出现图标

## 数据说明

- 数据保存在浏览器 localStorage 中，不会上传服务器
- 清除浏览器缓存会丢失数据，建议定期用「设置 → 导出」备份数据
- 换设备使用时，可通过「设置 → 导入」恢复备份

## 技术栈

- 纯 HTML + CSS + JavaScript（零依赖框架）
- Chart.js（CDN 引入，用于图表）
- localStorage（数据存储）
- PWA（支持添加到主屏幕）
