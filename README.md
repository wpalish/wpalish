<div align="center">

```
 ██╗    ██╗██████╗  █████╗ ██╗     ██╗███████╗██╗  ██╗
 ██║    ██║██╔══██╗██╔══██╗██║     ██║██╔════╝██║  ██║
 ██║ █╗ ██║██████╔╝███████║██║     ██║███████╗███████║
 ██║███╗██║██╔═══╝ ██╔══██║██║     ██║╚════██║██╔══██║
 ╚███╔███╔╝██║     ██║  ██║███████╗██║███████║██║  ██║
  ╚══╝╚══╝ ╚═╝     ╚═╝  ╚═╝╚══════╝╚═╝╚══════╝╚═╝  ╚═╝
```

**Building AI infrastructure from Kazakhstan, one commit at a time.**

![visitors](https://visitor-badge.laobi.icu/badge?page_id=wpalish.wpalish)
[![GitHub followers](https://img.shields.io/github/followers/wpalish?style=flat&color=0969da)](https://github.com/wpalish)

</div>

---

I've been shipping production TypeScript and AI infrastructure since before "AI-native" became a buzzword. What started as internal tools for Kazakh startups evolved into open-source systems that developers actually use — agent frameworks, animation primitives, IoT platforms, streaming hooks.

I don't build demos. I build the infrastructure layer underneath the demos.

## Philosophy

Three rules for everything I ship:

1. **No magic** — internals should be readable, forkable, understandable
2. **Real problems first** — if I can't deploy it or use it myself, it doesn't ship  
3. **Open by default** — I'd rather 1,000 people fork it than 1 person pay for a closed version

I've been building this publicly since 2022. The timestamps matter.

## What I'm building

| Repo | What it actually is | Status |
|------|--------------------|----|
| [agent-kit](https://github.com/wpalish/agent-kit) | Multi-agent orchestration — tools, memory, parallelism, Claude at the core | 🔨 Active |
| [ai-saas-starter](https://github.com/wpalish/ai-saas-starter) | Claude streaming + auth + billing in one repo, Edge runtime | ✅ Stable |
| [react-ai-hooks](https://github.com/wpalish/react-ai-hooks) | `useChat`, `useStream`, `useCompletion` — streaming primitives for React | ✅ Stable |
| [motion-primitives](https://github.com/wpalish/motion-primitives) | Framer Motion components: magnetic, scroll-parallax, text reveal | ✅ Stable |
| [terra-platform](https://github.com/wpalish/terra-platform) | Agricultural IoT — SSE sensor feeds, real-time threshold alerts | 🔨 Active |
| [nextjs-dashboard](https://github.com/wpalish/nextjs-dashboard) | tRPC v11 + next-auth v5 + Prisma — production admin template | ✅ Stable |
| [telegram-ai-bot](https://github.com/wpalish/telegram-ai-bot) | Telegram × Claude with Redis conversation memory + streaming | ✅ Stable |
| [kz-addresses](https://github.com/wpalish/kz-addresses) | Kazakhstan address data — trilingual KAZ/RUS/ENG, all 20 regions | ✅ Stable |
| [madasy-studio](https://github.com/wpalish/madasy-studio) | Agency portfolio — Next.js 14, animated, Almaty-based studio | ✅ Stable |

## Stack I actually use

```
Language   TypeScript · Rust · Python
Runtime    Node.js · Edge (Cloudflare Workers / Vercel)
AI         Claude API · multi-agent patterns · streaming · tool use
Frontend   Next.js 14 · React 18 · Tailwind · Framer Motion
Backend    tRPC v11 · Prisma · PostgreSQL · Redis
Infra      Docker · GitHub Actions · Railway · Vercel
```

## Current focus

Building **[agent-kit](https://github.com/wpalish/agent-kit)** — a TypeScript framework for multi-agent systems with Claude at the core.

Tool registry, parallel agent runners, shared memory store, orchestrator/worker topology. The goal: make multi-agent systems boring to build. Most agent frameworks either do too much or not enough. This one is the Lego bricks — you assemble the architecture.

## Why Kazakhstan

I'm from Almaty 🇰🇿. Most of what I've built solves problems I saw in Central Asian tech ecosystems — address data nobody had cleaned up, IoT platforms nobody had open-sourced, AI tooling never localized for non-English devs. There's serious infrastructure missing in this part of the world and I plan to fill it, piece by piece.

The intersection of AI + local context is where interesting problems live.

---

<div align="center">

![Stats](https://github-readme-stats.vercel.app/api?username=wpalish&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=wpalish&layout=compact&theme=tokyonight&hide_border=true)

![Streak](https://streak-stats.demolab.com?user=wpalish&theme=tokyonight&hide_border=true)

[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=wpalish&theme=tokyo-night&hide_border=true)](https://github.com/wpalish)

**Building in public from Almaty, Kazakhstan**

[Twitter](https://twitter.com/wpalish) · [LinkedIn](https://linkedin.com/in/wpalish)

</div>
