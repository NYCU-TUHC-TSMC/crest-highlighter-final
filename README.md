# Crest Highlighter Final

這個 repo 是整個 Crest Highlighter 專案的 umbrella repository。

實際程式碼分成兩個 git submodule：

- `frontend/` → `NYCU-TUHC-TSMC/crest-highlighter-frontend`
- `backend/` → `NYCU-TUHC-TSMC/crest-highlighter`

## Clone

```bash
git clone --recurse-submodules https://github.com/NYCU-TUHC-TSMC/crest-highlighter-final.git
cd crest-highlighter-final
```

如果已經 clone 但 submodule 還沒拉下來：

```bash
git submodule update --init --recursive
```

## Update submodules to latest main

```bash
git submodule update --remote --merge
git add frontend backend
git commit -m "Update frontend and backend submodules"
```

## Repositories

| Path | Repo | Purpose |
| --- | --- | --- |
| `frontend/` | `crest-highlighter-frontend` | React/Vite 前端、Shorts UI、YouTube 上傳 UI |
| `backend/` | `crest-highlighter` | API、pipeline、EKS/KEDA/GPU/YouTube backend |

