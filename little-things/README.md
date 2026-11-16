# ✿ Little Things｜生活裡的小知識

以溫柔簡約的卡片收藏生活、旅行、理財與學習知識的靜態網站。

## 功能
- 四大主題分類篩選
- 標題、摘要、標籤即時搜尋
- 文章閱讀彈窗
- 深色模式（本機儲存偏好）
- 響應式手機／桌面排版
- 由 JSON 資料驅動的文章擴充

## 本機預覽
在專案資料夾執行：
```bash
python -m http.server 8000
```
瀏覽 `http://localhost:8000`。請勿直接雙擊 `index.html`，因為瀏覽器可能阻擋本機 `fetch()` 讀取 JSON。

## 新增文章
先閱讀 [AGENTS.md](AGENTS.md)，再依其中的資料格式在 `data/articles.json` 加入文章。無須修改 HTML 或 JavaScript。

## 部署到 GitHub Pages
1. 在 GitHub 建立公開 repository，名稱可用 `little-things`。
2. 將本專案所有檔案與資料夾上傳至 repository 根目錄。
3. 進入 `Settings` → `Pages` → `Build and deployment`。
4. `Source` 選擇 `Deploy from a branch`，分支選 `main`、資料夾選 `/(root)`，按 `Save`。
5. 等待部署完成，前往 GitHub Pages 顯示的公開網址確認功能。
一般網址格式：`https://你的帳號.github.io/little-things/`，實際以 GitHub 顯示為準。

## 專案結構
```text
little-things/
├── AGENTS.md
├── README.md
├── index.html
├── css/
│   └── style.css
├── js/
│   └── app.js
└── data/
    └── articles.json
```

## AI 可擴充性示範
讓 AI 讀取 `AGENTS.md` 後，只修改 `data/articles.json` 新增文章，首頁便會自動生成卡片並納入搜尋與分類。這讓內容更新可重複執行，不必每次重寫頁面。
