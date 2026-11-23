<div align="center">

<img src="../assets/nightglean-lockup.png" width="720" alt="长夜拾星 · Nightglean Studio" />

# 长夜拾星工作室 · Nightglean Studio

**独立开发 · 原生实现 · 先把「能不能不这样做」问一遍**

一个很小的独立工作室，做 Android 应用与工程实验。
不追框架，不堆依赖，尽量让每一条构建链路都能被自己读懂。

[![Android](https://img.shields.io/badge/Android-5.0%2B-3DDC84?logo=android&logoColor=white)](https://github.com/nightglean)
[![No Gradle](https://img.shields.io/badge/build-no%20Gradle-1f6feb)](https://github.com/nightglean)
[![License](https://img.shields.io/badge/license-MIT-2ea44f)](https://github.com/nightglean)
[![Website](https://img.shields.io/badge/site-nightglean.github.io-c2a878)](https://nightglean.github.io/)

[English](README.md) · **简体中文**

</div>

---

### 项目

| 项目 | 是什么 | 技术取向 | 状态 |
| --- | --- | --- | --- |
| **拾光 OneStar**<br>[wang-sunyang/onestar](https://github.com/wang-sunyang/onestar) | 「每日星」记录应用：一天记一笔心情，累积成一片手绘星图，支持桌面小组件、心情曲线、年度长图海报 | 纯 Java + Canvas 自绘，无 Gradle / 无 AndroidX / 无第三方 SDK；`aapt2 + javac + d8 + apksigner` 手工构建，JNI 层用 `zig cc` 编译 | 0.12.x 迭代中，targetSdk 37 |
| **AppFunction Guard**<br>[wang-sunyang/appfunction-guard](https://github.com/wang-sunyang/appfunction-guard) | Android 16 的 `AppFunctions` 让 AI Agent 能直接调用 App 内的函数；这个库补上平台没给的逐函数授权、限流、参数校验与审计链路 | Kotlin 2.2，`minSdk 26`，MIT；单一拦截点插在平台与业务逻辑之间 | alpha |
| **moltdisk · 蜕冗**<br>[wang-sunyang/moltdisk](https://github.com/wang-sunyang/moltdisk) | 磁盘体检工具：找出能由源码重建的构建产物（`node_modules`、`target`、`dist`、`venv`、`Pods`），算体积、排序，并给出「凭什么可删」的证据。它自己不删任何东西 | Rust 2021，MSRV 1.80，MIT；无删除代码路径，`-y` 直接报错 | v0.1.0 |
| **Marvis · Persona Spec**<br>[wang-sunyang/marvis-persona-spec](https://github.com/wang-sunyang/marvis-persona-spec) | 一份可被程序检查的人格规范：30 格台词位、20 条禁句、一个能跑的 lint 脚本、10 条基准测试，附 Fault Bloom 视觉系统 | Python lint + Markdown 规范，CI 里做灰阶报告到门禁的两段式接入 | v3 |

> 以上六个仓库——[onestar](https://github.com/wang-sunyang/onestar)、[appfunction-guard](https://github.com/wang-sunyang/appfunction-guard)、[moltdisk](https://github.com/wang-sunyang/moltdisk)、[marvis-persona-spec](https://github.com/wang-sunyang/marvis-persona-spec)、[duyinbu](https://github.com/wang-sunyang/duyinbu)、[summer-color-broadcast](https://github.com/wang-sunyang/summer-color-broadcast)——目前仍在个人账号（[wang-sunyang](https://github.com/wang-sunyang)）下维护，须同时满足两项条件后才迁入本组织：存在已打标签、公开可获取至少一个发布周期的发行版；至少有三次外部贡献完整走完 issue → PR → review → merge 流程。已有治理文件的项目在其文件中写明该判据——如《渡阴簿》与《夏色广播》见 `GOVERNANCE.md` §1.1。判据定义在各仓库，不在本页；本页只记录判据存在。六个仓库中后两个目前为私有仓，对应链接要等转公开后才能打开。组织页面的 `.github` 仓库只承载这份简介与品牌资产。

### 视觉

<div align="center">

<img src="../assets/nightglean-poster.png" width="360" alt="长夜拾星 · 竹简刻字海报" />

<sub>竹简四片，字刻在片心、对齐在缝间；横版 lockup 用于文档抬头，方形 mark 用于头像与图标位。</sub>

</div>

深底是常态：这个工作室的东西多在夜里写完。标识以竹简四片为一组，缝宽固定，字形按楚文字笔意重绘，四个字的视觉中心落在各自片心的同一条水平线上。

### 做事方式

- **原生优先**：界面用 Canvas 逐帧画，不套 WebView，不为了「快」牺牲可控性。
- **依赖克制**：能自己写的一行，就不引入一个包。构建链的每一环都要说得清做了什么。
- **可复现**：命令行能编译出同一种 APK，构建过程不依赖 IDE 的隐式魔法。
- **文档写实**：README 里同时记限制、踩坑和已知问题，不只写亮点。

### 最近

| 方向 | 内容 |
| --- | --- |
| OneStar 0.12.x | targetSdk 升到 37、签名与发布链路加固、16 KB 页对齐复核、大屏方向守卫 |
| moltdisk 0.1.0 | 首个正式版发布：审计报告、`why` 子命令与证据链，删除能力在发布前被整段移除 |
| Marvis Persona Spec v3 | 人格矩阵、禁句表与 lint 闸门成型，接入 CI 做灰阶观测 |
| 工程文档 | 构建规范、发版清单与跨平台开发约定持续补齐 |

### 构建状态

| 仓库 | 工作流 | 状态 |
| --- | --- | --- |
| onestar | `android.yml` | [![build](https://img.shields.io/github/actions/workflow/status/wang-sunyang/onestar/android.yml?branch=main&label=build)](https://github.com/wang-sunyang/onestar/actions/workflows/android.yml) |
| onestar | `regression.yml` | [![regression](https://img.shields.io/github/actions/workflow/status/wang-sunyang/onestar/regression.yml?branch=main&label=regression)](https://github.com/wang-sunyang/onestar/actions/workflows/regression.yml) |
| appfunction-guard | `build.yml` | [![build](https://img.shields.io/github/actions/workflow/status/wang-sunyang/appfunction-guard/build.yml?branch=main&label=build)](https://github.com/wang-sunyang/appfunction-guard/actions/workflows/build.yml) |
| moltdisk | `ci.yml` | [![ci](https://img.shields.io/github/actions/workflow/status/wang-sunyang/moltdisk/ci.yml?branch=main&label=ci)](https://github.com/wang-sunyang/moltdisk/actions/workflows/ci.yml) |
| marvis-persona-spec | `persona-lint.yml` | [![lint](https://img.shields.io/github/actions/workflow/status/wang-sunyang/marvis-persona-spec/persona-lint.yml?branch=main&label=lint)](https://github.com/wang-sunyang/marvis-persona-spec/actions/workflows/persona-lint.yml) |

### 链接

- 官网：[nightglean.github.io](https://nightglean.github.io/)
- 作者主页：[wang-sunyang](https://github.com/wang-sunyang)
- 个人站点：[wang-sunyang.github.io](https://wang-sunyang.github.io)
- 问题与建议：欢迎在对应仓库提 Issue

<div align="center">
<sub>nightglean studio — small tools, hand-built.</sub>
</div>
