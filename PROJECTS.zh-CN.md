<div align="center">

[English](PROJECTS.md) · **简体中文** · [← 回到主页](README.zh-CN.md)

# 完整项目经历 · Colin

<a href="https://github.com/colinli007">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1200&color=2F81F7&center=true&vCenter=true&width=520&lines=AI+%E5%85%A8%E6%A0%88%E5%B7%A5%E7%A8%8B%E5%B8%88;%E6%B5%B7%E5%A4%96+AI+%E4%BA%A7%E5%93%81+%C2%B7+%E8%A7%86%E9%A2%91%E7%BC%96%E8%BE%91%E5%99%A8%E5%BC%95%E6%93%8E;%E7%BC%96%E8%BE%91%E5%99%A8%E5%BC%95%E6%93%8E+%C2%B7+%E5%BC%80%E6%BA%90%E7%BB%B4%E6%8A%A4" alt="AI 全栈工程师" />
</a>

<p>
  <a href="https://www.douyin.com/user/MS4wLjABAAAAlJlcNMyzb8sTPP6J9vip0pnzAuAHiHN7_aBNztGQX-k"><img src="https://img.shields.io/badge/抖音-AI_内容分享-000000?style=flat-square&logo=tiktok&logoColor=white" alt="抖音" /></a>
  <a href="https://blog.csdn.net/weixin_44309374"><img src="https://img.shields.io/badge/CSDN-技术博客-FC5531?style=flat-square&logo=csdn&logoColor=white" alt="CSDN" /></a>
  <a href="https://www.npmjs.com/~li1164267803"><img src="https://img.shields.io/badge/npm-li1164267803-CB3837?style=flat-square&logo=npm&logoColor=white" alt="npm" /></a>
  <a href="mailto:xiwenpp@163.com"><img src="https://img.shields.io/badge/Email-xiwenpp@163.com-2F81F7?style=flat-square" alt="Email" /></a>
</p>

</div>

## 🙋 关于我

- 🤖 **AI 全栈工程师**，前端出身，近两年专注**海外 AI 产品**：AI 视频生成 SaaS 的 Web 编辑器、AI 内容工具与浏览器插件
- 🐍 **后端与 AI 工程**：1 年 Python 经验，个人项目中用 FastAPI 接入大模型（OpenAI SDK 兼容接口）、搭建 RAG 知识库与 SSE 流式输出，Node.js（Fastify）服务开发，正在系统学习 Agent 工程
- 🧩 **全端交付经验**：小程序 / H5 / PC Web / CRM / SaaS 后台 / App / Chrome 插件 / Electron 桌面端
- 🏥 **行业覆盖**：教育、医疗、海外 AI、直播、IM 即时通讯
- 🎬 **编辑器与动画**：视频画布编辑器引擎、时间轴播放引擎、GSAP 动效、Three.js 3D 场景
- ⚡ **AI 辅助工程**：日常用 Claude Code / Cursor 做需求拆解、编码、Review 与自动化，自己写 Agent Skill 提效
- 📱 曾运营 **30w+ 粉丝**抖音账号，正在分享 AI 编程与 AI 工具实战

## 🛠 技术栈

<p>
  <img src="https://skillicons.dev/icons?i=react,vue,nextjs,ts,tailwind,vite,flutter,electron,nodejs,py,fastapi,threejs,docker&perline=13" alt="tech stack" />
</p>

<p>
  <img src="https://img.shields.io/badge/uni--app-2B9939?style=flat-square" alt="uni-app" />
  <img src="https://img.shields.io/badge/React_Native-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React Native" />
  <img src="https://img.shields.io/badge/Chrome_Extension_MV3-4285F4?style=flat-square&logo=googlechrome&logoColor=white" alt="Chrome Extension" />
  <img src="https://img.shields.io/badge/Canvas-E34F26?style=flat-square" alt="Canvas" />
  <img src="https://img.shields.io/badge/GSAP-0AE448?style=flat-square&logo=greensock&logoColor=black" alt="GSAP" />
  <img src="https://img.shields.io/badge/SSE_流式输出-555?style=flat-square" alt="SSE" />
  <img src="https://img.shields.io/badge/TipTap-1A1A1A?style=flat-square" alt="TipTap" />
  <img src="https://img.shields.io/badge/Yjs_协作-30BCED?style=flat-square" alt="Yjs" />
</p>

**AI 工具**

<p>
  <img src="https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=claude&logoColor=white" alt="Claude Code" />
  <img src="https://img.shields.io/badge/Cursor-000000?style=flat-square&logo=cursor&logoColor=white" alt="Cursor" />
  <img src="https://img.shields.io/badge/ChatGPT-10A37F?style=flat-square" alt="ChatGPT" />
</p>

## 💼 代表作品

### 🎬 [Leadde](https://leadde.ai) · 海外 AI 视频生成 SaaS（对标 HeyGen / Synthesia）

面向企业培训、产品教程场景：300+ AI 数字人、88 种语言配音，PPT / PDF / 脚本一键生成视频，在线编辑后云端渲染导出。

**我的角色：Web 视频编辑器核心开发者**

- **自研画布编辑器引擎**：React 19 + react-moveable 的 1920×1080 DOM 画布，支持多选、成组 / 解组（旋转矩阵换算）、对齐吸附、裁剪平移、剪贴板与快捷键，按 core / interactions / history / sync 分层
- **状态架构与撤销重做**：设计 Zustand 按 Slice 拆分的画布 Store，快照 + 命令混合的撤销重做，保证 Store / DOM / 交互控件三方状态一致
- **预览播放引擎**：rAF 驱动、以音频时钟为基准，逐帧同步多页时间轴、转场、视频修剪、入场动画与 GSAP 动效（受控 seek）
- **编辑器即渲染器**：出片录制复用同一套画布逐帧驱动，按媒体 → 首帧稳定 → 动效挂载 → 字体就绪依次判定，保证成片与预览一致
- **文字自动反色**：沿图层 z 序做 alpha 合成推算文字下方的真实背景（含旋转图层逆变换、视频帧离屏采样），自动选出可读的文字颜色
- **实时协作**：基于 Yjs / y-websocket 的协作通道，断线整体重建 + 退避重连，统一只读门控
- **前后端链路**：编辑器对接后端的 SSE 流式生成与异步视频任务；排查并修复 Headless 录制链路中 Playwright 拦截 CDN gzip 资源、导致成片字体丢失的问题
- GSAP 动效组件、数字人视频页、编辑器浮动工具栏与右键菜单

技术栈：React 19 · TypeScript · Vite · Zustand + immer · react-moveable · TipTap · GSAP · Yjs · MUI · Tailwind · Storybook

### 📝 [Lynote](https://lynote.ai) · 海外 AI 内容工具（10 种语言）

| 产品 | 技术要点 |
|---|---|
| [YouTube Transcript Generator](https://chromewebstore.google.com/detail/lynote-youtube-transcript/cpdecpnpoaahhdlfjnpokjpemdnjhekf)<br/>Chrome 插件 | Shadow DOM 注入 YouTube 侧栏并隔离样式与事件；Service Worker 代理请求绕过 CORS；Zustand + `chrome.storage` 跨标签页同步登录态；翻译暂停 / 继续 / 重试状态机；MV3 下通过沙盒 iframe 接入 GA4 |
| [AI Humanizer & Detector](https://chromewebstore.google.com/detail/lynote-ai-humanizer-detec/egbpdidbaamhhibpipaehgonalpkmmic)<br/>Chrome 插件 | 划词浮动工具条，首次出现选区才懒加载 Shadow DOM 与 React 树；选区上下自动翻转定位；插件 → 官网带语言前缀的交接协议 |
| [lynote.ai](https://lynote.ai) 官网 & SaaS 工具站 | 旧站迁移 Next.js 15 App Router 与首页 SSR；POST SSE 流式翻译及暂停 / 停止重构；AI 视频总结与分享短链；网页与插件登录态互通；多语言 SEO 与数据埋点 |

技术栈：WXT · React 19 · Next.js 15 · TypeScript · Zustand · Tailwind · antd / MUI · next-intl / i18next

### 🖥 Electron + Python 桌面自动化客户端（商业化产品）

- Electron 主进程 + Python 子进程双进程架构，stdin / NDJSON 事件流通信
- 配套 License 授权服务（Fastify）、Ed25519 签名的自动更新、Windows / macOS 双端打包

## 📚 正在学习

- **AI Agent 工程**：Agent 编排与工作流状态机、Tool Calling、结构化输出与 Prompt 工程、LangGraph
- **多模型接入**：OpenAI / Gemini / Claude 等模型调用、流式输出、限流与成本控制
- **AI 视频后端链路**：文档解析 → 脚本生成 → TTS 配音 → 数字人 → Headless 渲染合成
- **后端基础**：FastAPI、Redis（分布式锁 / Streams 推送）、MySQL / MongoDB、异步任务调度、Docker 部署

## 🌱 开源

### [daybrush/moveable](https://github.com/daybrush/moveable) · 协助维护中

我在生产环境的视频编辑器里基于 `react-moveable` 做画布交互，已在 [#1156](https://github.com/daybrush/moveable/issues/1156) 提出协助维护，目前等作者回复。

想带上游的能力：

- **可持久化的组**（[#1133](https://github.com/daybrush/moveable/issues/1133)，2024 年开至今）：合组 / 解组作为真实可序列化的实体，而不是运行时的 `targets` 数组 —— 组本身是一个图层，能存盘、能重新加载、能嵌套
- **组内递归缩放**（[#1020](https://github.com/daybrush/moveable/issues/1020)）：按子元素类型分发（文本走 font-size、媒体走内部裁剪偏移、SVG 走 viewport 尺寸），而不是统一套 scale

### 其它

- [colbymchenry/codegraph#1288](https://github.com/colbymchenry/codegraph/pull/1288)：修复导入超大资源文件导致整个代码索引 OOM 的问题，附回归测试（Open）
- [xiwen-html2canvas](https://github.com/colinli007/xiwen-html2canvas)：针对 html2canvas 生成图片不清晰，额外加了两个 API
