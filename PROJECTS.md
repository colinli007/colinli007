<div align="center">

**English** · [简体中文](PROJECTS.zh-CN.md) · [← Back to profile](README.md)

# Full project history · Colin

<a href="https://github.com/colinli007">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1200&color=2F81F7&center=true&vCenter=true&width=520&lines=Senior+Frontend+%2F+Full-Stack+Engineer;AI+Video+Editor+%C2%B7+Agent+Services;10+Years+%C2%B7+Frontend+Team+Lead" alt="Senior Frontend / Full-Stack Engineer" />
</a>

<p>
  <a href="https://www.npmjs.com/~li1164267803"><img src="https://img.shields.io/badge/npm-li1164267803-CB3837?style=flat-square&logo=npm&logoColor=white" alt="npm" /></a>
  <a href="https://blog.csdn.net/weixin_44309374"><img src="https://img.shields.io/badge/Blog-CSDN-FC5531?style=flat-square&logo=csdn&logoColor=white" alt="CSDN" /></a>
  <a href="mailto:xiwenpp@163.com"><img src="https://img.shields.io/badge/Email-xiwenpp@163.com-2F81F7?style=flat-square" alt="Email" /></a>
</p>

</div>

## 🙋 About me

- 👨‍💻 **Senior frontend / full-stack engineer** with about 10 years in software; BSc in Computer Science, China University of Petroleum. I've led a frontend team, owning technical design, task breakdown, shared infrastructure and delivery of core features.
- 🎬 **Canvas editors** — DOM/SVG canvases, Moveable/Selecto interaction, layer and history state, undo/redo, timeline playback engines, GSAP, Yjs real-time collaboration.
- 🤖 **Full stack and agents** — on a React/Vue foundation, Node.js/Fastify agent services (annotation passing, session edits, SSE resume and task-state recovery) and Python/FastAPI APIs (SQLAlchemy, MySQL, Redis, version checks and CAS optimistic concurrency).
- 📱 **Every surface** — desktop web, H5, WeChat mini programs, mobile apps, Chrome extensions, Electron; Flutter native SDK bridging, React Native/Expo apps, Tencent IM/TRTC real-time audio/video.
- 🧱 **Engineering** — Qiankun micro-frontend migration, shared component libraries, multi-environment builds and CLI release for mini programs, Jest, CI/CD.
- 🏥 **Industries** — overseas AI video and digital humans, live streaming, healthcare, online education, local services.
- ⚡ **AI-assisted engineering** — Claude Code / Cursor for breakdown, coding, review and automation; I write my own agent skills.
- 📱 Previously ran a **300k+ follower** Douyin account; now sharing AI coding in practice.

## 🛠 Tech stack

| Area | Technologies |
|---|---|
| Frontend | React, Vue 2/3, TypeScript, Next.js, Zustand, Vite, Webpack, Tailwind CSS |
| Editors | DOM/SVG canvas, Moveable/Selecto, layer and history state, timelines, GSAP, TipTap, SSE, Yjs/WebSocket |
| Backend & agents | Python/FastAPI, SQLAlchemy, MySQL, Redis, Node.js/Fastify; persistence, version checks and concurrent updates |
| Cross-platform & tooling | uni-app, WeChat mini programs, Flutter/Dart, React Native/Expo, Electron, Chrome Extension MV3, Qiankun, Jest, CI/CD |
| AI tools | Claude Code, Codex, Cursor |

## 🏢 Experience

| When | Company | Role | Focus |
|---|---|---|---|
| 2024.11 – now | 01.AI | Frontend lead & full-stack | Overseas AI video and digital-human products; leading the frontend team and core development, building agent services and canvas backend APIs |
| 2022.04 – 2024.10 | Nuoxin Chuanglian | Senior frontend engineer / frontend owner | Healthcare mini programs, admin consoles and campaigns; drove the micro-frontend migration, shared components and the release pipeline |
| 2018.08 – 2022.03 | Baidu | Frontend engineer | Education: online classrooms and teaching services across web, app and mini programs |
| 2016.07 – 2018.08 | 58.com | Frontend engineer | Joined as an intern in my final year and stayed on after graduating; local services, real-estate H5 pages and merchant consoles |

## 💼 Selected work

### 🎬 [Leadde](https://leadde.ai) · AI video creation platform (in the HeyGen / Synthesia space)

Built for corporate training and product tutorials: 300+ AI avatars, voiceover in 88 languages, one-click video from PPT / PDF / script, edited in the browser and rendered in the cloud.

**My role: frontend lead; core developer of the canvas editor, the agent service and the canvas backend APIs**

- **In-house canvas editor engine** — a 1920×1080 DOM canvas on React 19 + react-moveable, with multi-select, group / ungroup (rotation-matrix conversion), alignment snapping, crop-and-pan, clipboard and keyboard shortcuts, layered as core / interactions / history / sync
- **State architecture and undo/redo** — a slice-based Zustand canvas store with hybrid snapshot + command undo, keeping store, DOM and interaction controls in agreement
- **Preview playback engine** — rAF-driven and clocked off audio, synchronising multi-page timelines, transitions, video trims, entrance animations and GSAP (controlled seek) frame by frame
- **Editor as renderer** — export recording drives the same canvas frame by frame, gated in order on media → first stable frame → animation mounted → fonts ready, so the exported video matches the preview
- **Automatic text contrast** — composites alpha down the layer z-order to work out the real background behind text (including inverse transforms for rotated layers and offscreen sampling of video frames), then picks a readable text colour
- **Real-time collaboration** — a Yjs / y-websocket channel with full rebuild on disconnect, backoff reconnect and a unified read-only gate
- **Front-to-back** — SSE streaming generation and async video jobs; tracked down and fixed a headless recording bug where Playwright intercepted gzipped CDN assets and the exported video lost its fonts
- **iframe editing SDK** — element location, image replacement and annotated screenshots, giving the agent precise context for targeted edits
- **Agent service** — Node.js/TypeScript modules that pass element annotations and scene references to the agent and handle session-scoped edits; wired SDK distribution, the iframe message bridge and error receipts, together with SSE resume and task-state recovery on the frontend
- **Persistence and read-back** — Python/FastAPI config, layer and asset APIs for saving, querying and restoring; incremental layer edits by stable ID, with version checks, CAS optimistic concurrency and bounded retries to resolve write conflicts
- GSAP animation components, the avatar video page, the editor's floating toolbar and context menu

Stack: React 19 · TypeScript · Vite · Zustand + immer · react-moveable · TipTap · GSAP · Yjs · Node.js/Fastify · Codex App Server · Python/FastAPI · MySQL/Redis

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

### 🎙 Digital-human live-streaming platform

A SaaS for businesses and operators to edit digital-human avatars, generate live scripts and manage live interaction.

- **Live editing and interaction** — React/TypeScript drag-and-resize for avatars and cloud-phone login authorisation; AI script continuation and a browser extension that collects live comments, feeding updates back to the stream
- **Delivery** — avatar editing, authorisation and interaction logic organised as hooks and shared components; automated deployment with Node.js scripts

### 📡 Flutter live-streaming SDK wrapper

A cross-platform layer letting Flutter apps call native Android/iOS live-streaming capabilities: a unified Dart API wrapping native SDK initialisation, authorisation and streaming calls, handling cross-platform messaging and platform differences through integration and debugging.

### 🏥 TCM online hospital and healthcare operations console

Online consultations, e-prescriptions and healthcare operations for patients, doctors and operators.

- **Mini program** — chose uni-app, set up the project and built the core flows (online consultation, e-prescriptions); Tencent IM/TRTC for text, image, audio and video between doctors and patients
- **Engineering and reuse** — multi-environment builds, CLI packaging and release for mini programs, coding standards; built and migrated micro-apps on Vue + Qiankun, with shared UI and ECharts chart components

### 🎓 Baidu · online classrooms and teaching services

Live teaching, classroom interaction and lesson preparation for teachers and students: integrated a live-streaming SDK, SSE updates, html2canvas courseware generation and Cocos Creator mini-games; reworked the caching strategy and extended shared form-validation and table components.

### 🏠 58.com · local services and merchant consoles

Real-estate and local-services pages plus merchant consoles: shared list filtering, pagination, upload and form validation; image lazy-loading, on-demand assets, parallel requests and caching for speed, and key behaviour tracking.

## 🌱 Open source

- [flatpickr-ce](https://github.com/colinli007/flatpickr-ce) — a lightweight, dependency-free date/time picker web component with date, time and range selection; locales, themes and plugins, working inside iframes and Shadow DOM, installable from npm
- [lanmao-reader](https://github.com/colinli007/lanmao-reader) — a cross-platform reader (Android / iOS) in Flutter/Riverpod + SQLite, compatible with Legado book sources; a rule engine, QuickJS over FFI and an isolate task pool, with timeout cancellation and rule replay tests
- [easy-music](https://github.com/colinli007/easy-music) — a local music player for Android and iOS in React Native/Expo: SQLite library, source resolution separated from playback control, background playback and a cancellable offline download queue
- [agent-skills](https://github.com/colinli007/agent-skills) — the Claude Code / Codex agent skills I use day to day
- [xiwen-html2canvas](https://github.com/colinli007/xiwen-html2canvas) — two extra APIs on top of html2canvas to fix blurry output

## 📚 Currently learning

- **AI agent engineering** — orchestration and workflow state machines, tool calling, structured output, prompt engineering, LangGraph
- **Multi-model integration** — OpenAI / Gemini / Claude, streaming, rate limiting and cost control
- **AI video backends** — document parsing → script generation → TTS → avatar → headless render and compositing
- **Going deeper on the backend** — Redis distributed locks / Streams, MongoDB, async job scheduling, Docker
