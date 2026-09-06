# code-in-harmony

> 🎸 My little corner of the internet — a hand-drawn, music-flavored personal site for [**olisNeuron**](https://github.com/olisNeuron).

Live at **[www.olisneuron.wiki](https://www.olisneuron.wiki)**.

A single-page, zero-build static site. No frameworks, no bundlers — just one lovingly hand-written `index.html`, a pile of inline SVG doodles, and a quiet obsession with the Beatles, Pink Floyd, and data structures.

---

## ✨ Features

- **One file, zero dependencies** — the whole site lives in `index.html` (only external resource is Google Fonts).
- **Hand-drawn doodle aesthetic** — paper grain, tape strips, tilted cards, and hand-drawn fonts (Rock Salt, Caveat, Patrick Hand, Indie Flower…).
- **Custom SVG art** — the hero Pink Floyd prism, the Abbey Road Beatles crossing, and a set of reusable doodle icons (`#d-star`, `#d-guitar`, `#d-bomb`, …).
- **Terminal typing effect** — the hero title types itself out, then stays put.
- **Bilingual EN / 中文** — a one-click language toggle backed by a tiny `data-i18n` system, with the choice persisted in `localStorage`.
- **Responsive** — fluid grid, clamp-based type, and a collapsible nav for small screens.
- **Music as a theme** — section kickers and cards riff on records, tracks, and instruments.

## 🧭 Sections

| Section | What's in it |
| --- | --- |
| **Hero** | Typed title, one-line intro, calls to action, prism + rainbow doodle |
| **About** | Self-intro, "currently wondering…" list, Feynman quote, hand-drawn Abbey Road crossing |
| **Projects** | 4 tilted cards linking to my public repos (`cs61b-spring-2025`, `cmu15213-lab`, `my-llm-wiki`, `olisNeuron`) |
| **Skills** | Chips grouped into languages, systems & tools, DSA, and AI & knowledge |
| **Contact** | GitHub, Bilibili, and a back-to-top link |

## 🗂 Structure

```
code-in-harmony/
├── index.html   # the entire site (markup + CSS + SVG + JS)
├── CNAME        # custom domain for GitHub Pages → www.olisneuron.wiki
└── README.md
```

## 🚀 Run it locally

It's static, so any way of serving the folder works:

```bash
# Python
python3 -m http.server 8000
# then open http://localhost:8000

# or Node
npx serve .
```

Or just double-click `index.html` — it runs straight from the filesystem.

## 🌐 Deploy

This repo is configured for **GitHub Pages**:

1. Push to the `main` branch.
2. In *Settings → Pages*, set the source to `main` (root) — the `CNAME` file already points at `www.olisneuron.wiki`.
3. Point your DNS at GitHub Pages and add a CNAME record for `www` if needed.

## 🛠 Customizing

- **Colors / fonts** — everything is tokenized in the `:root` block at the top of `<style>`.
- **Copy / translations** — edit the `I18N` object at the bottom of the `<script>` (both `en` and `zh` dictionaries).
- **Typing speed** — tweak the delays in `typeTick()`.
- **Doodles** — add a new `<g id="d-…">` inside the SVG `<defs>` and reuse it with `<use href="#d-…">`.

## ⚖️ License

Code is MIT. The doodles, copy, and musical obsessions are all mine — feel free to take inspiration, but please make it your own. 🎵

---

## 中文简介

这是 [**olisNeuron**](https://github.com/olisNeuron) 的个人主页，线上地址为 **[www.olisneuron.wiki](https://www.olisneuron.wiki)**。

一个单页、零构建的静态站点——没有框架、没有打包工具，只有一个手写的 `index.html`、一堆内联 SVG 涂鸦，以及对披头士、平克·弗洛伊德和数据结构的热爱。

**特性：** 手绘涂鸦风、自制 SVG 插画、终端打字效果、中英双语一键切换（`localStorage` 记住选择）、响应式布局、以音乐为主题。

**本地预览：** `python3 -m http.server 8000` 或直接双击 `index.html`。

**部署：** 推送至 `main` 分支，GitHub Pages 源设为 root，`CNAME` 已指向 `www.olisneuron.wiki`。
