<div align="center">

# 长夜拾星 · Nightglean Studio

**官网源码 · 单页静态站点**

[![site](https://img.shields.io/badge/site-nightglean.github.io-c2a878)](https://nightglean.github.io/)
[![build](https://img.shields.io/badge/build-none-1f6feb)](https://github.com/nightglean/nightglean.github.io)
[![no Jekyll](https://img.shields.io/badge/Jekyll-off-4b5563)](https://github.com/nightglean/nightglean.github.io/blob/main/.nojekyll)

线上地址：**<https://nightglean.github.io/>**

</div>

---

### 这是什么

长夜拾星工作室的门面页。一个 HTML 文件，把工作室是谁、在做什么、怎么做事讲清楚，然后停下。

深底、竹简四片标识、宋体正文。没有构建步骤，没有依赖，没有客户端脚本。

### 目录

| 文件 | 作用 |
| --- | --- |
| `index.html` | 首页全部内容：样式内联在 `<head>`，无外链 CSS / JS / 字体 |
| `404.html` | 自定义 404，Pages 命中缺失路径时返回 |
| `.nojekyll` | 关掉 Jekyll，让 Pages 原样托管静态文件 |

### 本地预览

```bash
# 仓库根目录执行，然后访问 http://localhost:8000/
python3 -m http.server 8000
```

直接双击 `index.html` 也能看，只是 `404.html` 的行为需要走 HTTP 服务才贴近线上。

### 项目链接

官网上列的四个项目，目前都在个人账号下维护，待发布与协作链路稳定后迁入本组织。

| 项目 | 是什么 | 技术取向 | 状态 |
| --- | --- | --- | --- |
| [拾光 OneStar](https://github.com/yangyang2857-rgb/onestar) | 一天记一笔心情，累积成一片手绘星图；桌面小组件、心情曲线、年度长图海报 | 纯 Java + Canvas 自绘，无 Gradle / 无 AndroidX / 无第三方 SDK；`aapt2 + javac + d8 + apksigner` 手工构建，JNI 层用 `zig cc` 编译 | 0.12.x · targetSdk 37 |
| [AppFunction Guard](https://github.com/yangyang2857-rgb/appfunction-guard) | 补上 Android 16 `AppFunctions` 缺的逐函数授权、限流、参数校验与审计链路 | Kotlin 2.2，`minSdk 26`，MIT；单一拦截点插在平台与业务逻辑之间 | alpha |
| [moltdisk · 蜕冗](https://github.com/yangyang2857-rgb/moltdisk) | 磁盘体检：找出能由源码重建的构建产物，算体积、排序，给出「凭什么可删」的证据；它自己不删任何东西 | Rust 2021，MSRV 1.80，MIT；无删除代码路径，`-y` 直接报错 | v0.1.0 |
| [Marvis · Persona Spec](https://github.com/yangyang2857-rgb/marvis-persona-spec) | 一份能被程序检查的人格规范：30 格台词位、20 条禁句、一个能跑的 lint 脚本、10 条基准测试 | Python lint + Markdown 规范，CI 里做灰阶报告到门禁的两段式接入 | v3 |

### 部署

GitHub Pages，`main` 分支根目录，无需 Actions。

推送到 `main` 即发布，通常几十秒内生效。自定义域名未配置，站点走 `github.io` 默认域，因此 HTTPS 由 GitHub 托管、无需证书维护。

### 约定与限制

- **不为视觉引入依赖**：字体只用系统栈（宋体 / 思源宋体 / 无衬线兜底），图标是内联 SVG data URI，断网也完整可读。
- **单文件优先**：样式内联，改一处不用同步两处；文件变大也认。
- **锚点不跨页**：站内定位只靠 `#main`、`#work`、`#way`、`#now`，不依赖脚本，也不做同页 JS 跳转。
- **无障碍兜底**：竹简四字是装饰，`sr-only` 文本提供真实标题；正文有跳到正文的 skip 链接。
- **不做浏览器兼容矩阵**：目标是近两年的主流浏览器，移动端先行；旧内核只保证内容可读。
- **没有埋点**：不放统计脚本，不引第三方请求。

### 链接

- 官网：<https://nightglean.github.io/>
- 组织：[github.com/nightglean](https://github.com/nightglean)
- 作者主页：[yangyang2857-rgb](https://github.com/yangyang2857-rgb)
- 个人站点：<https://yangyang2857-rgb.github.io>
- 问题与建议：在本仓库或 [nightglean/.github](https://github.com/nightglean/.github/issues) 提 Issue

<div align="center">
<sub>nightglean studio — small tools, hand-built.</sub>
</div>
