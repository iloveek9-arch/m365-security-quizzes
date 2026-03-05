
# 公司教育訓練測驗（GitHub Pages 版）

這個專案包含兩個可直接部署到 GitHub Pages 的測驗頁面：

- `index.html` — 防範電器火災（114/11，保全戊卷）
- `滅火器介紹quiz.html` — 滅火器介紹與使用操作（114/12，保全己卷）

## 快速部署到 GitHub Pages

1. 登入 GitHub → 新增一個 Repository（例如：`m365-security-quizzes`）。
2. 直接把本資料夾內所有檔案上傳到 **repo 根目錄**（`index.html`、`滅火器介紹quiz.html`、`README.md`）。
3. 進入 **Settings → Pages**：
   - **Build and deployment** → **Source** 選擇 **Deploy from a branch**。
   - **Branch** 選擇 `main` 與 `/ (root)`。
   - 儲存後，等候 1~2 分鐘，頁面上會顯示你的網站網址（例如：
     `https://<你的帳號>.github.io/<你的 repo 名稱>/`）。

## 連結（部署後）
- 防範電器火災（預設首頁）：
  `https://<你的帳號>.github.io/<你的 repo 名稱>/`
- 滅火器介紹與使用操作：
  `https://<你的帳號>.github.io/<你的 repo 名稱>/滅火器介紹quiz.html`

> 若想以「選單頁」整合兩個卷別，可將 `index.html` 改成入口頁（或新增 `home.html` 再把它改名為 `index.html`）。

## 備註
- 頁面為 **純前端**，功能包含：亂數出題、交卷詳解（可關閉）、本機暫存、CSV 匯出。
- 已內建 **Google 試算表 Apps Script Web App** 端點；交卷時會以 `POST` 記錄（`application/x-www-form-urlencoded`）。
- 若要限制只有公司帳號可寫入，請在 Apps Script 部署時選「僅限網域內任何人」。
