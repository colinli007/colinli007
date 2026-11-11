<div align="center">

**English** · [简体中文](README.zh-CN.md)

# Hi, I'm Colin 👋

<a href="https://github.com/colinli007">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1200&color=2F81F7&center=true&vCenter=true&width=520&lines=AI+Full-Stack+Engineer;AI+Video+SaaS+%C2%B7+Web+Canvas+Editor;Editor+Engines+%C2%B7+Open+Source" alt="AI Full-Stack Engineer" />
</a>

<p>
  <a href="https://www.npmjs.com/~li1164267803"><img src="https://img.shields.io/badge/npm-li1164267803-CB3837?style=flat-square&logo=npm&logoColor=white" alt="npm" /></a>
  <a href="https://blog.csdn.net/weixin_44309374"><img src="https://img.shields.io/badge/Blog-CSDN-FC5531?style=flat-square&logo=csdn&logoColor=white" alt="CSDN" /></a>
  <a href="https://www.douyin.com/user/MS4wLjABAAAAlJlcNMyzb8sTPP6J9vip0pnzAuAHiHN7_aBNztGQX-k"><img src="https://img.shields.io/badge/Douyin-AI_Content-000000?style=flat-square&logo=tiktok&logoColor=white" alt="Douyin" /></a>
  <a href="mailto:xiwenpp@163.com"><img src="https://img.shields.io/badge/Email-xiwenpp@163.com-2F81F7?style=flat-square" alt="Email" /></a>
</p>

<a href="PROJECTS.md"><img src="https://img.shields.io/badge/%F0%9F%93%96_Full_project_history-%E2%86%92-1F6FEB?style=for-the-badge&labelColor=2F81F7" alt="Full project history" /></a>

</div>

## 🙋 About me

- 🤖 **AI full-stack engineer**, frontend by background. For the past two years I've worked on AI products for overseas markets: an AI video generation SaaS, AI content tools, and browser extensions.
- 🎬 My main craft is **editor engines** — a DOM-based 1920×1080 canvas editor, undo/redo, a frame-accurate timeline playback engine, GSAP animation, and Yjs real-time collaboration.
- 🧩 Shipped across mini programs / H5 / desktop web / CRM / SaaS / mobile apps / Chrome extensions / Electron, in education, healthcare, live streaming and IM.
- 🐍 One year of Python; building RAG pipelines and LLM applications with FastAPI, and going deeper into agent orchestration.
- 🌱 I maintain and contribute to open source around **canvas interaction and transform tooling** — see below.

## 🛠 Tech stack

<p>
  <img src="https://skillicons.dev/icons?i=react,vue,nextjs,ts,tailwind,vite,flutter,electron,nodejs,py,fastapi,threejs,docker&perline=13" alt="tech stack" />
</p>

<p>
  <img src="https://img.shields.io/badge/uni--app-2B9939?style=flat-square" alt="uni-app" />
  <img src="https://img.shields.io/badge/React_Native-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React Native" />
  <img src="https://img.shields.io/badge/Chrome_Extension_MV3-4285F4?style=flat-square&logo=googlechrome&logoColor=white" alt="Chrome Extension" />
  <img src="https://img.shields.io/badge/GSAP-0AE448?style=flat-square&logo=greensock&logoColor=black" alt="GSAP" />
  <img src="https://img.shields.io/badge/Yjs-30BCED?style=flat-square" alt="Yjs" />
  <img src="https://img.shields.io/badge/TipTap-1A1A1A?style=flat-square" alt="TipTap" />
  <img src="https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=claude&logoColor=white" alt="Claude Code" />
  <img src="https://img.shields.io/badge/Cursor-000000?style=flat-square&logo=cursor&logoColor=white" alt="Cursor" />
</p>

## 🌱 Open source

- **[daybrush/moveable](https://github.com/daybrush/moveable)** — I build on `react-moveable` in production and have offered to help maintain it: [#1156](https://github.com/daybrush/moveable/issues/1156). The work I'd like to bring upstream is **persistent groups** — group / ungroup as real, serializable entities rather than a runtime `targets` array ([#1133](https://github.com/daybrush/moveable/issues/1133) has been open since 2024) — and **recursive group resize dispatched by child type**, so text, SVG and cropped media each scale correctly instead of taking one uniform scale ([#1020](https://github.com/daybrush/moveable/issues/1020)). Currently waiting on the author.
- **[colbymchenry/codegraph#1288](https://github.com/colbymchenry/codegraph/pull/1288)** — fixed an OOM that took down the whole code index when an oversized asset file was imported, with a regression test.
- **[agent-skills](https://github.com/colinli007/agent-skills)** — the Claude Code / Codex agent skills I actually use day to day.
- **[ease-music](https://github.com/colinli007/ease-music)** — open-source local music player for Android and iOS. No built-in sources; it plays only the music you already own.
- **[xiwen-html2canvas](https://github.com/colinli007/xiwen-html2canvas)** — two extra APIs on top of html2canvas to fix blurry output.

## 💼 Selected work

**🎬 [Leadde](https://leadde.ai)** · AI video generation SaaS (in the HeyGen / Synthesia space)

Core developer of the web video editor: an in-house DOM canvas editor, undo/redo, the timeline preview playback engine, GSAP animation, and Yjs real-time collaboration.

**📝 [Lynote](https://lynote.ai)** · AI content tools

- [YouTube Transcript Generator](https://chromewebstore.google.com/detail/lynote-youtube-transcript/cpdecpnpoaahhdlfjnpokjpemdnjhekf) — transcript, translation and AI summary for YouTube
- [AI Humanizer & Detector](https://chromewebstore.google.com/detail/lynote-ai-humanizer-detec/egbpdidbaamhhibpipaehgonalpkmmic) — select-to-rewrite and AI detection
- [lynote.ai](https://lynote.ai) — Next.js SSR, SSE streaming translation, 10 languages

**🖥 Desktop automation client** · Electron + Python dual-process, with a licensing service and signed auto-update

> 📖 Implementation details for each project: **[full project history](PROJECTS.md)**
