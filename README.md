# frontpage-learning

个人前端学习项目集合，包含 CRT 终端风格个人主页和若干创意/工程类 HTML 实验。

## 仓库结构

```
frontpage-learning/
├── projects_frontpage/
│   └── projects.html        # CRT 终端风格个人主页，展示 11 个项目导航卡片
├── cyberpunk_city/
│   └── cyberpunk_city.html  # 赛博朋克城市粒子生成效果
└── index/                   # Git Submodule → particle_effects_web
```

## 项目说明

### `projects_frontpage` — 个人主页

CRT 终端风格的项目导航页，磷光绿配色、扫描线动效和打字机光标，以卡片网格展示 11 个项目入口。

**技术栈：** Vanilla HTML/CSS · CSS Animation · Google Fonts

### `cyberpunk_city` — 城市粒子效果

基于 Canvas 2D 的程序化赛博朋克城市生成器，霓虹灯光 + 粒子雨，鼠标交互驱动粒子流场。

**技术栈：** HTML Canvas 2D · Vanilla JavaScript

### `index` (Submodule) — 手势粒子特效

独立仓库 [`particle_effects_web`](https://github.com/A1RER/particle_effects_web)，通过 Git Submodule 引入。使用 MediaPipe 实时追踪手部 21 个关键点，五指指尖各自驱动独立粒子流场，60fps 运行。

**技术栈：** MediaPipe · Canvas 2D · JavaScript

## 主页项目列表

个人主页 (`projects.html`) 中展示的 11 个项目：

| # | 项目 | 类别 | 技术栈 |
|---|------|------|--------|
| 01 | 天眸通感 · SKYSENSE 5G / ISAR IMAGING | Research | MATLAB · ISAR · 5G ISAC |
| 02 | 手势粒子特效 · GESTURE PARTICLE FX | Creative / Frontend | MediaPipe · Canvas 2D · JS |
| 03 | 图书管理系统 · LIBRARY MGMT SYS | Engineering | Java · MySQL · Swing |
| 04 | 赛博朋克城市 · NEO CITY GEN | Creative / Frontend | Canvas 2D · JS · Generative |
| 05 | 算法与AI实践 · ALGORITHM & AI PRACTICE | AI / Algorithm | Python · AI · Algorithm |
| 06 | AIGC学习 · AIGC LEARNING 15 WEEKS | AI / Learning | Python · AIGC |
| 07 | 社会力模型仿真 · SOCIAL FORCE MODEL SIM | Simulation | Python · SFM |
| 08 | 信号与系统 · SIGNAL & SYSTEM STUDY | Coursework | MATLAB · Python · DSP |
| 09 | 数据结构 · DATA STRUCTURE C LANG | Coursework | C · CQUPT |
| 10 | 局域网扫描器 · LAN SCANNER | Networking Tool | Python · Network |
| 11 | MATLAB RC | MATLAB Project | MATLAB · Simulation |

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
