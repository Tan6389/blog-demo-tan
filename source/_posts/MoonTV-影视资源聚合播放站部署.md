---
abbrlink: ''
ai: null
aplayer: null
aside: null
background: '#fff'
categories:
- 前端
comments: null
copyright: null
copyright_author: null
copyright_author_href: null
copyright_info: null
copyright_url: null
cover: https://img.617171.xyz/file/AgACAgQAAyEGAAScPoQGAAM1aWkAAd34luwJgC0M478RJcsqzAUOAAJcC2sbJJBJU1BLsUecAwybAQADAgADeAADOAQ.jpg
date: '2025-07-26T00:03:40+08:00'
description: null
highlight_shrink: null
katex: null
keywords: null
mathjax: null
swiper_index: 10
tags:
- 影视
title: MoonTV-影视资源聚合播放站部署
toc: null
toc_number: null
toc_style_simple: null
top: ''
top_group_index: 10
top_img: null
updated: '2025-10-18T12:49:59.723+08:00'
---
🎬 MoonTV 是一个开箱即用的、跨平台的影视聚合播放器。它基于 Next.js 14 + Tailwind CSS + TypeScript 构建，支持多资源搜索、在线播放、收藏同步、播放记录、本地/云端存储，让你可以随时随地畅享海量免费影视内容。

## 实例

影视(用户名/密码:guest)
https://yogmaewrhvqi.us-west-1.clawcloudrun.com/

✨ 功能特性
🔍 多源聚合搜索：内置数十个免费资源站点，一次搜索立刻返回全源结果。
📄 丰富详情页：支持剧集列表、演员、年份、简介等完整信息展示。
▶️ 流畅在线播放：集成 HLS.js & ArtPlayer。
❤️ 收藏 + 继续观看：支持 Redis/D1 存储，多端同步进度。
📱 PWA：离线缓存、安装到桌面/主屏，移动端原生体验。
🌗 响应式布局：桌面侧边栏 + 移动底部导航，自适应各种屏幕尺寸。
🚀 极简部署：一条 Docker 命令即可将完整服务跑起来，或免费部署到 Vercel 和 Cloudflare。
👿 智能去广告：自动跳过视频中的切片广告（实验性）

![这是图片描述](https://free.picui.cn/free/2025/10/03/68df44901aeb9.png)

# 部署

本项目支持 Vercel、Docker 和 Cloudflare 部署。

**1、Vercel 部署**
推荐使用，零运维成本，免费额度足够个人使用。
仓库：https://github.com/senshinya/MoonTV
Fork 本仓库到你的 GitHub 账户。
登陆 Vercel，点击 Add New → Project，选择 Fork 后的仓库。
（强烈建议）设置 PASSWORD 环境变量。
保持默认设置完成首次部署。
如需自定义 config.json，请直接修改 Fork 后仓库中该文件。
每次 Push 到 main 分支将自动触发重新构建。
部署完成后即可通过分配的域名访问，也可以绑定自定义域名。

**2、Cloudflare 部署**
Cloudflare Pages 的环境变量尽量设置为密钥而非文本

**普通部署（localstorage）**
Fork 本仓库到你的 GitHub 账户。
登陆 Cloudflare，点击 计算（Workers）-> Workers 和 Pages，点击创建
选择 Pages，导入现有的 Git 存储库，选择 Fork 后的仓库
构建命令填写 pnpm install –frozen-lockfile && pnpm run pages:build，预设框架为无，构建输出目录为 .vercel/output/static
保持默认设置完成首次部署。进入设置，将兼容性标志设置为 nodejs_compat
（强烈建议）首次部署完成后进入设置，新增 PASSWORD 密钥（变量和机密下），而后重试部署。
如需自定义 config.json，请直接修改 Fork 后仓库中该文件。
每次 Push 到 main 分支将自动触发重新构建。
D1 支持
点击 存储和数据库 -> D1 SQL 数据库，创建一个新的数据库，名称随意
进入刚创建的数据库，点击左上角的 Explore Data，将D1 初始化 中的内容粘贴到 Query 窗口后点击 Run All，等待运行完成
返回你的 pages 项目，进入 设置 -> 绑定，添加绑定 D1 数据库，选择你刚创建的数据库，变量名称填 DB
设置环境变量 NEXT_PUBLIC_STORAGE_TYPE，值为 d1；设置 USERNAME 和 PASSWORD 作为站长账号
重试部署
