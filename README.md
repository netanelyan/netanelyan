# Hey, I'm Netanel 👋

**I like problems where the constraint is the interesting part.**

Developer from Israel, currently in my **3rd year of [Magshimim](https://www.magshimim.cyber.org.il/)**, Israel's national cyber & programming excellence program. I spend most of my time on low-level systems work - a renderer for chip layouts too big to fit on a GPU, and an operating system written from the bootloader up. The rest of it goes into automation and web platforms that keep a small e-commerce operation running without me touching it.

---

## 🚀 What I'm building

### [manhattan-project](https://github.com/netanelyan/manhattan-project) - a chip layout viewer in the browser
Pan and zoom a chip die like a street map, from the whole design down to the rectangles inside a single cell. The layouts are far too large to hand to a GPU whole, so the data is a **tile pyramid in three representations** and the viewer picks a level from the zoom against a measured budget of **~2M rectangles at 60fps**. Tiles are binary and read as typed-array views straight over the bytes, so nothing is parsed at runtime. Block instancing turns a 349M-placement chip view into **one tile fetch and 70 draw calls**. Tested on a real ISPD 2015 design: 4,634 macros, 680,869 components.

`C → WebAssembly` · `WebGL2` · `JavaScript` · no build step, no dependencies

### [nyrf-os](https://github.com/netanelyan/nyrf-os) - an x86_64 OS from scratch
Bootloader, kernel, and every layer underneath, booted through **UEFI**. My own boot application takes the framebuffer and memory map from firmware, loads an external ELF kernel, exits boot services, and hands over control. What makes it its own thing isn't that it boots - it's that **timing consistency**, not raw compute, is the constraint driving every design decision: deterministic scheduling and direct I/O access. POC 1 is complete and passing on QEMU + OVMF, all eight success criteria, 10 runs out of 10. Magshimim year project.

`C` · `x86-64 Assembly` · `UEFI` · `QEMU/OVMF`

### [tiyul-plus](https://github.com/netanelyan/tiyul-plus) - an AI travel agent that speaks Hebrew
Live at **[tiyulplus.com](https://www.tiyulplus.com)**. Tell it where, when and who's coming, and it plans a real mapped day-by-day trip in conversation. The planning loop is grounded in a **validated tool layer over a curated catalog**, so the model can't invent a place, a price or a kashrut status. 166 destinations across 83 countries, 1,814 places, full Hebrew RTL, and astronomically computed Shabbat times in the destination's real local clock.

`TypeScript` · `Next.js` · `Supabase` · `Claude API`

<p align="center">
  <a href="https://github.com/netanelyan/manhattan-project">
    <img src="https://github-stats-extended.vercel.app/api/pin/?username=netanelyan&repo=manhattan-project&theme=github_dark&hide_border=true" alt="manhattan-project" />
  </a>
  <a href="https://github.com/netanelyan/nyrf-os">
    <img src="https://github-stats-extended.vercel.app/api/pin/?username=netanelyan&repo=nyrf-os&theme=github_dark&hide_border=true" alt="nyrf-os" />
  </a>
</p>

---

## 🎓 Magshimim track

Three years of deep-diving into how computers actually work:

- **Python & networking** - sockets, protocols, and building real tools
- **C & C++** - memory, pointers, and low-level programming ([cpp-gallery](https://github.com/netanelyan/cpp-gallery): an SQLite-backed image gallery manager with WinAPI integration, [gifMaker](https://github.com/netanelyan/gifMaker) built with raylib, [chess](https://github.com/netanelyan/chess): full OOP chess engine)
- **Networking & systems** - [magshimim-trivia](https://github.com/netanelyan/magshimim-trivia): a multiplayer trivia game with a **C++ server** and **C#/WPF client** over a custom binary TCP protocol (1-byte code, 4-byte length, JSON payload), backed by SQLite, with a Python test client for the protocol
- **Assembly & OS internals** - the final project above 🧠

<p align="center">
  <a href="https://github.com/netanelyan/magshimim-trivia">
    <img src="https://github-stats-extended.vercel.app/api/pin/?username=netanelyan&repo=magshimim-trivia&theme=github_dark&hide_border=true" alt="magshimim-trivia" />
  </a>
  <a href="https://github.com/netanelyan/cpp-gallery">
    <img src="https://github-stats-extended.vercel.app/api/pin/?username=netanelyan&repo=cpp-gallery&theme=github_dark&hide_border=true" alt="cpp-gallery" />
  </a>
</p>

---

## 🔧 Automation & the things that run themselves

**Automating everything that shouldn't be done twice.**

- 🤖 **[brickdeal-automation](https://github.com/netanelyan/brickdeal-automation)** - a Telegram deal-flow pipeline running 24/7 in production: channel ingestion, dedupe, AliExpress affiliate API (HMAC-signed), AI title polishing, human-in-the-loop approval gate, scheduler, and self-monitoring. Deployed on a VPS with pm2, ~1,400 lines and one JSON file for storage
- 📰 **[tiyul-social](https://github.com/netanelyan/tiyul-social)** - a Hebrew travel-content pipeline: reads primary sources, drafts a post, renders a card, and publishes to Instagram **only after a human taps approve** on Telegram. No claim ships without a source fetched at generation time from an allowlisted domain
- 📦 **[shopify-order-automation](https://github.com/netanelyan/shopify-order-automation)** - turns raw store exports into translated, price-calculated, supplier-ready order documents, so fulfillment runs on scripts instead of copy-paste
- 🛒 **Storefronts & web** - [blackz-web](https://github.com/netanelyan/blackz-web), [brickdeal-website](https://github.com/netanelyan/brickdeal-website), [clutch-webpage](https://github.com/netanelyan/clutch-webpage)
- ⚙️ **Whatever saves me a click** - if I did it twice manually, it becomes a script

---

## 📌 More projects

| Project | What it is |
|---|---|
| [chess](https://github.com/netanelyan/chess) | Full object-oriented chess in C++ with per-piece move validation |
| [gifMaker](https://github.com/netanelyan/gifMaker) | GIF creation tool in C, built with raylib |
| [simple-gui-chat](https://github.com/netanelyan/simple-gui-chat) | A GUI chat app built in Python |
| [simple-browser](https://github.com/netanelyan/simple-browser) | A custom web browser built with C# Windows Forms |

---

## 📊 Stats

<p align="center">
  <img height="165" src="https://github-stats-extended.vercel.app/api?username=netanelyan&show_icons=true&theme=github_dark&hide_border=true&count_private=true&include_all_commits=true&rank_icon=github&show=prs_merged&custom_title=Netanel%27s%20Stats" alt="GitHub stats" />
  <img height="165" src="https://github-stats-extended.vercel.app/api/top-langs/?username=netanelyan&layout=compact&theme=github_dark&hide_border=true&langs_count=8&hide=html,css&custom_title=What%20I%20Write%20In" alt="Top languages" />
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=netanelyan&theme=github-dark-blue&hide_border=true" alt="Contribution streak" />
</p>

---

## 🧰 Stack

**Systems:** `C` · `C++` · `x86-64 Assembly` · `WebAssembly` · `WebGL2` · `Linux/VPS`
**Web & apps:** `TypeScript` · `JavaScript` · `Next.js` · `Node.js` · `C#` · `Python` · `HTML/CSS`
**Data & infra:** `SQLite` · `Supabase` · `REST APIs` · `Azure Functions` · `Git`

---

## 📫 Find me

- Instagram: [@netanel.yan](https://www.instagram.com/netanel.yan/)

---

*"If it can be automated, it will be."*
