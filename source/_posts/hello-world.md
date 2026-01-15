---
abbrlink: ''
ai: null
aplayer: null
aside: null
background: '#fff'
categories:
- 生活
comments: null
copyright: null
copyright_author: null
copyright_author_href: null
copyright_info: null
copyright_url: null
cover: https://img.617171.xyz/file/AgACAgQAAyEGAAScPoQGAAMxaWj_pe-EEvTpoFPw3j-jNfwG-88AAlgLaxskkElTCq0QrBsj5b0BAAMCAAN5AAM4BA.jpg
date: '2025-05-01T00:13:55+08:00'
description: null
highlight_shrink: null
katex: null
keywords: null
mathjax: true
swiper_index: 10
tags:
- hello world
title: hello world
toc: null
toc_number: null
toc_style_simple: null
top: null
top_group_index: 10
top_img: null
updated: '2025-09-21T23:11:21.843+08:00'
---
#### 新建博文

```
hexo new 这是一篇新的博文
```

#### 新建标签页

```
hexo new page 新建的标签页
```

#### 更新追番

```
hexo bangumi -u 
```

#### 部署网页

```
hexo cl; hexo g; hexo d
```

#### 本地预览

```
hexo cl; hexo s
```

#### 添加更改

```
git add .
```

#### 提交更改

```
git commit -m "添加内容"
```

### 插入图片

```
![这是图片描述](https://cdn-fusion.imgcdn.store/i/2025/qHZq7swABcLLFMXX.jpg)
```

## 插入PDF

```
<embed src="/file/example.pdf" type="application/pdf" width="100%" height="600px" />
```

## 更换电脑后继续编辑

如果你只是想在新电脑上继续编辑原有源代码，核心操作其实很简单，重点在**代码同步**和**基础环境复用**，无需复杂的VS Code设置同步流程。以下是更简化的步骤：

### 一、**前提：代码已托管在GitHub**

如果原电脑的代码已推送到GitHub仓库，新电脑只需：

1. **克隆仓库到本地**：
   在新电脑打开终端，进入目标文件夹，输入命令（以GitHub仓库为例）

`git clone https://github.com/你的用户名/仓库名.git`

2. **用VS Code打开项目**：
   在VS Code中点击左上角「文件」→「打开文件夹」，选择刚克隆的仓库目录，即可直接编辑代码。

### 二、**若代码未托管：手动迁移代码**

如果代码在原电脑本地（未上传GitHub），需先拷贝到新电脑：

1. **备份代码**：
   将原电脑中项目文件夹复制到U盘、移动硬盘或云盘（如百度云、OneDrive）。
2. **在新电脑导入**：
   将备份的项目文件夹复制到新电脑，用VS Code直接打开文件夹即可编辑。

### 三、**恢复基础编辑环境（可选）**

如果希望VS Code的扩展、主题等和原电脑一致，可简化操作：

1. **安装常用扩展**：
   比如Markdown编辑、Git工具等，直接在VS Code扩展市场搜索安装（例如搜索“Markdown All in One”“GitLens”）。
2. **复用主题和设置**：
   - 主题：在VS Code中按`Ctrl+K Ctrl+T`，选择原电脑使用的主题（如默认主题或第三方主题）。
   - 快捷键/字体等设置：若记得具体配置，可在新电脑的`设置（Ctrl+,）`中手动调整，或从原电脑复制`settings.json`文件到新电脑（路径见下方）：
     - Windows：`%APPDATA%\Code\User\settings.json`
     - macOS：`~/.config/Code/User/settings.json`

### 四、**关键提醒：避免重复操作**

- **无需同步全部VS Code设置**：若仅编辑代码，扩展和主题可按需安装，不必强求100%一致。
- **优先保障代码可访问**：只要代码在GitHub或已拷贝到新电脑，用VS Code打开即可编辑，其他环境配置可逐步补充。

总结：**核心操作就是克隆/复制代码到新电脑，用VS Code打开即可编辑**。环境配置（扩展、主题等）属于优化项，可根据需要逐步恢复，无需一开始就追求完整同步。

## 数学内容渲染

```
# 源码
- 简单加减： $a + b = c$  ，渲染后是行内的 a + b = c 
- 变量与系数： $y = kx + b$  ，渲染为 y = kx + b 
```

$a + b = c$ 

**以下为测试内容**
以下是一些常见数学公式的 Markdown（结合 Hexo 支持的渲染，通常用 KaTeX 或 MathJax 渲染，需确保博客主题已配置好数学公式渲染环境 ）样板，可直接放到 Hexo 文章的 Markdown 文件中测试：

1. 行内公式

- 简单加减： $a + b = c$  ，渲染后是行内的 a + b = c 。
- 变量与系数： $y = kx + b$  ，渲染为 y = kx + b 。

2. 独立公式块（带编号或不带）

- 不带编号的公式块（用  $$  包裹 ）：

$$
\int_{a}^{b} f(x) \, dx
$$

 

渲染后是独立的积分公式：

\int_{a}^{b} f(x) \, dx

- 带编号的公式块（不同渲染引擎语法有差异，以 MathJax 为例，用  \begin{equation}  等环境 ）：

$$
\begin{equation}
\sum_{i=1}^{n} i = \frac{n(n + 1)}{2}
\end{equation}
$$

 

渲染后会显示带编号（如 (1) 等，依顺序）的求和公式：

3. 矩阵与行列式

- 矩阵：

$$
\begin{bmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \cdots & a_{mn}
\end{bmatrix}
$$

 

渲染出矩阵：

\begin{bmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \cdots & a_{mn}
\end{bmatrix}

- 行列式：

$$
\begin{vmatrix}
1 & 2 \\
3 & 4
\end{vmatrix}
$$

 

渲染结果：

\begin{vmatrix}
1 & 2 \\
3 & 4
\end{vmatrix}

4. 复杂公式（如微积分、向量等）

- 向量点积：

$$
\vec{a} \cdot \vec{b} = |\vec{a}| |\vec{b}| \cos\theta
$$

 

渲染：

\vec{a} \cdot \vec{b} = |\vec{a}| |\vec{b}| \cos\theta

- 二阶导数：

$$
\frac{d^2 y}{dx^2} + y = 0
$$

 

渲染：

\frac{d^2 y}{dx^2} + y = 0

将这些内容放到你的 Hexo 博客文章的  .md  文件中，部署或本地预览（ hexo s  ）后，查看是否能正确渲染。若未正确显示，检查主题配置里是否启用了 KaTeX/MathJax ，以及相关 CDN 或依赖是否加载正常 。
