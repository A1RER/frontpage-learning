# frontpage-learning

个人前端学习项目集合，包含个人主页和若干创意/工程类 HTML 实验。

## 仓库结构

```
frontpage-learning/
├── projects_frontpage/
│   └── projects.html        # 赛博朋克风格个人主页，展示项目导航
├── cyberpunk_city/
│   └── cyberpunk_city.html  # 赛博朋克城市粒子生成效果
└── index/                   # Git Submodule → particle_effects_web
```

## 项目说明

### `projects_frontpage` — 个人主页
CRT 终端风格的项目导航页，采用磷光绿配色、扫描线动效和打字机光标，展示各个项目的入口链接。

**技术栈：** Vanilla HTML/CSS · CSS Animation · Google Fonts

### `cyberpunk_city` — 城市粒子效果
基于 Canvas 2D 的程序化赛博朋克城市生成器，鼠标交互驱动粒子流场。

**技术栈：** HTML Canvas 2D · Vanilla JavaScript

### `index` (Submodule) — 手势粒子特效
独立仓库 [`particle_effects_web`](https://github.com/A1RER/particle_effects_web)，通过 Git Submodule 引入。使用 MediaPipe 实时追踪手部关键点，五指指尖各自驱动独立粒子流场，60fps 运行。

**技术栈：** MediaPipe · Canvas 2D · JavaScript

## 快速开始

克隆时需要同时初始化子模块：

```bash
git clone --recurse-submodules <repo-url>
```

若已克隆但未初始化子模块：

```bash
git submodule update --init
```

所有文件均为纯静态 HTML，直接用浏览器打开即可运行，无需构建步骤。

## 子模块更新

```bash
# 拉取 particle_effects_web 的最新代码
git submodule update --remote index

# 同步主仓库的 submodule 指针
git add index && git commit -m "chore: update submodule"
```
