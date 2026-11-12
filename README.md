# fred09280928.github.io

瀏覽器程式的入口選單。全部純靜態，沒有 build step。

## 新增一個程式

1. 在那個程式的 repo 打開 Pages（Settings → Pages → `main` / `root`），確認 `https://fred09280928.github.io/<repo>/` 打得開。
2. 在這個 repo 的 `apps.json` 加一筆：

```json
{"name": "顯示名稱", "desc": "一句話說明", "url": "/<repo>/", "tags": ["分類"], "status": "live"}
```

- `url` 一律用**絕對路徑** `/repo/`，不要寫完整網域（換網域時不用改）。
- `status`：`live` 顯示綠點，`soon` 半透明、不可點（施工中）。
- `tags` 是選填的字串陣列，只影響顯示的分類標籤。

3. commit 後 Pages 約一分鐘生效。

## 檔案

- `index.html` — 讀 `apps.json` 畫卡片；沒有 build step。
- `style.css` — 深淺色跟隨系統（`prefers-color-scheme`）。
- `apps.json` — 唯一的資料檔。
- `404.html` — 走錯路徑時導回選單。
