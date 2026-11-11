<div align="center">

**English** · [简体中文](PROJECTS.zh-CN.md) · [← Back to profile](README.md)

# Full project history · Colin

<a href="https://github.com/colinli007">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1200&color=2F81F7&center=true&vCenter=true&width=520&lines=AI+Full-Stack+Engineer;AI+Video+SaaS+%C2%B7+Web+Canvas+Editor;Editor+Engines+%C2%B7+Open+Source" alt="AI Full-Stack Engineer" />
</a>

<p>
  <a href="https://www.npmjs.com/~li1164267803"><img src="https://img.shields.io/badge/npm-li1164267803-CB3837?style=flat-square&logo=npm&logoColor=white" alt="npm" /></a>
  <a href="https://blog.csdn.net/weixin_44309374"><img src="https://img.shields.io/badge/Blog-CSDN-FC5531?style=flat-square&logo=csdn&logoColor=white" alt="CSDN" /></a>
  <a href="mailto:xiwenpp@163.com"><img src="https://img.shields.io/badge/Email-xiwenpp@163.com-2F81F7?style=flat-square" alt="Email" /></a>
</p>

</div>

## 🙋 About me

- 🤖 **AI full-stack engineer**, frontend by background. The past two years have been **AI products for overseas markets**: the web editor of an AI video generation SaaS, AI content tools, and browser extensions.
- 🐍 **Backend and AI engineering**: one year of Python — LLMs behind FastAPI (OpenAI-compatible SDKs), RAG knowledge bases, SSE streaming; Node.js (Fastify) services; currently working through agent engineering.
- 🧩 **Full-surface delivery**: mini programs / H5 / desktop web / CRM / SaaS admin / mobile apps / Chrome extensions / Electron.
- 🏥 **Industries**: education, healthcare, overseas AI, live streaming, IM.
- 🎬 **Editors and animation**: video canvas editor engines, timeline playback engines, GSAP, Three.js scenes.
- ⚡ **AI-assisted engineering**: Claude Code / Cursor for breakdown, coding, review and automation; I write my own agent skills.
- 📱 Previously ran a **300k+ follower** Douyin account; now sharing AI coding in practice.

## 🛠 Tech stack

<p>
  <img src="https://skillicons.dev/icons?i=react,vue,nextjs,ts,tailwind,vite,flutter,electron,nodejs,py,fastapi,threejs,docker&perline=13" alt="tech stack" />
</p>

<p>
  <img src="https://img.shields.io/badge/uni--app-2B9939?style=flat-square" alt="uni-app" />
  <img src="https://img.shields.io/badge/React_Native-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React Native" />
  <img src="https://img.shields.io/badge/Chrome_Extension_MV3-4285F4?style=flat-square&logo=googlechrome&logoColor=white" alt="Chrome Extension" />
  <img src="https://img.shields.io/badge/Canvas-E34F26?style=flat-square" alt="Canvas" />
  <img src="https://img.shields.io/badge/GSAP-0AE448?style=flat-square&logo=greensock&logoColor=black" alt="GSAP" />
  <img src="https://img.shields.io/badge/SSE-555?style=flat-square" alt="SSE" />
  <img src="https://img.shields.io/badge/TipTap-1A1A1A?style=flat-square" alt="TipTap" />
  <img src="https://img.shields.io/badge/Yjs-30BCED?style=flat-square" alt="Yjs" />
</p>

## 💼 Selected work

### 🎬 [Leadde](https://leadde.ai) · AI video generation SaaS (in the HeyGen / Synthesia space)

Built for corporate training and product tutorials: 300+ AI avatars, voiceover in 88 languages, one-click video from PPT / PDF / script, edited in the browser and rendered in the cloud.

**My role: core developer of the web video editor**

- **In-house canvas editor engine** — a 1920×1080 DOM canvas on React 19 + react-moveable, with multi-select, group / ungroup (rotation-matrix conversion), alignment snapping, crop-and-pan, clipboard and keyboard shortcuts, layered as core / interactions / history / sync
- **State architecture and undo/redo** — a slice-based Zustand canvas store with hybrid snapshot + command undo, keeping store, DOM and interaction controls in agreement
- **Preview playback engine** — rAF-driven and clocked off audio, synchronising multi-page timelines, transitions, video trims, entrance animations and GSAP (controlled seek) frame by frame
- **Editor as renderer** — export recording drives the same canvas frame by frame, gated in order on media → first stable frame → animation mounted → fonts ready, so the exported video matches the preview
- **Automatic text contrast** — composites alpha down the layer z-order to work out the real background behind text (including inverse transforms for rotated layers and offscreen sampling of video frames), then picks a readable text colour
- **Real-time collaboration** — a Yjs / y-websocket channel with full rebuild on disconnect, backoff reconnect and a unified read-only gate
- **Front-to-back** — SSE streaming generation and async video jobs; tracked down and fixed a headless recording bug where Playwright intercepted gzipped CDN assets and the exported video lost its fonts
- GSAP animation components, the avatar video page, the editor's floating toolbar and context menu

Stack: React 19 · TypeScript · Vite · Zustand + immer · react-moveable · TipTap · GSAP · Yjs · MUI · Tailwind · Storybook

### 📝 [Lynote](https://lynote.ai) · AI content tools (10 languages)

| Product | Engineering notes |
|---|---|
| [YouTube Transcript Generator](https://chromewebstore.google.com/detail/lynote-youtube-transcript/cpdecpnpoaahhdlfjnpokjpemdnjhekf)<br/>Chrome extension | Shadow DOM injection into the YouTube sidebar with style and event isolation; service worker request proxy to sidestep CORS; Zustand + `chrome.storage` to sync auth across tabs; a pause / resume / retry state machine for translation; GA4 via a sandboxed iframe under MV3 |
| [AI Humanizer & Detector](https://chromewebstore.google.com/detail/lynote-ai-humanizer-detec/egbpdidbaamhhibpipaehgonalpkmmic)<br/>Chrome extension | Floating toolbar on text selection, lazily mounting the Shadow DOM and React tree only on first selection; auto flip above/below the selection; a locale-prefixed handoff protocol from extension to website |
| [lynote.ai](https://lynote.ai) website & SaaS tools | Migrated the legacy site to Next.js 15 App Router with SSR on the home page; POST SSE streaming translation with pause / stop; AI video summaries and short share links; shared auth between web and extension; multilingual SEO and analytics |

Stack: WXT · React 19 · Next.js 15 · TypeScript · Zustand · Tailwind · antd / MUI · next-intl / i18next

### 🖥 Electron + Python desktop automation client (commercial product)

- Dual-process architecture: Electron main process + Python subprocess, communicating over stdin with an NDJSON event stream
- A companion licensing service (Fastify), Ed25519-signed auto-update, and packaging for both Windows and macOS

## 🌱 Open source

### [daybrush/moveable](https://github.com/daybrush/moveable) · offering to help maintain

I build canvas interaction on `react-moveable` in a production video editor. I've offered to help maintain the project in [#1156](https://github.com/daybrush/moveable/issues/1156) and am waiting on the author.

What I'd like to bring upstream:

- **Persistent groups** ([#1133](https://github.com/daybrush/moveable/issues/1133), open since 2024) — group / ungroup as real, serializable entities rather than a runtime `targets` array: the group is itself a layer that can be saved, reloaded and nested
- **Recursive group resize** ([#1020](https://github.com/daybrush/moveable/issues/1020)) — dispatched by child type (font-size for text, inner crop offsets for media, viewport dimensions for SVG) instead of one uniform scale

### Other

- [colbymchenry/codegraph#1288](https://github.com/colbymchenry/codegraph/pull/1288) — fixed an OOM that took down the whole code index when an oversized asset file was imported, with a regression test (open)
- [xiwen-html2canvas](https://github.com/colinli007/xiwen-html2canvas) — two extra APIs on top of html2canvas to fix blurry output

## 📚 Currently learning

- **AI agent engineering** — orchestration and workflow state machines, tool calling, structured output, prompt engineering, LangGraph
- **Multi-model integration** — OpenAI / Gemini / Claude, streaming, rate limiting and cost control
- **AI video backends** — document parsing → script generation → TTS → avatar → headless render and compositing
- **Backend fundamentals** — FastAPI, Redis (distributed locks / Streams), MySQL / MongoDB, async job scheduling, Docker
