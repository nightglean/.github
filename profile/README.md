<div align="center">

# Nightglean

**独立开发 · 原生实现 · 先把"能不能不这样做"问一遍**

一个很小的独立工作室，做 Android 应用与工程实验。
不追框架，不堆依赖，尽量让每一条构建链路都能被自己读懂。

[![Android](https://img.shields.io/badge/Android-5.0%2B-3DDC84?logo=android&logoColor=white)](https://github.com/nightglean)
[![No Gradle](https://img.shields.io/badge/build-no%20Gradle-1f6feb)](https://github.com/nightglean)
[![License](https://img.shields.io/badge/license-MIT-2ea44f)](https://github.com/nightglean)

</div>

---

## 项目

| 项目 | 是什么 | 技术取向 | 状态 |
| --- | --- | --- | --- |
| **拾光 OneStar**<br>[yangyang2857-rgb/onestar](https://github.com/yangyang2857-rgb/onestar) | 「每日星」记录应用：一天记一笔心情，累积成一片手绘星图，支持桌面小组件、心情曲线、年度长图海报 | 纯 Java + Canvas 自绘，无 Gradle / 无 AndroidX / 无第三方 SDK；`aapt2 + javac + d8 + apksigner` 手工构建，JNI 层用 `zig cc` 编译 | v0.12.x 迭代中 |

> OneStar 目前仍在个人账号下维护，待发布链路稳定后迁移至本组织。组织页面的 `.github` 仓库只承载这份简介。

## 做事方式

- **原生优先**：界面用 Canvas 逐帧画，不套 WebView，不为了"快"牺牲可控性。
- **依赖克制**：能自己写的一行，就不引入一个包。构建链的每一环都要说得清做了什么。
- **可复现**：命令行能编译出同一种 APK，构建过程不依赖 IDE 的隐式魔法。
- **文档写实**：README 里同时记限制、踩坑和已知问题，不只写亮点。

## 最近

| 方向 | 内容 |
| --- | --- |
| OneStar 0.12.x | targetSdk 升级、签名与发布链路加固、大屏方向守卫 |
| 工程文档 | 构建规范、发版清单与跨平台开发约定持续补齐 |

## 链接

- 作者主页：[yangyang2857-rgb](https://github.com/yangyang2857-rgb)
- 个人站点：[yangyang2857-rgb.github.io](https://yangyang2857-rgb.github.io)
- 问题与建议：欢迎在对应仓库提 Issue

<div align="center">
<sub>nightglean studio — small tools, hand-built.</sub>
</div>
