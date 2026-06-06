# 盈缺 — 我的第一个网页

一个采用 Apple 风格设计的个人主页，使用 HTML、CSS、JavaScript 构建，无需构建工具，打开即可运行。

## 在线预览

本地打开 `index.html` 即可在浏览器中查看。

## 项目结构

```
my-first-website/
├── index.html          # 主页面（HTML + CSS + JavaScript）
├── assets/
│   └── logo-cat.svg    # 导航栏 Logo（可替换为自己的图片）
└── README.md
```

## 功能概览

### 导航栏

- 左侧：**Logo + 盈缺**（Logo 图片位于 `assets/logo-cat.svg`）
- **摄影作品** — 小下拉菜单（占位，待扩展）
- **我的项目** — Insta360 风格 Mega 菜单
  - 左侧：项目列表
  - 右侧：悬停时显示项目介绍
  - 当前项目：`agen_youtube`（介绍待填写）
- **联系我** — 全宽 Mega 菜单
  - 抖音 / B站 / 微信 / 邮箱（图标 + 账号）

导航在 Hero 区域为透明白字，滚动后自动切换为毛玻璃浅色样式。

### 页面模块

| 模块 | 说明 |
|------|------|
| Hero | 首屏欢迎区 |
| 关于我 | 个人介绍卡片 |
| 我的兴趣 | 摄影、摩托车、徒步等标签 |
| 幕后故事 | AI 协作创作说明 |
| 摄影预约 | 表单 + 校验 + 成功弹窗 |
| 点赞 / 点踩 | 互动计数 |
| 联系方式 | 底部联系图标与详情 |
| 页脚 | 版权信息 |

### 摄影预约表单

- 字段：姓名、联系方式、拍摄需求
- 空字段校验：红框 + 轻微抖动 + 行内提示
- 提交成功后显示 Apple 风格 Modal（非 `alert`）
- 暂未接入后端或数据库

## 如何运行

1. 克隆或下载本项目
2. 双击 `index.html`，或用浏览器打开
3. 也可使用本地服务器（可选）：

```bash
# Python 3
python3 -m http.server 8080

# 然后访问 http://localhost:8080
```

## 技术栈

- **HTML** — 页面结构
- **CSS** — 样式、动画、响应式布局
- **JavaScript** — 交互逻辑（表单校验、导航 Mega 菜单、点赞等）

无框架、无打包工具，所有代码集中在 `index.html` 中，便于学习和修改。

## 常见自定义

### 更换 Logo

修改导航栏中的图片路径：

```html
<img src="assets/logo-cat.svg" alt="盈缺 Logo" class="nav-logo">
```

### 修改联系方式

在 HTML 中搜索 `nav-contact-col`，或在 JavaScript 中搜索 `contactData` 对象。

### 添加项目

在「我的项目」Mega 菜单中：

1. 左侧列表添加 `<button class="nav-project-item" data-project="项目id">`
2. 右侧添加 `<div class="nav-project-panel" data-project-panel="项目id">`

### 修改摄影预约初始人数

搜索 JavaScript 中的 `var count = 777` 并修改数值。

## Git 分支

| 分支 | 说明 |
|------|------|
| `main` | 主分支 |
| `1.1` | 功能迭代分支（导航 Mega 菜单等） |

## 开发记录

- **Day 1** — 网站诞生
- **Day 2** — 兴趣爱好与页面优化
- **Day 3** — 摄影预约表单

## 作者

盈缺 — 用好奇心与 AI 制作
