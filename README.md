# PyNotes｜Python 初學者學習筆記

這是一個整理 Python 常見錯誤的繁體中文靜態網站。每篇文章包含錯誤範例、原因、修正方法和練習題。

## 網站內容
- [TypeError](lessons/typeerror.html)
- [IndexError](lessons/indexerror.html)
- [KeyError](lessons/keyerror.html)
- [NameError](lessons/nameerror.html)
- [ZeroDivisionError（依規則擴充的示範頁面）](lessons/zero-division-error.html)

## 本機開啟
直接用瀏覽器開啟 `index.html`，或在專案目錄執行 `python -m http.server 8000` 後開啟 `http://localhost:8000`。

## GitHub Pages 發布
1. 將所有檔案上傳到 GitHub Repository 的 `main` 分支，保留資料夾結構。
2. 前往 **Settings → Pages → Build and deployment**。
3. 選擇 **Deploy from a branch**，分支選 `main`，資料夾選 `/(root)`，按 **Save**。
4. 等待 GitHub Pages 部署完成，開啟 `https://qiuyili920917-ux.github.io/pynotes-learning/`。

## 如何擴充
請先閱讀 [AGENTS.md](AGENTS.md)。新增教學時依照既有頁面建立 `lessons/<slug>.html`，並更新首頁卡片、相關連結與 README。`zero-division-error.html` 是依這套規則製作的示範擴充頁面。

## 使用技術
HTML5、CSS3、原生 JavaScript；無 API、無額外依賴。
