# Crest Highlighter

[![SVG Banners](https://svg-banners.vercel.app/api?type=rainbow&text1=Crest%20Highlighter%20%20🎬&width=800&height=210)](https://github.com/NYCU-TUHC-TSMC/crest-highlighter-final)

<p align="center">
  <a href="https://d3qzwgiikng9x7.cloudfront.net">Live Demo</a> ·
  <a href="https://github.com/NYCU-TUHC-TSMC/crest-highlighter-frontend">Frontend</a> ·
  <a href="https://github.com/NYCU-TUHC-TSMC/crest-highlighter">Backend</a>
</p>

Crest Highlighter 是一個把直播影片轉成 Shorts 精華的 AI 剪輯系統。前端負責上傳、預覽、剪輯與 YouTube 發佈體驗；後端負責轉錄、精彩片段分析、autocut 成品輸出與雲端任務排程。

## Overview

這個 repo 是整個專案的 umbrella repository，透過 submodule 把前端與後端固定在可重現的版本。

| Path | Repository | Purpose |
| --- | --- | --- |
| `frontend/` | [`crest-highlighter-frontend`](https://github.com/NYCU-TUHC-TSMC/crest-highlighter-frontend) | React/Vite 前端、Shorts UI、YouTube 上傳 UI |
| `backend/` | [`crest-highlighter`](https://github.com/NYCU-TUHC-TSMC/crest-highlighter) | API、pipeline、EKS/KEDA/GPU/YouTube backend |

## Clone

```bash
git clone --recurse-submodules https://github.com/NYCU-TUHC-TSMC/crest-highlighter-final.git
cd crest-highlighter-final
```

如果已經 clone 但 submodule 還沒拉下來：

```bash
git submodule update --init --recursive
```

## Update submodules

把前後端 submodule 更新到各自最新的 `main`：

```bash
git submodule update --remote --merge
git add frontend backend
git commit -m "Update frontend and backend submodules"
```

## Repository layout

```text
crest-highlighter-final/
├── frontend/   # crest-highlighter-frontend submodule
├── backend/    # crest-highlighter backend submodule
├── .gitmodules
└── README.md
```

