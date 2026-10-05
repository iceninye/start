# Ice Apps Hub

個人 Web Apps 入口頁 — `index.html` 靜態單頁，列出所有 live apps 嘅卡片。

🔗 **Live**:
- Cloudflare Workers: https://hub.iceninye.workers.dev/

## 結構

```
index.html           單頁 + inline CSS + 1 個 JS clock
assets/icon.svg      favicon
wrangler.json        Cloudflare Workers static assets 設定
```

## 內容

| App | 版本 | 連結 |
|---|---|---|
| 屯馬綫列車動態圖 | v0.4.4 | https://tml-traffic.iceninye.workers.dev/ |
| 港鐵實時到站資訊 | v52.8.1 | https://mtr-app.iceninye.workers.dev/ |

## 設計

- **純前端**：冇 build step、冇 bundler、冇 framework
- **零追蹤**：無 analytics、無 cookies、無 3rd-party CDN
- **自動深淺色**：跟 `prefers-color-scheme`
- **無障礙**：semantic HTML、focus ring、`prefers-reduced-motion`
- **Responsive**：CSS Grid `auto-fit minmax(280px, 1fr)`

## 部署

```bash
# Cloudflare Workers
npx wrangler deploy

# 或者直接 drag-and-drop index.html 入 Cloudflare Pages
```

## 授權

純 HTML/CSS/JS，冇依賴。MIT。
